## `mongo:5-focal`

```console
$ docker pull mongo@sha256:b6fd565936463501f7306f33937fbdbaeaf5fd6f50b7cc588fcda00912815b3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:936020698d1b62b73f6bd40d52f172eb90e2a79e955aa4de26975100e5e991c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264115423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5c3a4a39357089dba98c45932dc6167895ddc1c67a1689e788f37f6b6be1ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 03 Oct 2024 19:50:58 GMT
ARG RELEASE
# Thu, 03 Oct 2024 19:50:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 03 Oct 2024 19:50:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 03 Oct 2024 19:50:58 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 03 Oct 2024 19:50:58 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 03 Oct 2024 19:50:58 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 19:50:58 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
ENV GOSU_VERSION=1.17
# Thu, 03 Oct 2024 19:50:58 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 03 Oct 2024 19:50:58 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 03 Oct 2024 19:50:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 03 Oct 2024 19:50:58 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 03 Oct 2024 19:50:58 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 03 Oct 2024 19:50:58 GMT
ENV MONGO_MAJOR=5.0
# Thu, 03 Oct 2024 19:50:58 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
ENV MONGO_VERSION=5.0.29
# Thu, 03 Oct 2024 19:50:58 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
VOLUME [/data/db /data/configdb]
# Thu, 03 Oct 2024 19:50:58 GMT
ENV HOME=/data/db
# Thu, 03 Oct 2024 19:50:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Oct 2024 19:50:58 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 03 Oct 2024 19:50:58 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d380bfc6fcf8b68699c463635194d2da9803a09170711b405a6ffe7668cc39f0`  
		Last Modified: Wed, 16 Oct 2024 16:14:32 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b17f1371bec020a957853272f96067233a3d5a66743e02cb5459c1959251dc`  
		Last Modified: Wed, 16 Oct 2024 16:14:32 GMT  
		Size: 3.1 MB (3094296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39a037a173106a91637ebc915599ffe755814435b729ed5a59cdaf2231c49c0`  
		Last Modified: Wed, 16 Oct 2024 16:14:32 GMT  
		Size: 1.1 MB (1091694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d542d385b104eb0bca109e4807b956ae6857889d80fc355870e3c696cfe612`  
		Last Modified: Wed, 16 Oct 2024 16:14:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871b7a258289c9cce865a23c5a24aba93e4f404f4ff357b0caacbc93946cc39d`  
		Last Modified: Wed, 16 Oct 2024 16:14:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a70aeac42a87ae67a9e6cfc29e99794fc614a8721d04f2f84fbf4ad40e076`  
		Last Modified: Wed, 16 Oct 2024 16:14:36 GMT  
		Size: 232.4 MB (232411218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bc41c01381d29ee67860fd9f692963693af05d4c5c2963d3b852e1efe61024`  
		Last Modified: Wed, 16 Oct 2024 16:14:33 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:d4c8b00b278138b7a6df0a97c25114138d73dbcb30c056997d9645da8fca6c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3062442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca7a78fc3d31fe54bbc7f563a44f5c2672dc37de3fe42cc579387889e8f5164`

```dockerfile
```

-	Layers:
	-	`sha256:09158372aee366d7c9424116a1a77b1cef8135d97543a7399de435d8cd9f488e`  
		Last Modified: Wed, 16 Oct 2024 16:14:32 GMT  
		Size: 3.0 MB (3034989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36670d765ee37fbfdf321c414be605c155de574b4b6380f30669e4e12b21872f`  
		Last Modified: Wed, 16 Oct 2024 16:14:32 GMT  
		Size: 27.5 KB (27453 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:eac518877392fb2bdcc968ffdec2efff10c6a009b78711aa4e197b235bb6f1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253736670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba66909d91e08c0db9151e3e4275075ad7283c9bda86ca53c35ee1b390b4ff8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 03 Oct 2024 19:50:58 GMT
ARG RELEASE
# Thu, 03 Oct 2024 19:50:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 03 Oct 2024 19:50:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 03 Oct 2024 19:50:58 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 03 Oct 2024 19:50:58 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 03 Oct 2024 19:50:58 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 19:50:58 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
ENV GOSU_VERSION=1.17
# Thu, 03 Oct 2024 19:50:58 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 03 Oct 2024 19:50:58 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 03 Oct 2024 19:50:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 03 Oct 2024 19:50:58 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 03 Oct 2024 19:50:58 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 03 Oct 2024 19:50:58 GMT
ENV MONGO_MAJOR=5.0
# Thu, 03 Oct 2024 19:50:58 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
ENV MONGO_VERSION=5.0.29
# Thu, 03 Oct 2024 19:50:58 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
VOLUME [/data/db /data/configdb]
# Thu, 03 Oct 2024 19:50:58 GMT
ENV HOME=/data/db
# Thu, 03 Oct 2024 19:50:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 19:50:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Oct 2024 19:50:58 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 03 Oct 2024 19:50:58 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50588583ff15e46b7a87e27ae5835332552d3627410108ac1f0dc934679f58af`  
		Last Modified: Wed, 16 Oct 2024 03:47:01 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e44286a463db6dec1fc60b013d9de6a41f49cc5329eadf22fbe75b9de683c86`  
		Last Modified: Wed, 16 Oct 2024 03:47:02 GMT  
		Size: 2.9 MB (2943252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d3d32809b1814b6515e87589a457b242bc93e4d6127d92cfe93bb2062b2f42`  
		Last Modified: Wed, 16 Oct 2024 03:47:02 GMT  
		Size: 1.0 MB (1023815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52860ec9b55a94c6dbd4038edb9e2a4a3758acd4e92833a4583a2e1b4692db8`  
		Last Modified: Wed, 16 Oct 2024 03:47:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3841fcbc85530c0675c07b19a812ee16ebfd3dd1193130f9609f3860bc56e512`  
		Last Modified: Wed, 16 Oct 2024 03:47:02 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880fc9bfbf4b0b1afdcf507e12fffe0bf3ea75cddc352ed97d69609c4dc47574`  
		Last Modified: Wed, 16 Oct 2024 03:47:08 GMT  
		Size: 223.8 MB (223788624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010b5e33bdffee747dcfe26472c866edba58b8b561f1ceeccf000d72b86e56ac`  
		Last Modified: Wed, 16 Oct 2024 03:47:03 GMT  
		Size: 5.0 KB (4992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:154659c19b0394127f6c311b65920395b332bc088e8543aa0ec859a45b71942d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3062936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862d2156e9bf5a2a3b17111bd4b2daaa73e756477db15bd7cdcbbcbc7c85c589`

```dockerfile
```

-	Layers:
	-	`sha256:ee8675232cd70a99bbe308335e7081aafe623112531a138d88107607eb94e2ab`  
		Last Modified: Wed, 16 Oct 2024 03:47:02 GMT  
		Size: 3.0 MB (3035287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5ab4d62aa9dac2547a110a20fedb3a337468678d12131863602641aed76953`  
		Last Modified: Wed, 16 Oct 2024 03:47:01 GMT  
		Size: 27.6 KB (27649 bytes)  
		MIME: application/vnd.in-toto+json
