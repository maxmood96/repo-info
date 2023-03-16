## `mongo:4-focal`

```console
$ docker pull mongo@sha256:46b356edf6dde9a5c563591ec8ef79251ebb97a00c73e7d43e835d4a0e008eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:c99f39e72bb4211af66b630d3b196a9d49578387e6ff07e6835ac403ebd20b0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175742383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afef20758bd3d32ba19f0c36cabe79973a98279ca35a1d7e2260cbca1e5ba395`
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
# Thu, 16 Mar 2023 03:54:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 16 Mar 2023 03:54:02 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 16 Mar 2023 03:54:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 03:54:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 03:54:02 GMT
ENV MONGO_MAJOR=4.4
# Thu, 16 Mar 2023 03:54:03 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 16 Mar 2023 03:54:03 GMT
ENV MONGO_VERSION=4.4.19
# Thu, 16 Mar 2023 03:54:20 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 16 Mar 2023 03:54:21 GMT
VOLUME [/data/db /data/configdb]
# Thu, 16 Mar 2023 03:54:21 GMT
ENV HOME=/data/db
# Thu, 16 Mar 2023 03:54:21 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Thu, 16 Mar 2023 03:54:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 03:54:21 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:54:21 GMT
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
	-	`sha256:7cd34415fce503659a7e131d6a264949678ff19d7e8d2b967e9eb60792081909`  
		Last Modified: Thu, 16 Mar 2023 03:56:51 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631546192af055384aeec4322a0798a398426a4efcc055353c99c71daee785e9`  
		Last Modified: Thu, 16 Mar 2023 03:56:51 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eba270fc49c23df8f5a66b60139bbcf1544c0fc98ecba48cde4fef6e61f1218`  
		Last Modified: Thu, 16 Mar 2023 03:57:07 GMT  
		Size: 137.6 MB (137551479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb8ee86e3d81b0a460a343b239b38aa20b6fc77d16b9a226e9befd197844170`  
		Last Modified: Thu, 16 Mar 2023 03:56:51 GMT  
		Size: 5.0 KB (5021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:641f67f5e8624fa3606ab5369e28f17e67ffe7b2d6f8d0c756928259cfd663f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171369539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a7c7bd46c408551602751fa9f9849b4afc378fc20ae6a4d2fc1df63d16ee3a`
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
# Thu, 16 Mar 2023 02:37:38 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 16 Mar 2023 02:37:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 16 Mar 2023 02:37:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 02:37:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 16 Mar 2023 02:37:38 GMT
ENV MONGO_MAJOR=4.4
# Thu, 16 Mar 2023 02:37:39 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 16 Mar 2023 02:37:39 GMT
ENV MONGO_VERSION=4.4.19
# Thu, 16 Mar 2023 02:37:52 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 16 Mar 2023 02:37:53 GMT
VOLUME [/data/db /data/configdb]
# Thu, 16 Mar 2023 02:37:54 GMT
ENV HOME=/data/db
# Thu, 16 Mar 2023 02:37:54 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Thu, 16 Mar 2023 02:37:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 02:37:54 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 02:37:54 GMT
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
	-	`sha256:b4c913866724811831f9457a18b18a5d0bcfbde922e542445e23df77e5b3fffc`  
		Last Modified: Thu, 16 Mar 2023 02:40:00 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245531967d5720bc20e919d7fd62b8ac7762360b744bc0ac8d563d5a652219a5`  
		Last Modified: Thu, 16 Mar 2023 02:40:00 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63c6eea48706858baedcdc6a574d122d08f056319f6dcca328f5c6d05a169d7`  
		Last Modified: Thu, 16 Mar 2023 02:40:11 GMT  
		Size: 134.8 MB (134795395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a134bdd2c3b7a9d9aafee650605874d73057c75848b065b5c8186169b38b76cc`  
		Last Modified: Thu, 16 Mar 2023 02:40:00 GMT  
		Size: 5.0 KB (5020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
