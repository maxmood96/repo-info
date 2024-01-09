## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:635bd7db1921f7ede76d4a8ba9c16e37cbdf6cb895a1350b82fb9fa8ebfa5f47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:705a3fdde24a5f86a2bd7306089f3d6afa9a59bfe16898ca74f9c4d2a31b74ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260098362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e325fe350a8c10ce4361f16a48f9219358f18dcfd88d613a9f683bf82ccbed23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV GOSU_VERSION=1.16
# Sat, 06 Jan 2024 05:07:23 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_MAJOR=7.0
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_VERSION=7.0.5
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
VOLUME [/data/db /data/configdb]
# Sat, 06 Jan 2024 05:07:23 GMT
ENV HOME=/data/db
# Sat, 06 Jan 2024 05:07:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jan 2024 05:07:23 GMT
EXPOSE map[27017/tcp:{}]
# Sat, 06 Jan 2024 05:07:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a486411936734b0d1d201c8a0ed8e9d449a64d5033fdc33411ec95bc26460efb`  
		Last Modified: Tue, 12 Dec 2023 11:55:25 GMT  
		Size: 29.5 MB (29547485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf348a38ee3764a123bf0477630d012e13073afe4aedd026bb5d64952bf835f`  
		Last Modified: Tue, 09 Jan 2024 00:55:02 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa8507b7d7629c948643943bc8e652f1dd750b995652791abf7f9439d88af46`  
		Last Modified: Tue, 09 Jan 2024 00:55:03 GMT  
		Size: 5.0 MB (5049470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841ef8d499cd76e2eeba092a22d46b0f720fe2447e6babb438f0e03b3b0bc8fb`  
		Last Modified: Tue, 09 Jan 2024 00:55:03 GMT  
		Size: 1.1 MB (1100996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97788ce9e1a0e1bf098ad21d4d80479e30fc1b26733ee042a48da4d722bee9b7`  
		Last Modified: Tue, 09 Jan 2024 00:55:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194a4afa48556ffe207b8f42f7ae3dfe3e3a297385056bdeed1d23e693506883`  
		Last Modified: Tue, 09 Jan 2024 00:55:03 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becfac27bfec68d62f2788257f550e310f63882f591bdaf54e4ac3a53088b1fa`  
		Last Modified: Tue, 09 Jan 2024 00:55:03 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d2c40642ff820b758d7dcf165f8fe4876601656a6d99fe47476ce04532ce87`  
		Last Modified: Tue, 09 Jan 2024 00:55:10 GMT  
		Size: 224.4 MB (224391840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1634c5425c0432caaf5f3a24247490800eb360f1151b94343856f6761cf0c6cc`  
		Last Modified: Tue, 09 Jan 2024 00:55:04 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:872bebbd347613e0961d2500c12344f8cd6f80beacf32684d648c4e456e38806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5413157016effd15ed2ed061fed80db91d2d7edd84c83a9d1ecbe492e0ba1f5d`

```dockerfile
```

-	Layers:
	-	`sha256:e5bde17fbc2955d4fb6069d15730df158a9cf105c8caab704a6d2f3984500649`  
		Last Modified: Tue, 09 Jan 2024 00:55:02 GMT  
		Size: 2.7 MB (2728666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7361227254d6714da2874c9ae82ae16c728f708121e67e61ad7127ea364c76fa`  
		Last Modified: Tue, 09 Jan 2024 00:55:02 GMT  
		Size: 29.5 KB (29526 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:e10095c9dd9e608d3b90ecb223beb283683e95d47e56ad462342216ea9ce47f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251974069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19244b26d023a78d4d43d4fa2de9ed1f53b2968f90e06a79fd4755ca9a00b72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV GOSU_VERSION=1.16
# Sat, 06 Jan 2024 05:07:23 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_MAJOR=7.0
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_VERSION=7.0.5
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
VOLUME [/data/db /data/configdb]
# Sat, 06 Jan 2024 05:07:23 GMT
ENV HOME=/data/db
# Sat, 06 Jan 2024 05:07:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jan 2024 05:07:23 GMT
EXPOSE map[27017/tcp:{}]
# Sat, 06 Jan 2024 05:07:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:005e2837585d0b391170fd9faf2e0c279d64ba0eb011cda8dedf28cb5839861e`  
		Last Modified: Tue, 12 Dec 2023 11:55:31 GMT  
		Size: 27.4 MB (27358237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60b3ed21100ca2d890876fbf18f05af88846ecbf268dc5e5a49ce0438d31830`  
		Last Modified: Sat, 16 Dec 2023 21:11:13 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fcf60fea85148cf8db272596d20236398f26e0a280d8cec374de81aa444e97`  
		Last Modified: Sat, 16 Dec 2023 21:11:14 GMT  
		Size: 5.0 MB (4992669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05da3aee34af09b4d42d3f493c4227bc34d568cf8f4b2f78f030e25bf7dd43f7`  
		Last Modified: Wed, 20 Dec 2023 22:07:31 GMT  
		Size: 1.0 MB (1034220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f2bf503f3292952c7caabc35876274ecfcaf7bb99db01a8a0b85769a553daf`  
		Last Modified: Wed, 20 Dec 2023 22:07:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e4d672dd05819ee13c1f7a322f1561438e1546bd44102d683fa47c120195dd`  
		Last Modified: Wed, 20 Dec 2023 22:07:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bc5c1505579051eaf1b474fb0494f6f67210f3a472eae4e81673a680766cd8`  
		Last Modified: Wed, 20 Dec 2023 22:07:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4ad5c1464eb1c1b74b314759565411a2f3dbacb9644c9af562f209847811a2`  
		Last Modified: Tue, 09 Jan 2024 02:13:22 GMT  
		Size: 218.6 MB (218580361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b57f98427ff490fe6848837da214296312fdfaf7d87fdbe8039669032474ec`  
		Last Modified: Tue, 09 Jan 2024 02:13:16 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:4e6a1ee67ae583f7686d9b44776da90f1e141ce702b3204de22fca28eab5b179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac18134d1f2ab386ac8f4e085e3bcac6e6ad69ce95287e84514fac5912f29856`

```dockerfile
```

-	Layers:
	-	`sha256:b9c93581c67997cebd78badb22f97f91646c01e9384d81d459684eb7aa8de940`  
		Last Modified: Tue, 09 Jan 2024 02:13:16 GMT  
		Size: 2.7 MB (2729028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15996bb2c0a4ddea8433a2139818a107336c774ce8758cdac609de294c7d30b2`  
		Last Modified: Tue, 09 Jan 2024 02:13:16 GMT  
		Size: 29.4 KB (29383 bytes)  
		MIME: application/vnd.in-toto+json
