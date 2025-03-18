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
$ docker pull couchdb@sha256:2817ad50b5c5cf7461f5963670466197426605a790a19a6208068c509a2d8a59
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
$ docker pull couchdb@sha256:0d0f27fc156274e23d4bb0c0286857c0fb1ea6c11316c12dea12c09a5d9aa84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133217708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053646816ef0480bc9d53b56cd594a0b5f9f40320861a94a95424cae9fcd25fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119e86acdcda03a05c1bc4f413cfa10d4c3baf6fc0fb948298ba32486fba56f`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26667909256fb1c2c11f8f66d8574a91b7865e284ac9468c0e9d6ea5f8bb8187`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 7.9 MB (7874939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b2b32a58bd87dc79007ee66ff939bc6fa2c08988698d75b5fce8db774c54e3`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 392.1 KB (392121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6e0cc1cf8d818639781ac12deddea0ee97da056cb8c7e66ea89cc0b3de4c59`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 76.3 KB (76287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a9148e7b3ae4af29a1f54229ea9d2a3740f880f4a9d2092312bb0b36e0471`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63676e1594260979fc6ead2713ef435fd9d98ef6aab559775aee6f4dbb8318ee`  
		Last Modified: Mon, 17 Mar 2025 23:19:10 GMT  
		Size: 96.7 MB (96664068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5531d971294e6eef1103868b479f8cfbd628f10069aa363516e3609a743de6`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df4d3f8786c0f873002516e84fccd71d71d1c00ce830aebc56a5f30c78016de`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d848f4fa7ff22fd859bb70af21cbf3dd58a683a72f9e05d725f9ffbffb2fc`  
		Last Modified: Mon, 17 Mar 2025 23:19:09 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66edba0cea7b5c08657ccc11ad41629d7953d284c935aff2cbb081a744c4942b`  
		Last Modified: Mon, 17 Mar 2025 23:19:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:cff00481b44bd445694591f497ddc366c86c5994a9cb2383ecc1e2efa1aa2f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734920f9c18e4d8543d604a7b8a026864d5e18b1dc9e2eb0ef9f00982ef07bb6`

```dockerfile
```

-	Layers:
	-	`sha256:80c4f4db0657e1b8949205014571203374d7ddd03e103c05304a27a669f03aa0`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 3.9 MB (3933589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3f9a06d84940d2544fd2dbe6075a6195abf96cd0670b3f3ecba8d6f4fb3bbc`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4235c10986cf4e6ad6efd3854ebe699e66858a63362e63c99cef183da360a839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132528410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2898f28ba57f645595fbd8d5bd1548bb5ff6766af34dad291ac2a257e022b549`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c33caa8f1c37207c6ab6e1ca5650c5d57d5a6dbf9a1ef519d3ddbead7841e0`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa47721d1ca081323ac6f4a47a1be344d0c706dc6b459ee279e38768405b7c6e`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 7.7 MB (7654537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9aafd07b43466115ae13ea095e08aec4c6fc240c79b85b17e5de9003740099e`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 348.9 KB (348938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed36b683ab7401d9d40e036ce36e420276d84506b8cce89be9c61609d4a714`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 76.3 KB (76284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd69118bdb1eede7f9e00435174dad5792736d452fca6453626a8e3a160b6026`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1ae2e969dbdc756c20fe194695b1e886c3abb9e31a37a91b840771627c21d`  
		Last Modified: Tue, 18 Mar 2025 05:47:15 GMT  
		Size: 96.4 MB (96399175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b79c5d92cc88e34e15abcd58be7ef03fefc14b6c36e4843e241180817df6b68`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c52a367fe442effe162e647012b056524285d86987b4c93af6aa950b50abc`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3629c4ee1604981244b3c413c46175af50cce9ad264273960b89e147e6f541a3`  
		Last Modified: Tue, 18 Mar 2025 05:47:13 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7288eb637596167f724710f8b75f0065ce17f586424ac441b863b276f3d3e503`  
		Last Modified: Tue, 18 Mar 2025 05:47:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ccf4066f87bdcae21316cb9f28493e975f6283d776e0a5f1a44a7f7f234dac3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee84e959f5607c147c19611c944aaaef5086d36d51c5bea0cc8f6b554e2ad4e`

```dockerfile
```

-	Layers:
	-	`sha256:cb6e5450c1da1629614bf516edbe60f7bfebc4adf94711974ed2b164d491249c`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 3.9 MB (3933882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2984aa27ffef7bd2fcda7ba5e210acd3f2cdc3dd042562222e58e630aff2bdb`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:8dea9e194a22159ea358128138988b63f72c626801577e6c3c19515c5b828a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55f8f76699a3bb68c9635bf84d95d7275bc81ce766120d29b36496a5485a4a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fff4085857b75f955d31db3d1c8ea50eaadbf6fd1a589e6cc82547ce0538e8`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c1de50e3e3779d8b50904209521f50f18d5be8cfefacc829ad006b72bc97c1`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 7.4 MB (7387912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9358d54429af4b5850c3a0009db2d388e8039bfa84b3f1d5de61739a5634ba4e`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 355.6 KB (355602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75d4154da95f28f7b46f23d395dba959f2e0090e5f9b4921b90099da94bc177`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 76.3 KB (76338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0a5daf834d8d5d9ffe7a32edde70179feea152ac5ddd0f6d8fb64d2b8d0fa`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624b1f9868098fd18264b805a2b40c71b54828fd8c30450a7c91f98f9298bc13`  
		Last Modified: Tue, 18 Mar 2025 02:39:26 GMT  
		Size: 95.3 MB (95289553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bc1381e02da40861f0194763b5d3a57eae6551945039083d3362fe716690bb`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0ac32ced35b60906f48a5468aac39053da45bee48d27f0b90c9c7be3e8948f`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f25754a45af3246f53c512f27bef5ed2c05ff1a4d39bad5eb00813f162c63a`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe59d94e128d095b5c96da87643a41f7f6021740a9b98e626ed7e09804bf62a`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:8b77911560a3e86bb7b788cd1e33ed39a310fac7f40a163314601139a862f6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba0dde34782e26b9c808a216d4ec698e234f4900acb004f78f3c9c9c00cbacc`

```dockerfile
```

-	Layers:
	-	`sha256:a5bcaef38230d3916476a94e827e476a62c13005fdb261f07aa4df222e70620d`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 3.9 MB (3932677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ebd6bb3bd3309122989cf41a614d92a06482e06b77665893f58ba41f20c4755`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:480c03d21bbe7380622afd212eb533dd2c57187aed4de2a581b2bbf9bbbb6e3c
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
$ docker pull couchdb@sha256:843a4b14c2866528828ec65594a6504e24e9e90aaa459532c7c19731d1bed89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155526106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecb9bff1e4b8e342e1181bbe81dbbd5fd650c6eb2645b009e6834744be2392d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a8b0ae0dcc4020d289309a30b5e61f2752bb86ee9c06208bfd5d678a1c33ea`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2fba5de125c16a4984794e1dfa3e1b6f4a60bb17857b5804e58919a60318f0`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 7.9 MB (7874949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bd6a8af5e563a24c7a02304439ce9203607b03618bfd2b71f68489573c4996`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 77.3 MB (77297508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7ac445ebb09ff4a31c7444d9da19dccdee34798107e08ca28b39423a54ec07`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 415.0 KB (414961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d4551120e8a8784b777c61df9054f6b55ecc56f6ffc66432f4d26773128f89`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 99.3 KB (99324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88b8831979b4f3fb68a279ca056c851f3331c155bf61b8fe8ec0fb4b3a235e`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd333fd6fede6b8a9440ad53cfa20c1946945ddd66a73749e8c2f39e408c418`  
		Last Modified: Mon, 17 Mar 2025 23:14:36 GMT  
		Size: 41.6 MB (41632619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7acb021b38ccfd706854543aaaa48736e387f1e60cb767464a08983a5c0957e`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5b02fcdcedfc3a36b048fa49990f7e6916b5c99fa08506abbd7e113b31bc21a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e22bff18db5e7bda13209389149a9d2f553c3f8ad587440c8c99ce9114cc0dc`

```dockerfile
```

-	Layers:
	-	`sha256:2399a29666758b3e34aaa9f780e0562ac9230ffbcdd7ad72f5cb5eecc13185a2`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 3.5 MB (3462078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17d40ea86b19f032c232f1bd4aa32522a2ef844b6f487db6e13836f6a523efd0`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d1a3a84a3df0fe4ca75d7bc2ae5ae8839e9bc8995574b40a984d35bbb28c30fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154326836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37fc5d7fd12fa100c47ace85b27029357cb64546ebcf3b4f620cdabe08ba97e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1122399be6ebcbc5eb0c3718a224fd593404e643cff71a3607bcf9d1b490ae1`  
		Last Modified: Tue, 18 Mar 2025 05:42:23 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d9c714980df1bae6526a96d2475632434af8aae89aa63746733d0e58de1bc0`  
		Last Modified: Tue, 18 Mar 2025 05:42:24 GMT  
		Size: 7.7 MB (7654511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f109be71759b9e4f04f072216c5a972e9d3155df5ee4a0d82af77024ba7b2f`  
		Last Modified: Tue, 18 Mar 2025 05:42:25 GMT  
		Size: 76.6 MB (76624286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd18e3f49d6508087473a9e2cb39df1b8f1c7d86659e3b331b7b71b6dc976aaf`  
		Last Modified: Tue, 18 Mar 2025 05:42:23 GMT  
		Size: 371.7 KB (371710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9762ce4a25997657cf259e8155a196f4caba6d40f4be8e826475c57ca44c1c84`  
		Last Modified: Tue, 18 Mar 2025 05:42:25 GMT  
		Size: 99.2 KB (99247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3a605b3db57b20ba9ff353f60aa933d66d3c72a6bc2e22c2375bc0892f7ed8`  
		Last Modified: Tue, 18 Mar 2025 05:42:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ea072b9e62ea1e78fe7fad3341ba4a2542843dc3207d9485e268c92358fbc9`  
		Last Modified: Tue, 18 Mar 2025 05:42:26 GMT  
		Size: 41.5 MB (41531163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf48c8a13478a41f445e27b539434b8449ab1f509ee6819d7f5014a19ded91a`  
		Last Modified: Tue, 18 Mar 2025 05:42:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc2c7e0a7a60bd15317e3387aecd9c56f9169968483c2f117a056dbdaa6e3bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865acf78a7ec05ed58f47e39296dcd5930261ffb3357be1eeb186e5c4b3b2f6a`

```dockerfile
```

-	Layers:
	-	`sha256:50557058ab99050c2a5e27df1016013b0b31061c45da485a47a6f7da42015b48`  
		Last Modified: Tue, 18 Mar 2025 05:42:24 GMT  
		Size: 3.5 MB (3460754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fbaf5e4300d54a099b2705897f95858f79075f9b83018c24703e0bb7b5e264`  
		Last Modified: Tue, 18 Mar 2025 05:42:23 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:0f419b5abe7840611a4b8bb2efe680ce0885785782ea76427c4fc77ce32c37a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149147053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d8647f6456245be9d375555fecba69fd6c842b4e0fb54213929b999a44970f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e720cb9f4a4cd7e11f8791a6e98ff5694298e69d690f0890c38dfd48d9de945`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9df99bc8f4b12baba40764d153c92413f0ac45797459e4a9dfae8b511b017`  
		Last Modified: Tue, 18 Mar 2025 02:31:32 GMT  
		Size: 7.4 MB (7387934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfcfe3bb3ee8a55d32841fe268b6a556078d92a21601fafed81bd6455b617d7`  
		Last Modified: Tue, 18 Mar 2025 02:31:33 GMT  
		Size: 73.1 MB (73065130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acf41391bd54ff1af050714ce1ea5c03a13aeadd6ce4c0d8ba2d9095d3a447f`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 378.0 KB (378042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d5c57ca9b0d60383c2565827fe955f2baf3aad038fe1308d1a3ad9f4d53d28`  
		Last Modified: Tue, 18 Mar 2025 02:31:32 GMT  
		Size: 99.4 KB (99410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4bb03624919b9a8994bf34ac959f72de679cf4f360665d580bf4beb99011d7`  
		Last Modified: Tue, 18 Mar 2025 02:31:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930bd62fabf26859d589b122c231c229df73c0bed821183bb8ad71b677b5f14`  
		Last Modified: Tue, 18 Mar 2025 02:31:34 GMT  
		Size: 41.4 MB (41353597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a106e335e81ba51b376b8fdc3b22bf50cefd349fb7b2a6370c554cf2529d75ba`  
		Last Modified: Tue, 18 Mar 2025 02:31:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:000ca8119debf7df8a69d388ce93e7869bfac53d6d9282c23f31795ca7c8e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cc3d38bc75fd99eacb21321f3c435b4aca7549b0dfaada69a752c321584e7c`

```dockerfile
```

-	Layers:
	-	`sha256:361d0930ea5eb2f5860f03e1cb3cc9021a80aede57f5cdaa226d283ede1e48e5`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 3.5 MB (3455499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b199b67ccee64144e37c10ac1a64902962caec2a9d721d4a45535281e2adb19`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:d05a2e16abb42c4f348c0a762365cb6331b5288fedc87046937a77b648e311f6
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
$ docker pull couchdb@sha256:63b2f2a1d7354ba6b957cf8746478e73612f62fbd1e0c5af51808a7a89120585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96704956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5248f2b3d64c1d44fac433b2d49139c14798dcae24cfb04f8f6b19eb08b1b8a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643154e4e28c3cb4a899fb1f1473d062fcf0582e9ab8eabc7117a163d39d1040`  
		Last Modified: Mon, 17 Mar 2025 23:14:24 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2525b643b4eb9b983190357e35c6c6572e1a93777e006102c45186e3203e4e6b`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 7.9 MB (7874911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b380d687f6a12b92a83262140fcb539898e46e4f5a413114a18082b3f1f95`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 392.1 KB (392125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3267d055b66be954875966cd9c418c9c40a4cbfbd8b8b2146b5aed235d4e4d0c`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 76.3 KB (76300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c44e82d771c6ec0abcd8d0519a7118a116168dedfdadc7dc2e67c5092b7b9c`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0c41c7ea2b57a61f6f41511e6a61caeefa26ec3f0a427f93c26dcccd10d531`  
		Last Modified: Mon, 17 Mar 2025 23:14:26 GMT  
		Size: 60.2 MB (60151328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c81dbef0a7b08bb95cd9e60deca4ebdcf629ea9cb7e446c184ef1e028e68cf6`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4f38d3303624979620cd76434545eede922a23b4702b7debf9bfbdf44c80fc`  
		Last Modified: Mon, 17 Mar 2025 23:14:26 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c950154cd3a56381ae446b6dab3d1bbe351edbce5c110631dac92244253ac107`  
		Last Modified: Mon, 17 Mar 2025 23:14:26 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5996f6c1201b42ad75900866d284c04c68193a030bab2adb5b03d534c59281`  
		Last Modified: Mon, 17 Mar 2025 23:14:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ed18c300cfd96b12ed106169ff49b12e260671172028d954a38c84a82916f0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a9fc98fd1305311e06fdec240b1a9d40953ce92e11c3e318e02b5252b4b495`

```dockerfile
```

-	Layers:
	-	`sha256:a4e542d43c71e0728b11bae3564dfdff055d2a812fea1d10e3f02fe347a83be8`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 3.7 MB (3734868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a331d8c23b3a2704e8a8d0087fb79bf5571336fade383e792f1c9ed96445441c`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5b823cb5cd19854b52641b0b04d9f29b12f00b1d787c38931b095e8a377aec79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96063606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a26679f5684848f9ae4a9f41dc14e77ff451a9ee13b5dd8b29e5f2b9526a5c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c33caa8f1c37207c6ab6e1ca5650c5d57d5a6dbf9a1ef519d3ddbead7841e0`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa47721d1ca081323ac6f4a47a1be344d0c706dc6b459ee279e38768405b7c6e`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 7.7 MB (7654537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9aafd07b43466115ae13ea095e08aec4c6fc240c79b85b17e5de9003740099e`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 348.9 KB (348938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed36b683ab7401d9d40e036ce36e420276d84506b8cce89be9c61609d4a714`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 76.3 KB (76284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384ae146a3002ea15148d77de99cf23d787ae9f044f59fc8169d8ade234fb163`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c74bffaa09ab0befabf6a1b727b7767da13b1810a8347b268d396661bf1a`  
		Last Modified: Tue, 18 Mar 2025 05:36:45 GMT  
		Size: 59.9 MB (59934381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d1097c2036f2ad104e0b00a2513c37c7fa68860e32dfdb2cd8c90163308d8`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aa4f2354e1a36cb4dba67fd34afc5c1c7645d6ed7199f2ed407b2c1d85d622`  
		Last Modified: Tue, 18 Mar 2025 05:36:44 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d7bfedb6632a4806dae309c0258955e6aef67a3268e1f7fb6a19ae4e9701f`  
		Last Modified: Tue, 18 Mar 2025 05:36:44 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56969042131049c518abfbb029a1a786d1f52d8e383ad4206d072d9a32b5ef61`  
		Last Modified: Tue, 18 Mar 2025 05:36:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:261a812557978521ef744b362440cd7d3598649b2ed00cb67a2682670ed8ebf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ca71063cd763ad481305fcf32e293e151ccf1ffe991fdd51f6747ce4017836`

```dockerfile
```

-	Layers:
	-	`sha256:9a28064e65c9f9424f72014c70aa718c74f6eb0a7c64bcfd36e266edb4cab794`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 3.7 MB (3735137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42817116f2173841e56226f368a064c065f9890286f4e7d549ecfcd9484fbf29`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4a0a33a067f3303379443d248ac835d1cdbdf37d0cb2ff2684eb145b3eb6af08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102840888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e125ea0d28af960490fa22b385b8cf5c5fc4ab0d3109c2a2c06dd86ea835db83`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
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
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a195f613a32924328138451b51e05a39fd04e90dd5b54ad64ca1d5cd1daf1593`  
		Last Modified: Tue, 18 Mar 2025 04:23:06 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44848f9b8cdcf53ec0c21c93ff5c8ba7572a486a201ef3fc6206ad26be9f4611`  
		Last Modified: Tue, 18 Mar 2025 04:23:07 GMT  
		Size: 8.9 MB (8890133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f445f478a922a4e15f57fd32e5148b1f7f217a97a2555fcb1b73324d032e303`  
		Last Modified: Tue, 18 Mar 2025 04:23:07 GMT  
		Size: 444.7 KB (444700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10008ae9d35d78696576c2d1d1fc55b2ec2dec4e354f0f00f637c9f3ac69c0a2`  
		Last Modified: Tue, 18 Mar 2025 04:23:06 GMT  
		Size: 76.4 KB (76361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2f24bc63063511d477176f769abe1a0a92c0ac894c9168f039a089a54f7bef`  
		Last Modified: Tue, 18 Mar 2025 04:23:07 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e163a213ed2b44fd75d35824a76405079a745e2f2249db7a939e4e215c919b7`  
		Last Modified: Tue, 18 Mar 2025 04:23:10 GMT  
		Size: 61.4 MB (61376441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a434e08a66f05d5018df4139ec805f90198d9638468976be672ccbbf4a147a64`  
		Last Modified: Tue, 18 Mar 2025 04:23:08 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc07660205fdddbe67db0b63eb1336d0023506c1b69d760e80bf0076db561b0f`  
		Last Modified: Tue, 18 Mar 2025 04:23:08 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb1c1e90ab293acd64fea07f88d96fec4842eb0299e753dc39c752cba6741af`  
		Last Modified: Tue, 18 Mar 2025 04:23:08 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e349d326ac4d50f0d83aea27d634ad4c831c6acf184f8a072268bffb74eda7`  
		Last Modified: Tue, 18 Mar 2025 04:23:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a813533c7c87320a2d7424de64da4143d34278d4babe9e2f0b0f0b607aa614ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849641aaf31af14b4169595842fccb9d21ba8ae64f455572e8367253c3d4e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:f55b12d6f4684e81a1136afa02b1610383b72b94171024f03d4305c214b00d53`  
		Last Modified: Tue, 18 Mar 2025 04:23:07 GMT  
		Size: 3.7 MB (3739372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9904eea143bede419ca450256624615cfcb3b3cb5788e18d754adf85c2675d6a`  
		Last Modified: Tue, 18 Mar 2025 04:23:06 GMT  
		Size: 31.2 KB (31235 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:b78f8d1f5c8213e06b9a8483a0f4a946fc557514c4595cbf5e80f33410771941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93427351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a2660253235e8d309b25c03406e47a7dc6f63a1c0281167235c57a9952887a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fff4085857b75f955d31db3d1c8ea50eaadbf6fd1a589e6cc82547ce0538e8`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c1de50e3e3779d8b50904209521f50f18d5be8cfefacc829ad006b72bc97c1`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 7.4 MB (7387912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9358d54429af4b5850c3a0009db2d388e8039bfa84b3f1d5de61739a5634ba4e`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 355.6 KB (355602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75d4154da95f28f7b46f23d395dba959f2e0090e5f9b4921b90099da94bc177`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 76.3 KB (76338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0afded4898fa201d22af08a7a8332e900a7d1df8c92f76edd9129ec8aaee5b`  
		Last Modified: Tue, 18 Mar 2025 02:21:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbd2311946cc07279411345b90fa9f436a65f977ca133c1c01af0a66a312b4f`  
		Last Modified: Tue, 18 Mar 2025 02:21:57 GMT  
		Size: 58.7 MB (58741004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae69ba6d28860d1d9452e7b9974d35554a2aad68a9c4db6c57dd1b8e9d799dce`  
		Last Modified: Tue, 18 Mar 2025 02:21:56 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b288fdb8d672f28fa327c61c42498c4658f0778f0c5ea8e959442e50f9581726`  
		Last Modified: Tue, 18 Mar 2025 02:21:56 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b64bbbce2743133724d29bb9f1f35b2cdbe4258461b24d90508eccdcfbbca46`  
		Last Modified: Tue, 18 Mar 2025 02:21:57 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aca748287ce0553b680ab7995eeb3f768c69ca4750a7e155d586ac8b746748`  
		Last Modified: Tue, 18 Mar 2025 02:21:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f68217fdaee645e016c503dd78555ad8c4f7d1acf2288fe86fb065a3d64b903f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338e990115f463a47e278b98f101e480e1887f0ff648d9dd53285ace506f339d`

```dockerfile
```

-	Layers:
	-	`sha256:e5c78728bfb4dc58e88430aec86de040a82cb6b231fecdcfc63724b0256a5de2`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 3.7 MB (3733956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abda4ec2568664b7b98fce5c6bf56a7e507e9d3abd5cfd3a1aad3a03c2b0890d`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:d05a2e16abb42c4f348c0a762365cb6331b5288fedc87046937a77b648e311f6
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
$ docker pull couchdb@sha256:63b2f2a1d7354ba6b957cf8746478e73612f62fbd1e0c5af51808a7a89120585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96704956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5248f2b3d64c1d44fac433b2d49139c14798dcae24cfb04f8f6b19eb08b1b8a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643154e4e28c3cb4a899fb1f1473d062fcf0582e9ab8eabc7117a163d39d1040`  
		Last Modified: Mon, 17 Mar 2025 23:14:24 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2525b643b4eb9b983190357e35c6c6572e1a93777e006102c45186e3203e4e6b`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 7.9 MB (7874911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b380d687f6a12b92a83262140fcb539898e46e4f5a413114a18082b3f1f95`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 392.1 KB (392125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3267d055b66be954875966cd9c418c9c40a4cbfbd8b8b2146b5aed235d4e4d0c`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 76.3 KB (76300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c44e82d771c6ec0abcd8d0519a7118a116168dedfdadc7dc2e67c5092b7b9c`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0c41c7ea2b57a61f6f41511e6a61caeefa26ec3f0a427f93c26dcccd10d531`  
		Last Modified: Mon, 17 Mar 2025 23:14:26 GMT  
		Size: 60.2 MB (60151328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c81dbef0a7b08bb95cd9e60deca4ebdcf629ea9cb7e446c184ef1e028e68cf6`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4f38d3303624979620cd76434545eede922a23b4702b7debf9bfbdf44c80fc`  
		Last Modified: Mon, 17 Mar 2025 23:14:26 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c950154cd3a56381ae446b6dab3d1bbe351edbce5c110631dac92244253ac107`  
		Last Modified: Mon, 17 Mar 2025 23:14:26 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5996f6c1201b42ad75900866d284c04c68193a030bab2adb5b03d534c59281`  
		Last Modified: Mon, 17 Mar 2025 23:14:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ed18c300cfd96b12ed106169ff49b12e260671172028d954a38c84a82916f0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a9fc98fd1305311e06fdec240b1a9d40953ce92e11c3e318e02b5252b4b495`

```dockerfile
```

-	Layers:
	-	`sha256:a4e542d43c71e0728b11bae3564dfdff055d2a812fea1d10e3f02fe347a83be8`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 3.7 MB (3734868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a331d8c23b3a2704e8a8d0087fb79bf5571336fade383e792f1c9ed96445441c`  
		Last Modified: Mon, 17 Mar 2025 23:14:25 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5b823cb5cd19854b52641b0b04d9f29b12f00b1d787c38931b095e8a377aec79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96063606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a26679f5684848f9ae4a9f41dc14e77ff451a9ee13b5dd8b29e5f2b9526a5c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c33caa8f1c37207c6ab6e1ca5650c5d57d5a6dbf9a1ef519d3ddbead7841e0`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa47721d1ca081323ac6f4a47a1be344d0c706dc6b459ee279e38768405b7c6e`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 7.7 MB (7654537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9aafd07b43466115ae13ea095e08aec4c6fc240c79b85b17e5de9003740099e`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 348.9 KB (348938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed36b683ab7401d9d40e036ce36e420276d84506b8cce89be9c61609d4a714`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 76.3 KB (76284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384ae146a3002ea15148d77de99cf23d787ae9f044f59fc8169d8ade234fb163`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364c74bffaa09ab0befabf6a1b727b7767da13b1810a8347b268d396661bf1a`  
		Last Modified: Tue, 18 Mar 2025 05:36:45 GMT  
		Size: 59.9 MB (59934381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d1097c2036f2ad104e0b00a2513c37c7fa68860e32dfdb2cd8c90163308d8`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aa4f2354e1a36cb4dba67fd34afc5c1c7645d6ed7199f2ed407b2c1d85d622`  
		Last Modified: Tue, 18 Mar 2025 05:36:44 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d7bfedb6632a4806dae309c0258955e6aef67a3268e1f7fb6a19ae4e9701f`  
		Last Modified: Tue, 18 Mar 2025 05:36:44 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56969042131049c518abfbb029a1a786d1f52d8e383ad4206d072d9a32b5ef61`  
		Last Modified: Tue, 18 Mar 2025 05:36:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:261a812557978521ef744b362440cd7d3598649b2ed00cb67a2682670ed8ebf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ca71063cd763ad481305fcf32e293e151ccf1ffe991fdd51f6747ce4017836`

```dockerfile
```

-	Layers:
	-	`sha256:9a28064e65c9f9424f72014c70aa718c74f6eb0a7c64bcfd36e266edb4cab794`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 3.7 MB (3735137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42817116f2173841e56226f368a064c065f9890286f4e7d549ecfcd9484fbf29`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4a0a33a067f3303379443d248ac835d1cdbdf37d0cb2ff2684eb145b3eb6af08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102840888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e125ea0d28af960490fa22b385b8cf5c5fc4ab0d3109c2a2c06dd86ea835db83`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
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
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a195f613a32924328138451b51e05a39fd04e90dd5b54ad64ca1d5cd1daf1593`  
		Last Modified: Tue, 18 Mar 2025 04:23:06 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44848f9b8cdcf53ec0c21c93ff5c8ba7572a486a201ef3fc6206ad26be9f4611`  
		Last Modified: Tue, 18 Mar 2025 04:23:07 GMT  
		Size: 8.9 MB (8890133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f445f478a922a4e15f57fd32e5148b1f7f217a97a2555fcb1b73324d032e303`  
		Last Modified: Tue, 18 Mar 2025 04:23:07 GMT  
		Size: 444.7 KB (444700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10008ae9d35d78696576c2d1d1fc55b2ec2dec4e354f0f00f637c9f3ac69c0a2`  
		Last Modified: Tue, 18 Mar 2025 04:23:06 GMT  
		Size: 76.4 KB (76361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2f24bc63063511d477176f769abe1a0a92c0ac894c9168f039a089a54f7bef`  
		Last Modified: Tue, 18 Mar 2025 04:23:07 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e163a213ed2b44fd75d35824a76405079a745e2f2249db7a939e4e215c919b7`  
		Last Modified: Tue, 18 Mar 2025 04:23:10 GMT  
		Size: 61.4 MB (61376441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a434e08a66f05d5018df4139ec805f90198d9638468976be672ccbbf4a147a64`  
		Last Modified: Tue, 18 Mar 2025 04:23:08 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc07660205fdddbe67db0b63eb1336d0023506c1b69d760e80bf0076db561b0f`  
		Last Modified: Tue, 18 Mar 2025 04:23:08 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb1c1e90ab293acd64fea07f88d96fec4842eb0299e753dc39c752cba6741af`  
		Last Modified: Tue, 18 Mar 2025 04:23:08 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e349d326ac4d50f0d83aea27d634ad4c831c6acf184f8a072268bffb74eda7`  
		Last Modified: Tue, 18 Mar 2025 04:23:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a813533c7c87320a2d7424de64da4143d34278d4babe9e2f0b0f0b607aa614ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849641aaf31af14b4169595842fccb9d21ba8ae64f455572e8367253c3d4e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:f55b12d6f4684e81a1136afa02b1610383b72b94171024f03d4305c214b00d53`  
		Last Modified: Tue, 18 Mar 2025 04:23:07 GMT  
		Size: 3.7 MB (3739372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9904eea143bede419ca450256624615cfcb3b3cb5788e18d754adf85c2675d6a`  
		Last Modified: Tue, 18 Mar 2025 04:23:06 GMT  
		Size: 31.2 KB (31235 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:b78f8d1f5c8213e06b9a8483a0f4a946fc557514c4595cbf5e80f33410771941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93427351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a2660253235e8d309b25c03406e47a7dc6f63a1c0281167235c57a9952887a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fff4085857b75f955d31db3d1c8ea50eaadbf6fd1a589e6cc82547ce0538e8`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c1de50e3e3779d8b50904209521f50f18d5be8cfefacc829ad006b72bc97c1`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 7.4 MB (7387912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9358d54429af4b5850c3a0009db2d388e8039bfa84b3f1d5de61739a5634ba4e`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 355.6 KB (355602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75d4154da95f28f7b46f23d395dba959f2e0090e5f9b4921b90099da94bc177`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 76.3 KB (76338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0afded4898fa201d22af08a7a8332e900a7d1df8c92f76edd9129ec8aaee5b`  
		Last Modified: Tue, 18 Mar 2025 02:21:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbd2311946cc07279411345b90fa9f436a65f977ca133c1c01af0a66a312b4f`  
		Last Modified: Tue, 18 Mar 2025 02:21:57 GMT  
		Size: 58.7 MB (58741004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae69ba6d28860d1d9452e7b9974d35554a2aad68a9c4db6c57dd1b8e9d799dce`  
		Last Modified: Tue, 18 Mar 2025 02:21:56 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b288fdb8d672f28fa327c61c42498c4658f0778f0c5ea8e959442e50f9581726`  
		Last Modified: Tue, 18 Mar 2025 02:21:56 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b64bbbce2743133724d29bb9f1f35b2cdbe4258461b24d90508eccdcfbbca46`  
		Last Modified: Tue, 18 Mar 2025 02:21:57 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aca748287ce0553b680ab7995eeb3f768c69ca4750a7e155d586ac8b746748`  
		Last Modified: Tue, 18 Mar 2025 02:21:57 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f68217fdaee645e016c503dd78555ad8c4f7d1acf2288fe86fb065a3d64b903f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338e990115f463a47e278b98f101e480e1887f0ff648d9dd53285ace506f339d`

```dockerfile
```

-	Layers:
	-	`sha256:e5c78728bfb4dc58e88430aec86de040a82cb6b231fecdcfc63724b0256a5de2`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 3.7 MB (3733956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abda4ec2568664b7b98fce5c6bf56a7e507e9d3abd5cfd3a1aad3a03c2b0890d`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:2817ad50b5c5cf7461f5963670466197426605a790a19a6208068c509a2d8a59
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
$ docker pull couchdb@sha256:0d0f27fc156274e23d4bb0c0286857c0fb1ea6c11316c12dea12c09a5d9aa84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133217708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053646816ef0480bc9d53b56cd594a0b5f9f40320861a94a95424cae9fcd25fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119e86acdcda03a05c1bc4f413cfa10d4c3baf6fc0fb948298ba32486fba56f`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26667909256fb1c2c11f8f66d8574a91b7865e284ac9468c0e9d6ea5f8bb8187`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 7.9 MB (7874939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b2b32a58bd87dc79007ee66ff939bc6fa2c08988698d75b5fce8db774c54e3`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 392.1 KB (392121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6e0cc1cf8d818639781ac12deddea0ee97da056cb8c7e66ea89cc0b3de4c59`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 76.3 KB (76287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a9148e7b3ae4af29a1f54229ea9d2a3740f880f4a9d2092312bb0b36e0471`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63676e1594260979fc6ead2713ef435fd9d98ef6aab559775aee6f4dbb8318ee`  
		Last Modified: Mon, 17 Mar 2025 23:19:10 GMT  
		Size: 96.7 MB (96664068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5531d971294e6eef1103868b479f8cfbd628f10069aa363516e3609a743de6`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df4d3f8786c0f873002516e84fccd71d71d1c00ce830aebc56a5f30c78016de`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d848f4fa7ff22fd859bb70af21cbf3dd58a683a72f9e05d725f9ffbffb2fc`  
		Last Modified: Mon, 17 Mar 2025 23:19:09 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66edba0cea7b5c08657ccc11ad41629d7953d284c935aff2cbb081a744c4942b`  
		Last Modified: Mon, 17 Mar 2025 23:19:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:cff00481b44bd445694591f497ddc366c86c5994a9cb2383ecc1e2efa1aa2f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734920f9c18e4d8543d604a7b8a026864d5e18b1dc9e2eb0ef9f00982ef07bb6`

```dockerfile
```

-	Layers:
	-	`sha256:80c4f4db0657e1b8949205014571203374d7ddd03e103c05304a27a669f03aa0`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 3.9 MB (3933589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3f9a06d84940d2544fd2dbe6075a6195abf96cd0670b3f3ecba8d6f4fb3bbc`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4235c10986cf4e6ad6efd3854ebe699e66858a63362e63c99cef183da360a839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132528410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2898f28ba57f645595fbd8d5bd1548bb5ff6766af34dad291ac2a257e022b549`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c33caa8f1c37207c6ab6e1ca5650c5d57d5a6dbf9a1ef519d3ddbead7841e0`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa47721d1ca081323ac6f4a47a1be344d0c706dc6b459ee279e38768405b7c6e`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 7.7 MB (7654537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9aafd07b43466115ae13ea095e08aec4c6fc240c79b85b17e5de9003740099e`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 348.9 KB (348938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed36b683ab7401d9d40e036ce36e420276d84506b8cce89be9c61609d4a714`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 76.3 KB (76284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd69118bdb1eede7f9e00435174dad5792736d452fca6453626a8e3a160b6026`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1ae2e969dbdc756c20fe194695b1e886c3abb9e31a37a91b840771627c21d`  
		Last Modified: Tue, 18 Mar 2025 05:47:15 GMT  
		Size: 96.4 MB (96399175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b79c5d92cc88e34e15abcd58be7ef03fefc14b6c36e4843e241180817df6b68`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c52a367fe442effe162e647012b056524285d86987b4c93af6aa950b50abc`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3629c4ee1604981244b3c413c46175af50cce9ad264273960b89e147e6f541a3`  
		Last Modified: Tue, 18 Mar 2025 05:47:13 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7288eb637596167f724710f8b75f0065ce17f586424ac441b863b276f3d3e503`  
		Last Modified: Tue, 18 Mar 2025 05:47:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:ccf4066f87bdcae21316cb9f28493e975f6283d776e0a5f1a44a7f7f234dac3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee84e959f5607c147c19611c944aaaef5086d36d51c5bea0cc8f6b554e2ad4e`

```dockerfile
```

-	Layers:
	-	`sha256:cb6e5450c1da1629614bf516edbe60f7bfebc4adf94711974ed2b164d491249c`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 3.9 MB (3933882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2984aa27ffef7bd2fcda7ba5e210acd3f2cdc3dd042562222e58e630aff2bdb`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:8dea9e194a22159ea358128138988b63f72c626801577e6c3c19515c5b828a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55f8f76699a3bb68c9635bf84d95d7275bc81ce766120d29b36496a5485a4a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fff4085857b75f955d31db3d1c8ea50eaadbf6fd1a589e6cc82547ce0538e8`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c1de50e3e3779d8b50904209521f50f18d5be8cfefacc829ad006b72bc97c1`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 7.4 MB (7387912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9358d54429af4b5850c3a0009db2d388e8039bfa84b3f1d5de61739a5634ba4e`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 355.6 KB (355602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75d4154da95f28f7b46f23d395dba959f2e0090e5f9b4921b90099da94bc177`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 76.3 KB (76338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0a5daf834d8d5d9ffe7a32edde70179feea152ac5ddd0f6d8fb64d2b8d0fa`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624b1f9868098fd18264b805a2b40c71b54828fd8c30450a7c91f98f9298bc13`  
		Last Modified: Tue, 18 Mar 2025 02:39:26 GMT  
		Size: 95.3 MB (95289553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bc1381e02da40861f0194763b5d3a57eae6551945039083d3362fe716690bb`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0ac32ced35b60906f48a5468aac39053da45bee48d27f0b90c9c7be3e8948f`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f25754a45af3246f53c512f27bef5ed2c05ff1a4d39bad5eb00813f162c63a`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe59d94e128d095b5c96da87643a41f7f6021740a9b98e626ed7e09804bf62a`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:8b77911560a3e86bb7b788cd1e33ed39a310fac7f40a163314601139a862f6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba0dde34782e26b9c808a216d4ec698e234f4900acb004f78f3c9c9c00cbacc`

```dockerfile
```

-	Layers:
	-	`sha256:a5bcaef38230d3916476a94e827e476a62c13005fdb261f07aa4df222e70620d`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 3.9 MB (3932677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ebd6bb3bd3309122989cf41a614d92a06482e06b77665893f58ba41f20c4755`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:480c03d21bbe7380622afd212eb533dd2c57187aed4de2a581b2bbf9bbbb6e3c
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
$ docker pull couchdb@sha256:843a4b14c2866528828ec65594a6504e24e9e90aaa459532c7c19731d1bed89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155526106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecb9bff1e4b8e342e1181bbe81dbbd5fd650c6eb2645b009e6834744be2392d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a8b0ae0dcc4020d289309a30b5e61f2752bb86ee9c06208bfd5d678a1c33ea`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2fba5de125c16a4984794e1dfa3e1b6f4a60bb17857b5804e58919a60318f0`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 7.9 MB (7874949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bd6a8af5e563a24c7a02304439ce9203607b03618bfd2b71f68489573c4996`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 77.3 MB (77297508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7ac445ebb09ff4a31c7444d9da19dccdee34798107e08ca28b39423a54ec07`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 415.0 KB (414961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d4551120e8a8784b777c61df9054f6b55ecc56f6ffc66432f4d26773128f89`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 99.3 KB (99324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88b8831979b4f3fb68a279ca056c851f3331c155bf61b8fe8ec0fb4b3a235e`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd333fd6fede6b8a9440ad53cfa20c1946945ddd66a73749e8c2f39e408c418`  
		Last Modified: Mon, 17 Mar 2025 23:14:36 GMT  
		Size: 41.6 MB (41632619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7acb021b38ccfd706854543aaaa48736e387f1e60cb767464a08983a5c0957e`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5b02fcdcedfc3a36b048fa49990f7e6916b5c99fa08506abbd7e113b31bc21a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e22bff18db5e7bda13209389149a9d2f553c3f8ad587440c8c99ce9114cc0dc`

```dockerfile
```

-	Layers:
	-	`sha256:2399a29666758b3e34aaa9f780e0562ac9230ffbcdd7ad72f5cb5eecc13185a2`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 3.5 MB (3462078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17d40ea86b19f032c232f1bd4aa32522a2ef844b6f487db6e13836f6a523efd0`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d1a3a84a3df0fe4ca75d7bc2ae5ae8839e9bc8995574b40a984d35bbb28c30fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154326836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37fc5d7fd12fa100c47ace85b27029357cb64546ebcf3b4f620cdabe08ba97e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1122399be6ebcbc5eb0c3718a224fd593404e643cff71a3607bcf9d1b490ae1`  
		Last Modified: Tue, 18 Mar 2025 05:42:23 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d9c714980df1bae6526a96d2475632434af8aae89aa63746733d0e58de1bc0`  
		Last Modified: Tue, 18 Mar 2025 05:42:24 GMT  
		Size: 7.7 MB (7654511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f109be71759b9e4f04f072216c5a972e9d3155df5ee4a0d82af77024ba7b2f`  
		Last Modified: Tue, 18 Mar 2025 05:42:25 GMT  
		Size: 76.6 MB (76624286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd18e3f49d6508087473a9e2cb39df1b8f1c7d86659e3b331b7b71b6dc976aaf`  
		Last Modified: Tue, 18 Mar 2025 05:42:23 GMT  
		Size: 371.7 KB (371710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9762ce4a25997657cf259e8155a196f4caba6d40f4be8e826475c57ca44c1c84`  
		Last Modified: Tue, 18 Mar 2025 05:42:25 GMT  
		Size: 99.2 KB (99247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3a605b3db57b20ba9ff353f60aa933d66d3c72a6bc2e22c2375bc0892f7ed8`  
		Last Modified: Tue, 18 Mar 2025 05:42:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ea072b9e62ea1e78fe7fad3341ba4a2542843dc3207d9485e268c92358fbc9`  
		Last Modified: Tue, 18 Mar 2025 05:42:26 GMT  
		Size: 41.5 MB (41531163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf48c8a13478a41f445e27b539434b8449ab1f509ee6819d7f5014a19ded91a`  
		Last Modified: Tue, 18 Mar 2025 05:42:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc2c7e0a7a60bd15317e3387aecd9c56f9169968483c2f117a056dbdaa6e3bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865acf78a7ec05ed58f47e39296dcd5930261ffb3357be1eeb186e5c4b3b2f6a`

```dockerfile
```

-	Layers:
	-	`sha256:50557058ab99050c2a5e27df1016013b0b31061c45da485a47a6f7da42015b48`  
		Last Modified: Tue, 18 Mar 2025 05:42:24 GMT  
		Size: 3.5 MB (3460754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fbaf5e4300d54a099b2705897f95858f79075f9b83018c24703e0bb7b5e264`  
		Last Modified: Tue, 18 Mar 2025 05:42:23 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:0f419b5abe7840611a4b8bb2efe680ce0885785782ea76427c4fc77ce32c37a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149147053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d8647f6456245be9d375555fecba69fd6c842b4e0fb54213929b999a44970f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e720cb9f4a4cd7e11f8791a6e98ff5694298e69d690f0890c38dfd48d9de945`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9df99bc8f4b12baba40764d153c92413f0ac45797459e4a9dfae8b511b017`  
		Last Modified: Tue, 18 Mar 2025 02:31:32 GMT  
		Size: 7.4 MB (7387934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfcfe3bb3ee8a55d32841fe268b6a556078d92a21601fafed81bd6455b617d7`  
		Last Modified: Tue, 18 Mar 2025 02:31:33 GMT  
		Size: 73.1 MB (73065130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acf41391bd54ff1af050714ce1ea5c03a13aeadd6ce4c0d8ba2d9095d3a447f`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 378.0 KB (378042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d5c57ca9b0d60383c2565827fe955f2baf3aad038fe1308d1a3ad9f4d53d28`  
		Last Modified: Tue, 18 Mar 2025 02:31:32 GMT  
		Size: 99.4 KB (99410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4bb03624919b9a8994bf34ac959f72de679cf4f360665d580bf4beb99011d7`  
		Last Modified: Tue, 18 Mar 2025 02:31:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930bd62fabf26859d589b122c231c229df73c0bed821183bb8ad71b677b5f14`  
		Last Modified: Tue, 18 Mar 2025 02:31:34 GMT  
		Size: 41.4 MB (41353597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a106e335e81ba51b376b8fdc3b22bf50cefd349fb7b2a6370c554cf2529d75ba`  
		Last Modified: Tue, 18 Mar 2025 02:31:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:000ca8119debf7df8a69d388ce93e7869bfac53d6d9282c23f31795ca7c8e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cc3d38bc75fd99eacb21321f3c435b4aca7549b0dfaada69a752c321584e7c`

```dockerfile
```

-	Layers:
	-	`sha256:361d0930ea5eb2f5860f03e1cb3cc9021a80aede57f5cdaa226d283ede1e48e5`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 3.5 MB (3455499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b199b67ccee64144e37c10ac1a64902962caec2a9d721d4a45535281e2adb19`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2`

```console
$ docker pull couchdb@sha256:2817ad50b5c5cf7461f5963670466197426605a790a19a6208068c509a2d8a59
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
$ docker pull couchdb@sha256:0d0f27fc156274e23d4bb0c0286857c0fb1ea6c11316c12dea12c09a5d9aa84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133217708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053646816ef0480bc9d53b56cd594a0b5f9f40320861a94a95424cae9fcd25fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119e86acdcda03a05c1bc4f413cfa10d4c3baf6fc0fb948298ba32486fba56f`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26667909256fb1c2c11f8f66d8574a91b7865e284ac9468c0e9d6ea5f8bb8187`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 7.9 MB (7874939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b2b32a58bd87dc79007ee66ff939bc6fa2c08988698d75b5fce8db774c54e3`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 392.1 KB (392121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6e0cc1cf8d818639781ac12deddea0ee97da056cb8c7e66ea89cc0b3de4c59`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 76.3 KB (76287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a9148e7b3ae4af29a1f54229ea9d2a3740f880f4a9d2092312bb0b36e0471`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63676e1594260979fc6ead2713ef435fd9d98ef6aab559775aee6f4dbb8318ee`  
		Last Modified: Mon, 17 Mar 2025 23:19:10 GMT  
		Size: 96.7 MB (96664068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5531d971294e6eef1103868b479f8cfbd628f10069aa363516e3609a743de6`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df4d3f8786c0f873002516e84fccd71d71d1c00ce830aebc56a5f30c78016de`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d848f4fa7ff22fd859bb70af21cbf3dd58a683a72f9e05d725f9ffbffb2fc`  
		Last Modified: Mon, 17 Mar 2025 23:19:09 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66edba0cea7b5c08657ccc11ad41629d7953d284c935aff2cbb081a744c4942b`  
		Last Modified: Mon, 17 Mar 2025 23:19:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:cff00481b44bd445694591f497ddc366c86c5994a9cb2383ecc1e2efa1aa2f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734920f9c18e4d8543d604a7b8a026864d5e18b1dc9e2eb0ef9f00982ef07bb6`

```dockerfile
```

-	Layers:
	-	`sha256:80c4f4db0657e1b8949205014571203374d7ddd03e103c05304a27a669f03aa0`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 3.9 MB (3933589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3f9a06d84940d2544fd2dbe6075a6195abf96cd0670b3f3ecba8d6f4fb3bbc`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4235c10986cf4e6ad6efd3854ebe699e66858a63362e63c99cef183da360a839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132528410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2898f28ba57f645595fbd8d5bd1548bb5ff6766af34dad291ac2a257e022b549`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c33caa8f1c37207c6ab6e1ca5650c5d57d5a6dbf9a1ef519d3ddbead7841e0`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa47721d1ca081323ac6f4a47a1be344d0c706dc6b459ee279e38768405b7c6e`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 7.7 MB (7654537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9aafd07b43466115ae13ea095e08aec4c6fc240c79b85b17e5de9003740099e`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 348.9 KB (348938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed36b683ab7401d9d40e036ce36e420276d84506b8cce89be9c61609d4a714`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 76.3 KB (76284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd69118bdb1eede7f9e00435174dad5792736d452fca6453626a8e3a160b6026`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1ae2e969dbdc756c20fe194695b1e886c3abb9e31a37a91b840771627c21d`  
		Last Modified: Tue, 18 Mar 2025 05:47:15 GMT  
		Size: 96.4 MB (96399175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b79c5d92cc88e34e15abcd58be7ef03fefc14b6c36e4843e241180817df6b68`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c52a367fe442effe162e647012b056524285d86987b4c93af6aa950b50abc`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3629c4ee1604981244b3c413c46175af50cce9ad264273960b89e147e6f541a3`  
		Last Modified: Tue, 18 Mar 2025 05:47:13 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7288eb637596167f724710f8b75f0065ce17f586424ac441b863b276f3d3e503`  
		Last Modified: Tue, 18 Mar 2025 05:47:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:ccf4066f87bdcae21316cb9f28493e975f6283d776e0a5f1a44a7f7f234dac3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee84e959f5607c147c19611c944aaaef5086d36d51c5bea0cc8f6b554e2ad4e`

```dockerfile
```

-	Layers:
	-	`sha256:cb6e5450c1da1629614bf516edbe60f7bfebc4adf94711974ed2b164d491249c`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 3.9 MB (3933882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2984aa27ffef7bd2fcda7ba5e210acd3f2cdc3dd042562222e58e630aff2bdb`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; s390x

```console
$ docker pull couchdb@sha256:8dea9e194a22159ea358128138988b63f72c626801577e6c3c19515c5b828a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55f8f76699a3bb68c9635bf84d95d7275bc81ce766120d29b36496a5485a4a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fff4085857b75f955d31db3d1c8ea50eaadbf6fd1a589e6cc82547ce0538e8`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c1de50e3e3779d8b50904209521f50f18d5be8cfefacc829ad006b72bc97c1`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 7.4 MB (7387912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9358d54429af4b5850c3a0009db2d388e8039bfa84b3f1d5de61739a5634ba4e`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 355.6 KB (355602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75d4154da95f28f7b46f23d395dba959f2e0090e5f9b4921b90099da94bc177`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 76.3 KB (76338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0a5daf834d8d5d9ffe7a32edde70179feea152ac5ddd0f6d8fb64d2b8d0fa`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624b1f9868098fd18264b805a2b40c71b54828fd8c30450a7c91f98f9298bc13`  
		Last Modified: Tue, 18 Mar 2025 02:39:26 GMT  
		Size: 95.3 MB (95289553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bc1381e02da40861f0194763b5d3a57eae6551945039083d3362fe716690bb`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0ac32ced35b60906f48a5468aac39053da45bee48d27f0b90c9c7be3e8948f`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f25754a45af3246f53c512f27bef5ed2c05ff1a4d39bad5eb00813f162c63a`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe59d94e128d095b5c96da87643a41f7f6021740a9b98e626ed7e09804bf62a`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:8b77911560a3e86bb7b788cd1e33ed39a310fac7f40a163314601139a862f6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba0dde34782e26b9c808a216d4ec698e234f4900acb004f78f3c9c9c00cbacc`

```dockerfile
```

-	Layers:
	-	`sha256:a5bcaef38230d3916476a94e827e476a62c13005fdb261f07aa4df222e70620d`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 3.9 MB (3932677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ebd6bb3bd3309122989cf41a614d92a06482e06b77665893f58ba41f20c4755`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2-nouveau`

```console
$ docker pull couchdb@sha256:480c03d21bbe7380622afd212eb533dd2c57187aed4de2a581b2bbf9bbbb6e3c
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
$ docker pull couchdb@sha256:843a4b14c2866528828ec65594a6504e24e9e90aaa459532c7c19731d1bed89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155526106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecb9bff1e4b8e342e1181bbe81dbbd5fd650c6eb2645b009e6834744be2392d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a8b0ae0dcc4020d289309a30b5e61f2752bb86ee9c06208bfd5d678a1c33ea`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2fba5de125c16a4984794e1dfa3e1b6f4a60bb17857b5804e58919a60318f0`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 7.9 MB (7874949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bd6a8af5e563a24c7a02304439ce9203607b03618bfd2b71f68489573c4996`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 77.3 MB (77297508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7ac445ebb09ff4a31c7444d9da19dccdee34798107e08ca28b39423a54ec07`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 415.0 KB (414961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d4551120e8a8784b777c61df9054f6b55ecc56f6ffc66432f4d26773128f89`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 99.3 KB (99324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88b8831979b4f3fb68a279ca056c851f3331c155bf61b8fe8ec0fb4b3a235e`  
		Last Modified: Mon, 17 Mar 2025 23:14:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd333fd6fede6b8a9440ad53cfa20c1946945ddd66a73749e8c2f39e408c418`  
		Last Modified: Mon, 17 Mar 2025 23:14:36 GMT  
		Size: 41.6 MB (41632619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7acb021b38ccfd706854543aaaa48736e387f1e60cb767464a08983a5c0957e`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5b02fcdcedfc3a36b048fa49990f7e6916b5c99fa08506abbd7e113b31bc21a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e22bff18db5e7bda13209389149a9d2f553c3f8ad587440c8c99ce9114cc0dc`

```dockerfile
```

-	Layers:
	-	`sha256:2399a29666758b3e34aaa9f780e0562ac9230ffbcdd7ad72f5cb5eecc13185a2`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 3.5 MB (3462078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17d40ea86b19f032c232f1bd4aa32522a2ef844b6f487db6e13836f6a523efd0`  
		Last Modified: Mon, 17 Mar 2025 23:14:32 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d1a3a84a3df0fe4ca75d7bc2ae5ae8839e9bc8995574b40a984d35bbb28c30fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154326836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37fc5d7fd12fa100c47ace85b27029357cb64546ebcf3b4f620cdabe08ba97e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1122399be6ebcbc5eb0c3718a224fd593404e643cff71a3607bcf9d1b490ae1`  
		Last Modified: Tue, 18 Mar 2025 05:42:23 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d9c714980df1bae6526a96d2475632434af8aae89aa63746733d0e58de1bc0`  
		Last Modified: Tue, 18 Mar 2025 05:42:24 GMT  
		Size: 7.7 MB (7654511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f109be71759b9e4f04f072216c5a972e9d3155df5ee4a0d82af77024ba7b2f`  
		Last Modified: Tue, 18 Mar 2025 05:42:25 GMT  
		Size: 76.6 MB (76624286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd18e3f49d6508087473a9e2cb39df1b8f1c7d86659e3b331b7b71b6dc976aaf`  
		Last Modified: Tue, 18 Mar 2025 05:42:23 GMT  
		Size: 371.7 KB (371710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9762ce4a25997657cf259e8155a196f4caba6d40f4be8e826475c57ca44c1c84`  
		Last Modified: Tue, 18 Mar 2025 05:42:25 GMT  
		Size: 99.2 KB (99247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3a605b3db57b20ba9ff353f60aa933d66d3c72a6bc2e22c2375bc0892f7ed8`  
		Last Modified: Tue, 18 Mar 2025 05:42:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ea072b9e62ea1e78fe7fad3341ba4a2542843dc3207d9485e268c92358fbc9`  
		Last Modified: Tue, 18 Mar 2025 05:42:26 GMT  
		Size: 41.5 MB (41531163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf48c8a13478a41f445e27b539434b8449ab1f509ee6819d7f5014a19ded91a`  
		Last Modified: Tue, 18 Mar 2025 05:42:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc2c7e0a7a60bd15317e3387aecd9c56f9169968483c2f117a056dbdaa6e3bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865acf78a7ec05ed58f47e39296dcd5930261ffb3357be1eeb186e5c4b3b2f6a`

```dockerfile
```

-	Layers:
	-	`sha256:50557058ab99050c2a5e27df1016013b0b31061c45da485a47a6f7da42015b48`  
		Last Modified: Tue, 18 Mar 2025 05:42:24 GMT  
		Size: 3.5 MB (3460754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fbaf5e4300d54a099b2705897f95858f79075f9b83018c24703e0bb7b5e264`  
		Last Modified: Tue, 18 Mar 2025 05:42:23 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:0f419b5abe7840611a4b8bb2efe680ce0885785782ea76427c4fc77ce32c37a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149147053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d8647f6456245be9d375555fecba69fd6c842b4e0fb54213929b999a44970f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e720cb9f4a4cd7e11f8791a6e98ff5694298e69d690f0890c38dfd48d9de945`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9df99bc8f4b12baba40764d153c92413f0ac45797459e4a9dfae8b511b017`  
		Last Modified: Tue, 18 Mar 2025 02:31:32 GMT  
		Size: 7.4 MB (7387934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfcfe3bb3ee8a55d32841fe268b6a556078d92a21601fafed81bd6455b617d7`  
		Last Modified: Tue, 18 Mar 2025 02:31:33 GMT  
		Size: 73.1 MB (73065130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acf41391bd54ff1af050714ce1ea5c03a13aeadd6ce4c0d8ba2d9095d3a447f`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 378.0 KB (378042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d5c57ca9b0d60383c2565827fe955f2baf3aad038fe1308d1a3ad9f4d53d28`  
		Last Modified: Tue, 18 Mar 2025 02:31:32 GMT  
		Size: 99.4 KB (99410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4bb03624919b9a8994bf34ac959f72de679cf4f360665d580bf4beb99011d7`  
		Last Modified: Tue, 18 Mar 2025 02:31:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9930bd62fabf26859d589b122c231c229df73c0bed821183bb8ad71b677b5f14`  
		Last Modified: Tue, 18 Mar 2025 02:31:34 GMT  
		Size: 41.4 MB (41353597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a106e335e81ba51b376b8fdc3b22bf50cefd349fb7b2a6370c554cf2529d75ba`  
		Last Modified: Tue, 18 Mar 2025 02:31:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:000ca8119debf7df8a69d388ce93e7869bfac53d6d9282c23f31795ca7c8e808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cc3d38bc75fd99eacb21321f3c435b4aca7549b0dfaada69a752c321584e7c`

```dockerfile
```

-	Layers:
	-	`sha256:361d0930ea5eb2f5860f03e1cb3cc9021a80aede57f5cdaa226d283ede1e48e5`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 3.5 MB (3455499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b199b67ccee64144e37c10ac1a64902962caec2a9d721d4a45535281e2adb19`  
		Last Modified: Tue, 18 Mar 2025 02:31:31 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:2817ad50b5c5cf7461f5963670466197426605a790a19a6208068c509a2d8a59
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
$ docker pull couchdb@sha256:0d0f27fc156274e23d4bb0c0286857c0fb1ea6c11316c12dea12c09a5d9aa84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133217708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053646816ef0480bc9d53b56cd594a0b5f9f40320861a94a95424cae9fcd25fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119e86acdcda03a05c1bc4f413cfa10d4c3baf6fc0fb948298ba32486fba56f`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26667909256fb1c2c11f8f66d8574a91b7865e284ac9468c0e9d6ea5f8bb8187`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 7.9 MB (7874939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b2b32a58bd87dc79007ee66ff939bc6fa2c08988698d75b5fce8db774c54e3`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 392.1 KB (392121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6e0cc1cf8d818639781ac12deddea0ee97da056cb8c7e66ea89cc0b3de4c59`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 76.3 KB (76287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397a9148e7b3ae4af29a1f54229ea9d2a3740f880f4a9d2092312bb0b36e0471`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63676e1594260979fc6ead2713ef435fd9d98ef6aab559775aee6f4dbb8318ee`  
		Last Modified: Mon, 17 Mar 2025 23:19:10 GMT  
		Size: 96.7 MB (96664068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5531d971294e6eef1103868b479f8cfbd628f10069aa363516e3609a743de6`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df4d3f8786c0f873002516e84fccd71d71d1c00ce830aebc56a5f30c78016de`  
		Last Modified: Mon, 17 Mar 2025 23:19:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d848f4fa7ff22fd859bb70af21cbf3dd58a683a72f9e05d725f9ffbffb2fc`  
		Last Modified: Mon, 17 Mar 2025 23:19:09 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66edba0cea7b5c08657ccc11ad41629d7953d284c935aff2cbb081a744c4942b`  
		Last Modified: Mon, 17 Mar 2025 23:19:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:cff00481b44bd445694591f497ddc366c86c5994a9cb2383ecc1e2efa1aa2f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734920f9c18e4d8543d604a7b8a026864d5e18b1dc9e2eb0ef9f00982ef07bb6`

```dockerfile
```

-	Layers:
	-	`sha256:80c4f4db0657e1b8949205014571203374d7ddd03e103c05304a27a669f03aa0`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 3.9 MB (3933589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3f9a06d84940d2544fd2dbe6075a6195abf96cd0670b3f3ecba8d6f4fb3bbc`  
		Last Modified: Mon, 17 Mar 2025 23:19:07 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4235c10986cf4e6ad6efd3854ebe699e66858a63362e63c99cef183da360a839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132528410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2898f28ba57f645595fbd8d5bd1548bb5ff6766af34dad291ac2a257e022b549`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c33caa8f1c37207c6ab6e1ca5650c5d57d5a6dbf9a1ef519d3ddbead7841e0`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa47721d1ca081323ac6f4a47a1be344d0c706dc6b459ee279e38768405b7c6e`  
		Last Modified: Tue, 18 Mar 2025 05:36:43 GMT  
		Size: 7.7 MB (7654537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9aafd07b43466115ae13ea095e08aec4c6fc240c79b85b17e5de9003740099e`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 348.9 KB (348938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed36b683ab7401d9d40e036ce36e420276d84506b8cce89be9c61609d4a714`  
		Last Modified: Tue, 18 Mar 2025 05:36:42 GMT  
		Size: 76.3 KB (76284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd69118bdb1eede7f9e00435174dad5792736d452fca6453626a8e3a160b6026`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1ae2e969dbdc756c20fe194695b1e886c3abb9e31a37a91b840771627c21d`  
		Last Modified: Tue, 18 Mar 2025 05:47:15 GMT  
		Size: 96.4 MB (96399175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b79c5d92cc88e34e15abcd58be7ef03fefc14b6c36e4843e241180817df6b68`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c52a367fe442effe162e647012b056524285d86987b4c93af6aa950b50abc`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3629c4ee1604981244b3c413c46175af50cce9ad264273960b89e147e6f541a3`  
		Last Modified: Tue, 18 Mar 2025 05:47:13 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7288eb637596167f724710f8b75f0065ce17f586424ac441b863b276f3d3e503`  
		Last Modified: Tue, 18 Mar 2025 05:47:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:ccf4066f87bdcae21316cb9f28493e975f6283d776e0a5f1a44a7f7f234dac3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee84e959f5607c147c19611c944aaaef5086d36d51c5bea0cc8f6b554e2ad4e`

```dockerfile
```

-	Layers:
	-	`sha256:cb6e5450c1da1629614bf516edbe60f7bfebc4adf94711974ed2b164d491249c`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 3.9 MB (3933882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2984aa27ffef7bd2fcda7ba5e210acd3f2cdc3dd042562222e58e630aff2bdb`  
		Last Modified: Tue, 18 Mar 2025 05:47:12 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:8dea9e194a22159ea358128138988b63f72c626801577e6c3c19515c5b828a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55f8f76699a3bb68c9635bf84d95d7275bc81ce766120d29b36496a5485a4a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fff4085857b75f955d31db3d1c8ea50eaadbf6fd1a589e6cc82547ce0538e8`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c1de50e3e3779d8b50904209521f50f18d5be8cfefacc829ad006b72bc97c1`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 7.4 MB (7387912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9358d54429af4b5850c3a0009db2d388e8039bfa84b3f1d5de61739a5634ba4e`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 355.6 KB (355602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75d4154da95f28f7b46f23d395dba959f2e0090e5f9b4921b90099da94bc177`  
		Last Modified: Tue, 18 Mar 2025 02:21:55 GMT  
		Size: 76.3 KB (76338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0a5daf834d8d5d9ffe7a32edde70179feea152ac5ddd0f6d8fb64d2b8d0fa`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624b1f9868098fd18264b805a2b40c71b54828fd8c30450a7c91f98f9298bc13`  
		Last Modified: Tue, 18 Mar 2025 02:39:26 GMT  
		Size: 95.3 MB (95289553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bc1381e02da40861f0194763b5d3a57eae6551945039083d3362fe716690bb`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0ac32ced35b60906f48a5468aac39053da45bee48d27f0b90c9c7be3e8948f`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f25754a45af3246f53c512f27bef5ed2c05ff1a4d39bad5eb00813f162c63a`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe59d94e128d095b5c96da87643a41f7f6021740a9b98e626ed7e09804bf62a`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:8b77911560a3e86bb7b788cd1e33ed39a310fac7f40a163314601139a862f6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba0dde34782e26b9c808a216d4ec698e234f4900acb004f78f3c9c9c00cbacc`

```dockerfile
```

-	Layers:
	-	`sha256:a5bcaef38230d3916476a94e827e476a62c13005fdb261f07aa4df222e70620d`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 3.9 MB (3932677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ebd6bb3bd3309122989cf41a614d92a06482e06b77665893f58ba41f20c4755`  
		Last Modified: Tue, 18 Mar 2025 02:39:24 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json
