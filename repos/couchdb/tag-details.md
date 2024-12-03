<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.2`](#couchdb342)
-	[`couchdb:3.4.2-nouveau`](#couchdb342-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

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

### `couchdb:3` - linux; amd64

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

### `couchdb:3` - unknown; unknown

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

### `couchdb:3` - linux; arm64 variant v8

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

### `couchdb:3` - unknown; unknown

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

### `couchdb:3` - linux; s390x

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

### `couchdb:3` - unknown; unknown

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

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:732c1da782a9fafe5c94e4fc05b247360bbf07c2f38f48730b61cd29335a18fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:ee3c19ed84984c039b2aed6c9778f961d9d93f68e527d7430ddecad8f3a1e6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155342527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303b5c2e55f983b7ee77545598858abd612b8be35e8f84bd91fd671257dfa9f8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b98581970ff034bd529aa26ca12985e1754b525da12b09d70af3afd68237dec`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad44d7c547c5b4af935adb2d65f110daa2908d5e03b73bf0ab7586b3d9508055`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 7.7 MB (7680091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56274944153676d0005183f9e215ec98e6e7472eddc5cf21529268cdd42779ac`  
		Last Modified: Tue, 03 Dec 2024 02:30:14 GMT  
		Size: 77.3 MB (77283848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2ce4fc68f42259f450845e7d641d1dacce777d2e5a8e84f4c962ce84b1d317`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 415.0 KB (414979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369ef73f7e71d1762b7655789406b41950edaa9d021d59fcbcd99437c9290b1`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 99.3 KB (99275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2357ef9f7a1531b8f41bbb206494d4830505a15cb69eb5692cd61b76c0e54d`  
		Last Modified: Tue, 03 Dec 2024 02:30:15 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279b904e61f002e3c6e6a1291643a131b5e7baa407204a1b3cd7d0a1b3c93389`  
		Last Modified: Tue, 03 Dec 2024 02:30:16 GMT  
		Size: 41.6 MB (41630870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec70c3c80f6e9ae7f7a2020188828dc2c2126616bf7f67a70f2abc6c5a57e984`  
		Last Modified: Tue, 03 Dec 2024 02:30:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:cf1cbbc70dcd900a27e44cbca90120d8ec57695a3ca1d26e28182a6f3edc5b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b307ee6fcc8d74c05f3f3c53b8e833866b239892d62ed652b73dc79de86b0c`

```dockerfile
```

-	Layers:
	-	`sha256:6d4feac5f0676816359cf6e4ed69fef2b22e74a88f239b1beda607fb80e24a5a`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 3.5 MB (3473837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ddb8926a39928e1bef08870795effae205dc9ba496060f6eed74d82a1799eb`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f71f156d8ea97ac5a1a9d3428b6801a2314b2d51d027603df62086928167d1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155395393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea534a63294b54cdb4032044b38258ef0b217c1d24baab024a67b410ab8e019`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f27311cf459d2dcc491d124b0207b7ddb24b839cd838dc8ac4e0f59546cdc`  
		Last Modified: Tue, 12 Nov 2024 11:22:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136edbc8e932535e5b082121b430f39e8c59a9b5414da4be2512971d1ac1164f`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 7.7 MB (7654500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5cb31d0cc00c24636b47d511f24d67bb61941038936f91922dc2e1a5bdbfb`  
		Last Modified: Tue, 12 Nov 2024 11:22:48 GMT  
		Size: 76.6 MB (76583825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6b710de5abf310302d33c0dfc43afcd7f8eadfd3e6c328c61aa277044d8d76`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 371.7 KB (371716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268db4a4b80fa4e519d1a26fa5d6382df8df33e19d63f21dc3bdb09b53dc56f2`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 99.2 KB (99243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3a2582a518b4000dd7ef5c817f5319a8c2d678c2fab8196e7051e02d2168a4`  
		Last Modified: Tue, 12 Nov 2024 11:22:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2454d2f2a5242fdfd6712fbea60eb15cb3d6cbd208f47691102354250262809`  
		Last Modified: Tue, 12 Nov 2024 11:22:49 GMT  
		Size: 41.5 MB (41526874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b879b3c3e60af5a96bea846d460ec7217b4bd814982062edeae65e9549be48f`  
		Last Modified: Tue, 12 Nov 2024 11:22:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1660b8bda29f20af133467684cfd3a71c475ab15f0bbc39cbb100bf3fedfb0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b679c5b6fb5420330b007be7aa6a7de72ad81cc10e91e719a2295a571ac8952b`

```dockerfile
```

-	Layers:
	-	`sha256:41b0d5c1a70050cdf819efb713cfc261f7eea26141463ca09930433b73849ddd`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 3.5 MB (3473758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d7d86a4e50de07693ded530d5eed50c87e65a758234937458b013c3af30693`  
		Last Modified: Tue, 12 Nov 2024 11:22:46 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:78b2608987f018fac2cd4759f3c5f66568433802fbea35b0f2ee4cbf946d5d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148967286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1882582f22070e4df3f0856060c2cc693cf367b521c6f911633590a8ce060b72`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd2d074f21bdd203a2fd183cffe3e3815c3d9d940d57fed8bc55c74741e400e`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354a85114ee6eb212fc2c26419f60433aa0ef174d027d581cf3702301d73f88c`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 7.2 MB (7194578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1071a9e3021abb79a6c6b4da3028cbb55bc209fabbf7d15d78c44b418261b076`  
		Last Modified: Tue, 03 Dec 2024 04:14:07 GMT  
		Size: 73.1 MB (73064424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ac56c18e58424283065b984082e48f090c2bc9760fc9c888a6bfa2154bb70b`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 378.1 KB (378058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142d0b872098335016954848d7bb541f1aaa55f65761a42e4530519237a19f0d`  
		Last Modified: Tue, 03 Dec 2024 04:14:05 GMT  
		Size: 99.4 KB (99374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b4ba328975dc41fbbd97e521fa416f0ba61388e06215adac680d504b8c110e`  
		Last Modified: Tue, 03 Dec 2024 04:14:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c9850d59b3c32b0060fcebf8e5a86123aeccb9f5d4f2ee4dd4d8d35951ead`  
		Last Modified: Tue, 03 Dec 2024 04:14:06 GMT  
		Size: 41.4 MB (41350001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d567022c96a29e59c406eadd309fde18ada5e8c173f57053f873875f8f7930d`  
		Last Modified: Tue, 03 Dec 2024 04:14:06 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c691120bc9ec3e23b564749cc4083f48ef2a5e46d50490cab818af0966512a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eb85fc081723015864f739973269bec9c437e614167fe8f4094eae370b8a10`

```dockerfile
```

-	Layers:
	-	`sha256:7350fb0515b510d03ca20474209976a6034d8599c0254f86d3077c05b563e25f`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 3.5 MB (3467250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5189496a205fc0b5adab44ba885a919654391a96b68ef7f895ffb3cbb91c9e`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:6b68cf5376a96ca02f3bf1a3576fad497956e27847d962dc3fecee27f000a5d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:b5cd9b6eecb6cb35a6973f6d252174d4a72a1015c672dd92b46e75c5bc9d7d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96536188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e412be3564bff4f564fddfd1b89d1e49e6f48323252a88dbde1671aa72496af`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:aeac27478226649c22e51cb4b9b7d0bbf1bcb07b6a89364d409f6d475d623a7c`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6409512f9790cef6c4acd129171f99c0dd5f4889497930a8c2b275b8374576`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 7.7 MB (7680135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfe15d87d04830d229f5334b5ed619bbb619763c0b9473a8cd6d6a9079d96d`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 392.1 KB (392098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b873ee4276dd9ce08cbb14837a6681f6839ddfde623b086118334539aa706a92`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 76.2 KB (76245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca480e3256faac540bd4422e74fc1e6d2d13c9373c10056099210110f83ca158`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c551858f2b7624b7af6a49ceb3f9f797cd6e82e56839bb593c5b9f16e423a7f`  
		Last Modified: Tue, 03 Dec 2024 02:29:56 GMT  
		Size: 60.2 MB (60150689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980f15e272b878a4bc343bdeddcd4c39c02960920358ff43872ae957f5fa5c50`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1b8971e38622f856a28ca2bf0e4d5975e899bdf3c7d93d3363905a03dee86a`  
		Last Modified: Tue, 03 Dec 2024 02:29:56 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03b8f6daac5ca4f069bcf99fa55bd22d5030accb971ef36d4f20846f364cb6`  
		Last Modified: Tue, 03 Dec 2024 02:29:56 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d5a15b15e2c4911d2703d7f86c3d59e9c7b908a224fc595c800ad97d8a51a`  
		Last Modified: Tue, 03 Dec 2024 02:29:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:afcf99778e416de9d027588de388e0d4bce5c7581e5ff75449a1d3fda1d3470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3769903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bf7fedb1942428e94dc88562723eee5b3b00ec59016b804065d204de7853c9`

```dockerfile
```

-	Layers:
	-	`sha256:b6680d21641045f93ca0cc5c9dfef06c7e284b14358ca6e00099dae92b271534`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 3.7 MB (3738711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d92b6e99d67c5590e2085f7590925ef229ca3c9feba7ff45ad40cdf2f71f24`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:822a021f423f46abd6fb6c4e6e547bf9bc0440460b5d4b99860a5e9053fbb692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97176895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbfe7feb34135430e2077ef64ff3729705a491dab74620dae23541e0922e658`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:188faad6202cbc6810f8bed8fd33cb94decb320dbbab9d7a9769636467beef60`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eec4a9f8fe004f1f1971bc1cc9504334f3dd5c1229e309fea6d28ec45d791d`  
		Last Modified: Tue, 12 Nov 2024 11:23:32 GMT  
		Size: 59.9 MB (59934433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8021b7422c76a4b10e845eab46ce231be63d1cb8bb8ec42b396b4be7d300ab7c`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615a9bc9770d409332e1bb6bbad76c5d4d47210e95c72ac0d43e1ce3a4e93a47`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7822e36b6a8dea3df36dd32e7cf73fe4622c3596db066f8060dfe6ce9e71a26`  
		Last Modified: Tue, 12 Nov 2024 11:23:31 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c11ac39256ff378a42c6e09a3e6e404069e69161eaf41a67d9b3bc24405613`  
		Last Modified: Tue, 12 Nov 2024 11:23:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:41435abe620c20aa0a168dfa8bb9ba53c540f52a34cef82888099b2370887e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4265801018d143ce31b15234085a2557b59ea75b2754dc12cf3d545135223925`

```dockerfile
```

-	Layers:
	-	`sha256:0a602319071a09c1941424546a7e8cf0f2b91cc328355d36d3d3e27a56256348`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 3.7 MB (3740227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcdf52b8d53806f81c2abf26e1e31550afafcc57976fc9be00a0a37a8506463b`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:566ad00a547f8cf73ee34234b2e496d3a1963973e487e416ba594b2431d51aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103917264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b853565bb2b3b4ecaeb7acbce0d4e64140783444d7298127aa388110fe94d56e`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bb2d0d6a96e0df1e64c6768058ba160ece9975ff41e747051744754a6602ac`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78490fd3e69ce38a495f7047ae8ed194959ec3f187a1ebfc990078722eae4362`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 8.9 MB (8890074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce01cb959b4fd862b60ae9837737c8ae2a0a17ad33e6c5971ac58b7e8068b1fc`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 444.7 KB (444666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c581212b5869c39bf5e3ecfba5232c2e6bd76f5314b89bee947fab2fb08535f`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 76.3 KB (76288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68175198b4e73d464d85218d95d1eb1f61316be8f306012d91e6674ef178c8b6`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b778ca3ac5159edb66416242074844e33086e769010222e9ae5bdbdb8efe66`  
		Last Modified: Tue, 12 Nov 2024 08:32:37 GMT  
		Size: 61.4 MB (61375448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4748275adde2dd6d571701074dee9d145b1826b47736443a7cda4aec44feafe8`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb300b001a0b8870a23250ca36ad63779ea1d7680fe6f3e194278916f85a2ca`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf6ae42c56873bcbb40d3d2a1a133c74dc5620616b14e4c81ab1e760651ceac`  
		Last Modified: Tue, 12 Nov 2024 08:32:36 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f6b7552bd2cfec853bf4223af75fa9da30bab35ce5eab4ea0bcc9bf30393`  
		Last Modified: Tue, 12 Nov 2024 08:32:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca42a705b9a242c3dc3df7d360d738a6f72b0c876655b2790b0dacd158d6e064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c28cf2c0195d25a74c4a91196a397496dbc660faa89953159ada59907f6c34`

```dockerfile
```

-	Layers:
	-	`sha256:95e9d15956bddda1858f37d80eb7c1da71110ad01af698fdca041f76596c5ffa`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 3.7 MB (3744462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c729809f0ae8c11a05e787e501746039c4f11b2995e85e66e1a94919a87b38c3`  
		Last Modified: Tue, 12 Nov 2024 08:32:33 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:9c4030647878ff41f311d4964084f18ff493acd06caaf1d725137b3add9e7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93251352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eece92425c40e8ea0b4833a37fdb9fc3a80a0aa8db4f2b0bd855f551f4d7e1e`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:61ac4ac6be1258a9d827afd7b8e955ac4332e2c629e1f56b6935f4e6af725f53`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5344b7559c1da221d8e84f994f10facb90dca5708a3600ef780f07afbc5b5a8`  
		Last Modified: Tue, 03 Dec 2024 04:15:10 GMT  
		Size: 58.7 MB (58740427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc4e46d45d0b767c95523551630aa0fea0f80d6e2962832ac992308271cda51`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e6e966b751d91206d065a25b8dfda9b157e0bc4980c2a43400a7f096e91fcc`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90698981597570a1303bb8bfacd17fcd5358e901919dc48b135922a8fe861e94`  
		Last Modified: Tue, 03 Dec 2024 04:15:10 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef56adbb737c2b158513a37f5e17dcc4a9ae2a146a79c3f19d3cadece4cb644`  
		Last Modified: Tue, 03 Dec 2024 04:15:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:4a671d8334093b4a8302dfd75ffb24f2b74ff246b176146e69fe1e76a3ba5168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3768991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796c3a6000546c6a7934afb084e7f97d97a680089d7c3f19e6615499969a4992`

```dockerfile
```

-	Layers:
	-	`sha256:9d7e3a01037cc67c312002cc039ec4df2216c09689fbf15deeb5085b9f322019`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 3.7 MB (3737799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c461c8d3fe66afc3f1e2450d84529d0e9c5d8afbec0eb3ce613f66b2b4fe7d8f`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:6b68cf5376a96ca02f3bf1a3576fad497956e27847d962dc3fecee27f000a5d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:b5cd9b6eecb6cb35a6973f6d252174d4a72a1015c672dd92b46e75c5bc9d7d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96536188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e412be3564bff4f564fddfd1b89d1e49e6f48323252a88dbde1671aa72496af`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:aeac27478226649c22e51cb4b9b7d0bbf1bcb07b6a89364d409f6d475d623a7c`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6409512f9790cef6c4acd129171f99c0dd5f4889497930a8c2b275b8374576`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 7.7 MB (7680135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfe15d87d04830d229f5334b5ed619bbb619763c0b9473a8cd6d6a9079d96d`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 392.1 KB (392098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b873ee4276dd9ce08cbb14837a6681f6839ddfde623b086118334539aa706a92`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 76.2 KB (76245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca480e3256faac540bd4422e74fc1e6d2d13c9373c10056099210110f83ca158`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c551858f2b7624b7af6a49ceb3f9f797cd6e82e56839bb593c5b9f16e423a7f`  
		Last Modified: Tue, 03 Dec 2024 02:29:56 GMT  
		Size: 60.2 MB (60150689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980f15e272b878a4bc343bdeddcd4c39c02960920358ff43872ae957f5fa5c50`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1b8971e38622f856a28ca2bf0e4d5975e899bdf3c7d93d3363905a03dee86a`  
		Last Modified: Tue, 03 Dec 2024 02:29:56 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03b8f6daac5ca4f069bcf99fa55bd22d5030accb971ef36d4f20846f364cb6`  
		Last Modified: Tue, 03 Dec 2024 02:29:56 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d5a15b15e2c4911d2703d7f86c3d59e9c7b908a224fc595c800ad97d8a51a`  
		Last Modified: Tue, 03 Dec 2024 02:29:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:afcf99778e416de9d027588de388e0d4bce5c7581e5ff75449a1d3fda1d3470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3769903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bf7fedb1942428e94dc88562723eee5b3b00ec59016b804065d204de7853c9`

```dockerfile
```

-	Layers:
	-	`sha256:b6680d21641045f93ca0cc5c9dfef06c7e284b14358ca6e00099dae92b271534`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 3.7 MB (3738711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d92b6e99d67c5590e2085f7590925ef229ca3c9feba7ff45ad40cdf2f71f24`  
		Last Modified: Tue, 03 Dec 2024 02:29:55 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:822a021f423f46abd6fb6c4e6e547bf9bc0440460b5d4b99860a5e9053fbb692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97176895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbfe7feb34135430e2077ef64ff3729705a491dab74620dae23541e0922e658`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:188faad6202cbc6810f8bed8fd33cb94decb320dbbab9d7a9769636467beef60`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eec4a9f8fe004f1f1971bc1cc9504334f3dd5c1229e309fea6d28ec45d791d`  
		Last Modified: Tue, 12 Nov 2024 11:23:32 GMT  
		Size: 59.9 MB (59934433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8021b7422c76a4b10e845eab46ce231be63d1cb8bb8ec42b396b4be7d300ab7c`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615a9bc9770d409332e1bb6bbad76c5d4d47210e95c72ac0d43e1ce3a4e93a47`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7822e36b6a8dea3df36dd32e7cf73fe4622c3596db066f8060dfe6ce9e71a26`  
		Last Modified: Tue, 12 Nov 2024 11:23:31 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c11ac39256ff378a42c6e09a3e6e404069e69161eaf41a67d9b3bc24405613`  
		Last Modified: Tue, 12 Nov 2024 11:23:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:41435abe620c20aa0a168dfa8bb9ba53c540f52a34cef82888099b2370887e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4265801018d143ce31b15234085a2557b59ea75b2754dc12cf3d545135223925`

```dockerfile
```

-	Layers:
	-	`sha256:0a602319071a09c1941424546a7e8cf0f2b91cc328355d36d3d3e27a56256348`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 3.7 MB (3740227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcdf52b8d53806f81c2abf26e1e31550afafcc57976fc9be00a0a37a8506463b`  
		Last Modified: Tue, 12 Nov 2024 11:23:30 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:566ad00a547f8cf73ee34234b2e496d3a1963973e487e416ba594b2431d51aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103917264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b853565bb2b3b4ecaeb7acbce0d4e64140783444d7298127aa388110fe94d56e`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bb2d0d6a96e0df1e64c6768058ba160ece9975ff41e747051744754a6602ac`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78490fd3e69ce38a495f7047ae8ed194959ec3f187a1ebfc990078722eae4362`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 8.9 MB (8890074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce01cb959b4fd862b60ae9837737c8ae2a0a17ad33e6c5971ac58b7e8068b1fc`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 444.7 KB (444666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c581212b5869c39bf5e3ecfba5232c2e6bd76f5314b89bee947fab2fb08535f`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 76.3 KB (76288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68175198b4e73d464d85218d95d1eb1f61316be8f306012d91e6674ef178c8b6`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b778ca3ac5159edb66416242074844e33086e769010222e9ae5bdbdb8efe66`  
		Last Modified: Tue, 12 Nov 2024 08:32:37 GMT  
		Size: 61.4 MB (61375448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4748275adde2dd6d571701074dee9d145b1826b47736443a7cda4aec44feafe8`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb300b001a0b8870a23250ca36ad63779ea1d7680fe6f3e194278916f85a2ca`  
		Last Modified: Tue, 12 Nov 2024 08:32:35 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf6ae42c56873bcbb40d3d2a1a133c74dc5620616b14e4c81ab1e760651ceac`  
		Last Modified: Tue, 12 Nov 2024 08:32:36 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f6b7552bd2cfec853bf4223af75fa9da30bab35ce5eab4ea0bcc9bf30393`  
		Last Modified: Tue, 12 Nov 2024 08:32:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ca42a705b9a242c3dc3df7d360d738a6f72b0c876655b2790b0dacd158d6e064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c28cf2c0195d25a74c4a91196a397496dbc660faa89953159ada59907f6c34`

```dockerfile
```

-	Layers:
	-	`sha256:95e9d15956bddda1858f37d80eb7c1da71110ad01af698fdca041f76596c5ffa`  
		Last Modified: Tue, 12 Nov 2024 08:32:34 GMT  
		Size: 3.7 MB (3744462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c729809f0ae8c11a05e787e501746039c4f11b2995e85e66e1a94919a87b38c3`  
		Last Modified: Tue, 12 Nov 2024 08:32:33 GMT  
		Size: 31.2 KB (31236 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:9c4030647878ff41f311d4964084f18ff493acd06caaf1d725137b3add9e7a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93251352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eece92425c40e8ea0b4833a37fdb9fc3a80a0aa8db4f2b0bd855f551f4d7e1e`
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
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:61ac4ac6be1258a9d827afd7b8e955ac4332e2c629e1f56b6935f4e6af725f53`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5344b7559c1da221d8e84f994f10facb90dca5708a3600ef780f07afbc5b5a8`  
		Last Modified: Tue, 03 Dec 2024 04:15:10 GMT  
		Size: 58.7 MB (58740427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc4e46d45d0b767c95523551630aa0fea0f80d6e2962832ac992308271cda51`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e6e966b751d91206d065a25b8dfda9b157e0bc4980c2a43400a7f096e91fcc`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90698981597570a1303bb8bfacd17fcd5358e901919dc48b135922a8fe861e94`  
		Last Modified: Tue, 03 Dec 2024 04:15:10 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef56adbb737c2b158513a37f5e17dcc4a9ae2a146a79c3f19d3cadece4cb644`  
		Last Modified: Tue, 03 Dec 2024 04:15:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:4a671d8334093b4a8302dfd75ffb24f2b74ff246b176146e69fe1e76a3ba5168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3768991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796c3a6000546c6a7934afb084e7f97d97a680089d7c3f19e6615499969a4992`

```dockerfile
```

-	Layers:
	-	`sha256:9d7e3a01037cc67c312002cc039ec4df2216c09689fbf15deeb5085b9f322019`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 3.7 MB (3737799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c461c8d3fe66afc3f1e2450d84529d0e9c5d8afbec0eb3ce613f66b2b4fe7d8f`  
		Last Modified: Tue, 03 Dec 2024 04:15:09 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

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

### `couchdb:3.4` - linux; amd64

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

### `couchdb:3.4` - unknown; unknown

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

### `couchdb:3.4` - linux; arm64 variant v8

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

### `couchdb:3.4` - unknown; unknown

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

### `couchdb:3.4` - linux; s390x

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

### `couchdb:3.4` - unknown; unknown

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

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:732c1da782a9fafe5c94e4fc05b247360bbf07c2f38f48730b61cd29335a18fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:ee3c19ed84984c039b2aed6c9778f961d9d93f68e527d7430ddecad8f3a1e6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155342527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303b5c2e55f983b7ee77545598858abd612b8be35e8f84bd91fd671257dfa9f8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b98581970ff034bd529aa26ca12985e1754b525da12b09d70af3afd68237dec`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad44d7c547c5b4af935adb2d65f110daa2908d5e03b73bf0ab7586b3d9508055`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 7.7 MB (7680091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56274944153676d0005183f9e215ec98e6e7472eddc5cf21529268cdd42779ac`  
		Last Modified: Tue, 03 Dec 2024 02:30:14 GMT  
		Size: 77.3 MB (77283848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2ce4fc68f42259f450845e7d641d1dacce777d2e5a8e84f4c962ce84b1d317`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 415.0 KB (414979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369ef73f7e71d1762b7655789406b41950edaa9d021d59fcbcd99437c9290b1`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 99.3 KB (99275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2357ef9f7a1531b8f41bbb206494d4830505a15cb69eb5692cd61b76c0e54d`  
		Last Modified: Tue, 03 Dec 2024 02:30:15 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279b904e61f002e3c6e6a1291643a131b5e7baa407204a1b3cd7d0a1b3c93389`  
		Last Modified: Tue, 03 Dec 2024 02:30:16 GMT  
		Size: 41.6 MB (41630870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec70c3c80f6e9ae7f7a2020188828dc2c2126616bf7f67a70f2abc6c5a57e984`  
		Last Modified: Tue, 03 Dec 2024 02:30:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:cf1cbbc70dcd900a27e44cbca90120d8ec57695a3ca1d26e28182a6f3edc5b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b307ee6fcc8d74c05f3f3c53b8e833866b239892d62ed652b73dc79de86b0c`

```dockerfile
```

-	Layers:
	-	`sha256:6d4feac5f0676816359cf6e4ed69fef2b22e74a88f239b1beda607fb80e24a5a`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 3.5 MB (3473837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ddb8926a39928e1bef08870795effae205dc9ba496060f6eed74d82a1799eb`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f71f156d8ea97ac5a1a9d3428b6801a2314b2d51d027603df62086928167d1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155395393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea534a63294b54cdb4032044b38258ef0b217c1d24baab024a67b410ab8e019`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f27311cf459d2dcc491d124b0207b7ddb24b839cd838dc8ac4e0f59546cdc`  
		Last Modified: Tue, 12 Nov 2024 11:22:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136edbc8e932535e5b082121b430f39e8c59a9b5414da4be2512971d1ac1164f`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 7.7 MB (7654500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5cb31d0cc00c24636b47d511f24d67bb61941038936f91922dc2e1a5bdbfb`  
		Last Modified: Tue, 12 Nov 2024 11:22:48 GMT  
		Size: 76.6 MB (76583825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6b710de5abf310302d33c0dfc43afcd7f8eadfd3e6c328c61aa277044d8d76`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 371.7 KB (371716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268db4a4b80fa4e519d1a26fa5d6382df8df33e19d63f21dc3bdb09b53dc56f2`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 99.2 KB (99243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3a2582a518b4000dd7ef5c817f5319a8c2d678c2fab8196e7051e02d2168a4`  
		Last Modified: Tue, 12 Nov 2024 11:22:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2454d2f2a5242fdfd6712fbea60eb15cb3d6cbd208f47691102354250262809`  
		Last Modified: Tue, 12 Nov 2024 11:22:49 GMT  
		Size: 41.5 MB (41526874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b879b3c3e60af5a96bea846d460ec7217b4bd814982062edeae65e9549be48f`  
		Last Modified: Tue, 12 Nov 2024 11:22:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1660b8bda29f20af133467684cfd3a71c475ab15f0bbc39cbb100bf3fedfb0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b679c5b6fb5420330b007be7aa6a7de72ad81cc10e91e719a2295a571ac8952b`

```dockerfile
```

-	Layers:
	-	`sha256:41b0d5c1a70050cdf819efb713cfc261f7eea26141463ca09930433b73849ddd`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 3.5 MB (3473758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d7d86a4e50de07693ded530d5eed50c87e65a758234937458b013c3af30693`  
		Last Modified: Tue, 12 Nov 2024 11:22:46 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:78b2608987f018fac2cd4759f3c5f66568433802fbea35b0f2ee4cbf946d5d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148967286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1882582f22070e4df3f0856060c2cc693cf367b521c6f911633590a8ce060b72`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd2d074f21bdd203a2fd183cffe3e3815c3d9d940d57fed8bc55c74741e400e`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354a85114ee6eb212fc2c26419f60433aa0ef174d027d581cf3702301d73f88c`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 7.2 MB (7194578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1071a9e3021abb79a6c6b4da3028cbb55bc209fabbf7d15d78c44b418261b076`  
		Last Modified: Tue, 03 Dec 2024 04:14:07 GMT  
		Size: 73.1 MB (73064424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ac56c18e58424283065b984082e48f090c2bc9760fc9c888a6bfa2154bb70b`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 378.1 KB (378058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142d0b872098335016954848d7bb541f1aaa55f65761a42e4530519237a19f0d`  
		Last Modified: Tue, 03 Dec 2024 04:14:05 GMT  
		Size: 99.4 KB (99374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b4ba328975dc41fbbd97e521fa416f0ba61388e06215adac680d504b8c110e`  
		Last Modified: Tue, 03 Dec 2024 04:14:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c9850d59b3c32b0060fcebf8e5a86123aeccb9f5d4f2ee4dd4d8d35951ead`  
		Last Modified: Tue, 03 Dec 2024 04:14:06 GMT  
		Size: 41.4 MB (41350001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d567022c96a29e59c406eadd309fde18ada5e8c173f57053f873875f8f7930d`  
		Last Modified: Tue, 03 Dec 2024 04:14:06 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c691120bc9ec3e23b564749cc4083f48ef2a5e46d50490cab818af0966512a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eb85fc081723015864f739973269bec9c437e614167fe8f4094eae370b8a10`

```dockerfile
```

-	Layers:
	-	`sha256:7350fb0515b510d03ca20474209976a6034d8599c0254f86d3077c05b563e25f`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 3.5 MB (3467250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5189496a205fc0b5adab44ba885a919654391a96b68ef7f895ffb3cbb91c9e`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2`

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

### `couchdb:3.4.2` - linux; amd64

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

### `couchdb:3.4.2` - unknown; unknown

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

### `couchdb:3.4.2` - linux; arm64 variant v8

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

### `couchdb:3.4.2` - unknown; unknown

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

### `couchdb:3.4.2` - linux; s390x

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

### `couchdb:3.4.2` - unknown; unknown

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

## `couchdb:3.4.2-nouveau`

```console
$ docker pull couchdb@sha256:732c1da782a9fafe5c94e4fc05b247360bbf07c2f38f48730b61cd29335a18fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:ee3c19ed84984c039b2aed6c9778f961d9d93f68e527d7430ddecad8f3a1e6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155342527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303b5c2e55f983b7ee77545598858abd612b8be35e8f84bd91fd671257dfa9f8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b98581970ff034bd529aa26ca12985e1754b525da12b09d70af3afd68237dec`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad44d7c547c5b4af935adb2d65f110daa2908d5e03b73bf0ab7586b3d9508055`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 7.7 MB (7680091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56274944153676d0005183f9e215ec98e6e7472eddc5cf21529268cdd42779ac`  
		Last Modified: Tue, 03 Dec 2024 02:30:14 GMT  
		Size: 77.3 MB (77283848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2ce4fc68f42259f450845e7d641d1dacce777d2e5a8e84f4c962ce84b1d317`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 415.0 KB (414979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369ef73f7e71d1762b7655789406b41950edaa9d021d59fcbcd99437c9290b1`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 99.3 KB (99275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2357ef9f7a1531b8f41bbb206494d4830505a15cb69eb5692cd61b76c0e54d`  
		Last Modified: Tue, 03 Dec 2024 02:30:15 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279b904e61f002e3c6e6a1291643a131b5e7baa407204a1b3cd7d0a1b3c93389`  
		Last Modified: Tue, 03 Dec 2024 02:30:16 GMT  
		Size: 41.6 MB (41630870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec70c3c80f6e9ae7f7a2020188828dc2c2126616bf7f67a70f2abc6c5a57e984`  
		Last Modified: Tue, 03 Dec 2024 02:30:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:cf1cbbc70dcd900a27e44cbca90120d8ec57695a3ca1d26e28182a6f3edc5b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b307ee6fcc8d74c05f3f3c53b8e833866b239892d62ed652b73dc79de86b0c`

```dockerfile
```

-	Layers:
	-	`sha256:6d4feac5f0676816359cf6e4ed69fef2b22e74a88f239b1beda607fb80e24a5a`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 3.5 MB (3473837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ddb8926a39928e1bef08870795effae205dc9ba496060f6eed74d82a1799eb`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f71f156d8ea97ac5a1a9d3428b6801a2314b2d51d027603df62086928167d1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155395393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea534a63294b54cdb4032044b38258ef0b217c1d24baab024a67b410ab8e019`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51f27311cf459d2dcc491d124b0207b7ddb24b839cd838dc8ac4e0f59546cdc`  
		Last Modified: Tue, 12 Nov 2024 11:22:46 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136edbc8e932535e5b082121b430f39e8c59a9b5414da4be2512971d1ac1164f`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 7.7 MB (7654500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b5cb31d0cc00c24636b47d511f24d67bb61941038936f91922dc2e1a5bdbfb`  
		Last Modified: Tue, 12 Nov 2024 11:22:48 GMT  
		Size: 76.6 MB (76583825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6b710de5abf310302d33c0dfc43afcd7f8eadfd3e6c328c61aa277044d8d76`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 371.7 KB (371716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268db4a4b80fa4e519d1a26fa5d6382df8df33e19d63f21dc3bdb09b53dc56f2`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 99.2 KB (99243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3a2582a518b4000dd7ef5c817f5319a8c2d678c2fab8196e7051e02d2168a4`  
		Last Modified: Tue, 12 Nov 2024 11:22:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2454d2f2a5242fdfd6712fbea60eb15cb3d6cbd208f47691102354250262809`  
		Last Modified: Tue, 12 Nov 2024 11:22:49 GMT  
		Size: 41.5 MB (41526874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b879b3c3e60af5a96bea846d460ec7217b4bd814982062edeae65e9549be48f`  
		Last Modified: Tue, 12 Nov 2024 11:22:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1660b8bda29f20af133467684cfd3a71c475ab15f0bbc39cbb100bf3fedfb0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b679c5b6fb5420330b007be7aa6a7de72ad81cc10e91e719a2295a571ac8952b`

```dockerfile
```

-	Layers:
	-	`sha256:41b0d5c1a70050cdf819efb713cfc261f7eea26141463ca09930433b73849ddd`  
		Last Modified: Tue, 12 Nov 2024 11:22:47 GMT  
		Size: 3.5 MB (3473758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d7d86a4e50de07693ded530d5eed50c87e65a758234937458b013c3af30693`  
		Last Modified: Tue, 12 Nov 2024 11:22:46 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:78b2608987f018fac2cd4759f3c5f66568433802fbea35b0f2ee4cbf946d5d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148967286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1882582f22070e4df3f0856060c2cc693cf367b521c6f911633590a8ce060b72`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd2d074f21bdd203a2fd183cffe3e3815c3d9d940d57fed8bc55c74741e400e`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354a85114ee6eb212fc2c26419f60433aa0ef174d027d581cf3702301d73f88c`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 7.2 MB (7194578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1071a9e3021abb79a6c6b4da3028cbb55bc209fabbf7d15d78c44b418261b076`  
		Last Modified: Tue, 03 Dec 2024 04:14:07 GMT  
		Size: 73.1 MB (73064424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ac56c18e58424283065b984082e48f090c2bc9760fc9c888a6bfa2154bb70b`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 378.1 KB (378058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142d0b872098335016954848d7bb541f1aaa55f65761a42e4530519237a19f0d`  
		Last Modified: Tue, 03 Dec 2024 04:14:05 GMT  
		Size: 99.4 KB (99374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b4ba328975dc41fbbd97e521fa416f0ba61388e06215adac680d504b8c110e`  
		Last Modified: Tue, 03 Dec 2024 04:14:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c9850d59b3c32b0060fcebf8e5a86123aeccb9f5d4f2ee4dd4d8d35951ead`  
		Last Modified: Tue, 03 Dec 2024 04:14:06 GMT  
		Size: 41.4 MB (41350001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d567022c96a29e59c406eadd309fde18ada5e8c173f57053f873875f8f7930d`  
		Last Modified: Tue, 03 Dec 2024 04:14:06 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c691120bc9ec3e23b564749cc4083f48ef2a5e46d50490cab818af0966512a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eb85fc081723015864f739973269bec9c437e614167fe8f4094eae370b8a10`

```dockerfile
```

-	Layers:
	-	`sha256:7350fb0515b510d03ca20474209976a6034d8599c0254f86d3077c05b563e25f`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 3.5 MB (3467250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5189496a205fc0b5adab44ba885a919654391a96b68ef7f895ffb3cbb91c9e`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

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
