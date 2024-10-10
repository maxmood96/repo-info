## `mongo:noble`

```console
$ docker pull mongo@sha256:56c00ac2a5bb10e8001acd2b41c74ee3e59b5d351220d179ff4b03c79090091e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:eec79b653f195ae10de932804970886bd44b74b33ab295021cd6066fdd2fa1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274427752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51fa15469cf87ad6195a5c649991bf52a3af8ed749fa8555c7f2e8abe554a7f`
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
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENV GOSU_VERSION=1.17
# Wed, 09 Oct 2024 22:01:30 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 09 Oct 2024 22:01:30 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 09 Oct 2024 22:01:30 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_MAJOR=8.0
# Wed, 09 Oct 2024 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_VERSION=8.0.1
# Wed, 09 Oct 2024 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
VOLUME [/data/db /data/configdb]
# Wed, 09 Oct 2024 22:01:30 GMT
ENV HOME=/data/db
# Wed, 09 Oct 2024 22:01:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 22:01:30 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 09 Oct 2024 22:01:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e6296f65cdc8587e12169a99b684d8d997e844c55f4fa74d62dedf44b9927f`  
		Last Modified: Wed, 09 Oct 2024 22:58:42 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db91cbf1eff9e48caccc4e3ef34642693390c19af141c0ebf4f879d1ed2be9c4`  
		Last Modified: Wed, 09 Oct 2024 22:58:43 GMT  
		Size: 1.8 MB (1819175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683a99ad3274a3088214323082b69d8ab01382e7b4de22e93892960fc5eec44b`  
		Last Modified: Wed, 09 Oct 2024 22:58:43 GMT  
		Size: 1.1 MB (1129322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e352f8b2074d565789fa60d0f17680e64546fcaf6a5c265975822075badcbbf7`  
		Last Modified: Wed, 09 Oct 2024 22:58:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5294c8cf575117329bc5c7ad8e3351bcd9a719f38b52ccff36933bd97c451c75`  
		Last Modified: Wed, 09 Oct 2024 22:58:44 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3e70601d5a0645f8920ca9f66bd008e8412823ec2c096f0f4ddaecf0193044`  
		Last Modified: Wed, 09 Oct 2024 22:58:49 GMT  
		Size: 241.7 MB (241722804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86114d4f17129f5e17683491f90fc2803b1896882e5996a6835c3fdcda3d7412`  
		Last Modified: Wed, 09 Oct 2024 22:58:44 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:42fa1a30456d1a4e63d297d69d70435fa3b4a81945026c469900a92467a181bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c89e3e9cfba1e1a9f97f3451c74d7af5dfdfd8300c77f11d0e3e9b546aa57c`

```dockerfile
```

-	Layers:
	-	`sha256:966716fa8cb28c624488d7d577ef7682de756424267fc22551b5e91f4040ffa1`  
		Last Modified: Wed, 09 Oct 2024 22:58:43 GMT  
		Size: 2.5 MB (2480732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35a8adff820bd21517fe23a7e4ba27839ad0498c2b961fbaade96e44516cf33`  
		Last Modified: Wed, 09 Oct 2024 22:58:42 GMT  
		Size: 28.3 KB (28323 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:9c9627a3edcebfdc753f0783698f8dece5b96fc4ff77d95553486b6450c0b0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263688295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5bcbb5a081cc3fed8e0cbff881989e0910701245339aa8a686f8c1761eb42b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENV GOSU_VERSION=1.17
# Wed, 09 Oct 2024 22:01:30 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 09 Oct 2024 22:01:30 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 09 Oct 2024 22:01:30 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_MAJOR=8.0
# Wed, 09 Oct 2024 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_VERSION=8.0.1
# Wed, 09 Oct 2024 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
VOLUME [/data/db /data/configdb]
# Wed, 09 Oct 2024 22:01:30 GMT
ENV HOME=/data/db
# Wed, 09 Oct 2024 22:01:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 22:01:30 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 09 Oct 2024 22:01:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0c4d5193bdabc1cc1473967db2645224cbad2e95a841621c02c179750a0061`  
		Last Modified: Wed, 02 Oct 2024 03:16:42 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b745a2d75ed5e1081baf2a9b8e3ed414025313a4dc8b07c93b43b4c8794e4d`  
		Last Modified: Wed, 02 Oct 2024 03:16:42 GMT  
		Size: 1.8 MB (1817032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2da8b2d31f7fa4728f45e1bee7d273f39bb431757e1b39e8d0dc921dcbd5ad`  
		Last Modified: Wed, 09 Oct 2024 22:58:18 GMT  
		Size: 1.1 MB (1059663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd676b77a3972bc7336f0696d60e1aaf8b7003b6119cd4852d43581647e8d80`  
		Last Modified: Wed, 09 Oct 2024 22:58:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eea1ca26a2261e72f18f672cf4dc126c479b4d2e1e8eadce89dd7a3192aadd`  
		Last Modified: Wed, 09 Oct 2024 22:58:18 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72a18ce6b02c3deeb7e4c3faef21903898b9c1f8bfab63e76e02a54118e5933`  
		Last Modified: Wed, 09 Oct 2024 22:58:23 GMT  
		Size: 231.9 MB (231919576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4ae86e659846d1b2bc392949eeb318070a6ec629eb2e012a20109f66252eef`  
		Last Modified: Wed, 09 Oct 2024 22:58:19 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:52c97fd38caf25744a258d94e1a0046bf0f1595d47e731e2c49c9022255635ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbb3c6988aa47e36ee785b554c3f99c53b72e7d9426b15be49e1815a9587b7b`

```dockerfile
```

-	Layers:
	-	`sha256:dc8700daeb1031b5f18674cbf0a019ef2d8ee4752c8535a55fbdf11354834111`  
		Last Modified: Wed, 09 Oct 2024 22:58:18 GMT  
		Size: 2.5 MB (2481868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ed9a4a05b4491d22fd8c79fe3d323ccc658252237a845dfa4fa56440b725d89`  
		Last Modified: Wed, 09 Oct 2024 22:58:18 GMT  
		Size: 28.5 KB (28544 bytes)  
		MIME: application/vnd.in-toto+json
