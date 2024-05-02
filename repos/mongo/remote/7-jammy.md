## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:bcacb598900303183d45d4252981b37cdb43d1c4e8421e1847f82c9d0344aff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:7b88befc893008d7139ce3276c093b3efd435023af8bb76a9d79fa90be1eaeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264736395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff65a94ec485e8c287c5f8c37f4fdb446778b49a93c07ad3c074f5a63d65c1c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 27 Apr 2024 00:09:59 GMT
ARG RELEASE
# Sat, 27 Apr 2024 00:09:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 00:09:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 00:09:59 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 00:09:59 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 00:09:59 GMT
CMD ["/bin/bash"]
# Sat, 27 Apr 2024 00:09:59 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ENV GOSU_VERSION=1.17
# Sat, 27 Apr 2024 00:09:59 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 27 Apr 2024 00:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 27 Apr 2024 00:09:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 27 Apr 2024 00:09:59 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 27 Apr 2024 00:09:59 GMT
ENV MONGO_MAJOR=7.0
# Sat, 27 Apr 2024 00:09:59 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ENV MONGO_VERSION=7.0.9
# Sat, 27 Apr 2024 00:09:59 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
VOLUME [/data/db /data/configdb]
# Sat, 27 Apr 2024 00:09:59 GMT
ENV HOME=/data/db
# Sat, 27 Apr 2024 00:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Apr 2024 00:09:59 GMT
EXPOSE map[27017/tcp:{}]
# Sat, 27 Apr 2024 00:09:59 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f9504c1103be21346fd6e414371588907b9bb28c71db205ec8311b042fbaa`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d18b647343a7a41c871efb02f6b02f6724eee802600da263dbd1d095a6bb37`  
		Last Modified: Thu, 02 May 2024 00:53:03 GMT  
		Size: 1.5 MB (1500683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24f68d810525daa4843b4680a92dded9399ec9fe269602ebb811fbf664cce5a`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 1.1 MB (1094543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df517147e11136e83dadce73e43b9288512a946487d4dbff49793a8e9e03352`  
		Last Modified: Thu, 02 May 2024 00:53:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d5ebe2f2e02233e33f2be8c4cddf803ae019b965d81b1b6be672fa9e52c7b0`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21b89d414fc9157d46db274523cabcaace09b0204a77607750d7118f2ffcd87`  
		Last Modified: Thu, 02 May 2024 00:53:07 GMT  
		Size: 232.6 MB (232600067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4138c7eb3b7136898bd53240fef7e2c908abbda8e2034405bae73f64deaa3d88`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:59e9a0952d2edad92916352d7a4504631bea18dbcf9242ca940de7dbb4777e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c68217397a7c2433dc9113b89c7016ff9fda2a514f4a0576babb619252efeb0`

```dockerfile
```

-	Layers:
	-	`sha256:ecbcc71e0822af72d9bb6f5ee7bf84df91f291efd18008101a78a2b3201867e1`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 3.0 MB (3001085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6fd1ab0b358bd6db6bbcf68f56385afa00234a205f04102393575a1a03f5675`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 27.7 KB (27739 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f89da4ff901b8917f81017fcd2fe30332402c9a9ff13cf31bf491609eaf2868d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256533537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db56901478f716dbcb40317cf5261563bda78d57790f7b103679f7d97af67e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Sat, 27 Apr 2024 00:09:59 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ENV GOSU_VERSION=1.17
# Sat, 27 Apr 2024 00:09:59 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 27 Apr 2024 00:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 27 Apr 2024 00:09:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 27 Apr 2024 00:09:59 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 27 Apr 2024 00:09:59 GMT
ENV MONGO_MAJOR=7.0
# Sat, 27 Apr 2024 00:09:59 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ENV MONGO_VERSION=7.0.9
# Sat, 27 Apr 2024 00:09:59 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
VOLUME [/data/db /data/configdb]
# Sat, 27 Apr 2024 00:09:59 GMT
ENV HOME=/data/db
# Sat, 27 Apr 2024 00:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Apr 2024 00:09:59 GMT
EXPOSE map[27017/tcp:{}]
# Sat, 27 Apr 2024 00:09:59 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ef8879b7897601a39e1de82a5f2c44f77b7ce9c9d504f735a3fcc247197bbbfc`  
		Last Modified: Wed, 17 Apr 2024 18:55:35 GMT  
		Size: 27.4 MB (27360350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac62ef1718e15efb54d5ac717ea8af42daeda72e61bb339d2ad69b803fe1745`  
		Last Modified: Tue, 30 Apr 2024 03:20:55 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1d3f8c0b5f99475ec4d208177a122a3bc4dd6bb85e9d042a73f103c2e48848`  
		Last Modified: Tue, 30 Apr 2024 03:20:56 GMT  
		Size: 1.5 MB (1465894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7dfc40e3b8ca56e38511f8e4d5aecaa6d45057157de4772843e2d9581e64e0`  
		Last Modified: Tue, 30 Apr 2024 04:45:13 GMT  
		Size: 1.0 MB (1027387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0a789799c68189f8e711099536278a60d8e64f8eef275ab4d33b744cf50b7f`  
		Last Modified: Tue, 30 Apr 2024 04:45:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442195f49bfda30ce73e4fc120d62f2e2b9d1b193e79b616960feeda2deeadf1`  
		Last Modified: Tue, 30 Apr 2024 04:45:12 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd254dada9a761962ff1c409409b9f77926985c5f3d2a45fb9a99cf31734c58a`  
		Last Modified: Tue, 30 Apr 2024 04:45:18 GMT  
		Size: 226.7 MB (226672743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341bb4f6c6e55150436a3b3a6637f62cb045664dfeb9b7a71bebe9fc74432986`  
		Last Modified: Tue, 30 Apr 2024 04:45:13 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:003c4edc28796c77bd455bd076a4225bebfb30884ad594d9da01e52f245e44f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d88a1b5f9eba81f013258f769929a366afd6cc9f6743e4eb27368c41bc7259f`

```dockerfile
```

-	Layers:
	-	`sha256:308956f7358efb1016d672c93e1140a9d2b7dba8f88caf9f1989670a94a37d9e`  
		Last Modified: Tue, 30 Apr 2024 04:45:13 GMT  
		Size: 3.0 MB (3001342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4b8190b599de29277811156e4065a61583a410dbb985d8db729788ea3b2cb91`  
		Last Modified: Tue, 30 Apr 2024 04:45:12 GMT  
		Size: 27.6 KB (27596 bytes)  
		MIME: application/vnd.in-toto+json
