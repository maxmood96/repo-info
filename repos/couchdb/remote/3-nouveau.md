## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:baf9a64c1d285d7824eadca2ced5920e99f79d5d1eb2cfd742f7961a60994625
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
$ docker pull couchdb@sha256:0760441508a04c4c9039005042bc8fbb7d4e9c441efe5c054be88d39fcc4af8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156378033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4018243b6579b4ebbc2e674d251bfaef1baa084734761f1a266b9f719cd443`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab75aebd886c9be0ee7b4ee28339e431a0b497e089561a987558b673ad6797`  
		Last Modified: Fri, 09 May 2025 01:48:39 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852a92f1ebda0c1224152be98b6d9700950524c8a6a9bcd6986fcb00e9ed673d`  
		Last Modified: Fri, 09 May 2025 13:41:05 GMT  
		Size: 7.9 MB (7874878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4461ff2ea16a599621941b4fcee4711521ba84e86d5314a74cd1d375b0d54da4`  
		Last Modified: Fri, 09 May 2025 13:41:02 GMT  
		Size: 77.3 MB (77325051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978b0dd7438e7247e12182be2d5b9548c538a9ceb566a2ccbbcaaad1efeb7399`  
		Last Modified: Fri, 09 May 2025 01:48:39 GMT  
		Size: 415.0 KB (414979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f354970eb1ee9dfb1cf1fe1754e7f486629e6854765524e66af1feb9990e5ff`  
		Last Modified: Fri, 09 May 2025 01:48:39 GMT  
		Size: 99.3 KB (99331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31beb4795edca4e38687b771af5cd0e185edc50c9f01f15b7437033faf9358`  
		Last Modified: Fri, 09 May 2025 01:48:39 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c466b712155d38ccf933748cb87fbda79c3452f6ab7f4a56c7be924115b4b0`  
		Last Modified: Fri, 09 May 2025 13:41:19 GMT  
		Size: 42.4 MB (42434265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72bf32f2e446080d1db9fcb3e5be1d590d01308eb7a93af4ed2955dcf15098b`  
		Last Modified: Fri, 09 May 2025 01:48:39 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:7e749f49becf3b999fbf6e4f1a836c3b8477d0a7d906120ee9fc18278df74c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f63f27268a030a521eed2b0958a40303b245ef5df08551b0f85654fc3e3cc27`

```dockerfile
```

-	Layers:
	-	`sha256:f9841b3c7c4b5ba2c2017fb4b6470f955f9181693cdfc9d317a99aa72c60e5ac`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 3.5 MB (3468472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66bc4962c889a3aae3880bcd640e64dc8746f8bd434cd016c5f18ab265d066a`  
		Last Modified: Tue, 06 May 2025 17:17:31 GMT  
		Size: 24.6 KB (24564 bytes)  
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
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
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
$ docker pull couchdb@sha256:6894b9d3fdf6f9a5176261f14ca3c651730ec73db9ce0a765a15e7a388d3c6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149988948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def79bef4e97280e0c980f63684e324dcc092b868ebffdca3086d2acd9046879`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a964195047607539333a13346b03ad72f2ad2936f990c34030f96b711db4d8d6`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35944b8be452548cffc3b1e219d96ee2c781cd22bfcf9556e2189bc35b49b2f0`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 7.4 MB (7387884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37c28b87d08942391748734f64343e220c6ce718982c62cadfe473b0e7eadde`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 73.1 MB (73076016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1fdb13b6204813e6a2b61535f8a84ab797314b04528ddfbc414041076fb881`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 378.1 KB (378084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63fee4f0f8bf582bdc0669dc2b702f84f1a6f98705c8a64b90b76089c9c0e17`  
		Last Modified: Tue, 06 May 2025 17:50:04 GMT  
		Size: 99.4 KB (99430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ed74fe9c91ae5451882f5fce49cce5b47e5b6ea72f551f1d1afe3baa15df8`  
		Last Modified: Tue, 06 May 2025 17:50:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d65d8e4597eadb5b291238e3185b9f77f85e1b800168cc2bf13e44ec6c6663`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 42.2 MB (42160785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c1cb17e9fbd6a9bb9d287e74d4e34aae2758743989aa26f811b27e477b142`  
		Last Modified: Tue, 06 May 2025 17:50:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d9b219d92f16a58e3cb1a7e838a3f1c08b8df07533420880d740fdab7986c446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80ac1a179e7abb201a9085ecfe46c8e1753c07accd3bada6a559bdd2b2b9beb`

```dockerfile
```

-	Layers:
	-	`sha256:9e60d3321d2c177f7279a87c7a52d401cd66706f2abc46b4774c75118fe11837`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 3.5 MB (3461893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5585a3fbd006fe2392f7b475da7f2e476800ea78a189a415cb5e70900d9b61`  
		Last Modified: Tue, 06 May 2025 17:50:03 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json
