## `mongo:jammy`

```console
$ docker pull mongo@sha256:5981ec7a4516497be916e58731c3d6675e2dd8921dee902fd6151e9249735fcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:7c7527b6cd8036e42318ce3b7db239fe975cdf31116c210b81b3579b73aa8c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258858644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576225b73f775759893e4ae91c3f02426d272b1155d9102303d198419b08ca20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 26 Aug 2024 16:01:29 GMT
ARG RELEASE
# Mon, 26 Aug 2024 16:01:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 26 Aug 2024 16:01:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 26 Aug 2024 16:01:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 26 Aug 2024 16:01:29 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 26 Aug 2024 16:01:29 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENV GOSU_VERSION=1.17
# Mon, 26 Aug 2024 16:01:29 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 26 Aug 2024 16:01:29 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_MAJOR=7.0
# Mon, 26 Aug 2024 16:01:29 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_VERSION=7.0.14
# Mon, 26 Aug 2024 16:01:29 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
VOLUME [/data/db /data/configdb]
# Mon, 26 Aug 2024 16:01:29 GMT
ENV HOME=/data/db
# Mon, 26 Aug 2024 16:01:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 16:01:29 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 26 Aug 2024 16:01:29 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f38bdd817c96307239a577b69e10ebc45ffb5a9a59e82a67eee7ff00238c928`  
		Last Modified: Tue, 17 Sep 2024 00:59:58 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5112d08ff2cfbe5af326624cefb1617d13b05bf3b59eae3359e7c3d1bed13e0`  
		Last Modified: Tue, 17 Sep 2024 00:59:58 GMT  
		Size: 1.5 MB (1500751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c004f25c40ba5cbb3e71bcc48c5a9f4c03bb355190bd98ea2104476462c7e88a`  
		Last Modified: Tue, 17 Sep 2024 00:59:58 GMT  
		Size: 1.1 MB (1094622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd951bc2af3888a7a041d4f8e9a7193021860261b631c73567d2715b4df67ea8`  
		Last Modified: Tue, 17 Sep 2024 00:59:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc5073f82e40a91af6372e4d5211fdc2e63b456ca1e7af449d0448634026882`  
		Last Modified: Tue, 17 Sep 2024 00:59:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63151b5ff27cc487d2f3fce6f03ee401d1d819cbb1dbf0bb0441944b754296ae`  
		Last Modified: Tue, 17 Sep 2024 01:00:04 GMT  
		Size: 226.7 MB (226720428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f006e63bfa2e77aa526e752290224b86f87333146dd073d9b56d92600a855c3f`  
		Last Modified: Tue, 17 Sep 2024 00:59:59 GMT  
		Size: 5.0 KB (4993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:8b7669d62306878bb48079c7a4dc2d98d01124f3b0f51966167d2d7e4bbac8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba544253209551632a31e4048d2b00181fa3749a591e9ea205d2628e433b038d`

```dockerfile
```

-	Layers:
	-	`sha256:4c5740f763f37f966ed7cf2498f9cc63807e5fb798ec94114552248027a4e854`  
		Last Modified: Tue, 17 Sep 2024 00:59:58 GMT  
		Size: 3.0 MB (3029337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c16fcf13b34d94174983e93a7fd78826de0a62c83a8aaaacddacc31dba8844e`  
		Last Modified: Tue, 17 Sep 2024 00:59:58 GMT  
		Size: 27.6 KB (27636 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4bf7ab82685a24504de4999e1ee560fcb560c4c59d42cb8cc79a63d360c210a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247523765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a402f23432b257c75b957786898ae02c7ffeeabaebfd4c0070c98dd9da3bd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 26 Aug 2024 16:01:29 GMT
ARG RELEASE
# Mon, 26 Aug 2024 16:01:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 26 Aug 2024 16:01:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 26 Aug 2024 16:01:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 26 Aug 2024 16:01:29 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 26 Aug 2024 16:01:29 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENV GOSU_VERSION=1.17
# Mon, 26 Aug 2024 16:01:29 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 26 Aug 2024 16:01:29 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_MAJOR=7.0
# Mon, 26 Aug 2024 16:01:29 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_VERSION=7.0.14
# Mon, 26 Aug 2024 16:01:29 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
VOLUME [/data/db /data/configdb]
# Mon, 26 Aug 2024 16:01:29 GMT
ENV HOME=/data/db
# Mon, 26 Aug 2024 16:01:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 16:01:29 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 26 Aug 2024 16:01:29 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d432f7e11fc48086f6b23b461b4268a559c6a802b1326ca3e5c5647993d6e1`  
		Last Modified: Tue, 17 Sep 2024 02:33:38 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef31e5dc901efbe6078de6e56ff381ffa14fd1001fd17df4de4e60c30d86891`  
		Last Modified: Tue, 17 Sep 2024 02:33:39 GMT  
		Size: 1.5 MB (1465829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482193604834afcf9eac46076f1cfffbfe9e11524480589dcc8c2f03f1010f5d`  
		Last Modified: Tue, 17 Sep 2024 02:33:39 GMT  
		Size: 1.0 MB (1027368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adedfd320f36d78c2ff8bbb54b63b96c40777891887f4da96f3bb95e66b515a7`  
		Last Modified: Tue, 17 Sep 2024 02:33:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c81ea1edc6a97903e277f3d0ab425a36aa0f7f969ae4d254b55117cca3336b`  
		Last Modified: Tue, 17 Sep 2024 02:33:39 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce773afd67038ecdb5b64802f7fbab13ca8f2a9d8326f883f21a5e5338f343`  
		Last Modified: Tue, 17 Sep 2024 02:33:45 GMT  
		Size: 217.7 MB (217665079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7aed8cbdcd654ebd71964afd58a3f4ebee8ab390863c923e3083775e41a20f`  
		Last Modified: Tue, 17 Sep 2024 02:33:40 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:7af021ff1d43e6d72786a6536649e56f0a87ba5a8959d5f167598b879f65d75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1fdf1f1a7729b9b4552a247839e22e0703acc99f8967a68622967b8f3490b1`

```dockerfile
```

-	Layers:
	-	`sha256:9c02f2915b8d5b7477c147ddadd92add998afaf08afd346dfb89d60ec8cbbb26`  
		Last Modified: Tue, 17 Sep 2024 02:33:39 GMT  
		Size: 3.0 MB (3029679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76e3a7bf5f828d87f4465abdc6f61ce714fa6e9b7d171662d752da729a62f903`  
		Last Modified: Tue, 17 Sep 2024 02:33:38 GMT  
		Size: 28.0 KB (27985 bytes)  
		MIME: application/vnd.in-toto+json
