## `mongo:jammy`

```console
$ docker pull mongo@sha256:3badb3f6c63707647ed499e4603d7539f00fe321cb5e40979637ee00030f869d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:8af4b380a9c3852c051b1d7ac95465751c05cf01bf760cd77302bb1eaae80075
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261137012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfa3f5bb5157c1581cbf9fe814b4de2eb7b971d7e2166f197b68131d6d8a4dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:46:00 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 13 Oct 2023 04:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:46:11 GMT
ENV GOSU_VERSION=1.16
# Fri, 13 Oct 2023 04:46:11 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 13 Oct 2023 04:46:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 04:46:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 04:46:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 04:46:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 04:46:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 04:46:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 04:46:22 GMT
ENV MONGO_MAJOR=7.0
# Fri, 13 Oct 2023 04:46:22 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 29 Nov 2023 01:39:12 GMT
ENV MONGO_VERSION=7.0.4
# Wed, 29 Nov 2023 01:39:38 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 29 Nov 2023 01:39:38 GMT
VOLUME [/data/db /data/configdb]
# Wed, 29 Nov 2023 01:39:39 GMT
ENV HOME=/data/db
# Wed, 29 Nov 2023 01:39:39 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 29 Nov 2023 01:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Nov 2023 01:39:39 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:39:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a7480baa9dd203af7b88b2fe7e6b4f81563a7ffb540e462456ae061accb837`  
		Last Modified: Fri, 13 Oct 2023 04:49:41 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9301fbd7df07e1041efa8f0b71daef6163a40cddd61abd63c7622c0031ee4c`  
		Last Modified: Fri, 13 Oct 2023 04:49:42 GMT  
		Size: 5.1 MB (5050516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4470f2e90f14923cd6b6c2b4c9482ab700e2ee6adb23b5509826a2994aec9c`  
		Last Modified: Fri, 13 Oct 2023 04:49:42 GMT  
		Size: 1.3 MB (1252869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d046ff8fd3271879d2f76a64b0ff765e3b484eb8c712dbab9ba3f3aae73de6`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e062d62b861ed7136f7640c09410c619e0b146c7ea00bbc076ede8ffe17a2428`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72919e34fde8aa9d4c9919b131ea251cd24f66df9b967a3e9a00fcb931a80f37`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470e2750512f37cac02aac0b8c6346700c9000d66c849c17f63067be7ff9651b`  
		Last Modified: Wed, 29 Nov 2023 01:42:10 GMT  
		Size: 224.4 MB (224385836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debd7eab1f4f4f0574e3ebc0bb5c5517b8cbca5ec93383a28a17e3aad1b2e0bc`  
		Last Modified: Wed, 29 Nov 2023 01:41:41 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:993cce3158e7c2f302bf26e0153faccfaca5831c497e68a3813893b11f73c35a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253089652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203fb0aeb494164ffddb68e653e75a612132fefc3d901739a0e1cf57a68249ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:07:59 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 13 Oct 2023 05:08:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 05:08:12 GMT
ENV GOSU_VERSION=1.16
# Fri, 13 Oct 2023 05:08:12 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 13 Oct 2023 05:08:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 05:08:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 05:08:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 05:08:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 05:08:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:22 GMT
ENV MONGO_MAJOR=7.0
# Fri, 13 Oct 2023 05:08:22 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 15 Nov 2023 01:48:15 GMT
ENV MONGO_VERSION=7.0.3
# Wed, 15 Nov 2023 01:48:37 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 15 Nov 2023 01:48:41 GMT
VOLUME [/data/db /data/configdb]
# Wed, 15 Nov 2023 01:48:41 GMT
ENV HOME=/data/db
# Wed, 15 Nov 2023 01:48:41 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 15 Nov 2023 01:48:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Nov 2023 01:48:41 GMT
EXPOSE 27017
# Wed, 15 Nov 2023 01:48:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53942a81bbed58a041019d02afca8f39cb3b5fc0b340c05513ba233089ddaa64`  
		Last Modified: Fri, 13 Oct 2023 05:11:43 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c77c1ea6f8e184bfebf5bd44a67db789f6dda84d9e1765f88df461c6fc366ba`  
		Last Modified: Fri, 13 Oct 2023 05:11:44 GMT  
		Size: 5.0 MB (4993892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ffa19aee38fa5d40fbbb7ad0fed2cd802350b3e0859506d008678f433b01`  
		Last Modified: Fri, 13 Oct 2023 05:11:43 GMT  
		Size: 1.2 MB (1186372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae10bad01057285cb468c4b8ac16543be6f76dd7617e0a1dd477c7cab4e8265`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208482253dd3d9820726079a672df6e91e9b83c81c36d5554103f854670ccfc1`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beb4a4f2118534d26af685b92befcd861724f9f1ce3cd9a0cfabfecfe1452df`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d8399c849e346dacbd60cf9862e89c06e19511069a55d363ebf497b4196a9f`  
		Last Modified: Wed, 15 Nov 2023 01:51:50 GMT  
		Size: 218.5 MB (218508770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39807cb848fcdb56e57ffe59695facd1b5ea2316e587d2977e3df4826574df1`  
		Last Modified: Wed, 15 Nov 2023 01:51:31 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
