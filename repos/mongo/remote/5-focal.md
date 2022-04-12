## `mongo:5-focal`

```console
$ docker pull mongo@sha256:276a782d5ffa90d6054305337c0d31a31bfe7ea544980e8969159036489e0835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:5b5263a7d25d06d5149904eaaacdb359edcd4f26a3d971265f85362dd2406655
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249706920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21ad2afe409e7d5cba51a409dadff2b9935b67b91934e44cdf7b44cd2778f33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:06:17 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 06 Apr 2022 04:06:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:06:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Apr 2022 04:06:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 06 Apr 2022 04:06:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Apr 2022 04:06:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Apr 2022 04:06:39 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 06 Apr 2022 04:06:39 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 06 Apr 2022 04:06:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 06 Apr 2022 04:06:40 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 06 Apr 2022 04:06:40 GMT
ENV MONGO_MAJOR=5.0
# Wed, 06 Apr 2022 04:06:40 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 11 Apr 2022 21:42:25 GMT
ENV MONGO_VERSION=5.0.7
# Mon, 11 Apr 2022 21:42:54 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 11 Apr 2022 21:42:56 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 11 Apr 2022 21:42:56 GMT
VOLUME [/data/db /data/configdb]
# Mon, 11 Apr 2022 21:42:56 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Mon, 11 Apr 2022 21:42:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Apr 2022 21:42:56 GMT
EXPOSE 27017
# Mon, 11 Apr 2022 21:42:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a086fc80eaabd12d02bd4065e009878cfc9362d238169ea745e39a263c2270`  
		Last Modified: Wed, 06 Apr 2022 04:09:02 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6592c2fb05fb80b5a3c01c92bc623faf5fc0ded7dd0551be39ea78a4d9efc8`  
		Last Modified: Wed, 06 Apr 2022 04:09:03 GMT  
		Size: 3.1 MB (3064007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad2281c276115bf50711681c05326e6a65cec55a5d727481ac937664a35efa`  
		Last Modified: Wed, 06 Apr 2022 04:09:03 GMT  
		Size: 6.5 MB (6505644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34073132290cb60828b8a5ca2eb216d7f6c21a306dd0ba675f0a297b5ed5acd0`  
		Last Modified: Wed, 06 Apr 2022 04:09:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec793bc1a2aee24538b2237e39e4a3a0a5f2d6d6362e613893093708f8ebcf4a`  
		Last Modified: Wed, 06 Apr 2022 04:09:00 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660887418c9b636f3ae29187f3e75b0b75f104c10c76177bda14c4f86c667dd4`  
		Last Modified: Wed, 06 Apr 2022 04:09:00 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6674b2f5c8282f9746304f125205ff9fa8213318e3f22e5904e54b5afd375cc8`  
		Last Modified: Mon, 11 Apr 2022 21:43:56 GMT  
		Size: 211.6 MB (211562254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ad8871da64841dd4393c3945e964a6e11fbed92e1abc7dbbee2271509f521a`  
		Last Modified: Mon, 11 Apr 2022 21:43:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f7bc3e1868adeb709abf3b25e3acca6c194d0977675d48c8307dbcbc2fabe7`  
		Last Modified: Mon, 11 Apr 2022 21:43:27 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:714b74ff465bd78abbae10bfcefe1bb331c6ad38c40a2226b0ad8db5428db25e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241848404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1658c558d2d5bd62863e0c8746b8b296387cc7f6bdbb295ec5e0b715247b10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:29:38 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 05 Apr 2022 23:29:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:29:49 GMT
ENV GOSU_VERSION=1.12
# Tue, 05 Apr 2022 23:29:50 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 05 Apr 2022 23:30:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Apr 2022 23:30:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Apr 2022 23:30:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 05 Apr 2022 23:30:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 05 Apr 2022 23:30:11 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 05 Apr 2022 23:30:12 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 05 Apr 2022 23:30:13 GMT
ENV MONGO_MAJOR=5.0
# Tue, 05 Apr 2022 23:30:14 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 11 Apr 2022 21:46:09 GMT
ENV MONGO_VERSION=5.0.7
# Mon, 11 Apr 2022 21:46:32 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 11 Apr 2022 21:46:32 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 11 Apr 2022 21:46:33 GMT
VOLUME [/data/db /data/configdb]
# Mon, 11 Apr 2022 21:46:35 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Mon, 11 Apr 2022 21:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Apr 2022 21:46:36 GMT
EXPOSE 27017
# Mon, 11 Apr 2022 21:46:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9275dc5f58a824992dd7134eb5d1a03b3444789e31773e1610b9604d7fd5293f`  
		Last Modified: Tue, 05 Apr 2022 23:33:26 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e820cd795df140b554de55a8fd8db2ab8e46f204bf20439b9fe7e342d06b323e`  
		Last Modified: Tue, 05 Apr 2022 23:33:27 GMT  
		Size: 2.9 MB (2911252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003e7508c0ed3f4cf57557f470f1fdf5d9d803515e608dd76cc5fdc86673f691`  
		Last Modified: Tue, 05 Apr 2022 23:33:28 GMT  
		Size: 6.2 MB (6247673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c926d087e859efce609d51a7725b4dc22aad4acbeea44ae5fcc9093aeae447`  
		Last Modified: Tue, 05 Apr 2022 23:33:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c8045d45d9657198979d78588596602f3074b44802c00a92565770e7eb13db`  
		Last Modified: Tue, 05 Apr 2022 23:33:24 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2561362d345d5c89d213f5606c562b6b692a8ecf8800ca8b4fd260e8bcc59dc9`  
		Last Modified: Tue, 05 Apr 2022 23:33:24 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce14378ef364a0a513134bbc3b63c762cf01047f38f6e0634fd5df52de6fb4e`  
		Last Modified: Mon, 11 Apr 2022 21:48:03 GMT  
		Size: 205.5 MB (205511504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2e8cf09fc93337256d677de212c10c59f3ceb22060fc6b919fc8c8bb5c84f3`  
		Last Modified: Mon, 11 Apr 2022 21:47:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2f4560781063c6f09360ce9f50171a0368d5aa42143e9a2157eb5afd4d2dc5`  
		Last Modified: Mon, 11 Apr 2022 21:47:36 GMT  
		Size: 5.0 KB (4951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
