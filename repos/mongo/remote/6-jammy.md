## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:455941e3468a6cc83f3655912cff91f199dae90953630240781587f5f2f024f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:028650e24cdc662da15e11809d63b4f2a0b7eb782f3ca4f80a303a4c255fab89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237158219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61eca46d7769696024576c77399590837fa7efd5265809638981ad7d7977e987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:00:25 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 04 May 2023 08:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:00:35 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 May 2023 08:00:35 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 04 May 2023 08:00:42 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 May 2023 08:00:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 04 May 2023 08:00:43 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 04 May 2023 08:00:43 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 04 May 2023 08:00:43 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 08:00:44 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 04 May 2023 08:00:44 GMT
ENV MONGO_MAJOR=6.0
# Thu, 04 May 2023 08:00:44 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 24 May 2023 01:40:05 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 24 May 2023 01:40:34 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 24 May 2023 01:40:35 GMT
VOLUME [/data/db /data/configdb]
# Wed, 24 May 2023 01:40:35 GMT
ENV HOME=/data/db
# Wed, 24 May 2023 01:40:36 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Wed, 24 May 2023 01:40:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 May 2023 01:40:36 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:40:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb83bb7be9889457cf3729cf50df2596a4c21e221943325d43e3621afc85296`  
		Last Modified: Thu, 04 May 2023 08:01:33 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95121721c4c526b9ccd2b5630e6b439780c39872431d4a3bedcbc4769350cdc`  
		Last Modified: Thu, 04 May 2023 08:01:34 GMT  
		Size: 5.0 MB (5027884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799041b403cabf54ac974c77fee7211729ec7ddc13fbabe98f93868f43a32fcb`  
		Last Modified: Thu, 04 May 2023 08:01:34 GMT  
		Size: 1.3 MB (1252462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1828e70ef29acb455c8b97fe8b6bc926a79a105e578b55cf78bd979be29535b5`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3781beae9e4d098a887d213f6d3fbb1c9c9648b3516672f63c534a6aa1ea67`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d575316233327cdb50cd97e5b06250f7e5733f3e9aa5a79ba8821492145fd78`  
		Last Modified: Thu, 04 May 2023 08:01:31 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf73eea516c85b3b9a343be653841792b483e848393886655392e7be08c1c876`  
		Last Modified: Wed, 24 May 2023 01:42:32 GMT  
		Size: 200.4 MB (200438961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cf5b4ad9679ad118d13d063177463f678e486a09decaacfe5557a68c1396b8`  
		Last Modified: Wed, 24 May 2023 01:42:08 GMT  
		Size: 5.0 KB (5023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d9ee96a095b04a9ed5d3c640cbd7d1a020bd7ad126d08746122adc0019c9121e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230834082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376ea24ce0f0ee79e7de9041303eab3dec2b8a9cef3edf96e122acf6243a1403`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:34:19 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 01 Jun 2023 23:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:34:30 GMT
ENV GOSU_VERSION=1.16
# Thu, 01 Jun 2023 23:34:30 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 01 Jun 2023 23:34:37 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 01 Jun 2023 23:34:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 01 Jun 2023 23:35:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 01 Jun 2023 23:35:08 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 01 Jun 2023 23:35:08 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 01 Jun 2023 23:35:08 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 01 Jun 2023 23:35:08 GMT
ENV MONGO_MAJOR=6.0
# Thu, 01 Jun 2023 23:35:08 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 01 Jun 2023 23:35:09 GMT
ENV MONGO_VERSION=6.0.6
# Thu, 01 Jun 2023 23:35:24 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 01 Jun 2023 23:35:28 GMT
VOLUME [/data/db /data/configdb]
# Thu, 01 Jun 2023 23:35:28 GMT
ENV HOME=/data/db
# Thu, 01 Jun 2023 23:35:28 GMT
COPY file:e3d6a34db83fe880626bff5d0b8d720ae43720caac9c739cbd1d336a129dad2d in /usr/local/bin/ 
# Thu, 01 Jun 2023 23:35:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Jun 2023 23:35:28 GMT
EXPOSE 27017
# Thu, 01 Jun 2023 23:35:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf03b60a39ae25134deb53f42e4002fa81339aad24608180a4aae7e64d70cd5`  
		Last Modified: Thu, 01 Jun 2023 23:36:36 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c113973dff3b28b9198806e84fbbc6cc893ae56fa8d80f1bedec18c70655d73`  
		Last Modified: Thu, 01 Jun 2023 23:36:37 GMT  
		Size: 5.0 MB (4992105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26b2cb251fdc9f6d66e0c3890a2ceec46f1e45f3d9ec57f1f659dffb9b9d0d`  
		Last Modified: Thu, 01 Jun 2023 23:36:36 GMT  
		Size: 1.2 MB (1184869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09a4405ccbc320c10f26573b811c3c42f8f3d65daa7a5a3c58d4c41222d0722`  
		Last Modified: Thu, 01 Jun 2023 23:36:36 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49809477b7bb57e05f2a735d4d771258df2d8cc913b3c5eb2988f73e88dee303`  
		Last Modified: Thu, 01 Jun 2023 23:37:00 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95542cdd3e5b30974b568070ec37d28b807470837376975358b8c1e87aea20d6`  
		Last Modified: Thu, 01 Jun 2023 23:37:00 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2f6dd7bfa2041692e36dffdeba82095f6c9dffb9172300696f825dfa8b0985`  
		Last Modified: Thu, 01 Jun 2023 23:37:18 GMT  
		Size: 196.3 MB (196259376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7733cfe8e25e9d4b1f3f759abaf52f6f99819d0604e179c2eee780294272528a`  
		Last Modified: Thu, 01 Jun 2023 23:37:00 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
