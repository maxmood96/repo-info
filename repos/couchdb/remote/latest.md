## `couchdb:latest`

```console
$ docker pull couchdb@sha256:a0dd9e6f018c220ddacb1217c87923ac8a8c74c9c75cc3859d9ce2a14aecf587
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:b2e6d8d61e30aa84a19692f45ad942f981149d097ee6bed324a891d1da951b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (133048842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2b4e5a5e0caec726f393251bb061f0e86c7e169c047c8a033a9db24cacf1ea`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7505c466d057390ebea55dd9477de60eaed7234ab6a9a27136d046fbf09d80f`  
		Last Modified: Tue, 03 Dec 2024 02:30:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715db634671e88dfc7f1b572fc9adbb5f3d8843818805efb86c1b06d773b3b80`  
		Last Modified: Tue, 03 Dec 2024 02:30:06 GMT  
		Size: 7.7 MB (7680157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d270f3606097339469cfcba157190f0a6630fe05d6a3af70fd6b90f5dfbbe235`  
		Last Modified: Tue, 03 Dec 2024 02:30:06 GMT  
		Size: 392.1 KB (392098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187937fad7ce958fd5252c5bb9797358f668802bed612aae6e6b20f10c06f08`  
		Last Modified: Tue, 03 Dec 2024 02:30:06 GMT  
		Size: 76.2 KB (76238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b46c202a80f2e39d694eab2f37623f47b7586101f6e66db09e01c898502a18`  
		Last Modified: Tue, 03 Dec 2024 02:30:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6c999b840516c7fea2db91eb97ecb1db7796ced77310e2ccaa4accd04304fe`  
		Last Modified: Tue, 03 Dec 2024 02:30:09 GMT  
		Size: 96.7 MB (96663343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd0bf127bec81b61f89a8eb35880d50e0bb436d412456ed75cbdb230f92850`  
		Last Modified: Tue, 03 Dec 2024 02:30:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df7bccc222c54f0520199b8f89c9e86b0f5c82d406e787bc7c0e5720ef24185`  
		Last Modified: Tue, 03 Dec 2024 02:30:07 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc499ef57cb263fe6cdc944042929bb4912d7504d1bd5b7723fe6f1fc28a5a43`  
		Last Modified: Tue, 03 Dec 2024 02:30:07 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d5a15b15e2c4911d2703d7f86c3d59e9c7b908a224fc595c800ad97d8a51a`  
		Last Modified: Tue, 03 Dec 2024 02:29:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:8d2b8a483ebd6d17e45c01c5aeb404febb3a6213f6fc03132cd57e598dc622ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14346ff92fd044ccf9d7d2d4165bf99680391eae1b56042fcfe444ab1d24ddbc`

```dockerfile
```

-	Layers:
	-	`sha256:dc524cff411e3288624210fb6eb91992bf946e27c64a48a3403e5d4952cab66d`  
		Last Modified: Tue, 03 Dec 2024 02:30:06 GMT  
		Size: 3.9 MB (3946489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e3f8ed74717030ac800f8fc2f5e0048c5ce254bb85a17bb9f6d1b16b056f8e1`  
		Last Modified: Tue, 03 Dec 2024 02:30:06 GMT  
		Size: 31.8 KB (31773 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:067e2a755be2756ea483e4229c43d721331f02e18e2efcc09cb0a396ca5d4ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133641051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da06e9cf1081ac6d6b506130132d045d6690e2274ba23ad5e301feb92a02bb4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aab7d56576ee0f12847b9dcdcb327c24340f1f0b628814c1cecc4b51198574d`  
		Last Modified: Tue, 12 Nov 2024 11:21:29 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d89bacbcab08f96154ca413ce7b2586d26213fec592900f078dbe419c63c48`  
		Last Modified: Tue, 12 Nov 2024 11:21:29 GMT  
		Size: 7.7 MB (7654499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2b24df4f156c2e4a5b9177788e9fa892fb6749bd618e3458d1f353b6ff221e`  
		Last Modified: Tue, 12 Nov 2024 11:21:29 GMT  
		Size: 348.9 KB (348922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa757569d43a708a0319a27a2ce917521efbe56512c7b498b34a0d7262ad0d4a`  
		Last Modified: Tue, 12 Nov 2024 11:21:29 GMT  
		Size: 76.3 KB (76253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0175cffb3e96ec1b2ab648f5196f9bbb14a8075a2af2150420a8e335b98311b6`  
		Last Modified: Tue, 12 Nov 2024 11:21:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a9f110561cbb42c3824d3e19e3eb192702cb7e1792b9405993ec455d4c0972`  
		Last Modified: Tue, 12 Nov 2024 11:21:34 GMT  
		Size: 96.4 MB (96398587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fe7460d11b43a878befba1b1f617e30866a0ded3b72f2e8b9fc5e5b5433cbc`  
		Last Modified: Tue, 12 Nov 2024 11:21:30 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff5e657bcac7f5d7815f28a980631882c40e45f58864668d107dd92b35805a`  
		Last Modified: Tue, 12 Nov 2024 11:21:31 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e51d75e906e0c8f9b4e3f24cdd46a9402aafeac1fba59a9f6f6cc1efeeb609`  
		Last Modified: Tue, 12 Nov 2024 11:21:31 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe39ad0cf1d498f6f82170c88c3032ecb9e0c5df41d1971cb5b8d0717f56416e`  
		Last Modified: Tue, 12 Nov 2024 11:21:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:351b1f48cb37fc6704bc72b1b499e9315a86a1e72be4dcd022e388ab36cdc6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3a492b8546d8a226cc375dba42252a67da90fa26d95ac8660fbe160bb95855`

```dockerfile
```

-	Layers:
	-	`sha256:af9671dc138eff75c412aed05415e91fc9001605d0513aa86eca400f752759a1`  
		Last Modified: Tue, 12 Nov 2024 11:21:29 GMT  
		Size: 3.9 MB (3948029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e584704b02cb083e4b559c6a15abf3975685e09b9f3c45bb48b23b99c87bead0`  
		Last Modified: Tue, 12 Nov 2024 11:21:29 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:e6fcc88070f7b0e86d5364736bc763fe86ae7d68687cd1fe4e42a0677bcddadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129799946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8625f7dcf4bdb30fb6ec3fc6a14398f7580328ef91b9627c343b75a1e44d25`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f62dd7c2ef02aef29904845392c52876ca049ce1a18728cc7dfef3b237efcf0`  
		Last Modified: Tue, 03 Dec 2024 04:12:39 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436b2be715bcc19374d608d84bd76f2cb06e9becd4d258135a5becff836470c1`  
		Last Modified: Tue, 03 Dec 2024 04:12:39 GMT  
		Size: 7.2 MB (7194556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e21c2f324c3e4afba3a13a1cb139b481a220178faa7426a75aaa7aaf6554881`  
		Last Modified: Tue, 03 Dec 2024 04:12:39 GMT  
		Size: 355.6 KB (355614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffcfa15e589dd6f0d70731ca77d3d607a4b3031517b18bc1bd30a3f93856382`  
		Last Modified: Tue, 03 Dec 2024 04:12:39 GMT  
		Size: 76.3 KB (76349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9dc587296357b232114101a046c8e4513d59d3bc7eff0c47807ba1d0e37f2f`  
		Last Modified: Tue, 03 Dec 2024 04:12:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318b01f237ee12236fd1c8259216248a2b7e3d6c1a2db3ca4dceae2843289bbf`  
		Last Modified: Tue, 03 Dec 2024 04:12:41 GMT  
		Size: 95.3 MB (95289016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d778ebc4fa1e6a714c7738d70a11cb7da534221d50550ba2feb67839c0c3c49`  
		Last Modified: Tue, 03 Dec 2024 04:12:40 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2287015740303ffa9ae9a3b36a3999c63b2dfcb3a41e4a49f18828b9f191ae`  
		Last Modified: Tue, 03 Dec 2024 04:12:40 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133d64d961c7746f95acb6a69db4ae91e99ec73afe41cbe693c6bf4b90a79b85`  
		Last Modified: Tue, 03 Dec 2024 04:12:40 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1961facbfe8c06d23a8297b4543d7f229dc0e4aee47299598f3de5bd12a3a65`  
		Last Modified: Tue, 03 Dec 2024 04:12:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:93204288eb86370630903751a00ab901c758dee1f1eb4f8a9b60f7603d56fba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06244342963b537a7a26150fa09c201d1117d3798bac4a15c76eaa76cd518551`

```dockerfile
```

-	Layers:
	-	`sha256:896a30693511d0b291dd35c9cd2b17620bd1df70f76a13769ee880aa2e6db66a`  
		Last Modified: Tue, 03 Dec 2024 04:12:39 GMT  
		Size: 3.9 MB (3945577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffb80ebdefa9fdb101a464a70a8f4f85afd2b0c735cdfca05f5781ae0ccc991`  
		Last Modified: Tue, 03 Dec 2024 04:12:39 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json
