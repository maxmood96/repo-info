## `mongo:4-focal`

```console
$ docker pull mongo@sha256:2b9d6fd6dca87bbe5ab42f44d6c0948a89c20f3a6e77d91ecaa4ac9cc91a0286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:9909a039a7d237d081bb208ce7eb7c9824dd091f8e277d4b32a8de188c3c53c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176053986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b0e0662b9a8a4413901fdaf4144b63a8daf3dd1ee72a47e1cedb97a73eb28c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:37:40 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 04 Jul 2023 18:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:37:54 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 18:37:54 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 04 Jul 2023 18:38:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 18:38:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 18:39:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 18:39:37 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 04 Jul 2023 18:39:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 04 Jul 2023 18:39:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 04 Jul 2023 18:39:38 GMT
ENV MONGO_MAJOR=4.4
# Tue, 04 Jul 2023 18:39:38 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 14 Jul 2023 00:21:37 GMT
ENV MONGO_VERSION=4.4.23
# Fri, 14 Jul 2023 00:21:55 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 14 Jul 2023 00:21:56 GMT
VOLUME [/data/db /data/configdb]
# Fri, 14 Jul 2023 00:21:56 GMT
ENV HOME=/data/db
# Fri, 14 Jul 2023 00:21:56 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Fri, 14 Jul 2023 00:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jul 2023 00:21:56 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 00:21:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb7d9e7beb16f8524b1364b05291e986d13fe9e41a3527c0df712b6488ccd5`  
		Last Modified: Tue, 04 Jul 2023 18:42:08 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8673b711682ec60ce786477043890cd2390b807b1ba6626eb5d11679187fa60`  
		Last Modified: Tue, 04 Jul 2023 18:42:09 GMT  
		Size: 8.4 MB (8374126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38f30c6ed576db67667e1e67bc05ec390f5bae0168fa33f40146fc13227c529`  
		Last Modified: Tue, 04 Jul 2023 18:42:08 GMT  
		Size: 1.3 MB (1256098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d115e2a9dcf0698551b83906207c5d79faa89c5a947f926bfe11cb95a4726b7`  
		Last Modified: Tue, 04 Jul 2023 18:42:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1908425bccb8c42abbd85af80e827c1bdd237508d4a179f7ce424743235f8ddc`  
		Last Modified: Tue, 04 Jul 2023 18:43:40 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc65cb70f9c5d23019a1ec2ebd4ac46858b127da4b9618f441ed0adcd47f6344`  
		Last Modified: Tue, 04 Jul 2023 18:43:40 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a284ad28140b7fc00027cb2d74d0bdaf3ffae73c0e3b4ec8803561bf503c9a4`  
		Last Modified: Fri, 14 Jul 2023 00:24:26 GMT  
		Size: 137.8 MB (137835065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0131638481b2b49b1847ea920767cead4bd43299a7ba9bd1fbb118ffc681b861`  
		Last Modified: Fri, 14 Jul 2023 00:24:10 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8515c3c4814ad3f9b514a128e9c01d7a7d7af966868f376feaac329329575e15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171662096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d976babc1855283f8800120bb6c5e0bdf89feadaf0f536e47db7308d8e0e33`
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
# Thu, 03 Aug 2023 01:23:28 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 03 Aug 2023 01:23:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 03 Aug 2023 01:23:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 03 Aug 2023 01:23:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 03 Aug 2023 01:23:28 GMT
ENV MONGO_MAJOR=4.4
# Thu, 03 Aug 2023 01:23:29 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 03 Aug 2023 01:23:29 GMT
ENV MONGO_VERSION=4.4.23
# Thu, 03 Aug 2023 01:23:43 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 03 Aug 2023 01:23:45 GMT
VOLUME [/data/db /data/configdb]
# Thu, 03 Aug 2023 01:23:45 GMT
ENV HOME=/data/db
# Thu, 03 Aug 2023 01:23:45 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Aug 2023 01:23:45 GMT
EXPOSE 27017
# Thu, 03 Aug 2023 01:23:45 GMT
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
	-	`sha256:948327c8378a5c7493d4b2a4919ba9643fcf30db27afb0ae2985ef7f52131330`  
		Last Modified: Thu, 03 Aug 2023 01:25:43 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e4d1f890c20d32367d528673dbd681b537b9dbc1fb6f7545d47d433026df9`  
		Last Modified: Thu, 03 Aug 2023 01:25:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7717044bfb24b7ec23b057d83df87f63294f1bc536c4bf905504132daf239aea`  
		Last Modified: Thu, 03 Aug 2023 01:25:55 GMT  
		Size: 135.1 MB (135060007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34d6b2ad845dd274277bb7fdbf8e0efc92e2fa3bacb6e60c5cbcbd3c754b00a`  
		Last Modified: Thu, 03 Aug 2023 01:25:43 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
