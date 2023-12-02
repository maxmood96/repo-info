## `mongo:5-focal`

```console
$ docker pull mongo@sha256:1e20fb5f09693f11cee0d2014f44cf692f9180dd3c95c5c5caddf28b7f267b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:d14e0d3e0ece7a0e109ee32f0be3121ddaea2efe3dc870e6d7abb3b5ea749bad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266417168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561bc342ad90953db30def6418eae58325cc8ff7425f212ad4c9f0973fe12124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:59:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 02 Dec 2023 04:59:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:59:47 GMT
ENV GOSU_VERSION=1.16
# Sat, 02 Dec 2023 04:59:47 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 02 Dec 2023 04:59:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 02 Dec 2023 04:59:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 02 Dec 2023 04:59:56 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 02 Dec 2023 04:59:56 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 02 Dec 2023 04:59:56 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 02 Dec 2023 04:59:56 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 02 Dec 2023 04:59:56 GMT
ENV MONGO_MAJOR=5.0
# Sat, 02 Dec 2023 04:59:57 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 02 Dec 2023 04:59:57 GMT
ENV MONGO_VERSION=5.0.23
# Sat, 02 Dec 2023 05:00:36 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 02 Dec 2023 05:00:38 GMT
VOLUME [/data/db /data/configdb]
# Sat, 02 Dec 2023 05:00:38 GMT
ENV HOME=/data/db
# Sat, 02 Dec 2023 05:00:38 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Sat, 02 Dec 2023 05:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 05:00:38 GMT
EXPOSE 27017
# Sat, 02 Dec 2023 05:00:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb776765d5965d8e2f178d00d709034bca0c320193a987f89eae31a99952cad`  
		Last Modified: Sat, 02 Dec 2023 05:03:01 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a3fe15d40f893f2521410fd8a116a1dda2ff2caa93c84aed4078e5f1f07d03`  
		Last Modified: Sat, 02 Dec 2023 05:03:02 GMT  
		Size: 8.4 MB (8374517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da6519053fccfa8a4aa2204abf86ba25e86f99d09def4f73508fab1c408a87d`  
		Last Modified: Sat, 02 Dec 2023 05:03:01 GMT  
		Size: 1.3 MB (1256231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd08c7e5990781a509ae889aeb7ccaf435703f181d8c1df0c11711537377c201`  
		Last Modified: Sat, 02 Dec 2023 05:02:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65127953ed016cdad7ddc9b0d192be418981e1a9410397cda84c88e7702de525`  
		Last Modified: Sat, 02 Dec 2023 05:02:59 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5497cf5773bafd50911e945ede6e679e1c232600908c5b5c9393debb0c3422`  
		Last Modified: Sat, 02 Dec 2023 05:02:59 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f9df4bced9f363f571638378b9d8988ab5e2113358f3c42443b3646767e4b2`  
		Last Modified: Sat, 02 Dec 2023 05:03:25 GMT  
		Size: 228.2 MB (228193703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657f0ff861f169d27645b4fc80dc50648658bdb510569a84fc8da305db92a6f0`  
		Last Modified: Sat, 02 Dec 2023 05:02:59 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0793ace436bd37071d9bea88dbf7a3945352fcf0dba7962ae02c501f0126ea3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259013928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1a5aa6a4712e9b57dfec1fcda4559e3695ffea65818354f23d9d0d310dfa32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:09:24 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 13 Oct 2023 05:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 05:10:10 GMT
ENV GOSU_VERSION=1.16
# Fri, 13 Oct 2023 05:10:10 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 13 Oct 2023 05:10:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 05:10:18 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 05:10:19 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 05:10:19 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 05:10:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:10:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:10:20 GMT
ENV MONGO_MAJOR=5.0
# Fri, 13 Oct 2023 05:10:20 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 29 Nov 2023 06:27:13 GMT
ENV MONGO_VERSION=5.0.23
# Wed, 29 Nov 2023 06:27:49 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 29 Nov 2023 06:27:52 GMT
VOLUME [/data/db /data/configdb]
# Wed, 29 Nov 2023 06:27:53 GMT
ENV HOME=/data/db
# Wed, 29 Nov 2023 06:27:53 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 29 Nov 2023 06:27:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Nov 2023 06:27:53 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 06:27:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b8a8f6982dd8543e2d7fd40d8f91e6309d0c05e390dc5b334b67e256b958a2`  
		Last Modified: Fri, 13 Oct 2023 05:12:47 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200bca1fe77ec7f3d81e8184db84343b21a8f5a5716a114e8757630c419f57e`  
		Last Modified: Fri, 13 Oct 2023 05:12:48 GMT  
		Size: 8.2 MB (8202367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c526910ee08da1a854493892a8c43d4429cc1ea180ce68d3494469e45be7b8c4`  
		Last Modified: Fri, 13 Oct 2023 05:12:47 GMT  
		Size: 1.2 MB (1189124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa0323df32ebd9c85f7a9b4745468fdf035c319ce3a6cf5c26ff2a58764693a`  
		Last Modified: Fri, 13 Oct 2023 05:12:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a60706d3c7c4fd4432368201105fb51c1327eeceb40b79ab47ada97cef0184`  
		Last Modified: Fri, 13 Oct 2023 05:12:44 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0730a4323d9a89d290e497140a9c999287677c447926a1a6b1c0cf13d6fed769`  
		Last Modified: Fri, 13 Oct 2023 05:12:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9fee049886fc68cb638585c7384464f660026d84bb517bae63d0546d5bdff6`  
		Last Modified: Wed, 29 Nov 2023 06:30:03 GMT  
		Size: 222.4 MB (222414244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769914d16f91fcd26846a16ae8c6f8a9c962661199c415a713e8b9bba72ead62`  
		Last Modified: Wed, 29 Nov 2023 06:29:43 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
