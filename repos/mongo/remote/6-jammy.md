## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:b157351c5213e50c71631cd8178e402b554535f6c664036eea4146cd55d34cd2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:b5489f93d5b80459a1ef03e23e5221c48e0bf8634ae69db9971721fc76329f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246832611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa646ba4202689bd6d399dbfca422c62bb890d439cbebe34079609e2ced4b80c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 22:11:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Aug 2024 22:11:36 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 21 Aug 2024 22:11:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 21 Aug 2024 22:11:36 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 21 Aug 2024 22:11:36 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 21 Aug 2024 22:11:36 GMT
ENV MONGO_MAJOR=6.0
# Wed, 21 Aug 2024 22:11:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
ENV MONGO_VERSION=6.0.17
# Wed, 21 Aug 2024 22:11:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
VOLUME [/data/db /data/configdb]
# Wed, 21 Aug 2024 22:11:36 GMT
ENV HOME=/data/db
# Wed, 21 Aug 2024 22:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Aug 2024 22:11:36 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 21 Aug 2024 22:11:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366ee75467e2eb0f95a1cee7da1d5ea4cd2b48ccdcd795355b5cc3e5d744a1b4`  
		Last Modified: Thu, 22 Aug 2024 00:55:47 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcee8979618b8b10989c4dabc156a3fb0e0ec663a484ae74b404bec7b7b0d859`  
		Last Modified: Thu, 22 Aug 2024 00:55:47 GMT  
		Size: 1.5 MB (1500906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17989fcadad4fa2ac70c03ea3d67479b3357530c9a3d7e919d5639f3b75c8aa`  
		Last Modified: Thu, 22 Aug 2024 00:55:47 GMT  
		Size: 1.1 MB (1094812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eb210752239e97f592ba8d65fa429d7d9417c7effddc3db54c59403832071f`  
		Last Modified: Thu, 22 Aug 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259765460ae5b1254f742a05a1aa1719c387c0b9c6cc8a8d9688315c4764af8a`  
		Last Modified: Thu, 22 Aug 2024 00:55:48 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd3b4fe943e2ab9392ab6fb7a280ac50bf8b7e57489e5f99cd66d92ff0ec411`  
		Last Modified: Thu, 22 Aug 2024 00:55:51 GMT  
		Size: 214.7 MB (214693710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ec3dcea0902b622a7fdaa74a8827943922048a2256c89e80fc8e8c5fba7a56`  
		Last Modified: Thu, 22 Aug 2024 00:55:48 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:6f582aa1b0f384aaa283eb56cd457df38c388a84b3680cb6d348c7ac62f185bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3055793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc1a73c89b813ddcb00b2e17b97d39d8edd8749f0419a4b400585ec42ea5069`

```dockerfile
```

-	Layers:
	-	`sha256:e1234f6dafe60528a5085b17db695cb247723fe78a856d08d071ea4ff44374e1`  
		Last Modified: Thu, 22 Aug 2024 00:55:47 GMT  
		Size: 3.0 MB (3028747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561fe73be2160005c0c8492d2b6775f3692a97bb722f2fe203cc0632cc34ac32`  
		Last Modified: Thu, 22 Aug 2024 00:55:47 GMT  
		Size: 27.0 KB (27046 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f6a4a7e8de2578ace921d956b6b09048263648158ad2af2d1448244b25607d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236876481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4792be2bd1aeb2715d2d4ec3f44fe7eb962ec7fe89052bd00077211e9d656738`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 22:11:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Aug 2024 22:11:36 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 21 Aug 2024 22:11:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 21 Aug 2024 22:11:36 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 21 Aug 2024 22:11:36 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 21 Aug 2024 22:11:36 GMT
ENV MONGO_MAJOR=6.0
# Wed, 21 Aug 2024 22:11:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
ENV MONGO_VERSION=6.0.17
# Wed, 21 Aug 2024 22:11:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
VOLUME [/data/db /data/configdb]
# Wed, 21 Aug 2024 22:11:36 GMT
ENV HOME=/data/db
# Wed, 21 Aug 2024 22:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Aug 2024 22:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Aug 2024 22:11:36 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 21 Aug 2024 22:11:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5099c6f371c3636e69be7e06e54581f64b8c31de3c79ee2e511aab3b0621b`  
		Last Modified: Sat, 17 Aug 2024 03:19:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b46311ab598f2b54f733e70bf994f009a4d0e96b1ca8244fe0c81dfda8c066`  
		Last Modified: Sat, 17 Aug 2024 03:19:08 GMT  
		Size: 1.5 MB (1465923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96d2188a6e85a3f714752496b0933daa09689e8b9723b520f1392134e7b6e37`  
		Last Modified: Sat, 17 Aug 2024 03:23:13 GMT  
		Size: 1.0 MB (1027491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b08dd7e1ef7258a0763bbced7d2f9aafe9cb2e19e106de39f82f818473f6e78`  
		Last Modified: Sat, 17 Aug 2024 03:23:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f48021e7022d7d6e9e153f98c4a931a22f17d81bb118daa96749a980bb58bb`  
		Last Modified: Sat, 17 Aug 2024 03:23:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1677b9bf9130bb7c342ae6945d32d8687984784bb2533af71159bea71b3b9312`  
		Last Modified: Thu, 22 Aug 2024 00:56:45 GMT  
		Size: 207.0 MB (207017222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1506014cf19f525aea0748ab542bbb178a3c40bfe5021330defcebed712f4487`  
		Last Modified: Thu, 22 Aug 2024 00:56:40 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:6b32fb30dca7d4b0c6dc3c0ec73d3a3e7a7db6ecf9f34bc3272ce087e8b91bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d6d86cb93d4009e8aca63266ada21bd3b33e09d6dc34dcdfc1b17b14380024`

```dockerfile
```

-	Layers:
	-	`sha256:9148c53a6bc8f0320891098f0988e93dd73bde5d1721728edcd029462d661f91`  
		Last Modified: Thu, 22 Aug 2024 00:56:40 GMT  
		Size: 3.0 MB (3029065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913f8c8964bee0f0c56438c9371bf96f01730b0adc40d5a328e17488e246ee9a`  
		Last Modified: Thu, 22 Aug 2024 00:56:40 GMT  
		Size: 27.4 KB (27370 bytes)  
		MIME: application/vnd.in-toto+json
