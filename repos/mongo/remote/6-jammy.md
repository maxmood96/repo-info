## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:2187ce220e3c40f6f3ca8c2f690a4906531e2913b60191be93b0d5f6ea3c371d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:c919e27692c1a0b9190089793012d1519ee45136a6a9650fc760cd98bee7e7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262340283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798c9b5c82b54c4c571a181323225c5a37e2663c317e9846ad16aa5516c2f970`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Tue, 29 Apr 2025 22:01:13 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 29 Apr 2025 22:01:13 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 29 Apr 2025 22:01:13 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 29 Apr 2025 22:01:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 29 Apr 2025 22:01:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 29 Apr 2025 22:01:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 29 Apr 2025 22:01:13 GMT
ENV MONGO_MAJOR=6.0
# Tue, 29 Apr 2025 22:01:13 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
ENV MONGO_VERSION=6.0.23
# Tue, 29 Apr 2025 22:01:13 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
VOLUME [/data/db /data/configdb]
# Tue, 29 Apr 2025 22:01:13 GMT
ENV HOME=/data/db
# Tue, 29 Apr 2025 22:01:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Apr 2025 22:01:13 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Apr 2025 22:01:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2073f89ae4caf8103f174f7fd19263944ec917b7a03ea9f99d494012ae67cd5`  
		Last Modified: Thu, 08 May 2025 17:04:37 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ee3b71c0eb20af15aaf0af1052b3e60df48348108253d00f976391f110017`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 1.5 MB (1513421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dfe4517ae9cfa8ed4d20e515203156fbd65f0e817ed26d4e2602fcd5d36283`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 1.1 MB (1095309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b4a1e8b877ee31123ff28981b9faaaee4552ded939e843c599920acc0295af`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8e956554f2a529bbda897109455bafdb3bd2d64ea17e55dd55867aeede5cb8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007fd3d08b1b167b6262e74d5a0fa53fa2aae8c42770e1e779341abb8f9efc31`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 230.2 MB (230191770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f7cd07b86a5c7640936a063107fa33e4967d62280d34d24db15b0c1cc74333`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:2ec713f5cf6c131d404fc8fa89f1dbe43bb6db6bee064e7f050d508530a0cb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3104539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e998510b3fe101ecdd39dcd6b8fd3dc6c79a9e7f94b203cd031d8187f343d597`

```dockerfile
```

-	Layers:
	-	`sha256:40db9f22ef070229039d1b368ccbba9f4b3a414a21ae85bbc00c3252e8f2faae`  
		Last Modified: Thu, 08 May 2025 17:11:03 GMT  
		Size: 3.1 MB (3076548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc66bf418ae92c76c9c6a7988f5875707a6005ec3bdbb6b12f1febf40762cc1f`  
		Last Modified: Thu, 08 May 2025 17:11:03 GMT  
		Size: 28.0 KB (27991 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:44ce393e28d0963b8d6fb7b67317d1a25c5a61fa16e4a5d39183626c1632185d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251292597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee5a100c5ab6731c31cdebe16d79d721f643c40b91ff2bafcca53c336f66533`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Tue, 29 Apr 2025 22:01:13 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 29 Apr 2025 22:01:13 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 29 Apr 2025 22:01:13 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 29 Apr 2025 22:01:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 29 Apr 2025 22:01:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 29 Apr 2025 22:01:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 29 Apr 2025 22:01:13 GMT
ENV MONGO_MAJOR=6.0
# Tue, 29 Apr 2025 22:01:13 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
ENV MONGO_VERSION=6.0.23
# Tue, 29 Apr 2025 22:01:13 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
VOLUME [/data/db /data/configdb]
# Tue, 29 Apr 2025 22:01:13 GMT
ENV HOME=/data/db
# Tue, 29 Apr 2025 22:01:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Apr 2025 22:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Apr 2025 22:01:13 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Apr 2025 22:01:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce56f0a8011ca6c11085efac0813204aa8e0b30940d28e473e44a10385190b2`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0887a6579a8ccf54ca39415d519174f0fec60b92d231d92f3d2018b22b2bd30`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 1.5 MB (1481677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e8b1332d082508fee41f60ab90894be980760533c538ee381d885b0d8dd899`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 1.0 MB (1027719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8183faf24da4f21257961db76d3d9e5444d61bcda13d01626dba25807b3e48e`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8ad90da2e4c2c07382ed632883b26fdd9de8abbc73abb15bfde07193aa5703`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8c28534d3f11f52ca1f149b5095eb706ee010c6c85409e7ed52bc3e7c1498f`  
		Last Modified: Thu, 08 May 2025 17:13:37 GMT  
		Size: 221.4 MB (221421821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674cc0436da5a148daf0a20c215b4e2911b7fe18bbdba9925572caf0de5abaf3`  
		Last Modified: Thu, 08 May 2025 17:06:35 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:6699af34f7f7e611357b7846da07b6b479edebd24cf5fba19b61a6931d743c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3105059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a046cbfbe3b1c88f40015bdbdd5f6edcb6c92e20bdb8514be8a31224165933`

```dockerfile
```

-	Layers:
	-	`sha256:d1670c06b0419f9d04245000c3d44bc3ee61044c8a780705501cf9c8abcde1a8`  
		Last Modified: Thu, 08 May 2025 17:11:23 GMT  
		Size: 3.1 MB (3076867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9fea5e7aa6269096cf0395ba0b7da6b9f3e015b4e177913ecc709c58742bdf`  
		Last Modified: Thu, 08 May 2025 17:11:22 GMT  
		Size: 28.2 KB (28192 bytes)  
		MIME: application/vnd.in-toto+json
