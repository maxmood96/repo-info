## `mongo:focal`

```console
$ docker pull mongo@sha256:52dbb83b1f808c727f5f649b89eb1a0287c8f8d44f94f51b296bda258c570101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:focal` - linux; amd64

```console
$ docker pull mongo@sha256:5255f45e7f87b4404388205351ef69e5f6c018976b355729afa01014faf7792a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246512678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98599fdfd656eada595e97b0389b911095dc7e914a2c194e0f0395cabec90fa`
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
# Tue, 02 Aug 2022 20:31:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 02 Aug 2022 20:31:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 02 Aug 2022 20:31:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 20:31:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 20:31:03 GMT
ENV MONGO_MAJOR=5.0
# Tue, 02 Aug 2022 20:31:04 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 02 Aug 2022 20:31:04 GMT
ENV MONGO_VERSION=5.0.10
# Tue, 02 Aug 2022 20:31:27 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 02 Aug 2022 20:31:28 GMT
VOLUME [/data/db /data/configdb]
# Tue, 02 Aug 2022 20:31:29 GMT
ENV HOME=/data/db
# Tue, 02 Aug 2022 20:31:29 GMT
COPY file:b7b44e96082c97da2e7f6248f8bbb2edd837542169af52bcc3f53a0cf8b74b7e in /usr/local/bin/ 
# Tue, 02 Aug 2022 20:31:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 20:31:29 GMT
EXPOSE 27017
# Tue, 02 Aug 2022 20:31:29 GMT
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
	-	`sha256:417812e2676cfb1081230e71a277704bbeb9a058b34dc34fc1f83a874410d437`  
		Last Modified: Tue, 02 Aug 2022 20:33:14 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905384a6c9a925f65f24476b0520ff9fbb65badb483ce7d3ce01d837894f2cb8`  
		Last Modified: Tue, 02 Aug 2022 20:33:14 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408fa3184a2548685c7bd8fcc9d68aca43a4244dabbc787fc939bd280065c6e1`  
		Last Modified: Tue, 02 Aug 2022 20:33:42 GMT  
		Size: 208.4 MB (208365877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778b067af4f1cacf3a7fd900865dcb4a58192633210ea2ae3917d09d1e98337f`  
		Last Modified: Tue, 02 Aug 2022 20:33:14 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a427e2fcc703a2a8bfabc8a4efbd528686f817e484cd151a95444fc6b5da3e46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238787864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8522acba0ea1eb4f6d65489562759853709e983e8a2ab13b9d08a1bf89477a34`
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
# Tue, 02 Aug 2022 18:47:04 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 02 Aug 2022 18:47:05 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 02 Aug 2022 18:47:06 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 18:47:07 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 18:47:08 GMT
ENV MONGO_MAJOR=5.0
# Tue, 02 Aug 2022 18:47:09 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 02 Aug 2022 18:47:10 GMT
ENV MONGO_VERSION=5.0.10
# Tue, 02 Aug 2022 18:47:38 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 02 Aug 2022 18:47:38 GMT
VOLUME [/data/db /data/configdb]
# Tue, 02 Aug 2022 18:47:39 GMT
ENV HOME=/data/db
# Tue, 02 Aug 2022 18:47:41 GMT
COPY file:b7b44e96082c97da2e7f6248f8bbb2edd837542169af52bcc3f53a0cf8b74b7e in /usr/local/bin/ 
# Tue, 02 Aug 2022 18:47:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:47:42 GMT
EXPOSE 27017
# Tue, 02 Aug 2022 18:47:43 GMT
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
	-	`sha256:33f0d07ad9ca0e23d2aa1f261353224866eb9e7e2aee1f1e0f55252f197a51a6`  
		Last Modified: Tue, 02 Aug 2022 18:51:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c25f5ea9839a3e6d5693d2a2ccb61e495710d2e0ae3523d52ab23a576c87a8`  
		Last Modified: Tue, 02 Aug 2022 18:51:18 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f9cf44c1e9cc8403cd0bfed5a7750a4dfcc084c43f8e5d17522d99f66556e5`  
		Last Modified: Tue, 02 Aug 2022 18:51:46 GMT  
		Size: 202.4 MB (202431223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd4a874cd214da54263710f8ce4f41f6039f1ea95996b3a072d99f7cb0988f9`  
		Last Modified: Tue, 02 Aug 2022 18:51:18 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
