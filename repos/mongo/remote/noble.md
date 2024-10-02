## `mongo:noble`

```console
$ docker pull mongo@sha256:c88144ecdf9886142ecfcb669eb6ed23294e3ec99ec3e097849b76b432b8f40a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:b07755058fd9ee3478bdef0a2614e51f7b73a91c85e221233444456e4ad9671e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274325363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72576a3db0329e0a60aae2259e2c9e26aff5ee3296a43100cb77e53062fae2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENV GOSU_VERSION=1.17
# Wed, 18 Sep 2024 22:02:51 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 18 Sep 2024 22:02:51 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_MAJOR=8.0
# Wed, 18 Sep 2024 22:02:51 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_VERSION=8.0.0
# Wed, 18 Sep 2024 22:02:51 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
VOLUME [/data/db /data/configdb]
# Wed, 18 Sep 2024 22:02:51 GMT
ENV HOME=/data/db
# Wed, 18 Sep 2024 22:02:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 22:02:51 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 18 Sep 2024 22:02:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2843f0424c9344edf24ab2b082e0db21487318b0ae337a6454823b3dcc7ec002`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a7a845331184c79fd0b6c2e978d9d9211da333f5cb9a85c280f4a7669a87c`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 1.8 MB (1819214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923fbc5d75e9896b4dde2dc1a6da962d656f88966bb945925dc1df1881fa39a5`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 1.1 MB (1129336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c9b75dcd29b36886e7bced4e2ec1122a4025f7c7ce3688b4606d9508a26e77`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3df91fefa244f2b7c08700a1864a6f84a5349164a9bed97b52128807ecb3f2`  
		Last Modified: Wed, 02 Oct 2024 01:58:54 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d7cdcf0d099dc078c04879f432e3ae704bfecad9e19f02a70b9227cb371216`  
		Last Modified: Wed, 02 Oct 2024 01:58:58 GMT  
		Size: 241.6 MB (241620364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26443d53f1837b2e304d0e1a22296d172190a44f4979bf2fb18e4a7dd849395f`  
		Last Modified: Wed, 02 Oct 2024 01:58:54 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:0462ccb311c105b57b1f038d62694ea681d76a28b407441a910a8681c32b6f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b0f9f9b733ffe95652e2c9f908484bbcc686cda9c42ac3f719924f172b786f`

```dockerfile
```

-	Layers:
	-	`sha256:10d2c2a1b23757434b4525efadbcdb6eac00b1a2f97142f3d5f2545995fe632e`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 2.5 MB (2480732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b59d9e314bcef24b14104fffec77b700563d83ea83e506581f022c5a26323745`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 27.6 KB (27632 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:52e508452e28dda823edd4568c372db3ed1c8d16f1351c539ca6accf18f7dc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265492241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2a1ab98ab14272d2a41e5d01a52a4fa849918b87aa382d0bda9a5b202e9d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENV GOSU_VERSION=1.17
# Wed, 18 Sep 2024 22:02:51 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 18 Sep 2024 22:02:51 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_MAJOR=8.0
# Wed, 18 Sep 2024 22:02:51 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_VERSION=8.0.0
# Wed, 18 Sep 2024 22:02:51 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
VOLUME [/data/db /data/configdb]
# Wed, 18 Sep 2024 22:02:51 GMT
ENV HOME=/data/db
# Wed, 18 Sep 2024 22:02:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 22:02:51 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 18 Sep 2024 22:02:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2163a8c5557b09c2a6a3d0acbf966c6e0c6a3a4808dad90d79c56be277bc5f`  
		Last Modified: Tue, 17 Sep 2024 02:31:38 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e00d6a0366086c03c90bba6170ac7dc7eaf856077c07b55ae99992551d7c71`  
		Last Modified: Tue, 17 Sep 2024 02:31:39 GMT  
		Size: 3.7 MB (3705250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6188151c6d05f8e194cc2a4f492d505250057a8694ec059e1d7df5f62548df57`  
		Last Modified: Thu, 19 Sep 2024 19:06:12 GMT  
		Size: 1.1 MB (1059571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dc4a887e4bb0eeeb957dcfd25c42c3f4224e44d1b028d2ab81d0acd20bbd2c`  
		Last Modified: Thu, 19 Sep 2024 19:06:12 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dcd2d7d2b1c8b061147ee9c2f984270209aa8766c71cbbcf93f557cb168d2c`  
		Last Modified: Thu, 19 Sep 2024 19:06:12 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df8a6b714b3d664bb83e698a07f8849512ac1ae6da633a5e9539af547144305`  
		Last Modified: Thu, 19 Sep 2024 19:06:17 GMT  
		Size: 231.8 MB (231835232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71e6ea971f719c646fe58ef7532e050756b4ca9d33f745e3014af5bcee1867a`  
		Last Modified: Thu, 19 Sep 2024 19:06:13 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:84027666dc413105f3fdebc18f402a013a00621ceea99085b6115d94e8ba3c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9de7ebdb6185f4d7522b25713e43daa1b4ce8f23308d7cbbb40cd472b5a8e7e`

```dockerfile
```

-	Layers:
	-	`sha256:ff0b87a4d8b9b9f6f0c5fec49512eff8cc00a446aaf973ee5e1d2931f1627cae`  
		Last Modified: Thu, 19 Sep 2024 19:06:12 GMT  
		Size: 2.5 MB (2481228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:709ed14c5423246f3c81f4052c8fd34799909a814dca6597d10b32fffc0df7e6`  
		Last Modified: Thu, 19 Sep 2024 19:06:12 GMT  
		Size: 28.0 KB (27976 bytes)  
		MIME: application/vnd.in-toto+json
