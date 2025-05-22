## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:69f0862d6fce32301cecfb5b1c3c1e4f9b3b762d725766e83dcc731a79ea94ce
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
$ docker pull couchdb@sha256:0e9d627a82619751cc0d6f42f899aa11e8b0fd01afa5f06cbc2de5dbc0151e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156377003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f486850fee961991297613cd422a46f6df9bf60911d27619b99ab996d1a18ef`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499470c9acbc00bcc886054c1cda3f5c8c36fbf550a642960f2726c99f7cccd`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0590250af4762255b25cff955958f055fdfcafdeb9007c8e4b4f571432bc98cc`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 7.9 MB (7876617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa6110867a1df8c941ceb29416c301977da6dcc8a82ce3dbf7d4931009ac58`  
		Last Modified: Wed, 21 May 2025 23:21:34 GMT  
		Size: 77.3 MB (77324631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5f96efa9cf3073c2562091ffd7f4ef6b7934631bc159dee2cda56169bb3c37`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 415.0 KB (414987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98d8ddcf13047ccfd1fc7c4747bc785c5cb1a0459ff93c5263a96defebe4d42`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 99.3 KB (99323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733d973b08d70309f6af91291d0d69983e350cf6377bd9a4649c156c22827d6`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749f6475cadf4afd508e15603543c680150a2dcf6641c3d8a64a766c1bc71bc`  
		Last Modified: Wed, 21 May 2025 23:21:35 GMT  
		Size: 42.4 MB (42434239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002a25bfa7ceaa38750737429b07cefd358da6cdc7699c3062c6602c8a5db5bc`  
		Last Modified: Wed, 21 May 2025 23:21:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e06b980a13665020a73a39fbad472958d45e6c263edc8c901c8c6782efd65326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3527788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e8f86012d808409684a3638c5fcf10b5cc3c3250ea82df6f6bc0c3cb24aaef`

```dockerfile
```

-	Layers:
	-	`sha256:6b81beb7bb8f78ee184908beda66bcd1024e3a72659520cb1cf1e11b7b3cc114`  
		Last Modified: Wed, 21 May 2025 23:21:32 GMT  
		Size: 3.5 MB (3503225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e797f8a70670a8c360e264c6b98942981c8680eb266df741b8e284dd2db0f5a`  
		Last Modified: Wed, 21 May 2025 23:21:31 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7fdb1df7e89b35ae184e2975f8ed5d5c72acd6e651588d7854923639ea383648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155180531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90792137fb7d00afa09943655aa32c8b56afb2ed23f9ca819aef6c02127e89b0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104637e2eb67ec32ff000f153eebca995c5a32bdca49fe1b16015251fd887842`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc58e96c4d79f04a31e09066efeea0f21f93f87a60cd80b537546b799ebbff9`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 7.7 MB (7654542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58f87545a1ea3e85e36bc4f13c6528480a4d096cabe6e23b6919d84a3a21fa`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 76.7 MB (76653670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886a375283a50138292c4ab34c2a2cd473c86f479a0657d206917439b9293ef4`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 371.7 KB (371732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf50ebfde2d6eb28578d23558bec7ad3fcf33ed5edbbda390b0c02b37636ab`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 99.3 KB (99262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a67aafe8a97aa0a8dd806d49d1da627072a88c7e466a6957064c3b1ac9f579`  
		Last Modified: Tue, 06 May 2025 17:58:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd40dddaef0fcda5c486a0d107b1aeac5eae87d112d92a7f8babc07a9c2bc5b`  
		Last Modified: Tue, 06 May 2025 17:58:59 GMT  
		Size: 42.3 MB (42332820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead4ac28d2805b9ad7d4bc386937a7df61b55d7493ee5c9fa48d6eab8baa75c`  
		Last Modified: Tue, 06 May 2025 17:58:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc0f7d743c3b12042d2363c435ba9a3136bffb0e8741d2777c0e9501b34fb0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b851a388ca66506c60d98b25da2535df558b509b5464f97e568dcd7055452f`

```dockerfile
```

-	Layers:
	-	`sha256:926a4dc0d56e3c9be08d364b9e30b94d534c9a7d479ce49b32d9a7fac0b85348`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 3.5 MB (3467148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22075a440bd6b34723136a723584525e19f147bda33189d33a6d6199161fb556`  
		Last Modified: Tue, 06 May 2025 17:58:55 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c144920a1f33f2407cb3611ea12b4e80ceebd4fa134fe745503729ed901bbe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149990045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e2d1ccfff6600840e8ab5f7799ad12211edb132dddf6c0f6f05b11f2e47fd8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26396a1c92d005f1f73ce8a5a786829b16fd7bfeea83b11aab47577c79125a6`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474be071a26fc29b13f67d8e56c399b46d3b8233fba772eddf197a41e47b3ce`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 7.4 MB (7391039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7557a7943629e9a5e09974b851cd3f71af7ae009a3c979a57c2005e05a04ae`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 73.1 MB (73075902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364ab5de64b0f27b98361254033eb8e64dab17927d0d5ed36673abde5d5a1116`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 378.1 KB (378082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9582aebb38d001676e191f1d1739f9651fb01da8c1d4099e8e0eb6e86e453`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 99.4 KB (99441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15939d7d9273f1580bd4614a899539324dde9b46bb9c958cb5ecd8b6e118b3b7`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9ca0b94e18b2399600f2856dafbb9e4ad3d61ca982c486d68ee6f2f8e2f845`  
		Last Modified: Thu, 22 May 2025 01:05:47 GMT  
		Size: 42.2 MB (42160892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afc856a01f3eda18d2caeeef10985ba6f113d6e40fa30d36627cffd35c50895`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:9026af3d06aa014b566e394abb7e54e49cf289dcb09ad6c4bc2363b87545ace7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3521210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbed73861a10a7185fb0f4d338c33bb2b7b13941e243ef568f46cd7853f1b44`

```dockerfile
```

-	Layers:
	-	`sha256:50da05748a9be431439b8d33cd60430c479b3050bc095b88e787d64e1bfbbbbc`  
		Last Modified: Thu, 22 May 2025 01:05:46 GMT  
		Size: 3.5 MB (3496646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67689b0e1b9ff33b91e6f02f0d07c8551e1671ab573b630d590e1607976d665`  
		Last Modified: Thu, 22 May 2025 01:05:45 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json
