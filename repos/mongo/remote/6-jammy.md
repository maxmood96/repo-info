## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:27abdfe0e306af65c579e317e54cf3976b7dbc8a15eb7b779373cbfa6e449d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:82f46c71cb9fab7953e12fea75528e83e596db259880fd9ee0d61d856d5db552
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248669277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9ad1792462215ed71bb41cf3b5cf0865b8248288a2371f0e796ab48403355b`
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
# Fri, 13 Oct 2023 04:47:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 04:47:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 04:47:00 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 04:47:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 04:47:00 GMT
ENV MONGO_MAJOR=6.0
# Fri, 13 Oct 2023 04:47:00 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 29 Nov 2023 01:39:46 GMT
ENV MONGO_VERSION=6.0.12
# Wed, 29 Nov 2023 01:40:09 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 29 Nov 2023 01:40:10 GMT
VOLUME [/data/db /data/configdb]
# Wed, 29 Nov 2023 01:40:10 GMT
ENV HOME=/data/db
# Wed, 29 Nov 2023 01:40:10 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 29 Nov 2023 01:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Nov 2023 01:40:10 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 01:40:11 GMT
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
	-	`sha256:64d7f1f42d4e63f3a98c47e874487926516bc0dfa4a0e15afbca43bf437b0138`  
		Last Modified: Fri, 13 Oct 2023 04:50:20 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9074c327c8ee15bc238143b75a23289ff5bb41c6eff8f25e3084fc4675dd171`  
		Last Modified: Fri, 13 Oct 2023 04:50:20 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b707ebdea7748e2056d8f7557f49c1002d867a3a3fd628ef55627d53e8a1a7ca`  
		Last Modified: Wed, 29 Nov 2023 01:42:48 GMT  
		Size: 211.9 MB (211918106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6374950bad611dd35e24da92d6b09dbdfa9a13d0249b06de29d7a6519152653`  
		Last Modified: Wed, 29 Nov 2023 01:42:24 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:71d9939101b60be695785613c3e50fe86b4146e2c78fdc12afdd963da9f5fc7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241674378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7b6db47e784385268417efe3f9fa9a04d8a0af97fea879b493e49b4275e90d`
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
# Fri, 13 Oct 2023 05:08:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 05:08:57 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 05:08:57 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:57 GMT
ENV MONGO_MAJOR=6.0
# Fri, 13 Oct 2023 05:08:58 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 29 Nov 2023 06:26:45 GMT
ENV MONGO_VERSION=6.0.12
# Wed, 29 Nov 2023 06:27:07 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 29 Nov 2023 06:27:11 GMT
VOLUME [/data/db /data/configdb]
# Wed, 29 Nov 2023 06:27:11 GMT
ENV HOME=/data/db
# Wed, 29 Nov 2023 06:27:11 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 29 Nov 2023 06:27:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Nov 2023 06:27:11 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 06:27:11 GMT
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
	-	`sha256:a2eeb452429f775ed20059880acafcb8a219c67db5b984e6749d02320470fe3a`  
		Last Modified: Fri, 13 Oct 2023 05:12:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d156383ae52ebf0a558b87523ef31a1be7b49ec6ede19657709b2efc8b0d27f`  
		Last Modified: Fri, 13 Oct 2023 05:12:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9033914511f7ba3e7dce9f02dfe609bcd50aab76691dbd7a0a7abeeb37ef1b2`  
		Last Modified: Wed, 29 Nov 2023 06:29:33 GMT  
		Size: 207.1 MB (207093499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64885ab603d21c667cf3b18a12da4e22d862d9879295bbf102439853cb7ee5b`  
		Last Modified: Wed, 29 Nov 2023 06:29:15 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
