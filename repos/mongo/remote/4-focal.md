## `mongo:4-focal`

```console
$ docker pull mongo@sha256:e2c8545263a4123574f2b22e89dbdba3490eee55829443be4fb80a0093b7c47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:e6270eb2e6cd23adb333b559747e0e4843ae81944bd1e2236f5fca64260061a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172781224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fdd3aa95735a99c08918abd5ecf12b425ab1259bffd5117207b9ab8b516e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:30:41 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 02 Aug 2022 20:30:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:30:50 GMT
ENV GOSU_VERSION=1.12
# Tue, 02 Aug 2022 20:30:50 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 02 Aug 2022 20:31:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 20:31:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 20:31:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 02 Aug 2022 20:31:39 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 02 Aug 2022 20:31:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 20:31:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 20:31:40 GMT
ENV MONGO_MAJOR=4.4
# Tue, 02 Aug 2022 20:31:40 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 02 Aug 2022 20:31:40 GMT
ENV MONGO_VERSION=4.4.15
# Tue, 02 Aug 2022 20:31:56 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 02 Aug 2022 20:31:57 GMT
VOLUME [/data/db /data/configdb]
# Tue, 02 Aug 2022 20:31:57 GMT
ENV HOME=/data/db
# Tue, 02 Aug 2022 20:31:57 GMT
COPY file:b7b44e96082c97da2e7f6248f8bbb2edd837542169af52bcc3f53a0cf8b74b7e in /usr/local/bin/ 
# Tue, 02 Aug 2022 20:31:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:31:57 GMT
EXPOSE 27017
# Tue, 02 Aug 2022 20:31:57 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016bc871e2b33f0e2a37272769ebd6defdb4b702f0d41ec1e685f0366b64e64a`  
		Last Modified: Tue, 02 Aug 2022 20:33:16 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd649edd82d79ffc6f573cd5da7909ae50596b95aca684a571aff6e36aa8cb`  
		Last Modified: Tue, 02 Aug 2022 20:33:17 GMT  
		Size: 3.1 MB (3059542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bf776c01e412c9cf35ea7a41f97370c486dee27a2aab228cf2e850a8863e8b`  
		Last Modified: Tue, 02 Aug 2022 20:33:17 GMT  
		Size: 6.5 MB (6506025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f0405a2fe343547a60a9d4182261ca02d70bb9e47d6cd248f3285d6b41e64c`  
		Last Modified: Tue, 02 Aug 2022 20:33:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14992f104363c835007cf3d79dc4a7ab88411061bef16f67348af373c14fb647`  
		Last Modified: Tue, 02 Aug 2022 20:33:57 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fd4469638d1a6ef58264ebd185e24ffb1b93cf9025de6e213a28bae3758be2`  
		Last Modified: Tue, 02 Aug 2022 20:33:57 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fe7cd58602a7a8f87114de32bc07385a3657155a7267e2826bd98d7295a158`  
		Last Modified: Tue, 02 Aug 2022 20:34:15 GMT  
		Size: 134.6 MB (134634424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294fa2ba585402c146a82d970595105f796cf5e68d49cee74f84ddf5782074b2`  
		Last Modified: Tue, 02 Aug 2022 20:33:57 GMT  
		Size: 5.0 KB (4951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:26b7b882d2ea3ac07b2a7f78ac59d04525443b50931d11472c2a8fe5e376ad98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167618687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af153048014169d41c7add552b9d065f0302252e6805c8e164eb09670ca22a5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:46:08 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 02 Aug 2022 18:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:46:42 GMT
ENV GOSU_VERSION=1.12
# Tue, 02 Aug 2022 18:46:43 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 02 Aug 2022 18:47:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:47:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:47:52 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 02 Aug 2022 18:47:53 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 02 Aug 2022 18:47:54 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 18:47:55 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 18:47:56 GMT
ENV MONGO_MAJOR=4.4
# Tue, 02 Aug 2022 18:47:57 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 02 Aug 2022 18:47:58 GMT
ENV MONGO_VERSION=4.4.15
# Tue, 02 Aug 2022 18:48:38 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 02 Aug 2022 18:48:38 GMT
VOLUME [/data/db /data/configdb]
# Tue, 02 Aug 2022 18:48:39 GMT
ENV HOME=/data/db
# Tue, 02 Aug 2022 18:48:41 GMT
COPY file:b7b44e96082c97da2e7f6248f8bbb2edd837542169af52bcc3f53a0cf8b74b7e in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:48:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:48:42 GMT
EXPOSE 27017
# Tue, 02 Aug 2022 18:48:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f92e7525120387a6bc9ec42b9ebfc8115309ab70f65a766e3fda1239d787f9`  
		Last Modified: Tue, 02 Aug 2022 18:51:20 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdda1347325980782ee9b7c6232d712c262b77bc097f712508cf17423dea0de`  
		Last Modified: Tue, 02 Aug 2022 18:51:21 GMT  
		Size: 2.9 MB (2907020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e02463a0f47d7c309281cbc5b4603815ec64c4653d4ed4ac37a06e6bb91b8e`  
		Last Modified: Tue, 02 Aug 2022 18:51:21 GMT  
		Size: 6.2 MB (6249317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9bc5b0968e9dc0079b9ed64930bcf14f8d69847b72f526a1dd1c8bd43df8cc`  
		Last Modified: Tue, 02 Aug 2022 18:51:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8545261514a7f06edbdfa364e41d204214006c10a5cd3f8fa3d3dbab8462d0`  
		Last Modified: Tue, 02 Aug 2022 18:52:03 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9428703c3af24b6c6867936bdcf957a9c2a7fc1201fc8956327be046401cdd59`  
		Last Modified: Tue, 02 Aug 2022 18:52:03 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28ceb5cc272d85e5d9da586964a4158dbb5ade4829e84d9810f11461d39acc`  
		Last Modified: Tue, 02 Aug 2022 18:52:20 GMT  
		Size: 131.3 MB (131262044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e753228b225776db97b295e52fd7bb4bb59c833dd8063d77605b5000c1b3cf3`  
		Last Modified: Tue, 02 Aug 2022 18:52:03 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
