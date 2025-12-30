<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.3`](#couchdb343)
-	[`couchdb:3.4.3-nouveau`](#couchdb343-nouveau)
-	[`couchdb:3.5`](#couchdb35)
-	[`couchdb:3.5-nouveau`](#couchdb35-nouveau)
-	[`couchdb:3.5.1`](#couchdb351)
-	[`couchdb:3.5.1-nouveau`](#couchdb351-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:3d5bc0a2ccb6556a6361cf8b4c7f215568fb0c0c2e5e8b44a747e1c138d99f7c
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
$ docker pull couchdb@sha256:57747ae2592b8ae8d17570494997c77e08aa7c6ec62ed426450d6dfaf2376b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727998b01b6d8db683ee8be2225c8b90d4182c30f86a59804115f4f81f15dc02`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:49:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:49:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:49:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:34 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 29 Dec 2025 23:49:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:46 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:49:46 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:49:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4da247384f3a99a20316fa166611c05b44fed7084eee310097ef1bdf514ba1`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166803e3fb395174c7c6adb5b75a40fab348e7ad68c4d66fb29b38bd709b2328`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 7.9 MB (7881766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfd08eb3284da772851758bd24632fbec89654d005465f4dfd980de4f7782`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 401.7 KB (401735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2aa3f63c0336e55777f05c65b0159f362bed7c1136eea5b0d9a8b44c04edc9d`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1be06be76b3897be7a41d4f6b6600f8f57490148abaf6472a4a8f0b2e56f2c`  
		Last Modified: Mon, 29 Dec 2025 23:50:12 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eefaa2cb4295681c6d96e4651fc485b07576b6a49711537a4a9f7283c42d94`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 105.5 MB (105457507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bd50c1024430503d97929bd6c7f0e389cb97fb1f2b3efd533f8b12de73bb22`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc660b6f24ee1a1a2c684fece0e6b7e0e02708724ce97da0a1f58d771ce32804`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1e239747f1b31084c3b43aee1c52536bcd8e41683da6d3e026067bf689cb3`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217819c94f97a81240ad47bd6d273fdf925ebaffb575e29a58865407d218f24b`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:793cd5d70d6987512f3de95cabd0dd75cdbd4b487f634d39204cca0c1259a5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea258ab00932437927460b3cb8c30d5021b781de8b83edfc3a03f547a60f94a`

```dockerfile
```

-	Layers:
	-	`sha256:d809f4ab990a6df7902a9088b2c15dd392c546dfb1dd9ecf6363cbcd8c258029`  
		Last Modified: Tue, 30 Dec 2025 02:34:08 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc7673097a4e547638a4434f9e9e888c882666dd9cac92ba358aef897409fc4`  
		Last Modified: Tue, 30 Dec 2025 02:34:09 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:681cd28217f5c317b9dc604f4246b8ee2e74a0eb6a4000b8739feb9b7428e8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141402906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6697230efc8f63d0880368053b055920186cc1a1bb1d0f656ad22c18bef25817`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:50:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:11 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 29 Dec 2025 23:50:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:50:23 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:50:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:50:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b28ac2949ff03d076b0d9c8f249d200b4bcf69165d413df5502ba3aaedf454`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dc6e1e29e7d607633a85bf66afea8f8890b3226d4e4624d67d98c4f64d2136`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c6ff449448e94fe2f6b83744855d7a4a51a68b9d1728d1862611e369a3df3b`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 370.5 KB (370489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cba339223745b3fd888daac1058d4ff730fe2d6f54b4dcc9447e9c8595a3519`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 76.5 KB (76463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539a2e947f04a8b08f17c261fffdef51bea21f220fa11e105a8859cce21f5d97`  
		Last Modified: Mon, 29 Dec 2025 23:50:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0623f96358d425f7c7c6e980fedd8edceec5093234fb6a47ed07223fc9610bac`  
		Last Modified: Mon, 29 Dec 2025 23:50:54 GMT  
		Size: 105.2 MB (105156261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c021dc14d00d1a5fa4b9aaabdb81fe6ee4b1eb8f7a7b803ff162b91259d532`  
		Last Modified: Mon, 29 Dec 2025 23:50:45 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227cb5d0e30b21b406c667ff03bf98fa15752b945418b4ff82ee27ae46ed1529`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded008b35a0d5d4f3da488006d2392e90f0159a48a34f52653bdfa9873ecc907`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a57cc7e2430c4170e48f2795917639ec5d0543504bba350447c5d07529915`  
		Last Modified: Mon, 29 Dec 2025 23:50:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f28093eee8046a743326e6ea677710c47e6d47e0bef6a915df0f6cbb83b2f29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967244bafb8f7690bf989609244cb13370aeb40e1d932ca4112055c2e1130d8`

```dockerfile
```

-	Layers:
	-	`sha256:0fb14dcfda03d85402b1dc4c686e205162a70c96082e9a1e2d5d2b04164d5836`  
		Last Modified: Tue, 30 Dec 2025 02:34:14 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66a7c455067fc1722c12cd4c459f4fcd43d8c7188963dfaf12e4a10d28ec3d1`  
		Last Modified: Tue, 30 Dec 2025 02:34:14 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:097a79b432ba83d04f56a870419464b2ae0012c7d22f3571be335cbe6fb1ae48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138764692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b664edaedd041921a1c187dce4b4ec17c8431ad36619bb30ccce7799916ec14`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 30 Dec 2025 00:43:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:16 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 30 Dec 2025 00:43:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Dec 2025 00:43:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 00:43:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:43:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Dec 2025 00:43:33 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 30 Dec 2025 00:43:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2c212caeb4bbcbc1a2aae869143027f520be5caa1135a217e767121ac1626f`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d04e9f82f45a67b46af862374c24224a6717000183ace0e83d43c9ea4933`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef43570a8365ddd2c2f530578f7ab6932ad0954dae69973159ba5e7e7dd29895`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 372.1 KB (372097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8d5ab8f8d42dae898c00fd1281dbb1c3495bb8300bae20147a7a55b5eeb20`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 76.4 KB (76448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cc6d8fa43d6a9106826c6d5bdcca5ddae9593536e39f608bd43fce2d9d5ba6`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe85005dced89895410b4c8872001a3b45d39077d67a253350bed39bf5131fc`  
		Last Modified: Tue, 30 Dec 2025 00:44:08 GMT  
		Size: 104.0 MB (104028236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7332b0b429f7a79fa4a9fc758b1f9691c3233b407385a6c2b9f2d0733e76d0`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377fda69dd4b138b08a08a414245a50daddd123c4777a6f603bc1250e4019fd`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f22f88c0a1beaede0681cf9efc3c9317c306f909002e24fb8f7f77ecc34a67f`  
		Last Modified: Tue, 30 Dec 2025 00:44:06 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68718752dcb618d114c82c2fba317c2a114392ae48854bba56a3aadbc75638ef`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:eff806d92f51590b41ba5bdc2564371adc66e1a4f6cc58d721e2d568d6ecd098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631566cdecdf5917d0fac5cef60417037a118a84354956afcac4de6f686aaaed`

```dockerfile
```

-	Layers:
	-	`sha256:cc24a91e945ce3d8b13559abd0468a49b0ce07e30f51f7063ea09b3f0d87b262`  
		Last Modified: Tue, 30 Dec 2025 02:34:19 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628f341500f6aec75f6745a857d74bdb9a9195dd735eb380666fbd2806ded2ee`  
		Last Modified: Tue, 30 Dec 2025 02:34:20 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:75bd21043980a7c636db8fd5d9d34c04518e3569c508c6ac54450c0949ec1834
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
$ docker pull couchdb@sha256:945e91e36f9f38dcc47025f11172e42a6abbbfdde757ea61607c4c8f9551ef1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd621b26d0f78da92f822e9161d6dcfefca8b7ea7ddabc7bfc311f7016bbb42`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:50 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:49:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:07 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:11 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:11 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:50:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:50:16 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:50:16 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:50:16 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:50:16 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dce4d2e8558c65ac1a60bc4200e439914980222a984f7999b7e74fc9b9e096c`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11d07e7d5c34a4f71e53f4dea48fc87aa684955ad01811329ed31f971bb2595`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 7.9 MB (7881778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec04402a7ca12958aadb841d478898ce974a783d8116ee07dce19e043d004037`  
		Last Modified: Mon, 29 Dec 2025 23:50:49 GMT  
		Size: 77.4 MB (77380629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6012f4a39813fae020f5b8f76b083fbb7c2a67816dff05129004b04c3b73827e`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 424.1 KB (424119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe66f4fc85b301fc3c3f8b7343ec158d096764c6dee5ca9027fd1b30dc2425ca`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 99.5 KB (99544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539a2e947f04a8b08f17c261fffdef51bea21f220fa11e105a8859cce21f5d97`  
		Last Modified: Mon, 29 Dec 2025 23:50:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b286f385771164d9449e280bf59a2f6cde567285cc84620ece635778ddf5640b`  
		Last Modified: Mon, 29 Dec 2025 23:50:43 GMT  
		Size: 42.4 MB (42436413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12703b1cdcea4825887128a9e3fa26d091c0ca9b8d19b19ec60bab35e89d6381`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6c837a5252b403588cee5c772d7296bd4b26c30191dbad1ac5559f7b674384fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c476b0f2c23680324acf38341f299bc99281ebbc1b83553a63b39ea297f4c5`

```dockerfile
```

-	Layers:
	-	`sha256:191d975035ad3380ee5bddb05472a78bdbd9549adb7989db2e3fbe1a4bd835a8`  
		Last Modified: Tue, 30 Dec 2025 02:34:21 GMT  
		Size: 3.7 MB (3658089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07d8d3dda9ce39dd8b007299ab8e5d3121e860339f884d4a6c41668ae503d8b0`  
		Last Modified: Tue, 30 Dec 2025 02:34:22 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:91840d6b1935926fe3f14b1a49288ff8bd6bd6085661c1e89cc05f0f63fd9217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155319049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4699635c99aead1d1b48894edc964efa791a2812854e6d556cf58a4b35e76a90`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:50:44 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:50:44 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:50:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:51:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:51:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:51:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:51:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:51:11 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:51:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:51:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c6cf1da0cafb42ee50f87d18f1179b8852984be2493056f7be16ddf098df68`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db538f0f6e5c48b9027d3bff5b408f0fe017e37ab35ac67c64ca996e8b1404b0`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 7.7 MB (7692025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257ed1b889cb7b176bd192e80932c6d572470ea854aa905df7b9216114a71ff`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 76.7 MB (76691592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec43333135ccd6e64cb882f33fabb71b4e1950235203b6ec0de59a37d32a3f`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 392.7 KB (392710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a511da4c54a9095157b7b2afac88d338be88b8ab2d6469a086c10b2bdfd126b`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 99.5 KB (99496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43254879df398217c0ee33f79c3e968ce39762b7d711613b9a890872f8177b02`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31c5db9d396b5ffcc05a253360eb4abec4ea784b3a9968ef728c4e6c294750d`  
		Last Modified: Mon, 29 Dec 2025 23:51:40 GMT  
		Size: 42.3 MB (42339137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5101b12acc67d71aa660bf156ac871c8fcc5364639486c328b0296ed90035e`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:63d46b909ba521b811d1a9462f8e6b1ca73dfe6dc7ad1706d9fc348d43738602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa1de027c19597a14e9aaa324a4042322864394ece6ed684e9429420711e6f0`

```dockerfile
```

-	Layers:
	-	`sha256:4a98c50d58754f26fb1bb843907a35460161c4c7ee06811a830033f112ff1bd8`  
		Last Modified: Tue, 30 Dec 2025 02:34:50 GMT  
		Size: 3.7 MB (3656765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45ec36b2e4cacde6a39c456516b187e1a2121e10f77390da694fe95705c6cec`  
		Last Modified: Tue, 30 Dec 2025 02:34:51 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:34f25dc7198140c53fb22bfa1d9d8691566e97945bf0478d5b049634cbef1cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20aca295d049aaa9d83f7f4d38df7bcd57f10bfec0ec92662b774857f8dace6c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 30 Dec 2025 00:43:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:24 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:24 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
VOLUME [/opt/nouveau/data]
# Tue, 30 Dec 2025 00:43:32 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 30 Dec 2025 00:43:32 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fdcb9c0069163bb36ba9027df3a96ec4c7928ee18d1883d279ec26a42c5820`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb42e11f427e48b107230c55cac96ab07ccdd27376e019fcc1c6084aef50780`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14a25893bb2b4c129226a950762d06f8b90d4d4a7e22e31f6de27a4a5430159`  
		Last Modified: Tue, 30 Dec 2025 00:44:09 GMT  
		Size: 73.1 MB (73143182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b68b06b55e7e7e8356bae906af85409d6929283fe00bf39f5d2b4a9057e172`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 394.4 KB (394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638cc3955040ebb33ec4269a27111b9a405e3a00c154ecf7b474606b9f41cdfa`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 99.6 KB (99576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3e3277464b6a1fc279bce56940994ab65f77e016beb93511fde0151c2583a`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0eb016d52c4ffcd47aadbe7ede831dfe2c00005157bf1c8497f377d835b22e`  
		Last Modified: Tue, 30 Dec 2025 00:44:05 GMT  
		Size: 42.2 MB (42164593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d4d000f28910ea40330d82411589b03cb147de0dcac2d684961820194f7438`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:05bacf883372d85634d236f15f2ed5dd4e46ad2642a83963ddf42e177ee584f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6008de5a7a77a2f1279820fce65cd1dc0f0e43ef939bc6cd277470afbb0b64`

```dockerfile
```

-	Layers:
	-	`sha256:00590dfe8e4a2fc14816f217ae5ab95565ba4f110e0d6204a055da0a1ab780c8`  
		Last Modified: Tue, 30 Dec 2025 02:34:55 GMT  
		Size: 3.6 MB (3648618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47fdc9def5a01ac08462ee60814639d6ab42e6871584c635678abe15161d93b3`  
		Last Modified: Tue, 30 Dec 2025 02:34:56 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:8336c8e64d3b2cd0acf439d6e653c2260d1d47ba6cd5cd17805dcefbb9da9a75
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
$ docker pull couchdb@sha256:ff705d86c308fd7485e6a54de73f86d42a3744a3e33762d8385acf9b1c43894d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fe7fbed2d22259a4d00f03938b7441256e26948318ed5ab0166f38f7cd1f62`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:50:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:50:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:50:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:46 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 29 Dec 2025 23:50:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:50:58 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:50:58 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:50:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d15e83c89dc92046ce8513dbc3e5bda9e6ec47fd4b02d0c1af6931954b685`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decc9d2a3fc90a1f3aa3e95018b2c425e2607160439736446ff9755a73de1c83`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 7.9 MB (7881777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead78062f3024d361050a4dd57e09369f355deaf2110dfe07b38496992c11a38`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 401.7 KB (401748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9e092b3893df2d97f5377606f76b15dd09626ba5d9d8da382911f6b9b92d5b`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 76.5 KB (76464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdb56fc21c0d1c6f6b36f4d174b35ec9b77f05ca39f0aecbce13d0079f89467`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b3596dff6e966812ac02d50ac0ec0539c48a9494d04f5d00daf422149a2149`  
		Last Modified: Mon, 29 Dec 2025 23:51:34 GMT  
		Size: 102.4 MB (102419846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749fc13405a180b1d3bdf11ed4d5c9469b17d86305b2cd467c7e4713b84b0e06`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0772c246f95c8bb72dc56b719df9cbe2517df9e6dfc8bcab9051c2ced540e50d`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651f65add2ff5d55229d535a1dc95a3d87ab855f8d9ad755a5d4ecb91d20e8a9`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c738bc2de24a10cf4f677a191625f795dd5a86c915ccf5ad7dc71d73b9685`  
		Last Modified: Mon, 29 Dec 2025 23:51:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:2d9e30e5ae70918d1037d45b083a96ab7e355020c534158eb1a9299fb9bdfcac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef63dc917788706dfbeb8d3c213b38924954349018fc1cd17b894b556b03622d`

```dockerfile
```

-	Layers:
	-	`sha256:a4bc56fa37e526e5de3e821d93e9851df90ad0baf75df175b1cdd69032767098`  
		Last Modified: Tue, 30 Dec 2025 02:34:35 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1049d92ab51e82474e35adcfcccb8f97b87e04de1aab7916033a46be205d9f`  
		Last Modified: Tue, 30 Dec 2025 02:34:36 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6c4315e4d0879da76cf740af0d532555d08a8843d96ef46fa1f4390c2a2159ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afea235c56d6ddb5c2d33a7785c8259807e7ef6f7d2a63454e591e5afad6967d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:50:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:11 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 29 Dec 2025 23:51:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:51:22 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:51:22 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:51:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b28ac2949ff03d076b0d9c8f249d200b4bcf69165d413df5502ba3aaedf454`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dc6e1e29e7d607633a85bf66afea8f8890b3226d4e4624d67d98c4f64d2136`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c6ff449448e94fe2f6b83744855d7a4a51a68b9d1728d1862611e369a3df3b`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 370.5 KB (370489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cba339223745b3fd888daac1058d4ff730fe2d6f54b4dcc9447e9c8595a3519`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 76.5 KB (76463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9a304c88fd98a1a095b970058190641d59470b847383c00231cbeb7dd4b0a`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1028465fb7adc55111dd3714373330acd270c76449e90d5493796a80740ab5e2`  
		Last Modified: Mon, 29 Dec 2025 23:51:53 GMT  
		Size: 102.2 MB (102169013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62edd8dd5f6a2c6c4236eaee0b6b622be7c6f6f997496b011808405e6eb972cb`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154161c10d72393c1d4bec615f21aa47cfddf9dd5cc24a64c15f0aa590ea4435`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646f9a190ca129a0b88dfff9c3cf008b99b1b89047abbebee88fc7fb72bbff58`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403c66c991179d07a989d0f5e08fc43e6151ca0e03ecd4a9c8df428553fc06b5`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:ac9a231eab81eabf72172886815a01be038950b6fce4733821e496c634a1276b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc8e6f8fda7d881c233e316eb65e00a20a9b8221429b7488098a76ad2ed880d`

```dockerfile
```

-	Layers:
	-	`sha256:efc3d040364ea67491bb30744a2eebbfa8206f4cdb26bd7b3efa3e88e38023c7`  
		Last Modified: Tue, 30 Dec 2025 02:34:40 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f78e67024f1d459eabd3f8a156435aa66fa7c566d56e7b16e37369b2a11ce16`  
		Last Modified: Tue, 30 Dec 2025 02:34:41 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:3c95a6c14d50f46109834df8d741401516c2f52a948e1752943f0fd993798d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135792275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa04167d90f66de07d3a79dbbf97192ac3a6e9a20232e9b9be670ccfca557e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 30 Dec 2025 00:43:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:16 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 30 Dec 2025 00:43:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:43:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Dec 2025 00:43:31 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 30 Dec 2025 00:43:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2c212caeb4bbcbc1a2aae869143027f520be5caa1135a217e767121ac1626f`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d04e9f82f45a67b46af862374c24224a6717000183ace0e83d43c9ea4933`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef43570a8365ddd2c2f530578f7ab6932ad0954dae69973159ba5e7e7dd29895`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 372.1 KB (372097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8d5ab8f8d42dae898c00fd1281dbb1c3495bb8300bae20147a7a55b5eeb20`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 76.4 KB (76448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cc6d8fa43d6a9106826c6d5bdcca5ddae9593536e39f608bd43fce2d9d5ba6`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca396414f155ebb0cc5c0e2eb881808ccfb18cabe08693ce79317284b1d71f6`  
		Last Modified: Tue, 30 Dec 2025 00:44:10 GMT  
		Size: 101.1 MB (101055826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fc800dc53b8ae9cda89fbeb0b41e0b5207b882fa39bdf61ed97d09417aa606`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0d89e6f3b0d4950b67e2e873444f54aeb37a28056fb9ba9baad7e3ba4a2d68`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541180d05fb42aee984cf5a975a407188af79f0bd0306f7db2127186f10f52aa`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed479a1ef0723c916a94c51ef27883d9f625c018d1be1cb44c98ec55f078cef`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:3061116c8f6ab2863431089e4b23a5fc50c156c292c89df3edc6f90635fc2a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771b824c652cdb39dd1401b4668b67dd5d9d684c148849534eceb9ac5016583b`

```dockerfile
```

-	Layers:
	-	`sha256:02de75eaf5b2dc50be38fec967aee7414d07fcafccf918c94dbe829df1252fce`  
		Last Modified: Tue, 30 Dec 2025 02:34:46 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ae1a2ae970d876f415258b51e7b199c93798abb45ee4ed35fa6030e85c8e65`  
		Last Modified: Tue, 30 Dec 2025 02:34:47 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:15a60594e418a843033717010bc8005d3f0c0ff946f50e5c22992a3ed36e2748
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
$ docker pull couchdb@sha256:df972c546a6885e4543313ad8c2b0053cf8714a3fb59d649d89b9ef423ad148f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99989ec912a9424567d54cd933dced4f7f794d6f557cbff2702df2431e8f4d2e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:50:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:50:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:51:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:51:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:51:14 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:14 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:51:19 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:51:19 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:51:19 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:51:19 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:51:19 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c01ee61cd7c9b56d374a202ee0d46c2e0da893812b4a948e349f2a35d466543`  
		Last Modified: Mon, 29 Dec 2025 23:51:44 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a100cb6919d3f60de8ea073ac2fa113cd374b600694934bd6f15d239c15ca8f`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 7.9 MB (7881846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7301c657c34a9a6d369824f607b5dbac4d76e29bc04eb05c6ce5165039faf5`  
		Last Modified: Mon, 29 Dec 2025 23:51:49 GMT  
		Size: 77.4 MB (77380714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa94eb84bfc0fa8788c84cbdd9eed85f90492efcacb0a348f48be48bc67c297`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 424.1 KB (424123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9b9573391200a94cbfbf4897da9e6aa9d54c4af1fcc8385036e92232f46be`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 99.5 KB (99549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e005bfb7a23f6ac0e0715ade61dc618c19457577dcad37f436daf36ddcc719`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b760955c7a59c5f3a73bd1aae595a41702221289b9493f18ae781a3ac88fc00`  
		Last Modified: Mon, 29 Dec 2025 23:51:46 GMT  
		Size: 42.4 MB (42436086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0240985660715c4c768cd427f938f136a9b3809dfab773cef38b594ab1f68a1`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a88798e4ef4ccd6a9784c58d3f0898df2a94e860f73d65e55015a565bd8b1b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7813f58468354cfd3ab96fc06c9d2a7c0ccab4beaf3e10bf73a8206cd926a6ec`

```dockerfile
```

-	Layers:
	-	`sha256:39a28044a58d7fe73deb9456bc234760244dad6696e91d4de110fa88c9ee2060`  
		Last Modified: Tue, 30 Dec 2025 02:34:49 GMT  
		Size: 3.7 MB (3657783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f7669556059c3c3f6be6f8a885fb81eff8f4db8b724582fc1db4f414144169`  
		Last Modified: Tue, 30 Dec 2025 02:34:50 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:816c23cecd3f78e84fbc835753125ad83243888a6faa72cf47040d62ec75704a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155317984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764a811b78458b07287273bba3804795d095713889cd0eb38d109ceb45765c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:51:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:51:31 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:51:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:51:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:51:52 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:53 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:51:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:51:58 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:51:58 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:51:58 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:51:58 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5e42927712cb08408bab95d296259f8357f1420c77b3514c0ddba9524d326`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fac362542ac63d9b5ce2473606ac9e2ae6c8dc1bd185324d508769c6700c0e`  
		Last Modified: Mon, 29 Dec 2025 23:52:24 GMT  
		Size: 7.7 MB (7691981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb429c28854773d7b3141dfab67edee63f656501a764e6e0093360b9553c154`  
		Last Modified: Mon, 29 Dec 2025 23:52:29 GMT  
		Size: 76.7 MB (76691659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99185cc4f9a57603526b2b641d4f249ad2fc0173a6ad44838eb1eda460778396`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 392.7 KB (392695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b013c7157f40125ea4cc376f03e211f57878569d1cd8c9310b59dec8fbdaab2`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 99.5 KB (99467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707dea8f42e1675f348e087d84f751464dd2a78ad39ece7eb3ec54029c05bfd`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc0e839b3313b449d793d42b552008615c2554dffb2a5e62b05d0fcf268543b`  
		Last Modified: Mon, 29 Dec 2025 23:52:26 GMT  
		Size: 42.3 MB (42338094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f45f9f2a3c6f8f126dcc89b12f249033f009d30b1e6f24cc906f1bfdafefbe6`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b3bfaacae41a46132505c69c40aa9d1703338555dad576c2fdfd430b772e5033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60d78b5d5127d1e65e73e89ee89d2b1e855dde7212c6b1c7c66670000fb39e`

```dockerfile
```

-	Layers:
	-	`sha256:3899bf6a49765906a1487ce497f80ed4c9f083e7370876be397431317d4b22a0`  
		Last Modified: Tue, 30 Dec 2025 02:34:54 GMT  
		Size: 3.7 MB (3656447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ffb2334e0d9ecbe9672378bec732bf9154cbcf70875531675fe311294a80a0`  
		Last Modified: Tue, 30 Dec 2025 02:34:55 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:40a9b98345cf6144b28a29193204570e84fd5298dd316c11bc004ae8c6d63e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf4339778cd3c6fce819c7625b8b632b43d482268c294a1508a39d5d32c567`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 30 Dec 2025 00:43:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:24 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:24 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:41 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 30 Dec 2025 00:43:41 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 30 Dec 2025 00:43:41 GMT
VOLUME [/opt/nouveau/data]
# Tue, 30 Dec 2025 00:43:41 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 30 Dec 2025 00:43:41 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fdcb9c0069163bb36ba9027df3a96ec4c7928ee18d1883d279ec26a42c5820`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb42e11f427e48b107230c55cac96ab07ccdd27376e019fcc1c6084aef50780`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14a25893bb2b4c129226a950762d06f8b90d4d4a7e22e31f6de27a4a5430159`  
		Last Modified: Tue, 30 Dec 2025 00:44:09 GMT  
		Size: 73.1 MB (73143182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b68b06b55e7e7e8356bae906af85409d6929283fe00bf39f5d2b4a9057e172`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 394.4 KB (394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638cc3955040ebb33ec4269a27111b9a405e3a00c154ecf7b474606b9f41cdfa`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 99.6 KB (99576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3e3277464b6a1fc279bce56940994ab65f77e016beb93511fde0151c2583a`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7794e73a05991361b50988477dc5ceee09ff0c4c0dee848a8d4093edf8965d6`  
		Last Modified: Tue, 30 Dec 2025 00:44:06 GMT  
		Size: 42.2 MB (42163168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c3b948a2c35379a5b2cd383735ac55d2114f118aa9f31492d42c2b661470c4`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4cd1968bd97da3978581c0f2fd399b4cfb9a8a015fe0458817d76c49c3add63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02e6a1bdf5d1a23b8504711b84a8b5fd146df7bdf2c8f8c2842c9bb6bc158b1`

```dockerfile
```

-	Layers:
	-	`sha256:1f22fc22aa7b3f7f4b754361c62001beb5ed9b51f885a6f779a57793e6090a63`  
		Last Modified: Tue, 30 Dec 2025 02:34:59 GMT  
		Size: 3.6 MB (3648312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e929bd7906731e6466d8fa1a58e4a04ba8786dd0d30976fda77ac625bbb332`  
		Last Modified: Tue, 30 Dec 2025 02:34:59 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:8336c8e64d3b2cd0acf439d6e653c2260d1d47ba6cd5cd17805dcefbb9da9a75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.3` - linux; amd64

```console
$ docker pull couchdb@sha256:ff705d86c308fd7485e6a54de73f86d42a3744a3e33762d8385acf9b1c43894d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139013682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fe7fbed2d22259a4d00f03938b7441256e26948318ed5ab0166f38f7cd1f62`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:50:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:50:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:50:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:46 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 29 Dec 2025 23:50:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:50:58 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:50:58 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:50:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d15e83c89dc92046ce8513dbc3e5bda9e6ec47fd4b02d0c1af6931954b685`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decc9d2a3fc90a1f3aa3e95018b2c425e2607160439736446ff9755a73de1c83`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 7.9 MB (7881777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead78062f3024d361050a4dd57e09369f355deaf2110dfe07b38496992c11a38`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 401.7 KB (401748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9e092b3893df2d97f5377606f76b15dd09626ba5d9d8da382911f6b9b92d5b`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 76.5 KB (76464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdb56fc21c0d1c6f6b36f4d174b35ec9b77f05ca39f0aecbce13d0079f89467`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b3596dff6e966812ac02d50ac0ec0539c48a9494d04f5d00daf422149a2149`  
		Last Modified: Mon, 29 Dec 2025 23:51:34 GMT  
		Size: 102.4 MB (102419846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749fc13405a180b1d3bdf11ed4d5c9469b17d86305b2cd467c7e4713b84b0e06`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0772c246f95c8bb72dc56b719df9cbe2517df9e6dfc8bcab9051c2ced540e50d`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651f65add2ff5d55229d535a1dc95a3d87ab855f8d9ad755a5d4ecb91d20e8a9`  
		Last Modified: Mon, 29 Dec 2025 23:51:21 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c738bc2de24a10cf4f677a191625f795dd5a86c915ccf5ad7dc71d73b9685`  
		Last Modified: Mon, 29 Dec 2025 23:51:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2d9e30e5ae70918d1037d45b083a96ab7e355020c534158eb1a9299fb9bdfcac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef63dc917788706dfbeb8d3c213b38924954349018fc1cd17b894b556b03622d`

```dockerfile
```

-	Layers:
	-	`sha256:a4bc56fa37e526e5de3e821d93e9851df90ad0baf75df175b1cdd69032767098`  
		Last Modified: Tue, 30 Dec 2025 02:34:35 GMT  
		Size: 4.1 MB (4125385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1049d92ab51e82474e35adcfcccb8f97b87e04de1aab7916033a46be205d9f`  
		Last Modified: Tue, 30 Dec 2025 02:34:36 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6c4315e4d0879da76cf740af0d532555d08a8843d96ef46fa1f4390c2a2159ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138415668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afea235c56d6ddb5c2d33a7785c8259807e7ef6f7d2a63454e591e5afad6967d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:50:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:11 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 29 Dec 2025 23:51:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:51:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:51:22 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:51:22 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:51:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b28ac2949ff03d076b0d9c8f249d200b4bcf69165d413df5502ba3aaedf454`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dc6e1e29e7d607633a85bf66afea8f8890b3226d4e4624d67d98c4f64d2136`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c6ff449448e94fe2f6b83744855d7a4a51a68b9d1728d1862611e369a3df3b`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 370.5 KB (370489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cba339223745b3fd888daac1058d4ff730fe2d6f54b4dcc9447e9c8595a3519`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 76.5 KB (76463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9a304c88fd98a1a095b970058190641d59470b847383c00231cbeb7dd4b0a`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1028465fb7adc55111dd3714373330acd270c76449e90d5493796a80740ab5e2`  
		Last Modified: Mon, 29 Dec 2025 23:51:53 GMT  
		Size: 102.2 MB (102169013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62edd8dd5f6a2c6c4236eaee0b6b622be7c6f6f997496b011808405e6eb972cb`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154161c10d72393c1d4bec615f21aa47cfddf9dd5cc24a64c15f0aa590ea4435`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646f9a190ca129a0b88dfff9c3cf008b99b1b89047abbebee88fc7fb72bbff58`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403c66c991179d07a989d0f5e08fc43e6151ca0e03ecd4a9c8df428553fc06b5`  
		Last Modified: Mon, 29 Dec 2025 23:51:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ac9a231eab81eabf72172886815a01be038950b6fce4733821e496c634a1276b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc8e6f8fda7d881c233e316eb65e00a20a9b8221429b7488098a76ad2ed880d`

```dockerfile
```

-	Layers:
	-	`sha256:efc3d040364ea67491bb30744a2eebbfa8206f4cdb26bd7b3efa3e88e38023c7`  
		Last Modified: Tue, 30 Dec 2025 02:34:40 GMT  
		Size: 4.1 MB (4125654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f78e67024f1d459eabd3f8a156435aa66fa7c566d56e7b16e37369b2a11ce16`  
		Last Modified: Tue, 30 Dec 2025 02:34:41 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:3c95a6c14d50f46109834df8d741401516c2f52a948e1752943f0fd993798d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135792275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fa04167d90f66de07d3a79dbbf97192ac3a6e9a20232e9b9be670ccfca557e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 30 Dec 2025 00:43:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:16 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 30 Dec 2025 00:43:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 00:43:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:43:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Dec 2025 00:43:31 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 30 Dec 2025 00:43:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2c212caeb4bbcbc1a2aae869143027f520be5caa1135a217e767121ac1626f`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d04e9f82f45a67b46af862374c24224a6717000183ace0e83d43c9ea4933`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef43570a8365ddd2c2f530578f7ab6932ad0954dae69973159ba5e7e7dd29895`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 372.1 KB (372097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8d5ab8f8d42dae898c00fd1281dbb1c3495bb8300bae20147a7a55b5eeb20`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 76.4 KB (76448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cc6d8fa43d6a9106826c6d5bdcca5ddae9593536e39f608bd43fce2d9d5ba6`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca396414f155ebb0cc5c0e2eb881808ccfb18cabe08693ce79317284b1d71f6`  
		Last Modified: Tue, 30 Dec 2025 00:44:10 GMT  
		Size: 101.1 MB (101055826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fc800dc53b8ae9cda89fbeb0b41e0b5207b882fa39bdf61ed97d09417aa606`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0d89e6f3b0d4950b67e2e873444f54aeb37a28056fb9ba9baad7e3ba4a2d68`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541180d05fb42aee984cf5a975a407188af79f0bd0306f7db2127186f10f52aa`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed479a1ef0723c916a94c51ef27883d9f625c018d1be1cb44c98ec55f078cef`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3061116c8f6ab2863431089e4b23a5fc50c156c292c89df3edc6f90635fc2a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771b824c652cdb39dd1401b4668b67dd5d9d684c148849534eceb9ac5016583b`

```dockerfile
```

-	Layers:
	-	`sha256:02de75eaf5b2dc50be38fec967aee7414d07fcafccf918c94dbe829df1252fce`  
		Last Modified: Tue, 30 Dec 2025 02:34:46 GMT  
		Size: 4.1 MB (4121581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ae1a2ae970d876f415258b51e7b199c93798abb45ee4ed35fa6030e85c8e65`  
		Last Modified: Tue, 30 Dec 2025 02:34:47 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:15a60594e418a843033717010bc8005d3f0c0ff946f50e5c22992a3ed36e2748
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:df972c546a6885e4543313ad8c2b0053cf8714a3fb59d649d89b9ef423ad148f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99989ec912a9424567d54cd933dced4f7f794d6f557cbff2702df2431e8f4d2e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:50:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:50:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:51:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:51:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:51:14 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:14 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:51:19 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:51:19 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:51:19 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:51:19 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:51:19 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c01ee61cd7c9b56d374a202ee0d46c2e0da893812b4a948e349f2a35d466543`  
		Last Modified: Mon, 29 Dec 2025 23:51:44 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a100cb6919d3f60de8ea073ac2fa113cd374b600694934bd6f15d239c15ca8f`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 7.9 MB (7881846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7301c657c34a9a6d369824f607b5dbac4d76e29bc04eb05c6ce5165039faf5`  
		Last Modified: Mon, 29 Dec 2025 23:51:49 GMT  
		Size: 77.4 MB (77380714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa94eb84bfc0fa8788c84cbdd9eed85f90492efcacb0a348f48be48bc67c297`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 424.1 KB (424123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9b9573391200a94cbfbf4897da9e6aa9d54c4af1fcc8385036e92232f46be`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 99.5 KB (99549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e005bfb7a23f6ac0e0715ade61dc618c19457577dcad37f436daf36ddcc719`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b760955c7a59c5f3a73bd1aae595a41702221289b9493f18ae781a3ac88fc00`  
		Last Modified: Mon, 29 Dec 2025 23:51:46 GMT  
		Size: 42.4 MB (42436086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0240985660715c4c768cd427f938f136a9b3809dfab773cef38b594ab1f68a1`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a88798e4ef4ccd6a9784c58d3f0898df2a94e860f73d65e55015a565bd8b1b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7813f58468354cfd3ab96fc06c9d2a7c0ccab4beaf3e10bf73a8206cd926a6ec`

```dockerfile
```

-	Layers:
	-	`sha256:39a28044a58d7fe73deb9456bc234760244dad6696e91d4de110fa88c9ee2060`  
		Last Modified: Tue, 30 Dec 2025 02:34:49 GMT  
		Size: 3.7 MB (3657783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f7669556059c3c3f6be6f8a885fb81eff8f4db8b724582fc1db4f414144169`  
		Last Modified: Tue, 30 Dec 2025 02:34:50 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:816c23cecd3f78e84fbc835753125ad83243888a6faa72cf47040d62ec75704a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155317984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f764a811b78458b07287273bba3804795d095713889cd0eb38d109ceb45765c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:51:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:51:31 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:51:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:51:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:51:52 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:53 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:51:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:51:58 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:51:58 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:51:58 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:51:58 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e5e42927712cb08408bab95d296259f8357f1420c77b3514c0ddba9524d326`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fac362542ac63d9b5ce2473606ac9e2ae6c8dc1bd185324d508769c6700c0e`  
		Last Modified: Mon, 29 Dec 2025 23:52:24 GMT  
		Size: 7.7 MB (7691981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb429c28854773d7b3141dfab67edee63f656501a764e6e0093360b9553c154`  
		Last Modified: Mon, 29 Dec 2025 23:52:29 GMT  
		Size: 76.7 MB (76691659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99185cc4f9a57603526b2b641d4f249ad2fc0173a6ad44838eb1eda460778396`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 392.7 KB (392695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b013c7157f40125ea4cc376f03e211f57878569d1cd8c9310b59dec8fbdaab2`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 99.5 KB (99467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707dea8f42e1675f348e087d84f751464dd2a78ad39ece7eb3ec54029c05bfd`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc0e839b3313b449d793d42b552008615c2554dffb2a5e62b05d0fcf268543b`  
		Last Modified: Mon, 29 Dec 2025 23:52:26 GMT  
		Size: 42.3 MB (42338094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f45f9f2a3c6f8f126dcc89b12f249033f009d30b1e6f24cc906f1bfdafefbe6`  
		Last Modified: Mon, 29 Dec 2025 23:52:23 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b3bfaacae41a46132505c69c40aa9d1703338555dad576c2fdfd430b772e5033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60d78b5d5127d1e65e73e89ee89d2b1e855dde7212c6b1c7c66670000fb39e`

```dockerfile
```

-	Layers:
	-	`sha256:3899bf6a49765906a1487ce497f80ed4c9f083e7370876be397431317d4b22a0`  
		Last Modified: Tue, 30 Dec 2025 02:34:54 GMT  
		Size: 3.7 MB (3656447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ffb2334e0d9ecbe9672378bec732bf9154cbcf70875531675fe311294a80a0`  
		Last Modified: Tue, 30 Dec 2025 02:34:55 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:40a9b98345cf6144b28a29193204570e84fd5298dd316c11bc004ae8c6d63e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf4339778cd3c6fce819c7625b8b632b43d482268c294a1508a39d5d32c567`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 30 Dec 2025 00:43:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:24 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:24 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:41 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 30 Dec 2025 00:43:41 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 30 Dec 2025 00:43:41 GMT
VOLUME [/opt/nouveau/data]
# Tue, 30 Dec 2025 00:43:41 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 30 Dec 2025 00:43:41 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fdcb9c0069163bb36ba9027df3a96ec4c7928ee18d1883d279ec26a42c5820`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb42e11f427e48b107230c55cac96ab07ccdd27376e019fcc1c6084aef50780`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14a25893bb2b4c129226a950762d06f8b90d4d4a7e22e31f6de27a4a5430159`  
		Last Modified: Tue, 30 Dec 2025 00:44:09 GMT  
		Size: 73.1 MB (73143182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b68b06b55e7e7e8356bae906af85409d6929283fe00bf39f5d2b4a9057e172`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 394.4 KB (394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638cc3955040ebb33ec4269a27111b9a405e3a00c154ecf7b474606b9f41cdfa`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 99.6 KB (99576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3e3277464b6a1fc279bce56940994ab65f77e016beb93511fde0151c2583a`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7794e73a05991361b50988477dc5ceee09ff0c4c0dee848a8d4093edf8965d6`  
		Last Modified: Tue, 30 Dec 2025 00:44:06 GMT  
		Size: 42.2 MB (42163168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c3b948a2c35379a5b2cd383735ac55d2114f118aa9f31492d42c2b661470c4`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4cd1968bd97da3978581c0f2fd399b4cfb9a8a015fe0458817d76c49c3add63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02e6a1bdf5d1a23b8504711b84a8b5fd146df7bdf2c8f8c2842c9bb6bc158b1`

```dockerfile
```

-	Layers:
	-	`sha256:1f22fc22aa7b3f7f4b754361c62001beb5ed9b51f885a6f779a57793e6090a63`  
		Last Modified: Tue, 30 Dec 2025 02:34:59 GMT  
		Size: 3.6 MB (3648312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e929bd7906731e6466d8fa1a58e4a04ba8786dd0d30976fda77ac625bbb332`  
		Last Modified: Tue, 30 Dec 2025 02:34:59 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:3d5bc0a2ccb6556a6361cf8b4c7f215568fb0c0c2e5e8b44a747e1c138d99f7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:57747ae2592b8ae8d17570494997c77e08aa7c6ec62ed426450d6dfaf2376b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727998b01b6d8db683ee8be2225c8b90d4182c30f86a59804115f4f81f15dc02`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:49:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:49:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:49:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:34 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 29 Dec 2025 23:49:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:46 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:49:46 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:49:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4da247384f3a99a20316fa166611c05b44fed7084eee310097ef1bdf514ba1`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166803e3fb395174c7c6adb5b75a40fab348e7ad68c4d66fb29b38bd709b2328`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 7.9 MB (7881766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfd08eb3284da772851758bd24632fbec89654d005465f4dfd980de4f7782`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 401.7 KB (401735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2aa3f63c0336e55777f05c65b0159f362bed7c1136eea5b0d9a8b44c04edc9d`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1be06be76b3897be7a41d4f6b6600f8f57490148abaf6472a4a8f0b2e56f2c`  
		Last Modified: Mon, 29 Dec 2025 23:50:12 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eefaa2cb4295681c6d96e4651fc485b07576b6a49711537a4a9f7283c42d94`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 105.5 MB (105457507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bd50c1024430503d97929bd6c7f0e389cb97fb1f2b3efd533f8b12de73bb22`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc660b6f24ee1a1a2c684fece0e6b7e0e02708724ce97da0a1f58d771ce32804`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1e239747f1b31084c3b43aee1c52536bcd8e41683da6d3e026067bf689cb3`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217819c94f97a81240ad47bd6d273fdf925ebaffb575e29a58865407d218f24b`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:793cd5d70d6987512f3de95cabd0dd75cdbd4b487f634d39204cca0c1259a5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea258ab00932437927460b3cb8c30d5021b781de8b83edfc3a03f547a60f94a`

```dockerfile
```

-	Layers:
	-	`sha256:d809f4ab990a6df7902a9088b2c15dd392c546dfb1dd9ecf6363cbcd8c258029`  
		Last Modified: Tue, 30 Dec 2025 02:34:08 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc7673097a4e547638a4434f9e9e888c882666dd9cac92ba358aef897409fc4`  
		Last Modified: Tue, 30 Dec 2025 02:34:09 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:681cd28217f5c317b9dc604f4246b8ee2e74a0eb6a4000b8739feb9b7428e8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141402906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6697230efc8f63d0880368053b055920186cc1a1bb1d0f656ad22c18bef25817`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:50:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:11 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 29 Dec 2025 23:50:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:50:23 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:50:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:50:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b28ac2949ff03d076b0d9c8f249d200b4bcf69165d413df5502ba3aaedf454`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dc6e1e29e7d607633a85bf66afea8f8890b3226d4e4624d67d98c4f64d2136`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c6ff449448e94fe2f6b83744855d7a4a51a68b9d1728d1862611e369a3df3b`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 370.5 KB (370489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cba339223745b3fd888daac1058d4ff730fe2d6f54b4dcc9447e9c8595a3519`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 76.5 KB (76463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539a2e947f04a8b08f17c261fffdef51bea21f220fa11e105a8859cce21f5d97`  
		Last Modified: Mon, 29 Dec 2025 23:50:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0623f96358d425f7c7c6e980fedd8edceec5093234fb6a47ed07223fc9610bac`  
		Last Modified: Mon, 29 Dec 2025 23:50:54 GMT  
		Size: 105.2 MB (105156261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c021dc14d00d1a5fa4b9aaabdb81fe6ee4b1eb8f7a7b803ff162b91259d532`  
		Last Modified: Mon, 29 Dec 2025 23:50:45 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227cb5d0e30b21b406c667ff03bf98fa15752b945418b4ff82ee27ae46ed1529`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded008b35a0d5d4f3da488006d2392e90f0159a48a34f52653bdfa9873ecc907`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a57cc7e2430c4170e48f2795917639ec5d0543504bba350447c5d07529915`  
		Last Modified: Mon, 29 Dec 2025 23:50:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:f28093eee8046a743326e6ea677710c47e6d47e0bef6a915df0f6cbb83b2f29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967244bafb8f7690bf989609244cb13370aeb40e1d932ca4112055c2e1130d8`

```dockerfile
```

-	Layers:
	-	`sha256:0fb14dcfda03d85402b1dc4c686e205162a70c96082e9a1e2d5d2b04164d5836`  
		Last Modified: Tue, 30 Dec 2025 02:34:14 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66a7c455067fc1722c12cd4c459f4fcd43d8c7188963dfaf12e4a10d28ec3d1`  
		Last Modified: Tue, 30 Dec 2025 02:34:14 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:097a79b432ba83d04f56a870419464b2ae0012c7d22f3571be335cbe6fb1ae48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138764692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b664edaedd041921a1c187dce4b4ec17c8431ad36619bb30ccce7799916ec14`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 30 Dec 2025 00:43:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:16 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 30 Dec 2025 00:43:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Dec 2025 00:43:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 00:43:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:43:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Dec 2025 00:43:33 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 30 Dec 2025 00:43:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2c212caeb4bbcbc1a2aae869143027f520be5caa1135a217e767121ac1626f`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d04e9f82f45a67b46af862374c24224a6717000183ace0e83d43c9ea4933`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef43570a8365ddd2c2f530578f7ab6932ad0954dae69973159ba5e7e7dd29895`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 372.1 KB (372097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8d5ab8f8d42dae898c00fd1281dbb1c3495bb8300bae20147a7a55b5eeb20`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 76.4 KB (76448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cc6d8fa43d6a9106826c6d5bdcca5ddae9593536e39f608bd43fce2d9d5ba6`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe85005dced89895410b4c8872001a3b45d39077d67a253350bed39bf5131fc`  
		Last Modified: Tue, 30 Dec 2025 00:44:08 GMT  
		Size: 104.0 MB (104028236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7332b0b429f7a79fa4a9fc758b1f9691c3233b407385a6c2b9f2d0733e76d0`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377fda69dd4b138b08a08a414245a50daddd123c4777a6f603bc1250e4019fd`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f22f88c0a1beaede0681cf9efc3c9317c306f909002e24fb8f7f77ecc34a67f`  
		Last Modified: Tue, 30 Dec 2025 00:44:06 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68718752dcb618d114c82c2fba317c2a114392ae48854bba56a3aadbc75638ef`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:eff806d92f51590b41ba5bdc2564371adc66e1a4f6cc58d721e2d568d6ecd098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631566cdecdf5917d0fac5cef60417037a118a84354956afcac4de6f686aaaed`

```dockerfile
```

-	Layers:
	-	`sha256:cc24a91e945ce3d8b13559abd0468a49b0ce07e30f51f7063ea09b3f0d87b262`  
		Last Modified: Tue, 30 Dec 2025 02:34:19 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628f341500f6aec75f6745a857d74bdb9a9195dd735eb380666fbd2806ded2ee`  
		Last Modified: Tue, 30 Dec 2025 02:34:20 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:75bd21043980a7c636db8fd5d9d34c04518e3569c508c6ac54450c0949ec1834
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:945e91e36f9f38dcc47025f11172e42a6abbbfdde757ea61607c4c8f9551ef1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd621b26d0f78da92f822e9161d6dcfefca8b7ea7ddabc7bfc311f7016bbb42`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:50 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:49:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:07 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:11 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:11 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:50:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:50:16 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:50:16 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:50:16 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:50:16 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dce4d2e8558c65ac1a60bc4200e439914980222a984f7999b7e74fc9b9e096c`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11d07e7d5c34a4f71e53f4dea48fc87aa684955ad01811329ed31f971bb2595`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 7.9 MB (7881778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec04402a7ca12958aadb841d478898ce974a783d8116ee07dce19e043d004037`  
		Last Modified: Mon, 29 Dec 2025 23:50:49 GMT  
		Size: 77.4 MB (77380629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6012f4a39813fae020f5b8f76b083fbb7c2a67816dff05129004b04c3b73827e`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 424.1 KB (424119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe66f4fc85b301fc3c3f8b7343ec158d096764c6dee5ca9027fd1b30dc2425ca`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 99.5 KB (99544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539a2e947f04a8b08f17c261fffdef51bea21f220fa11e105a8859cce21f5d97`  
		Last Modified: Mon, 29 Dec 2025 23:50:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b286f385771164d9449e280bf59a2f6cde567285cc84620ece635778ddf5640b`  
		Last Modified: Mon, 29 Dec 2025 23:50:43 GMT  
		Size: 42.4 MB (42436413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12703b1cdcea4825887128a9e3fa26d091c0ca9b8d19b19ec60bab35e89d6381`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6c837a5252b403588cee5c772d7296bd4b26c30191dbad1ac5559f7b674384fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c476b0f2c23680324acf38341f299bc99281ebbc1b83553a63b39ea297f4c5`

```dockerfile
```

-	Layers:
	-	`sha256:191d975035ad3380ee5bddb05472a78bdbd9549adb7989db2e3fbe1a4bd835a8`  
		Last Modified: Tue, 30 Dec 2025 02:34:21 GMT  
		Size: 3.7 MB (3658089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07d8d3dda9ce39dd8b007299ab8e5d3121e860339f884d4a6c41668ae503d8b0`  
		Last Modified: Tue, 30 Dec 2025 02:34:22 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:91840d6b1935926fe3f14b1a49288ff8bd6bd6085661c1e89cc05f0f63fd9217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155319049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4699635c99aead1d1b48894edc964efa791a2812854e6d556cf58a4b35e76a90`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:50:44 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:50:44 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:50:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:51:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:51:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:51:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:51:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:51:11 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:51:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:51:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c6cf1da0cafb42ee50f87d18f1179b8852984be2493056f7be16ddf098df68`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db538f0f6e5c48b9027d3bff5b408f0fe017e37ab35ac67c64ca996e8b1404b0`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 7.7 MB (7692025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257ed1b889cb7b176bd192e80932c6d572470ea854aa905df7b9216114a71ff`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 76.7 MB (76691592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec43333135ccd6e64cb882f33fabb71b4e1950235203b6ec0de59a37d32a3f`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 392.7 KB (392710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a511da4c54a9095157b7b2afac88d338be88b8ab2d6469a086c10b2bdfd126b`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 99.5 KB (99496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43254879df398217c0ee33f79c3e968ce39762b7d711613b9a890872f8177b02`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31c5db9d396b5ffcc05a253360eb4abec4ea784b3a9968ef728c4e6c294750d`  
		Last Modified: Mon, 29 Dec 2025 23:51:40 GMT  
		Size: 42.3 MB (42339137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5101b12acc67d71aa660bf156ac871c8fcc5364639486c328b0296ed90035e`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:63d46b909ba521b811d1a9462f8e6b1ca73dfe6dc7ad1706d9fc348d43738602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa1de027c19597a14e9aaa324a4042322864394ece6ed684e9429420711e6f0`

```dockerfile
```

-	Layers:
	-	`sha256:4a98c50d58754f26fb1bb843907a35460161c4c7ee06811a830033f112ff1bd8`  
		Last Modified: Tue, 30 Dec 2025 02:34:50 GMT  
		Size: 3.7 MB (3656765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45ec36b2e4cacde6a39c456516b187e1a2121e10f77390da694fe95705c6cec`  
		Last Modified: Tue, 30 Dec 2025 02:34:51 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:34f25dc7198140c53fb22bfa1d9d8691566e97945bf0478d5b049634cbef1cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20aca295d049aaa9d83f7f4d38df7bcd57f10bfec0ec92662b774857f8dace6c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 30 Dec 2025 00:43:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:24 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:24 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
VOLUME [/opt/nouveau/data]
# Tue, 30 Dec 2025 00:43:32 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 30 Dec 2025 00:43:32 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fdcb9c0069163bb36ba9027df3a96ec4c7928ee18d1883d279ec26a42c5820`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb42e11f427e48b107230c55cac96ab07ccdd27376e019fcc1c6084aef50780`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14a25893bb2b4c129226a950762d06f8b90d4d4a7e22e31f6de27a4a5430159`  
		Last Modified: Tue, 30 Dec 2025 00:44:09 GMT  
		Size: 73.1 MB (73143182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b68b06b55e7e7e8356bae906af85409d6929283fe00bf39f5d2b4a9057e172`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 394.4 KB (394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638cc3955040ebb33ec4269a27111b9a405e3a00c154ecf7b474606b9f41cdfa`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 99.6 KB (99576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3e3277464b6a1fc279bce56940994ab65f77e016beb93511fde0151c2583a`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0eb016d52c4ffcd47aadbe7ede831dfe2c00005157bf1c8497f377d835b22e`  
		Last Modified: Tue, 30 Dec 2025 00:44:05 GMT  
		Size: 42.2 MB (42164593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d4d000f28910ea40330d82411589b03cb147de0dcac2d684961820194f7438`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:05bacf883372d85634d236f15f2ed5dd4e46ad2642a83963ddf42e177ee584f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6008de5a7a77a2f1279820fce65cd1dc0f0e43ef939bc6cd277470afbb0b64`

```dockerfile
```

-	Layers:
	-	`sha256:00590dfe8e4a2fc14816f217ae5ab95565ba4f110e0d6204a055da0a1ab780c8`  
		Last Modified: Tue, 30 Dec 2025 02:34:55 GMT  
		Size: 3.6 MB (3648618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47fdc9def5a01ac08462ee60814639d6ab42e6871584c635678abe15161d93b3`  
		Last Modified: Tue, 30 Dec 2025 02:34:56 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:3d5bc0a2ccb6556a6361cf8b4c7f215568fb0c0c2e5e8b44a747e1c138d99f7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1` - linux; amd64

```console
$ docker pull couchdb@sha256:57747ae2592b8ae8d17570494997c77e08aa7c6ec62ed426450d6dfaf2376b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727998b01b6d8db683ee8be2225c8b90d4182c30f86a59804115f4f81f15dc02`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:49:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:49:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:49:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:34 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 29 Dec 2025 23:49:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:46 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:49:46 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:49:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4da247384f3a99a20316fa166611c05b44fed7084eee310097ef1bdf514ba1`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166803e3fb395174c7c6adb5b75a40fab348e7ad68c4d66fb29b38bd709b2328`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 7.9 MB (7881766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfd08eb3284da772851758bd24632fbec89654d005465f4dfd980de4f7782`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 401.7 KB (401735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2aa3f63c0336e55777f05c65b0159f362bed7c1136eea5b0d9a8b44c04edc9d`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1be06be76b3897be7a41d4f6b6600f8f57490148abaf6472a4a8f0b2e56f2c`  
		Last Modified: Mon, 29 Dec 2025 23:50:12 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eefaa2cb4295681c6d96e4651fc485b07576b6a49711537a4a9f7283c42d94`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 105.5 MB (105457507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bd50c1024430503d97929bd6c7f0e389cb97fb1f2b3efd533f8b12de73bb22`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc660b6f24ee1a1a2c684fece0e6b7e0e02708724ce97da0a1f58d771ce32804`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1e239747f1b31084c3b43aee1c52536bcd8e41683da6d3e026067bf689cb3`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217819c94f97a81240ad47bd6d273fdf925ebaffb575e29a58865407d218f24b`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:793cd5d70d6987512f3de95cabd0dd75cdbd4b487f634d39204cca0c1259a5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea258ab00932437927460b3cb8c30d5021b781de8b83edfc3a03f547a60f94a`

```dockerfile
```

-	Layers:
	-	`sha256:d809f4ab990a6df7902a9088b2c15dd392c546dfb1dd9ecf6363cbcd8c258029`  
		Last Modified: Tue, 30 Dec 2025 02:34:08 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc7673097a4e547638a4434f9e9e888c882666dd9cac92ba358aef897409fc4`  
		Last Modified: Tue, 30 Dec 2025 02:34:09 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:681cd28217f5c317b9dc604f4246b8ee2e74a0eb6a4000b8739feb9b7428e8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141402906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6697230efc8f63d0880368053b055920186cc1a1bb1d0f656ad22c18bef25817`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:50:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:11 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 29 Dec 2025 23:50:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:50:23 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:50:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:50:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b28ac2949ff03d076b0d9c8f249d200b4bcf69165d413df5502ba3aaedf454`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dc6e1e29e7d607633a85bf66afea8f8890b3226d4e4624d67d98c4f64d2136`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c6ff449448e94fe2f6b83744855d7a4a51a68b9d1728d1862611e369a3df3b`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 370.5 KB (370489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cba339223745b3fd888daac1058d4ff730fe2d6f54b4dcc9447e9c8595a3519`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 76.5 KB (76463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539a2e947f04a8b08f17c261fffdef51bea21f220fa11e105a8859cce21f5d97`  
		Last Modified: Mon, 29 Dec 2025 23:50:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0623f96358d425f7c7c6e980fedd8edceec5093234fb6a47ed07223fc9610bac`  
		Last Modified: Mon, 29 Dec 2025 23:50:54 GMT  
		Size: 105.2 MB (105156261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c021dc14d00d1a5fa4b9aaabdb81fe6ee4b1eb8f7a7b803ff162b91259d532`  
		Last Modified: Mon, 29 Dec 2025 23:50:45 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227cb5d0e30b21b406c667ff03bf98fa15752b945418b4ff82ee27ae46ed1529`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded008b35a0d5d4f3da488006d2392e90f0159a48a34f52653bdfa9873ecc907`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a57cc7e2430c4170e48f2795917639ec5d0543504bba350447c5d07529915`  
		Last Modified: Mon, 29 Dec 2025 23:50:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:f28093eee8046a743326e6ea677710c47e6d47e0bef6a915df0f6cbb83b2f29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967244bafb8f7690bf989609244cb13370aeb40e1d932ca4112055c2e1130d8`

```dockerfile
```

-	Layers:
	-	`sha256:0fb14dcfda03d85402b1dc4c686e205162a70c96082e9a1e2d5d2b04164d5836`  
		Last Modified: Tue, 30 Dec 2025 02:34:14 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66a7c455067fc1722c12cd4c459f4fcd43d8c7188963dfaf12e4a10d28ec3d1`  
		Last Modified: Tue, 30 Dec 2025 02:34:14 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; s390x

```console
$ docker pull couchdb@sha256:097a79b432ba83d04f56a870419464b2ae0012c7d22f3571be335cbe6fb1ae48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138764692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b664edaedd041921a1c187dce4b4ec17c8431ad36619bb30ccce7799916ec14`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 30 Dec 2025 00:43:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:16 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 30 Dec 2025 00:43:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Dec 2025 00:43:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 00:43:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:43:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Dec 2025 00:43:33 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 30 Dec 2025 00:43:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2c212caeb4bbcbc1a2aae869143027f520be5caa1135a217e767121ac1626f`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d04e9f82f45a67b46af862374c24224a6717000183ace0e83d43c9ea4933`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef43570a8365ddd2c2f530578f7ab6932ad0954dae69973159ba5e7e7dd29895`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 372.1 KB (372097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8d5ab8f8d42dae898c00fd1281dbb1c3495bb8300bae20147a7a55b5eeb20`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 76.4 KB (76448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cc6d8fa43d6a9106826c6d5bdcca5ddae9593536e39f608bd43fce2d9d5ba6`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe85005dced89895410b4c8872001a3b45d39077d67a253350bed39bf5131fc`  
		Last Modified: Tue, 30 Dec 2025 00:44:08 GMT  
		Size: 104.0 MB (104028236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7332b0b429f7a79fa4a9fc758b1f9691c3233b407385a6c2b9f2d0733e76d0`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377fda69dd4b138b08a08a414245a50daddd123c4777a6f603bc1250e4019fd`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f22f88c0a1beaede0681cf9efc3c9317c306f909002e24fb8f7f77ecc34a67f`  
		Last Modified: Tue, 30 Dec 2025 00:44:06 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68718752dcb618d114c82c2fba317c2a114392ae48854bba56a3aadbc75638ef`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:eff806d92f51590b41ba5bdc2564371adc66e1a4f6cc58d721e2d568d6ecd098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631566cdecdf5917d0fac5cef60417037a118a84354956afcac4de6f686aaaed`

```dockerfile
```

-	Layers:
	-	`sha256:cc24a91e945ce3d8b13559abd0468a49b0ce07e30f51f7063ea09b3f0d87b262`  
		Last Modified: Tue, 30 Dec 2025 02:34:19 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628f341500f6aec75f6745a857d74bdb9a9195dd735eb380666fbd2806ded2ee`  
		Last Modified: Tue, 30 Dec 2025 02:34:20 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:75bd21043980a7c636db8fd5d9d34c04518e3569c508c6ac54450c0949ec1834
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:945e91e36f9f38dcc47025f11172e42a6abbbfdde757ea61607c4c8f9551ef1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd621b26d0f78da92f822e9161d6dcfefca8b7ea7ddabc7bfc311f7016bbb42`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:50 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:49:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:07 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:11 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:11 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:50:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:50:16 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:50:16 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:50:16 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:50:16 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dce4d2e8558c65ac1a60bc4200e439914980222a984f7999b7e74fc9b9e096c`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11d07e7d5c34a4f71e53f4dea48fc87aa684955ad01811329ed31f971bb2595`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 7.9 MB (7881778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec04402a7ca12958aadb841d478898ce974a783d8116ee07dce19e043d004037`  
		Last Modified: Mon, 29 Dec 2025 23:50:49 GMT  
		Size: 77.4 MB (77380629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6012f4a39813fae020f5b8f76b083fbb7c2a67816dff05129004b04c3b73827e`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 424.1 KB (424119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe66f4fc85b301fc3c3f8b7343ec158d096764c6dee5ca9027fd1b30dc2425ca`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 99.5 KB (99544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539a2e947f04a8b08f17c261fffdef51bea21f220fa11e105a8859cce21f5d97`  
		Last Modified: Mon, 29 Dec 2025 23:50:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b286f385771164d9449e280bf59a2f6cde567285cc84620ece635778ddf5640b`  
		Last Modified: Mon, 29 Dec 2025 23:50:43 GMT  
		Size: 42.4 MB (42436413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12703b1cdcea4825887128a9e3fa26d091c0ca9b8d19b19ec60bab35e89d6381`  
		Last Modified: Mon, 29 Dec 2025 23:50:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6c837a5252b403588cee5c772d7296bd4b26c30191dbad1ac5559f7b674384fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c476b0f2c23680324acf38341f299bc99281ebbc1b83553a63b39ea297f4c5`

```dockerfile
```

-	Layers:
	-	`sha256:191d975035ad3380ee5bddb05472a78bdbd9549adb7989db2e3fbe1a4bd835a8`  
		Last Modified: Tue, 30 Dec 2025 02:34:21 GMT  
		Size: 3.7 MB (3658089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07d8d3dda9ce39dd8b007299ab8e5d3121e860339f884d4a6c41668ae503d8b0`  
		Last Modified: Tue, 30 Dec 2025 02:34:22 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:91840d6b1935926fe3f14b1a49288ff8bd6bd6085661c1e89cc05f0f63fd9217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155319049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4699635c99aead1d1b48894edc964efa791a2812854e6d556cf58a4b35e76a90`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:50:44 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:50:44 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 29 Dec 2025 23:50:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:51:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:51:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:51:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 29 Dec 2025 23:51:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 29 Dec 2025 23:51:11 GMT
VOLUME [/opt/nouveau/data]
# Mon, 29 Dec 2025 23:51:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 29 Dec 2025 23:51:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c6cf1da0cafb42ee50f87d18f1179b8852984be2493056f7be16ddf098df68`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db538f0f6e5c48b9027d3bff5b408f0fe017e37ab35ac67c64ca996e8b1404b0`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 7.7 MB (7692025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257ed1b889cb7b176bd192e80932c6d572470ea854aa905df7b9216114a71ff`  
		Last Modified: Mon, 29 Dec 2025 23:51:42 GMT  
		Size: 76.7 MB (76691592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec43333135ccd6e64cb882f33fabb71b4e1950235203b6ec0de59a37d32a3f`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 392.7 KB (392710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a511da4c54a9095157b7b2afac88d338be88b8ab2d6469a086c10b2bdfd126b`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 99.5 KB (99496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43254879df398217c0ee33f79c3e968ce39762b7d711613b9a890872f8177b02`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31c5db9d396b5ffcc05a253360eb4abec4ea784b3a9968ef728c4e6c294750d`  
		Last Modified: Mon, 29 Dec 2025 23:51:40 GMT  
		Size: 42.3 MB (42339137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5101b12acc67d71aa660bf156ac871c8fcc5364639486c328b0296ed90035e`  
		Last Modified: Mon, 29 Dec 2025 23:51:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:63d46b909ba521b811d1a9462f8e6b1ca73dfe6dc7ad1706d9fc348d43738602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa1de027c19597a14e9aaa324a4042322864394ece6ed684e9429420711e6f0`

```dockerfile
```

-	Layers:
	-	`sha256:4a98c50d58754f26fb1bb843907a35460161c4c7ee06811a830033f112ff1bd8`  
		Last Modified: Tue, 30 Dec 2025 02:34:50 GMT  
		Size: 3.7 MB (3656765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45ec36b2e4cacde6a39c456516b187e1a2121e10f77390da694fe95705c6cec`  
		Last Modified: Tue, 30 Dec 2025 02:34:51 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:34f25dc7198140c53fb22bfa1d9d8691566e97945bf0478d5b049634cbef1cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20aca295d049aaa9d83f7f4d38df7bcd57f10bfec0ec92662b774857f8dace6c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 30 Dec 2025 00:43:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:24 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:24 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
VOLUME [/opt/nouveau/data]
# Tue, 30 Dec 2025 00:43:32 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 30 Dec 2025 00:43:32 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fdcb9c0069163bb36ba9027df3a96ec4c7928ee18d1883d279ec26a42c5820`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb42e11f427e48b107230c55cac96ab07ccdd27376e019fcc1c6084aef50780`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14a25893bb2b4c129226a950762d06f8b90d4d4a7e22e31f6de27a4a5430159`  
		Last Modified: Tue, 30 Dec 2025 00:44:09 GMT  
		Size: 73.1 MB (73143182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b68b06b55e7e7e8356bae906af85409d6929283fe00bf39f5d2b4a9057e172`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 394.4 KB (394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638cc3955040ebb33ec4269a27111b9a405e3a00c154ecf7b474606b9f41cdfa`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 99.6 KB (99576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3e3277464b6a1fc279bce56940994ab65f77e016beb93511fde0151c2583a`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0eb016d52c4ffcd47aadbe7ede831dfe2c00005157bf1c8497f377d835b22e`  
		Last Modified: Tue, 30 Dec 2025 00:44:05 GMT  
		Size: 42.2 MB (42164593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d4d000f28910ea40330d82411589b03cb147de0dcac2d684961820194f7438`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:05bacf883372d85634d236f15f2ed5dd4e46ad2642a83963ddf42e177ee584f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6008de5a7a77a2f1279820fce65cd1dc0f0e43ef939bc6cd277470afbb0b64`

```dockerfile
```

-	Layers:
	-	`sha256:00590dfe8e4a2fc14816f217ae5ab95565ba4f110e0d6204a055da0a1ab780c8`  
		Last Modified: Tue, 30 Dec 2025 02:34:55 GMT  
		Size: 3.6 MB (3648618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47fdc9def5a01ac08462ee60814639d6ab42e6871584c635678abe15161d93b3`  
		Last Modified: Tue, 30 Dec 2025 02:34:56 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:3d5bc0a2ccb6556a6361cf8b4c7f215568fb0c0c2e5e8b44a747e1c138d99f7c
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
$ docker pull couchdb@sha256:57747ae2592b8ae8d17570494997c77e08aa7c6ec62ed426450d6dfaf2376b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142051351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727998b01b6d8db683ee8be2225c8b90d4182c30f86a59804115f4f81f15dc02`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:49:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:49:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:49:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:34 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 29 Dec 2025 23:49:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:49:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:46 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:49:46 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:49:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4da247384f3a99a20316fa166611c05b44fed7084eee310097ef1bdf514ba1`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166803e3fb395174c7c6adb5b75a40fab348e7ad68c4d66fb29b38bd709b2328`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 7.9 MB (7881766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556cfd08eb3284da772851758bd24632fbec89654d005465f4dfd980de4f7782`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 401.7 KB (401735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2aa3f63c0336e55777f05c65b0159f362bed7c1136eea5b0d9a8b44c04edc9d`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1be06be76b3897be7a41d4f6b6600f8f57490148abaf6472a4a8f0b2e56f2c`  
		Last Modified: Mon, 29 Dec 2025 23:50:12 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eefaa2cb4295681c6d96e4651fc485b07576b6a49711537a4a9f7283c42d94`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 105.5 MB (105457507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bd50c1024430503d97929bd6c7f0e389cb97fb1f2b3efd533f8b12de73bb22`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc660b6f24ee1a1a2c684fece0e6b7e0e02708724ce97da0a1f58d771ce32804`  
		Last Modified: Mon, 29 Dec 2025 23:50:08 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1e239747f1b31084c3b43aee1c52536bcd8e41683da6d3e026067bf689cb3`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217819c94f97a81240ad47bd6d273fdf925ebaffb575e29a58865407d218f24b`  
		Last Modified: Mon, 29 Dec 2025 23:50:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:793cd5d70d6987512f3de95cabd0dd75cdbd4b487f634d39204cca0c1259a5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea258ab00932437927460b3cb8c30d5021b781de8b83edfc3a03f547a60f94a`

```dockerfile
```

-	Layers:
	-	`sha256:d809f4ab990a6df7902a9088b2c15dd392c546dfb1dd9ecf6363cbcd8c258029`  
		Last Modified: Tue, 30 Dec 2025 02:34:08 GMT  
		Size: 4.2 MB (4184411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc7673097a4e547638a4434f9e9e888c882666dd9cac92ba358aef897409fc4`  
		Last Modified: Tue, 30 Dec 2025 02:34:09 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:681cd28217f5c317b9dc604f4246b8ee2e74a0eb6a4000b8739feb9b7428e8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141402906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6697230efc8f63d0880368053b055920186cc1a1bb1d0f656ad22c18bef25817`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 29 Dec 2025 23:49:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 29 Dec 2025 23:50:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 29 Dec 2025 23:50:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 29 Dec 2025 23:50:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:50:11 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 29 Dec 2025 23:50:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 29 Dec 2025 23:50:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:50:23 GMT
VOLUME [/opt/couchdb/data]
# Mon, 29 Dec 2025 23:50:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 29 Dec 2025 23:50:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b28ac2949ff03d076b0d9c8f249d200b4bcf69165d413df5502ba3aaedf454`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dc6e1e29e7d607633a85bf66afea8f8890b3226d4e4624d67d98c4f64d2136`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 7.7 MB (7692057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c6ff449448e94fe2f6b83744855d7a4a51a68b9d1728d1862611e369a3df3b`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 370.5 KB (370489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cba339223745b3fd888daac1058d4ff730fe2d6f54b4dcc9447e9c8595a3519`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 76.5 KB (76463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539a2e947f04a8b08f17c261fffdef51bea21f220fa11e105a8859cce21f5d97`  
		Last Modified: Mon, 29 Dec 2025 23:50:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0623f96358d425f7c7c6e980fedd8edceec5093234fb6a47ed07223fc9610bac`  
		Last Modified: Mon, 29 Dec 2025 23:50:54 GMT  
		Size: 105.2 MB (105156261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c021dc14d00d1a5fa4b9aaabdb81fe6ee4b1eb8f7a7b803ff162b91259d532`  
		Last Modified: Mon, 29 Dec 2025 23:50:45 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227cb5d0e30b21b406c667ff03bf98fa15752b945418b4ff82ee27ae46ed1529`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded008b35a0d5d4f3da488006d2392e90f0159a48a34f52653bdfa9873ecc907`  
		Last Modified: Mon, 29 Dec 2025 23:50:46 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a57cc7e2430c4170e48f2795917639ec5d0543504bba350447c5d07529915`  
		Last Modified: Mon, 29 Dec 2025 23:50:45 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:f28093eee8046a743326e6ea677710c47e6d47e0bef6a915df0f6cbb83b2f29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967244bafb8f7690bf989609244cb13370aeb40e1d932ca4112055c2e1130d8`

```dockerfile
```

-	Layers:
	-	`sha256:0fb14dcfda03d85402b1dc4c686e205162a70c96082e9a1e2d5d2b04164d5836`  
		Last Modified: Tue, 30 Dec 2025 02:34:14 GMT  
		Size: 4.2 MB (4184704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66a7c455067fc1722c12cd4c459f4fcd43d8c7188963dfaf12e4a10d28ec3d1`  
		Last Modified: Tue, 30 Dec 2025 02:34:14 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:097a79b432ba83d04f56a870419464b2ae0012c7d22f3571be335cbe6fb1ae48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138764692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b664edaedd041921a1c187dce4b4ec17c8431ad36619bb30ccce7799916ec14`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:43:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Dec 2025 00:43:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 30 Dec 2025 00:43:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 30 Dec 2025 00:43:11 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 30 Dec 2025 00:43:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:43:16 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 30 Dec 2025 00:43:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 30 Dec 2025 00:43:32 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Dec 2025 00:43:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 30 Dec 2025 00:43:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:43:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Dec 2025 00:43:33 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 30 Dec 2025 00:43:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2c212caeb4bbcbc1a2aae869143027f520be5caa1135a217e767121ac1626f`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a08d04e9f82f45a67b46af862374c24224a6717000183ace0e83d43c9ea4933`  
		Last Modified: Tue, 30 Dec 2025 00:44:02 GMT  
		Size: 7.4 MB (7398088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef43570a8365ddd2c2f530578f7ab6932ad0954dae69973159ba5e7e7dd29895`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 372.1 KB (372097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8d5ab8f8d42dae898c00fd1281dbb1c3495bb8300bae20147a7a55b5eeb20`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 76.4 KB (76448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cc6d8fa43d6a9106826c6d5bdcca5ddae9593536e39f608bd43fce2d9d5ba6`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe85005dced89895410b4c8872001a3b45d39077d67a253350bed39bf5131fc`  
		Last Modified: Tue, 30 Dec 2025 00:44:08 GMT  
		Size: 104.0 MB (104028236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7332b0b429f7a79fa4a9fc758b1f9691c3233b407385a6c2b9f2d0733e76d0`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377fda69dd4b138b08a08a414245a50daddd123c4777a6f603bc1250e4019fd`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f22f88c0a1beaede0681cf9efc3c9317c306f909002e24fb8f7f77ecc34a67f`  
		Last Modified: Tue, 30 Dec 2025 00:44:06 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68718752dcb618d114c82c2fba317c2a114392ae48854bba56a3aadbc75638ef`  
		Last Modified: Tue, 30 Dec 2025 00:44:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:eff806d92f51590b41ba5bdc2564371adc66e1a4f6cc58d721e2d568d6ecd098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631566cdecdf5917d0fac5cef60417037a118a84354956afcac4de6f686aaaed`

```dockerfile
```

-	Layers:
	-	`sha256:cc24a91e945ce3d8b13559abd0468a49b0ce07e30f51f7063ea09b3f0d87b262`  
		Last Modified: Tue, 30 Dec 2025 02:34:19 GMT  
		Size: 4.2 MB (4180607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628f341500f6aec75f6745a857d74bdb9a9195dd735eb380666fbd2806ded2ee`  
		Last Modified: Tue, 30 Dec 2025 02:34:20 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
