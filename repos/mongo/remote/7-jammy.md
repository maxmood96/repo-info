## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:5297d43e6ddb00aa8886ee1348a874c352394be1a886207cbba15806f9544de3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:7a7a75fe26fb1c7ebe0501bb497d70801b199f5d227bfcc5c5570c122ca2f1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (266032175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79058c7d13dd0449da52a4e68087d20db9413d13d67e091809bb97df848453d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 28 Jun 2024 22:05:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_MAJOR=7.0
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 28 Jun 2024 22:05:28 GMT
ENV HOME=/data/db
# Fri, 28 Jun 2024 22:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 22:05:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 28 Jun 2024 22:05:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e0f169ab6736bb57d228c2e76579217aa1445d26783faecb2e28f42537297b`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1561f2bd9c09caf7c29ae4609bb9efb69376378683f0dedd93916eb31cf3e0cb`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 1.5 MB (1500822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3cb06bfe6e0f41e739ea6c09024e2b6cffc182290980d6f8a59a2153e376d8`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 1.1 MB (1094628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3a93b1acbf3ee1fe9f4f4a62d0a2ea730b21322b9295aaf3fb6e9352fbbc78`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf3bf4e558d8be2c37ad2df7f1eefb1f9bd09c7b7dbe10567153f3f377342d`  
		Last Modified: Fri, 28 Jun 2024 23:56:07 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256b619d364b4af1d2336b895154c429aa0c0ee4413df5644003e3e289798d07`  
		Last Modified: Fri, 28 Jun 2024 23:56:10 GMT  
		Size: 233.9 MB (233895810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a32aa02a1619c6f4f427d2905c9461697de82c81695f247c60606626f006658`  
		Last Modified: Fri, 28 Jun 2024 23:56:07 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:b9f758c2e0d017d631aa46462d4c42a58d8ddb07c8802a5cd61c07a60db416c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3030862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8305bdeab66f7dbb68c9195bfb7ae5d3c95b852da00a9c21c03c4524d2018250`

```dockerfile
```

-	Layers:
	-	`sha256:c64cc76784abe4aa39e62356b580bec85e4eb881be8492f6d568c2e44b6d2118`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 3.0 MB (3003226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68f6c7579d53e1bebe091caddc7d5ca26a0adae66f9318bd09a3907526f4a0c`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 27.6 KB (27636 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:3d592fc4805168a80600d0a2300344e4e1bbe2c18226a52d2e2645de777314fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257711695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1f209b12c1d2acfac2c4d063c093a39499e8db44475073cb7ab427b09012d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 28 Jun 2024 22:05:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_MAJOR=7.0
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 28 Jun 2024 22:05:28 GMT
ENV HOME=/data/db
# Fri, 28 Jun 2024 22:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 22:05:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 28 Jun 2024 22:05:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab0f54223e2f06694e8a32dd2a1455a1aad475c9840691a4c63598717de3e79`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a724e63221774b2fcd311f891451a83234f1132255c0cb67f896c6003002374`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 1.5 MB (1467365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901e602b71c88a0922aa0afe1382749fb3c4070e0c79651cac9fe65d6778ad4e`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 1.0 MB (1028915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c63a2c02eae273a52a4d55f6fa7b0d982f706f8f99e71cd69bf99945b6428`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858880bdbb3411d7854f42b9def8ad3f8ff990b580c831a982fb1ba42bb52150`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2386ab574158b740092de2f7a3fa9286ec1111fa7f54cb7661b17516f38ba70`  
		Last Modified: Fri, 28 Jun 2024 23:56:11 GMT  
		Size: 227.8 MB (227846475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c55327c92fc01d00693b43ee151a7b735c7b67149495b6e9cca2dbf13d091c8`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:464a52b01648022052c0b917a7a03c504496029287b7ba963fb1c4287b1089a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3031553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a39d4eb9f91a7bf46e2bb2d3a3c00460fdf6c7189ce0b9e2045366214d68273`

```dockerfile
```

-	Layers:
	-	`sha256:8b00a0877469065b0f5a0266a5d333f8fc6ab0d47e5889be23860bccb215632b`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 3.0 MB (3003568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64bfae95b8bb5944c06f8ccf6dabff2197934b09c61b6929d761c351dc295e05`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 28.0 KB (27985 bytes)  
		MIME: application/vnd.in-toto+json
