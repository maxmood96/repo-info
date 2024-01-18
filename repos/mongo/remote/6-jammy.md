## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:c771483ddf7421e3fa60eda070ff0aa446db54b230530b0b3c6a5352ee902586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:06f71fd91888bdbeb4a288a6e81199385a88779c148a138c958d2f87785dd958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247636928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68283042fe990ea165e81d03a30dfe539fb48a090660cfe7e5b9c4266073dbb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 19 Dec 2023 19:08:50 GMT
ARG RELEASE
# Tue, 19 Dec 2023 19:08:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 19:08:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 19:08:50 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 19:08:50 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Tue, 19 Dec 2023 19:08:50 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV GOSU_VERSION=1.16
# Tue, 19 Dec 2023 19:08:50 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_MAJOR=6.0
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_VERSION=6.0.12
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
VOLUME [/data/db /data/configdb]
# Tue, 19 Dec 2023 19:08:50 GMT
ENV HOME=/data/db
# Tue, 19 Dec 2023 19:08:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 19:08:50 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 19 Dec 2023 19:08:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:29202e855b2021a2d7f92800619ed5f5e8ac402e267cfbb3d29a791feb13c1ee`  
		Last Modified: Thu, 11 Jan 2024 17:48:58 GMT  
		Size: 29.5 MB (29546295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdd825354e883a90a47c15b948118cc341596bdd51f71c94c2b7ea8e1652c7`  
		Last Modified: Wed, 17 Jan 2024 03:48:49 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce60d5e9abd47b5ebc32307564be20ed0df6b7678caac9a91569e65d9ca582c4`  
		Last Modified: Wed, 17 Jan 2024 03:48:49 GMT  
		Size: 5.0 MB (5049467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc08aafe5d71fc1337afa96203a59f9d5ab03fc1bc9b4ca0032b27d4fafddc63`  
		Last Modified: Wed, 17 Jan 2024 03:48:49 GMT  
		Size: 1.1 MB (1101004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c1362eef20689baca8b21e8b3774063bd2942db5ca794676d123c4243bc95c`  
		Last Modified: Wed, 17 Jan 2024 03:48:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de56dc19eb68bcb2b0dffdf597d410c243b63a4eced489ec3a29d054a7441cb`  
		Last Modified: Wed, 17 Jan 2024 03:48:49 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8b9dc65255f44626861d92bebce4930aa99e72ad9fc98adcbdc302f870b635`  
		Last Modified: Wed, 17 Jan 2024 03:48:50 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c96fd4a8647d572a6b7d43b22f9f9e46e25330cd96ede652b5e721af0e6b318`  
		Last Modified: Wed, 17 Jan 2024 03:48:54 GMT  
		Size: 211.9 MB (211931603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f139fcb00c83c555129e433bd43ceb2b4aefbe039cc260186d5245aa8cbb288`  
		Last Modified: Wed, 17 Jan 2024 03:48:50 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:f9a575edfbae5a14204f85e7389456d0ec48c387180950b6507e23a9463ce8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f923a24c7b3d40dfe6ceba28efc960342df78b4b9dd58edcf7511b7208cd5fd`

```dockerfile
```

-	Layers:
	-	`sha256:1f938421055c7f422f89aa7190656b30423aa32906e792576beabedeb4cbf3ea`  
		Last Modified: Wed, 17 Jan 2024 03:48:49 GMT  
		Size: 2.7 MB (2728601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:533499576d483cdcc716747df50a1d467da1e912d6ea2c142a52ddba0d0a6a1c`  
		Last Modified: Wed, 17 Jan 2024 03:48:49 GMT  
		Size: 28.9 KB (28941 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a52300244681ad47845725d990faffcc1d366e6112863bf9232214ab36dda7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240486239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aa5909ffc7a70ce800fbb2c8b573fb6399adef9cc714334fbd2bdf5ff2e511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 19 Dec 2023 19:08:50 GMT
ARG RELEASE
# Tue, 19 Dec 2023 19:08:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 19:08:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 19:08:50 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 19:08:50 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Tue, 19 Dec 2023 19:08:50 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV GOSU_VERSION=1.16
# Tue, 19 Dec 2023 19:08:50 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_MAJOR=6.0
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_VERSION=6.0.12
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
VOLUME [/data/db /data/configdb]
# Tue, 19 Dec 2023 19:08:50 GMT
ENV HOME=/data/db
# Tue, 19 Dec 2023 19:08:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 19:08:50 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 19 Dec 2023 19:08:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ce9ebea987c26664d067f7e14c93231c6d303e4acb322f15ddbf05b414646d64`  
		Last Modified: Thu, 11 Jan 2024 17:49:04 GMT  
		Size: 27.4 MB (27356849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff83b454cc4ba45c11a9ab7b50b075c4ebb4cdd441d079c096276cdf568b53`  
		Last Modified: Thu, 18 Jan 2024 17:29:34 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c80cbb3b35f304679783e06b6220e9620dba964cb97800f786ef04696945`  
		Last Modified: Thu, 18 Jan 2024 17:29:35 GMT  
		Size: 5.0 MB (4990764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6467c6c2b6cab5d20978a2a487a45c7addfcb07b71b83ef5eb096bee090becfb`  
		Last Modified: Thu, 18 Jan 2024 17:29:35 GMT  
		Size: 1.0 MB (1032939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46127fbd2d5e71bd51881fac2905f1e939d37284cc95e56fb886e09eed183ecf`  
		Last Modified: Thu, 18 Jan 2024 17:29:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3afdd67851025f57ef71b217c98522506ec95f1473cec4bc413a96f8a877bd73`  
		Last Modified: Thu, 18 Jan 2024 17:30:24 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171bc05d9a33e2528feda774c41d574aed1898ed95f201e378000f666a32de07`  
		Last Modified: Thu, 18 Jan 2024 17:30:24 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15ed16e186ef5b1e210f0bdac3c31a6d33bd22e6b68a326d09414fe162a63c`  
		Last Modified: Thu, 18 Jan 2024 17:30:30 GMT  
		Size: 207.1 MB (207097119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67827aee8c43d470bfe99aa46471ad32ea7dca9972bd52877ac8a4bb61868b23`  
		Last Modified: Thu, 18 Jan 2024 17:30:25 GMT  
		Size: 5.0 KB (4991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:9de043b81425ad55b809d311e9293aba1768e5d016c84e4794bd6628cb1f8a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2757752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6b820793efd16e08e0b280847e24fdd059c180ad6299af289ab5740c0f5a3f`

```dockerfile
```

-	Layers:
	-	`sha256:35dadbd183bdf6fc0250bce2e97a1e5341c46c9c9c349cba94eb8bd5e9137b6f`  
		Last Modified: Thu, 18 Jan 2024 17:30:25 GMT  
		Size: 2.7 MB (2728959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:657296553afa796e0f87b08958fa6adf11fa85c6b5e0991b4c94420d14c104f4`  
		Last Modified: Thu, 18 Jan 2024 17:30:24 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json
