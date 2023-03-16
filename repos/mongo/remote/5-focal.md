## `mongo:5-focal`

```console
$ docker pull mongo@sha256:112e4ac3174325c6d22ecc48c9771225f2088f200e3916ebc3483d4652f20c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:9dc529c92843d2a96f1f58f52fed91d5c54b8712d401d6d88a7d47e1511fb094
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253656480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29947283b3152fe54b8834dc10b3d3ce6bebe828fd2807bc01a6d50181a6c663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:53:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 16 Mar 2023 03:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:53:15 GMT
ENV GOSU_VERSION=1.16
# Thu, 16 Mar 2023 03:53:16 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 16 Mar 2023 03:53:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 16 Mar 2023 03:53:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 16 Mar 2023 03:53:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 16 Mar 2023 03:53:25 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 16 Mar 2023 03:53:25 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 03:53:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 03:53:25 GMT
ENV MONGO_MAJOR=5.0
# Thu, 16 Mar 2023 03:53:26 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 16 Mar 2023 03:53:26 GMT
ENV MONGO_VERSION=5.0.15
# Thu, 16 Mar 2023 03:53:49 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 16 Mar 2023 03:53:50 GMT
VOLUME [/data/db /data/configdb]
# Thu, 16 Mar 2023 03:53:50 GMT
ENV HOME=/data/db
# Thu, 16 Mar 2023 03:53:50 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Thu, 16 Mar 2023 03:53:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 03:53:51 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:53:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d49e5b1beefd7b6b70f379d149a8227a7b6c768198b797ea1204aa1431fd856`  
		Last Modified: Thu, 16 Mar 2023 03:56:15 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3a5d1d7825ca0378d0dd19cb5f5f2439ca29f8ff0fbb3271cab3b00cc3a4aa`  
		Last Modified: Thu, 16 Mar 2023 03:56:17 GMT  
		Size: 8.3 MB (8348387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36580a5e9522936b484bfba3ef86edd895d7fe80d3edf77e36d2a0dab073614`  
		Last Modified: Thu, 16 Mar 2023 03:56:15 GMT  
		Size: 1.3 MB (1255742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292748d3b156a3be87ebb9dcc6d3b6ba1153e5b7a50a7e3a3526622e643936df`  
		Last Modified: Thu, 16 Mar 2023 03:56:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0e58eccc199bfb7c389b31116f703685cd2a78728d07d49066f7cd6f9dd454`  
		Last Modified: Thu, 16 Mar 2023 03:56:13 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6743bdce573db3cd8680ce24b883b7b4b223d286de07eeb99ba71ea518c70a`  
		Last Modified: Thu, 16 Mar 2023 03:56:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea98025a8c93e1fefa04e69c4ad343bf2511c52a15bc4b3886cf30a722aeca28`  
		Last Modified: Thu, 16 Mar 2023 03:56:39 GMT  
		Size: 215.5 MB (215465574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b19046365cd8ef16a7d379ef26a779d256a9add15de6b4e1ab1e5920ac5821`  
		Last Modified: Thu, 16 Mar 2023 03:56:13 GMT  
		Size: 5.0 KB (5020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d5d419adc73efbf02f3a8a27251328b9350c9cb1223109ca1bd8f83d25a158f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246845648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8412a4f58f215d7cd70abd8f9dbfc259bf33fb2e8d76375aa27cfd06f3ef02ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:36:49 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 16 Mar 2023 02:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:37:00 GMT
ENV GOSU_VERSION=1.16
# Thu, 16 Mar 2023 02:37:00 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 16 Mar 2023 02:37:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 16 Mar 2023 02:37:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 16 Mar 2023 02:37:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 16 Mar 2023 02:37:08 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 16 Mar 2023 02:37:08 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 02:37:08 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 02:37:08 GMT
ENV MONGO_MAJOR=5.0
# Thu, 16 Mar 2023 02:37:08 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 16 Mar 2023 02:37:08 GMT
ENV MONGO_VERSION=5.0.15
# Thu, 16 Mar 2023 02:37:28 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 16 Mar 2023 02:37:31 GMT
VOLUME [/data/db /data/configdb]
# Thu, 16 Mar 2023 02:37:31 GMT
ENV HOME=/data/db
# Thu, 16 Mar 2023 02:37:31 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Thu, 16 Mar 2023 02:37:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 02:37:31 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 02:37:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada7907d2854f27099e0f65f3b0a40faf1dd1ea9f86d7787101f1df8d8fea3ec`  
		Last Modified: Thu, 16 Mar 2023 02:39:33 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8d5e9f809f2c75bf1e319b26c316147f61a1a6d4b7af8a79b1e69fdae857e`  
		Last Modified: Thu, 16 Mar 2023 02:39:34 GMT  
		Size: 8.2 MB (8180113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cf6b8f41302df7a56c599e509f7aa637d70f399d7da95682218e5ed7365be3`  
		Last Modified: Thu, 16 Mar 2023 02:39:32 GMT  
		Size: 1.2 MB (1189160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f414830828eaaafd751b67b343fd6d5c8f2616c6f5836ab18b6fb163931eb235`  
		Last Modified: Thu, 16 Mar 2023 02:39:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565f802dec5c667699e13318626edd96e0c7020759faf768c0c2491f25d5226b`  
		Last Modified: Thu, 16 Mar 2023 02:39:30 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3d921964dc71ea424870ec4f3d2dc789066044fd7f58ca0e49a77dde74d36c`  
		Last Modified: Thu, 16 Mar 2023 02:39:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb2f553a96a04a95c1daccac02f5a394e0dadfca9335bae43ca89de796e620d`  
		Last Modified: Thu, 16 Mar 2023 02:39:48 GMT  
		Size: 210.3 MB (210271503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7c9efbb98531ed6962ed3bdaf0c5b1263ea6f3dfd0df7f5fa765109847808e`  
		Last Modified: Thu, 16 Mar 2023 02:39:30 GMT  
		Size: 5.0 KB (5020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
