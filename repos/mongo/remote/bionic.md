## `mongo:bionic`

```console
$ docker pull mongo@sha256:ee8a1b33bdaeb890aa9e806b5e69161614b6bd067d57a939be752895b37c5b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:bionic` - linux; amd64

```console
$ docker pull mongo@sha256:9bed7cae49c95e0294775efe35c867094d69d844167a79194be63baf7e032328
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175678433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12d72fd1857f606033ea93d3eac092ef2ff5aec08a0d6f454f80d5cdd105161`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:12:02 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 18 Jun 2021 01:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:12:16 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 01:12:16 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 18 Jun 2021 01:12:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 01:12:29 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 01:12:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 01:12:31 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 18 Jun 2021 01:12:31 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 18 Jun 2021 01:12:31 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 18 Jun 2021 01:12:31 GMT
ENV MONGO_MAJOR=4.4
# Fri, 18 Jun 2021 01:12:32 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 18 Jun 2021 01:12:33 GMT
ENV MONGO_VERSION=4.4.6
# Fri, 18 Jun 2021 01:12:50 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 18 Jun 2021 01:12:52 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 18 Jun 2021 01:12:52 GMT
VOLUME [/data/db /data/configdb]
# Fri, 18 Jun 2021 01:12:52 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Fri, 18 Jun 2021 01:12:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 01:12:53 GMT
EXPOSE 27017
# Fri, 18 Jun 2021 01:12:53 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3380d70bde1cab6b4455704dcce83e027172549216daea62c6190b09bc05c4be`  
		Last Modified: Fri, 18 Jun 2021 01:15:13 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5e30e9886d48467be1dfb167593ca15886072e71381d7325c81cc55b028cc2`  
		Last Modified: Fri, 18 Jun 2021 01:15:14 GMT  
		Size: 3.0 MB (2978550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6583381983d84a9b981816a22a57d822fe9a7a1dddfd41349d0adbba81437e6`  
		Last Modified: Fri, 18 Jun 2021 01:15:14 GMT  
		Size: 5.8 MB (5829386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7873a283454075db613d13bef6cfbccba2b35e199aac1f0e31675f0c0acf4ace`  
		Last Modified: Fri, 18 Jun 2021 01:15:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378cc55e34d7d203d8033840afc0464596f275943047eb75d4e7fe531ff7d2a1`  
		Last Modified: Fri, 18 Jun 2021 01:15:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0d23db902f5758a35fa59df53400c72b0afca648916b9bf03f5774a37c4093`  
		Last Modified: Fri, 18 Jun 2021 01:15:10 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b86c693d31582524264269468b140e976e447a89264dfede3ee25e422b71d08`  
		Last Modified: Fri, 18 Jun 2021 01:15:30 GMT  
		Size: 140.2 MB (140161469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f74de0aa3d4cf58ff90332caf20f22d34e34016216fa7310cf2c31c6fd34c35`  
		Last Modified: Fri, 18 Jun 2021 01:15:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593404e78e3e3c5664f0b5f2a106e6acd4eee65d562e98f0e4f6fbd9652ce853`  
		Last Modified: Fri, 18 Jun 2021 01:15:10 GMT  
		Size: 4.5 KB (4472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:87109d03ec264a335dd911d2d61ba75ddb85c403034be97a7254285b07421b31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168094171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442b659cdc3c5c3b008fa63d0a1c30c1ecf4c32f2e700d17c1dafb94d5864b40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:50 GMT
ADD file:1c098d4ee63884766899c72e542e107525f0b7ade5528de87642587389864bcc in / 
# Thu, 17 Jun 2021 23:53:51 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:40:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 18 Jun 2021 00:40:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:40:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:40:35 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 18 Jun 2021 00:40:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:40:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:40:52 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:40:52 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 18 Jun 2021 00:40:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 18 Jun 2021 00:40:53 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 18 Jun 2021 00:40:53 GMT
ENV MONGO_MAJOR=4.4
# Fri, 18 Jun 2021 00:40:54 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 18 Jun 2021 00:40:54 GMT
ENV MONGO_VERSION=4.4.6
# Fri, 18 Jun 2021 00:41:15 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 18 Jun 2021 00:41:16 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 18 Jun 2021 00:41:16 GMT
VOLUME [/data/db /data/configdb]
# Fri, 18 Jun 2021 00:41:16 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:41:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:41:17 GMT
EXPOSE 27017
# Fri, 18 Jun 2021 00:41:17 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:55c604a74c4b0b41ef666f811f5e160693236be8ea130c6df723480f59cbb9b8`  
		Last Modified: Thu, 17 Jun 2021 23:55:41 GMT  
		Size: 23.7 MB (23728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ae63d6c1546e327e93b9a70308b895e4f8c0c488d4132554aa456011c2891b`  
		Last Modified: Fri, 18 Jun 2021 00:44:01 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ff824326e40aca12c8e9780428861a9675b5b55366f354c853a4145d2a9006`  
		Last Modified: Fri, 18 Jun 2021 00:44:01 GMT  
		Size: 2.7 MB (2669141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b6fdecd48a8062f5b47dded0087a71f8e3536e6b22f47e96365fb91285431a`  
		Last Modified: Fri, 18 Jun 2021 00:44:01 GMT  
		Size: 5.3 MB (5347199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c801f51a799a12dee09ac710bf7054307a9366c21b1f2bfe7fcd3c57674bba01`  
		Last Modified: Fri, 18 Jun 2021 00:44:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67ddedacab64bc025f06d68124ec89da46abe5b0d211ff32bb820095df8670a`  
		Last Modified: Fri, 18 Jun 2021 00:43:58 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278c286d75c54ec80f3e24a78b9a6402de83b28604fc4b87dacda0c7b5caa4aa`  
		Last Modified: Fri, 18 Jun 2021 00:43:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbf23426b69c8a18d4741a9a069b848a5b7436e9d41e4df24df831115dea5e7`  
		Last Modified: Fri, 18 Jun 2021 00:44:22 GMT  
		Size: 136.3 MB (136341319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5a46949e24656793e16cf1f9c1d47d92c60f4cab935ab9342eb91c5c65863b`  
		Last Modified: Fri, 18 Jun 2021 00:43:58 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6d415000232a2e128c19dfe3c455e804d8630c0c7fd8b3b7721c7207990482`  
		Last Modified: Fri, 18 Jun 2021 00:43:58 GMT  
		Size: 4.5 KB (4473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; s390x

```console
$ docker pull mongo@sha256:a5af5a74af47d316966ee0bb6487d648c5c4cce6cab32d9ab46d9546d4cc7261
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169487300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c13516915491cb166016e29f7521bc7c46deff5daf50f044b0d06976fdf71b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 17 Jun 2021 23:43:50 GMT
ADD file:cc2ee4aea9fbc14df65175678f3768999a62222c448822b8114b0adc46b28e9d in / 
# Thu, 17 Jun 2021 23:43:52 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:44:15 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 18 Jun 2021 00:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:44:28 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:44:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 18 Jun 2021 00:44:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:44:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Jun 2021 00:44:47 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 18 Jun 2021 00:44:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 18 Jun 2021 00:44:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 18 Jun 2021 00:44:49 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 18 Jun 2021 00:44:49 GMT
ENV MONGO_MAJOR=4.4
# Fri, 18 Jun 2021 00:44:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 18 Jun 2021 00:44:51 GMT
ENV MONGO_VERSION=4.4.6
# Fri, 18 Jun 2021 00:45:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 18 Jun 2021 00:45:53 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 18 Jun 2021 00:45:53 GMT
VOLUME [/data/db /data/configdb]
# Fri, 18 Jun 2021 00:45:53 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:45:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Jun 2021 00:45:54 GMT
EXPOSE 27017
# Fri, 18 Jun 2021 00:45:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:dc8b9e6580673058ca03527c82f177ec46b88568b02a42351a756002bdb90d3d`  
		Last Modified: Thu, 17 Jun 2021 23:45:21 GMT  
		Size: 25.4 MB (25366169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7460b77c0089aa1451f58f3d1cd77c5f7d68310192c9f7d686038b0721bab63c`  
		Last Modified: Fri, 18 Jun 2021 00:46:15 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f541d49e19e2ec42fa54a0cac108206c97af0ecd07e423a9e2cecf87c01a8bae`  
		Last Modified: Fri, 18 Jun 2021 00:46:15 GMT  
		Size: 2.7 MB (2708497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61822a88f708bb3dee2da3d16368f16d25c1cfd75b410a04a7061ed0b1ed404`  
		Last Modified: Fri, 18 Jun 2021 00:46:15 GMT  
		Size: 5.7 MB (5747572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0e9e457b7fab51b14df829de92c0451508732cc0904ffdeb129293baa2b0e3`  
		Last Modified: Fri, 18 Jun 2021 00:46:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e987c8f54588897da84efc66e39c688d7b046ebaa7d86b958b5f6cd613cc4d8b`  
		Last Modified: Fri, 18 Jun 2021 00:46:12 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac283ceec69fca5eea5cc9ef741f8a43aad0d9cb670b3b1605314a1c5f6431d`  
		Last Modified: Fri, 18 Jun 2021 00:46:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9b36df257b0eadfb7dacce58a7a9816792bd7a70c7b64eedb4734060d9f235`  
		Last Modified: Fri, 18 Jun 2021 00:46:31 GMT  
		Size: 135.7 MB (135656727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3bf0d468f33c5b4966728462c022f6d6b84a2db435ea842367e0b7f71d93e`  
		Last Modified: Fri, 18 Jun 2021 00:46:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32815d0b30f013b431c0ab482290c78ab64b8d5f517d91ffe60e575e4c1feed4`  
		Last Modified: Fri, 18 Jun 2021 00:46:12 GMT  
		Size: 4.5 KB (4473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
