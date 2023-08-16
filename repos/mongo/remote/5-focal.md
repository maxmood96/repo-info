## `mongo:5-focal`

```console
$ docker pull mongo@sha256:1a5e03d43d9c24e4b4444c6aa81087e0a3f8efb8a1411f4e20d13dda07e578e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:f493e0950c1c9b76ea0cdda9c2940c6d6360b60ac651b3e780f3eb6485e29fb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255302383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6514524550ec0552d27813fffdedad69a4e5fd0746099044ff69c24d2681384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 03:44:32 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 03 Aug 2023 03:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 03:44:43 GMT
ENV GOSU_VERSION=1.16
# Thu, 03 Aug 2023 03:44:43 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 03 Aug 2023 03:44:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 03 Aug 2023 03:44:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 03 Aug 2023 03:44:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 03 Aug 2023 03:44:53 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 03 Aug 2023 03:44:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 03 Aug 2023 03:44:54 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 03 Aug 2023 03:44:54 GMT
ENV MONGO_MAJOR=5.0
# Thu, 03 Aug 2023 03:44:54 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 15 Aug 2023 23:35:37 GMT
ENV MONGO_VERSION=5.0.20
# Tue, 15 Aug 2023 23:36:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 15 Aug 2023 23:36:12 GMT
VOLUME [/data/db /data/configdb]
# Tue, 15 Aug 2023 23:36:13 GMT
ENV HOME=/data/db
# Tue, 15 Aug 2023 23:36:13 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Tue, 15 Aug 2023 23:36:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Aug 2023 23:36:13 GMT
EXPOSE 27017
# Tue, 15 Aug 2023 23:36:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97968f0a09f53d77c97c3dd35ab241e67d46bebdbb67def88e16325ec93d3b9b`  
		Last Modified: Thu, 03 Aug 2023 03:46:18 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51fbef5da044637e07c3bec3d7a65f6b1ce998cdd96dc76c39f75f2ada305fb`  
		Last Modified: Thu, 03 Aug 2023 03:46:20 GMT  
		Size: 8.4 MB (8374112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4724921322014a775b57e03fb8dfc28cf7f69d8625ce79be4011cc72cef66422`  
		Last Modified: Thu, 03 Aug 2023 03:46:19 GMT  
		Size: 1.3 MB (1256021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a184e6b7d3fb5f29371d6ecf5d8eff4154526c3d88ee4e10c6b1c626ffa8398c`  
		Last Modified: Thu, 03 Aug 2023 03:46:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2759528c7f5fd34deb7ae4241fda2a30a638be4f344e686343e3987832242138`  
		Last Modified: Thu, 03 Aug 2023 03:46:16 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c283613406ab23beec249d20783d1af6820c36048260bffee83b46468af35603`  
		Last Modified: Thu, 03 Aug 2023 03:46:16 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880fe547e2a4f73e9a348eb1e015025b64a696f64f34b2b05874e5309c6dd47d`  
		Last Modified: Tue, 15 Aug 2023 23:37:46 GMT  
		Size: 217.1 MB (217082899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7f548a86663cc1a7c3eea2acd1c883e1714ac4fe97d2e74f63f5d5ac8c3e15`  
		Last Modified: Tue, 15 Aug 2023 23:37:20 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f10d78bdd1b88bcd16cc40edd266465f8e5125fae9a8b0994b857a919dedd32e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248418922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2301689d670c3f3c73b18967a70bcd9c885bbb23b6db6af4690c54d51f813b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:22:39 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 03 Aug 2023 01:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Aug 2023 01:22:49 GMT
ENV GOSU_VERSION=1.16
# Thu, 03 Aug 2023 01:22:49 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 03 Aug 2023 01:22:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 03 Aug 2023 01:22:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 03 Aug 2023 01:22:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 03 Aug 2023 01:22:57 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 03 Aug 2023 01:22:58 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 03 Aug 2023 01:22:58 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 03 Aug 2023 01:22:58 GMT
ENV MONGO_MAJOR=5.0
# Thu, 03 Aug 2023 01:22:58 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 15 Aug 2023 23:55:44 GMT
ENV MONGO_VERSION=5.0.20
# Tue, 15 Aug 2023 23:56:18 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 15 Aug 2023 23:56:21 GMT
VOLUME [/data/db /data/configdb]
# Tue, 15 Aug 2023 23:56:21 GMT
ENV HOME=/data/db
# Tue, 15 Aug 2023 23:56:21 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Tue, 15 Aug 2023 23:56:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Aug 2023 23:56:21 GMT
EXPOSE 27017
# Tue, 15 Aug 2023 23:56:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f97f1dcb6cee9058d0b4a2cca1be112f93e5ed4de0f2d70739c587be8522ea`  
		Last Modified: Thu, 03 Aug 2023 01:25:16 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07b44adadaead162cbe5a136832ec2eddeca5ac9be7fae2832c2385eea8b9d`  
		Last Modified: Thu, 03 Aug 2023 01:25:17 GMT  
		Size: 8.2 MB (8203065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9448017a1670b361903a0de679871ba19e162e1240793da4f9b10b633344b566`  
		Last Modified: Thu, 03 Aug 2023 01:25:16 GMT  
		Size: 1.2 MB (1189758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b53cff26f8548485b3ce5679cba67153e4c4d641f783853f6b9d47322907d97`  
		Last Modified: Thu, 03 Aug 2023 01:25:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b622933870167b97b7f020e1a0e4758ef4b720fc60314cd8c678123e898d57a3`  
		Last Modified: Thu, 03 Aug 2023 01:25:14 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46060c09e9934ef20d7b4b63e6edad38f8b847d5f213d57f43e1b1ae6bee5dd`  
		Last Modified: Thu, 03 Aug 2023 01:25:14 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f00e4c13eae356690bfc6aeb1affd5e21cc234a145babca8f49e1eca4d8d29c`  
		Last Modified: Tue, 15 Aug 2023 23:57:33 GMT  
		Size: 211.8 MB (211816832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4866f0a576fdcccc3a336c99f5da902955e9a27091670067e9c9db00d5c2d623`  
		Last Modified: Tue, 15 Aug 2023 23:57:15 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
