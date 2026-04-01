## `mongo:8-noble`

```console
$ docker pull mongo@sha256:06ebda3671a72318f5dc89231b3624a0641925fca893256c11341c1369498aed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:5483a68b6fe7737367be84fb963f0e440e67a87f2e57ea087e608da034e91318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.8 MB (337835002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703e11b25edb2d740a6a20ca0cccbe6a9d24691281f32ab5cdc9185dc9315208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 31 Mar 2026 23:26:48 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 31 Mar 2026 23:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 31 Mar 2026 23:27:09 GMT
ENV GOSU_VERSION=1.19
# Tue, 31 Mar 2026 23:27:09 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 31 Mar 2026 23:27:09 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 31 Mar 2026 23:27:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 31 Mar 2026 23:27:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 31 Mar 2026 23:27:09 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 31 Mar 2026 23:27:09 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 31 Mar 2026 23:27:09 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 31 Mar 2026 23:27:09 GMT
ENV MONGO_MAJOR=8.2
# Tue, 31 Mar 2026 23:27:09 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Tue, 31 Mar 2026 23:27:09 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 31 Mar 2026 23:27:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 31 Mar 2026 23:27:28 GMT
VOLUME [/data/db /data/configdb]
# Tue, 31 Mar 2026 23:27:28 GMT
ENV HOME=/data/db
# Tue, 31 Mar 2026 23:27:28 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 31 Mar 2026 23:27:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 23:27:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 23:27:28 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 31 Mar 2026 23:27:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c433b73ba83812fda699da6bcc062344bcd5026a5971632ce032f001016006`  
		Last Modified: Tue, 31 Mar 2026 23:28:05 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13335f999508cd14d9701b1ea3f1d61d67437bc9e1bc558f3d6de19373fd94ab`  
		Last Modified: Tue, 31 Mar 2026 23:28:05 GMT  
		Size: 1.5 MB (1509456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389b5cf90dda8117fedc83e8ee7501734d9cdd8989508a75ed32821b52b243f7`  
		Last Modified: Tue, 31 Mar 2026 23:28:05 GMT  
		Size: 933.7 KB (933671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5522a7abaf15b78f0c7131051bcd70f9a497a355d8ed0735e5ea1dcc8bdad29`  
		Last Modified: Tue, 31 Mar 2026 23:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a40f03c0faf52a637465168116f9647e29f772b4c4b314cd32674f5b812c36`  
		Last Modified: Tue, 31 Mar 2026 23:28:07 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b10863adf74a52704dbcd3b827d140e57c59f23bdcad587eeb4b22cab6148b2`  
		Last Modified: Tue, 31 Mar 2026 23:28:13 GMT  
		Size: 305.7 MB (305653283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d801d987e7362342aa9729af22fd7456bd3508b9b87c967068706d72b2e330e`  
		Last Modified: Tue, 31 Mar 2026 23:28:07 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:5e9cc51d5bb6f41d30818e82240891a6e3afa03f0b6f6e224b148d160d9075c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e9096c65b2e0d5fd466fdc17fae84a29ef6b29ce372658c2a9af1597ac70a5`

```dockerfile
```

-	Layers:
	-	`sha256:041d9739026b45385bc488cf3655ba92e96628f96d9ce10b696ab9daccff094c`  
		Last Modified: Tue, 31 Mar 2026 23:28:06 GMT  
		Size: 2.7 MB (2661252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd5782916fcd0aec1a7f69ecec61cf19396a6375450a94c3bfe1c20b83836b6`  
		Last Modified: Tue, 31 Mar 2026 23:28:05 GMT  
		Size: 28.7 KB (28736 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4a719b4e8e28b1868ba93e403d7b8512b5650909bbfada24e66ff65761266b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322524933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f571e595af3cef5dcbe06801e8f2110c71d1915408c9521b29547bc6581617`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Mar 2026 23:26:32 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 31 Mar 2026 23:26:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 31 Mar 2026 23:26:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 31 Mar 2026 23:26:57 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 31 Mar 2026 23:26:57 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 31 Mar 2026 23:26:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 31 Mar 2026 23:26:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 31 Mar 2026 23:26:57 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 31 Mar 2026 23:26:57 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 31 Mar 2026 23:26:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 31 Mar 2026 23:26:57 GMT
ENV MONGO_MAJOR=8.2
# Tue, 31 Mar 2026 23:26:57 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Tue, 31 Mar 2026 23:26:57 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 31 Mar 2026 23:27:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 31 Mar 2026 23:27:21 GMT
VOLUME [/data/db /data/configdb]
# Tue, 31 Mar 2026 23:27:21 GMT
ENV HOME=/data/db
# Tue, 31 Mar 2026 23:27:21 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 31 Mar 2026 23:27:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Mar 2026 23:27:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2026 23:27:21 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 31 Mar 2026 23:27:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e504acbc132ada1a91bc076cb7d386f7081c46f3f4f94a282ff436dbe641e`  
		Last Modified: Tue, 31 Mar 2026 23:27:56 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cda8f9a3eb1c72e1fc2c1d78ad0abc804958108d66510c3b0bbfd4a3529c184`  
		Last Modified: Tue, 31 Mar 2026 23:27:56 GMT  
		Size: 1.5 MB (1494487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cc0c9ce2814792bfc69df0ecadb7588811b80067b2d4eb1924f195eab9b203`  
		Last Modified: Tue, 31 Mar 2026 23:27:56 GMT  
		Size: 886.0 KB (886035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876014e1ab67724385d6919ceb558b9a1848807069846b583ec4f8b2827a8cfa`  
		Last Modified: Tue, 31 Mar 2026 23:27:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe619ad26ccf13544990affb2441fb8f14104ea46569d22b694bfb6d3f14b0`  
		Last Modified: Tue, 31 Mar 2026 23:27:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d64d3970a618229bf875110a085d7ae7929e31bfc1d5bcc4ead527c07b32b`  
		Last Modified: Tue, 31 Mar 2026 23:28:04 GMT  
		Size: 291.3 MB (291268100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb6c9ec0fb44bae23ff6dd3702b623859134fbb61c2df94d5c7765e3f8304c6`  
		Last Modified: Tue, 31 Mar 2026 23:27:58 GMT  
		Size: 5.0 KB (5005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:fb04c27bc88d6ebe56dce941bf0299cab45e0c56531b8f47d410d81f58222c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06c463b8920b1e126dab021c1a69d69ddf79c5c81847d04967b7dafc297c86e`

```dockerfile
```

-	Layers:
	-	`sha256:6ebd824c556db8a111f4ff4ad77c6dc30bd9d3a794836c2df64be6192454fbc1`  
		Last Modified: Tue, 31 Mar 2026 23:27:56 GMT  
		Size: 2.7 MB (2662388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a29bfc700cbf24d8fb1110c85d3d7c3d89913b833889e58c1d3818ceb7370aa`  
		Last Modified: Tue, 31 Mar 2026 23:27:56 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
