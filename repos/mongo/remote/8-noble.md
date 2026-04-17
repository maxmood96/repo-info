## `mongo:8-noble`

```console
$ docker pull mongo@sha256:0ebdca54ec8007f4bacd3790135f4a8db9ea2e9c62d296442776cf9d3b1c3422
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:9b18c8c1470a5aebb150ce87d6386f78f29ce74b96dfe55524161065eb8d71db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337912475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690f1371c118a8389ecd6c82c9a7f0e37320732b1d56935a24b29dfca6933f54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 23:50:19 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 16 Apr 2026 23:50:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 23:50:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 16 Apr 2026 23:50:40 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 16 Apr 2026 23:50:40 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 16 Apr 2026 23:50:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 16 Apr 2026 23:50:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Apr 2026 23:50:40 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 16 Apr 2026 23:50:40 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 16 Apr 2026 23:50:40 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 16 Apr 2026 23:50:40 GMT
ENV MONGO_MAJOR=8.2
# Thu, 16 Apr 2026 23:50:40 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Thu, 16 Apr 2026 23:50:40 GMT
ENV MONGO_VERSION=8.2.7
# Thu, 16 Apr 2026 23:50:59 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 16 Apr 2026 23:50:59 GMT
VOLUME [/data/db /data/configdb]
# Thu, 16 Apr 2026 23:50:59 GMT
ENV HOME=/data/db
# Thu, 16 Apr 2026 23:50:59 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Thu, 16 Apr 2026 23:50:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 23:50:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 23:50:59 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 16 Apr 2026 23:50:59 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6126dc5fffed1c732f651faa167bf6ba408a510f028e68a79b7d2d35034732e6`  
		Last Modified: Thu, 16 Apr 2026 23:51:38 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccce04f560d728b79fa3895199684b4c896129b6d94440c34640f2d075335798`  
		Last Modified: Thu, 16 Apr 2026 23:51:38 GMT  
		Size: 1.5 MB (1509443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39dec9b54489ef0be4a856eab8b7b406c3ff9e7a593eaa0341494bb2e0b4d16`  
		Last Modified: Thu, 16 Apr 2026 23:51:38 GMT  
		Size: 933.7 KB (933659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1842dab2ed35b809a2e5f47c3d6f343cce49c276cd317d0355215e46e91ee8`  
		Last Modified: Thu, 16 Apr 2026 23:51:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba27587cdb3406620cfa1ebdb8d8b76b7b84d75bc208144b501321f15436d182`  
		Last Modified: Thu, 16 Apr 2026 23:51:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c17794a12f9028e886018206db67226cd059f96e6fe28b4af17df2c3ad8bcb`  
		Last Modified: Thu, 16 Apr 2026 23:51:53 GMT  
		Size: 305.7 MB (305729798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de34182e2661d9635f86779fd67463b55f86fd33809d20e3462834f2c8cb50`  
		Last Modified: Thu, 16 Apr 2026 23:51:40 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:bfb665fa4b7bd98aa4fe04913845845bde85fe0a28aa4e494a44302faa6f91ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad4c34598a945ba1a65b0a9f8282c88c170482295952d5db58a3a9e3b87ce39`

```dockerfile
```

-	Layers:
	-	`sha256:bc0f43d24943641bf6e23252acb01a90807c74bd70f596361cdeac05ec1f1845`  
		Last Modified: Thu, 16 Apr 2026 23:51:38 GMT  
		Size: 2.7 MB (2661252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb1d46d977ea4953735494799265e9aef51ec618dc8d6d1fbb9e182e15ee24c`  
		Last Modified: Thu, 16 Apr 2026 23:51:38 GMT  
		Size: 28.7 KB (28736 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:daeaca33ba4577c9597973b5b094acf5d55186baa7c8d5a935076a7dc92e0f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322623836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b32a56a1ddc4c278d68124a8f0203663018f62828cadaa995a6cd595f6c9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 23:50:23 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 16 Apr 2026 23:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 23:50:47 GMT
ENV GOSU_VERSION=1.19
# Thu, 16 Apr 2026 23:50:47 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 16 Apr 2026 23:50:47 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 16 Apr 2026 23:50:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 16 Apr 2026 23:50:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Apr 2026 23:50:47 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 16 Apr 2026 23:50:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 16 Apr 2026 23:50:47 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 16 Apr 2026 23:50:47 GMT
ENV MONGO_MAJOR=8.2
# Thu, 16 Apr 2026 23:50:47 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Thu, 16 Apr 2026 23:50:47 GMT
ENV MONGO_VERSION=8.2.7
# Thu, 16 Apr 2026 23:51:12 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 16 Apr 2026 23:51:12 GMT
VOLUME [/data/db /data/configdb]
# Thu, 16 Apr 2026 23:51:12 GMT
ENV HOME=/data/db
# Thu, 16 Apr 2026 23:51:12 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Thu, 16 Apr 2026 23:51:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 23:51:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 23:51:12 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 16 Apr 2026 23:51:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66802f30f7fcf787ccc5367fdc0ed9c34b08ab15824a0668c6a55428d2d0cfd`  
		Last Modified: Thu, 16 Apr 2026 23:51:46 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1709c9d0832dfcfd973419ad9788538a9bc2512050e81b33ca6de0e0acad3c`  
		Last Modified: Thu, 16 Apr 2026 23:51:46 GMT  
		Size: 1.5 MB (1494522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84c22a37f50064958648bcd96cff4000e3cc1c21b755304013fcd2cd2bb2502`  
		Last Modified: Thu, 16 Apr 2026 23:51:46 GMT  
		Size: 886.1 KB (886067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39ecc3556d5cb39f951afdd0afc25f146b1077457adad695e9f030df6151d80`  
		Last Modified: Thu, 16 Apr 2026 23:51:46 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ffcd891f3a459ab7e70e82f49a2b625c5371c0e48db9dfa06cb0850c38d49e`  
		Last Modified: Thu, 16 Apr 2026 23:51:47 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d80cb43e0e20e8cf7d48bc86d2dfa30e6bcdf83f6c4019db30bedaac0750caf`  
		Last Modified: Thu, 16 Apr 2026 23:51:56 GMT  
		Size: 291.4 MB (291360867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2be4e5f985d4b9aad387be359f624796e13814be298a9ca62d18c759d9c67a7`  
		Last Modified: Thu, 16 Apr 2026 23:51:47 GMT  
		Size: 5.0 KB (5005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:914db1a4e745d7c7089bbcc90b5649ff49100a39b0b284906633ec8086524ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0e54f7869195dfd9446b1d0ebd8f4144fa113e60f5e8ef0093bb932f89f5a9`

```dockerfile
```

-	Layers:
	-	`sha256:742e8c4967d7beedeea3141e85e76c364e3f73dd1bab4e750d2b995256b1f647`  
		Last Modified: Thu, 16 Apr 2026 23:51:46 GMT  
		Size: 2.7 MB (2662388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b27a5ec737d155658aa658a7216d6a58e381660b7aac20c251352ff04fb1b45`  
		Last Modified: Thu, 16 Apr 2026 23:51:46 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
