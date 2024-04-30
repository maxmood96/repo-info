## `mongo:jammy`

```console
$ docker pull mongo@sha256:9e3e4450fc80e93483c01b89dd39f5e714beaa33882f3cf8076dabfcc11741ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:5d470d7b88a214841e571a13252a401f46c1a32d57de570097705843f5bc8ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264736646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0511af8eb426fabb576dfb4935914da173126610f9d0c753f793c9304b49a25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
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
	-	`sha256:e311a697a4031e52691ab1b5a8c325a448280fef9fc03d89dd97ab40f4245bce`  
		Last Modified: Wed, 17 Apr 2024 18:55:29 GMT  
		Size: 29.5 MB (29534028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23533be8db1770a0d81dd479b6436138ff17c21d42f9999d44b9669ed473f83e`  
		Last Modified: Mon, 29 Apr 2024 23:51:14 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512b6ec10602e5ad0605ae762e852d7f1bcda8b554e99fa6412f1e080a67572f`  
		Last Modified: Mon, 29 Apr 2024 23:51:15 GMT  
		Size: 1.5 MB (1500753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4a5c8a175cc86deb002cc957ff56486bb4eadaf416099fd09bdb1c01e63c1c`  
		Last Modified: Mon, 29 Apr 2024 23:51:15 GMT  
		Size: 1.1 MB (1094600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521a505ca08654a69453f13ab3dcfa1bbc45b14d4d7424dd5143b00ca822b5e`  
		Last Modified: Mon, 29 Apr 2024 23:51:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f78cd9b4f6aa602350a76a66bbd3bba18e14521187579592ba85e6a751519`  
		Last Modified: Mon, 29 Apr 2024 23:51:15 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70aea5e95a16a65e004bfe936288daa2d826cc47237a9a8b8d9c9f1afc2e4d2`  
		Last Modified: Mon, 29 Apr 2024 23:51:22 GMT  
		Size: 232.6 MB (232600108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0373510bb48b08bee75567f333670be96580351b27ac9a9ff59b803b5dff285`  
		Last Modified: Mon, 29 Apr 2024 23:51:16 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:08c012404856ca95e40eafadeb33a4b427793a6188dbe0fc98ad9f0049ddd983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e099e380c8379a207f18d1aa3a0b382191ee38c473c8330ff76f303590ee56af`

```dockerfile
```

-	Layers:
	-	`sha256:35bc79eeaebe35ef2f5b939bd2e4937ffaa3d4764de30c6f75028e1e0892db37`  
		Last Modified: Mon, 29 Apr 2024 23:51:15 GMT  
		Size: 3.0 MB (3001085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cb05595fed16d201b078e55d5cb9da61d3cafce3414ef5c6f655a3d092a9505`  
		Last Modified: Mon, 29 Apr 2024 23:51:14 GMT  
		Size: 27.7 KB (27739 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:jammy` - linux; arm64 variant v8

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

### `mongo:jammy` - unknown; unknown

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
