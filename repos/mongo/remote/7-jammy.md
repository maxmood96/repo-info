## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:64f56934686b90fc071a1170c36f6f08d378ea6932a94e4a7818850fadd9afe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

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

### `mongo:7-jammy` - unknown; unknown

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

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4e6a14311567d04fab842b9df6d2b88b8425362632f262da208c97af167df93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254327899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e108639233377e60500fa1b3fef208e0f65f8e84c3c5bd94f6a0d537e4d762`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 03 Apr 2024 16:02:10 GMT
ARG RELEASE
# Wed, 03 Apr 2024 16:02:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 03 Apr 2024 16:02:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 03 Apr 2024 16:02:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 03 Apr 2024 16:02:10 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 03 Apr 2024 16:02:10 GMT
CMD ["/bin/bash"]
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Apr 2024 16:02:10 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_MAJOR=7.0
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
VOLUME [/data/db /data/configdb]
# Wed, 03 Apr 2024 16:02:10 GMT
ENV HOME=/data/db
# Wed, 03 Apr 2024 16:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Apr 2024 16:02:10 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 03 Apr 2024 16:02:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7829398e6cec615872199f7d302253b64f2f90c209329783d7db2d99013a9c`  
		Last Modified: Tue, 16 Apr 2024 12:10:40 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645b7b6e30ae2933272d4495229ca7bb56b79fbc1005aa636c8957eb79a38e43`  
		Last Modified: Tue, 16 Apr 2024 12:10:40 GMT  
		Size: 1.5 MB (1466198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9416f2ad98ae59a1c7c69cae2cdab4ee63b45c1f46c8cf6ab438c601851ff3d8`  
		Last Modified: Tue, 16 Apr 2024 12:12:03 GMT  
		Size: 1.0 MB (1027737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c141eb816dba9a5ec37a62793d1ed1af07eec47144cf531d08c3c93d4cdd62e9`  
		Last Modified: Tue, 16 Apr 2024 12:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7205b41760fd6e4293127467d9ffbb32c9a90b8eca39a26f4f44a27be7aed7df`  
		Last Modified: Tue, 16 Apr 2024 12:12:03 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de730d42f0cf5a9abfc90c1dfd0f47c787200c1c62fbf9fe4064136199e4e4`  
		Last Modified: Tue, 16 Apr 2024 12:12:08 GMT  
		Size: 224.5 MB (224467256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73551f3233867abb518bb66a6a8ddedb60c771ebcc9c6710fa65b8abbbf485`  
		Last Modified: Tue, 16 Apr 2024 12:12:04 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:4a36d2155342e86d4af1166bd67f2164bb29b087ca9068c74d0db93efde02db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be1a22313e06c3018a055cfb9f6e5b5dc4828b2f327fc27a4812742bc9e10aa`

```dockerfile
```

-	Layers:
	-	`sha256:eb0e930dda23332049568bd81e595846e24cd75a14a4cb290bb858b8ab7970e8`  
		Last Modified: Tue, 16 Apr 2024 12:12:03 GMT  
		Size: 3.0 MB (3001302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf20a121e0a4e8df6064ec645e5de84f6d6b8b2e3bcde404049d0c4b549a75c`  
		Last Modified: Tue, 16 Apr 2024 12:12:02 GMT  
		Size: 27.6 KB (27592 bytes)  
		MIME: application/vnd.in-toto+json
