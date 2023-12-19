## `mongo:5-focal`

```console
$ docker pull mongo@sha256:bafaf819b4c5d856c86d99935d616bd0050873f9bf9576519ec285bb68bd2375
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:54fe7648d4347dada5fdc436676cbf0ad9f09006e795b8a8cac2869f006eef76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265209894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16406ab736a027d762623d0be5bebf9f7120344284696afbd8e8ee9390226b93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:05:33 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:05:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:05:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:05:33 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Nov 2023 23:05:33 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Mon, 27 Nov 2023 23:05:33 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:05:33 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:05:33 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_MAJOR=5.0
# Mon, 27 Nov 2023 23:05:33 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_VERSION=5.0.23
# Mon, 27 Nov 2023 23:05:33 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:05:33 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:05:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:05:33 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:05:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4c5dda70d863d7aca4b17d1dd606ad1b212bf17123728ce414761b2eb62e8`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95658ac9f2c28b95be9ecde47a89d7f9af6895dcd54c47fef5fd7787b421f7d`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 8.4 MB (8373078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b769201a4ea2df138447e9a23f121d26f803869661253f65284ed5887369d74`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 1.1 MB (1099562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261e840591340e9bfde64ab2fb476e89571f43d38604e518089b2b326b972702`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb80b579ed332a3bf30c5898fffcd804517037e36dec75c38ba0dc8243edc019`  
		Last Modified: Sat, 16 Dec 2023 10:50:15 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd07cdc415356ca309435937e56377281c8dfb8c92e3ffb1a112072f30a7eb6`  
		Last Modified: Sat, 16 Dec 2023 10:50:15 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4ab15557f211ae17c07dececdca2bf2b58d8edb2b03da932d1fe5a639b2ea0`  
		Last Modified: Sat, 16 Dec 2023 10:50:22 GMT  
		Size: 228.2 MB (228215931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c292b6d49a55b8f49c6f1e8f3da7dde07fce08db978a7d48be60b375d5ec72b2`  
		Last Modified: Sat, 16 Dec 2023 10:50:16 GMT  
		Size: 5.0 KB (4994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:5570a6843a6eeabdaf3c321c624757c8e1e340521b599adfa0f3f3c955ca6d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f88de4ee676e34af538ea82ab417334ddf4c9f1419a367fcab1f82665eda60b`

```dockerfile
```

-	Layers:
	-	`sha256:e2eed20bc5e9cd6fb9f0289703de86080f50461cf65b0d02cb05266eefd42180`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 2.7 MB (2729388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b5dcc03e35d960eb5464905fa799f925874da49bad1d39ff8b0790fcb5c2ccf`  
		Last Modified: Sat, 16 Dec 2023 10:50:14 GMT  
		Size: 28.0 KB (28044 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:799d3474a49a847973c1b65f35b5753fac34dc16764e5761524214779d0ba58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257626981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16351c6f65cfa15e2ece610ad35dbc14aba85c41dd71562fd66fb99f82b6b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:05:33 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:05:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:05:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:05:33 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Nov 2023 23:05:33 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Mon, 27 Nov 2023 23:05:33 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:05:33 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:05:33 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_MAJOR=5.0
# Mon, 27 Nov 2023 23:05:33 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENV MONGO_VERSION=5.0.23
# Mon, 27 Nov 2023 23:05:33 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:05:33 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:05:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:05:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:05:33 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:05:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ba6b7451f9d95719ad43508919c914407cf286d0b7fb6e1ee9a02cd51b045`  
		Last Modified: Mon, 18 Dec 2023 19:51:47 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ded41913893fb2c19b7f6cb4b21f0e12639a543c69be1d62dbe3afdf3fbc42`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 8.2 MB (8200494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deddfd4aa405910f1def1dd6fb5da28c8c01831f20100c68ba672328228d629`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 1.0 MB (1031331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae6f8162365a2edd63c6252640611da17bb92f5172d0303262b4f9b68dd2c79`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1686f053580301c2f6504c0ef8d13a7f65f23445102cac0146603ae02860dd83`  
		Last Modified: Mon, 18 Dec 2023 20:12:23 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316604761e220a553ad8ed656217b332d437c468e870fc287114bf671732137a`  
		Last Modified: Mon, 18 Dec 2023 20:12:24 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2289da9b1908d8949b57a4f0c4111bf980b656fc71e0be040390e55ed2841a`  
		Last Modified: Mon, 18 Dec 2023 20:12:29 GMT  
		Size: 222.4 MB (222411833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7623635c3201b34112ec6010684e1f3c501d6a3d5c6c5f76cf9b4feed28647f`  
		Last Modified: Mon, 18 Dec 2023 20:12:24 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:15a39a79e1310cc53a1f49063875089fe072f78866427e03a68b8e946c4bbd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c747a5e8fc6cd9d4f035709912d050959926f29d7b27eb266045187a7437837`

```dockerfile
```

-	Layers:
	-	`sha256:b23dcdcec2d30d00200a41b5acf56d1d0f1d6326fa03f4e7d75c498666153bc1`  
		Last Modified: Mon, 18 Dec 2023 20:12:24 GMT  
		Size: 2.7 MB (2729726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30bfb540fb105208b6fe4a22ad248564d3abe7afca737c6c5a38d7688164320`  
		Last Modified: Mon, 18 Dec 2023 20:12:23 GMT  
		Size: 27.9 KB (27897 bytes)  
		MIME: application/vnd.in-toto+json
