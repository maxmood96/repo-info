## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:9a56fae017737c45dd18483ca947640569ae65f9968f646476e0e9637f9fd65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:1235385d1f63a09c2ffad47c4b9393af1ee82ea2fff6660d81570a2e824e5ce2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241721809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a1e899030242f7e15177e7d25a1bcf2cee51891dd88c15dca6036e3c22ad54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 01:07:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 02 Sep 2023 01:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:07:27 GMT
ENV GOSU_VERSION=1.16
# Sat, 02 Sep 2023 01:07:27 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 02 Sep 2023 01:07:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 02 Sep 2023 01:07:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 02 Sep 2023 01:08:44 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 02 Sep 2023 01:08:44 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 02 Sep 2023 01:08:44 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 02 Sep 2023 01:08:44 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 02 Sep 2023 01:08:44 GMT
ENV MONGO_MAJOR=6.0
# Sat, 02 Sep 2023 01:08:45 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 02 Sep 2023 01:08:45 GMT
ENV MONGO_VERSION=6.0.9
# Sat, 02 Sep 2023 01:09:05 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 02 Sep 2023 01:09:07 GMT
VOLUME [/data/db /data/configdb]
# Sat, 02 Sep 2023 01:09:07 GMT
ENV HOME=/data/db
# Sat, 02 Sep 2023 01:09:07 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Sat, 02 Sep 2023 01:09:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 01:09:07 GMT
EXPOSE 27017
# Sat, 02 Sep 2023 01:09:07 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0ba5360de512f129bfe46f60bd4e1bb7baeb2ab7c0360795b42340bca2e4f3`  
		Last Modified: Sat, 02 Sep 2023 01:14:39 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27add3570ee3faa9da1b77c375b8bb99413712b5224b28a602ee63fd472d318`  
		Last Modified: Sat, 02 Sep 2023 01:14:40 GMT  
		Size: 5.1 MB (5050523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfb29d27eb410d190c80f9e2e77d260251df361480f9e7657d1411564a05e23`  
		Last Modified: Sat, 02 Sep 2023 01:14:40 GMT  
		Size: 1.3 MB (1252993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd1e00f8db01ad6cf6f6c0b79df726ee130c985e1cf6b617489d59d7def95c8`  
		Last Modified: Sat, 02 Sep 2023 01:14:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad85f1157a381c9692e0be08e724487abc5786c435add85c192c852ed5d7360`  
		Last Modified: Sat, 02 Sep 2023 01:15:54 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec76a5cb280a2beedb7ab129dc76f852b54bb8743bc851bce7d14d6a230cc194`  
		Last Modified: Sat, 02 Sep 2023 01:15:54 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861360d563a669b739fd83676cff3abb7e69d0c6b1136ef9c4c7d1d0d983e31`  
		Last Modified: Sat, 02 Sep 2023 01:16:18 GMT  
		Size: 205.0 MB (204970637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f575bac0eeb9bbee6c22f7ef6f6953e75120210494492e96efaf4ea76602d19`  
		Last Modified: Sat, 02 Sep 2023 01:15:54 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:3da34f9263057f76464023c6b6c210912437284af87931992b9705d95e888d25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234992729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e849acfdcaf9ca23ca1c766a0cdc8531e296aaae841fdab55d904d9587fb3c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:45:07 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Sep 2023 23:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:45:17 GMT
ENV GOSU_VERSION=1.16
# Fri, 01 Sep 2023 23:45:17 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 01 Sep 2023 23:45:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Sep 2023 23:45:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Sep 2023 23:46:23 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 01 Sep 2023 23:46:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Sep 2023 23:46:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Sep 2023 23:46:24 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Sep 2023 23:46:24 GMT
ENV MONGO_MAJOR=6.0
# Fri, 01 Sep 2023 23:46:24 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Sep 2023 23:46:24 GMT
ENV MONGO_VERSION=6.0.9
# Fri, 01 Sep 2023 23:46:45 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Sep 2023 23:46:48 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Sep 2023 23:46:48 GMT
ENV HOME=/data/db
# Fri, 01 Sep 2023 23:46:48 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Fri, 01 Sep 2023 23:46:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Sep 2023 23:46:49 GMT
EXPOSE 27017
# Fri, 01 Sep 2023 23:46:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08d376d18d097b2a779141737c301948af04b4f7cd3f2a3fe70a2839152ea98`  
		Last Modified: Fri, 01 Sep 2023 23:48:03 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da44cac7a76e566b31b1edc7a28854883516d28ec592194c83ddc94bb6eb6ca`  
		Last Modified: Fri, 01 Sep 2023 23:48:03 GMT  
		Size: 5.0 MB (4994973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb89f88e3931f6e3134429223ca20bda2f4b80e94999c49cda888b372d905db`  
		Last Modified: Fri, 01 Sep 2023 23:48:03 GMT  
		Size: 1.2 MB (1187414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96b6af4b2ed080ea89c623fcae6f1457d51040f56d1766faffba8fbe0a3ec9a`  
		Last Modified: Fri, 01 Sep 2023 23:48:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffb61f6c41da313c0ce6aeca1b9ed62bce29df95007f91ed4353475d6f201b9`  
		Last Modified: Fri, 01 Sep 2023 23:49:04 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4cff68fd8053edf413600dc5d575101d85e60a5d905c4bc7e5e5a9a4b97878`  
		Last Modified: Fri, 01 Sep 2023 23:49:04 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c609dbcadf8ec5f9fc373873a5ad68761d183d86238ff9d0d92b3ce1584be0a1`  
		Last Modified: Fri, 01 Sep 2023 23:49:21 GMT  
		Size: 200.4 MB (200408683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aafdc9fa478615d8390d8bd1f6f8a406f2804f79f24fc55529493047a9423e8`  
		Last Modified: Fri, 01 Sep 2023 23:49:04 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
