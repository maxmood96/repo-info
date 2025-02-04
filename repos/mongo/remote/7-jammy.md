## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:203e614e0b8388b6df80441c8ea9bd987bf508c5e361ec58b0d1afa5e2aefc43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:a3ba70fe8da14d155e158245fc89a9dd6adf92ae34976ebce24464a3c1573c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270222005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba5780f2781c48a7d8229550a8f77d57d67cecdc6b5859ad1cc6d8a0abc4a3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Dec 2024 23:06:36 GMT
ARG RELEASE
# Fri, 20 Dec 2024 23:06:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 23:06:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 23:06:36 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Dec 2024 23:06:36 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 20 Dec 2024 23:06:36 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENV GOSU_VERSION=1.17
# Fri, 20 Dec 2024 23:06:36 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 20 Dec 2024 23:06:36 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 20 Dec 2024 23:06:36 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_MAJOR=7.0
# Fri, 20 Dec 2024 23:06:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_VERSION=7.0.16
# Fri, 20 Dec 2024 23:06:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
VOLUME [/data/db /data/configdb]
# Fri, 20 Dec 2024 23:06:36 GMT
ENV HOME=/data/db
# Fri, 20 Dec 2024 23:06:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2024 23:06:36 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 20 Dec 2024 23:06:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc10604355c8d4592453d9f7de47831df482ecfa749076b56f43e0ae5fee52d`  
		Last Modified: Tue, 04 Feb 2025 04:25:52 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96efcbef81ea7762023510e96aabb4575f8970309e50e53f777005bb14d6d24f`  
		Last Modified: Tue, 04 Feb 2025 04:25:52 GMT  
		Size: 1.5 MB (1513272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fe8a8c4619eadaeae44fc144b28b368bce9625eeaf78c2eaf1e976f296da73`  
		Last Modified: Tue, 04 Feb 2025 04:25:53 GMT  
		Size: 1.1 MB (1095053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce7aaa046eeae8acaa1058fa7d32c5511f2295cb531b288f9804f95e0131616`  
		Last Modified: Tue, 04 Feb 2025 04:25:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd932e33dad7fa54ce655282a802c2051eb1e4e7f1c4a123d06862bf258f493`  
		Last Modified: Tue, 04 Feb 2025 04:25:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78813a729457761891af33dad9075a400d45e15a818a1d45e0345666c6080e1c`  
		Last Modified: Tue, 04 Feb 2025 04:25:59 GMT  
		Size: 238.1 MB (238070578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3c0e28664827fec39a08b95c6eab17da3dd52c64f8bb8352047da7f8546b7`  
		Last Modified: Tue, 04 Feb 2025 04:25:54 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:baee6d99346121b86ea87b44eae4df142648cc6118239d892e3cee9f2a159bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30a25c0e4cd35deeceac062d75a659beb0f197e03bba93ef15dc441cfe5d889`

```dockerfile
```

-	Layers:
	-	`sha256:32c51368f238e42366a0dc6424b5ceb7138c408a0edc2507e3edb640a4ebbbbd`  
		Last Modified: Tue, 04 Feb 2025 04:25:53 GMT  
		Size: 3.1 MB (3072196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713b382099089c3e792b49a3728d6a4a917135512b3dd6f2c4f43ac6f152bede`  
		Last Modified: Tue, 04 Feb 2025 04:25:52 GMT  
		Size: 28.0 KB (27991 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:3906d768163309d7282f80769b43a2b43d271ca98cdef484908df15b74b71f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247338378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082b79b5037cec2fa8ae4e2c4a09b749c47efdc01e274f7bed661a37d2ce787f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENV GOSU_VERSION=1.17
# Fri, 20 Dec 2024 23:06:36 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 20 Dec 2024 23:06:36 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 20 Dec 2024 23:06:36 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_MAJOR=7.0
# Fri, 20 Dec 2024 23:06:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_VERSION=7.0.16
# Fri, 20 Dec 2024 23:06:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
VOLUME [/data/db /data/configdb]
# Fri, 20 Dec 2024 23:06:36 GMT
ENV HOME=/data/db
# Fri, 20 Dec 2024 23:06:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2024 23:06:36 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 20 Dec 2024 23:06:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe71bf4de30ded530999b7bd82283cde3eb0ae8df19cef680273f3c6a553ff5`  
		Last Modified: Wed, 11 Dec 2024 21:36:18 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4a3559a03510d1db0f081c6c5cf8381a2dd6d06b4cfbd6ea87b98e552113a8`  
		Last Modified: Wed, 11 Dec 2024 21:36:18 GMT  
		Size: 1.5 MB (1481430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90ee5f3f39c5784babc660d7b481cf1e0f9175f09dd816bf1efada803828486`  
		Last Modified: Mon, 23 Dec 2024 17:28:44 GMT  
		Size: 1.0 MB (1027429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe1a0c20f49a59cb96ed1fb8cf12b66fa2a3dd4aeef0de977041276fce31dc`  
		Last Modified: Mon, 23 Dec 2024 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c521ffbbdc2ad589fafceec435247fef38e035d6562a24ce41b3269992816`  
		Last Modified: Mon, 23 Dec 2024 17:28:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd63593da07889a8fd0e054c37e74feeff4502a76e63ea543e34a083eb28ab5`  
		Last Modified: Mon, 23 Dec 2024 17:28:50 GMT  
		Size: 217.5 MB (217464021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68355a08d73353217626fe4f6722b8d51b0c2ac483f6efa43af9548cb5a992b`  
		Last Modified: Mon, 23 Dec 2024 17:28:45 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:33ebcfa424d3c5c06af601138b5db13bcbf4737e7c4936690b4286606390fbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da79e330a8abeb12906e235206ac052f9cd7cd9728d08028707664b7e93400e9`

```dockerfile
```

-	Layers:
	-	`sha256:aea94392cde32eb50e822709889bf48143202f706403ddd7408aa06ee231d7ef`  
		Last Modified: Mon, 23 Dec 2024 17:28:45 GMT  
		Size: 3.0 MB (3049590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af120660e43334504d95a774121b03fcc5dd882cf2666c31ea33286f659f1731`  
		Last Modified: Mon, 23 Dec 2024 17:28:44 GMT  
		Size: 28.2 KB (28194 bytes)  
		MIME: application/vnd.in-toto+json
