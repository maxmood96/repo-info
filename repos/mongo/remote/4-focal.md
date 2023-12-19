## `mongo:4-focal`

```console
$ docker pull mongo@sha256:6f7451c0fa9bebaa852e9f82f6b8f1742c61c2e0fcde28e1715c5de7e321b6f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:6f3fae786b761a82d094b9284d4ecd2d216270c1b3c4a19c0bd8cef64da46ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117df84dda1e340b123ae196151e70f2fa33b6cb33751caf81ac1de01c4041b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:03:16 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:03:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:03:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:03:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Nov 2023 23:03:16 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Mon, 27 Nov 2023 23:03:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:03:16 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:03:16 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_MAJOR=4.4
# Mon, 27 Nov 2023 23:03:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_VERSION=4.4.26
# Mon, 27 Nov 2023 23:03:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:03:16 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:03:16 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:03:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d18f61c3ac0a9bb54bc50e0db18f83a9ed34c6fb89415d4195b23abe8acabf`  
		Last Modified: Sat, 16 Dec 2023 10:50:05 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2db5fa05093cd487f8a8d8ffefc80f96b5d5492c6001a5b3be5752acf44ec0`  
		Last Modified: Sat, 16 Dec 2023 10:50:06 GMT  
		Size: 8.4 MB (8373121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737fa1765d74177222e2be07ccbeea58737735ea265a52dc3a9ed64e90ea04cb`  
		Last Modified: Sat, 16 Dec 2023 10:50:05 GMT  
		Size: 1.1 MB (1099582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823a8c8e936a45ee65477d6382488040f4509864f86cda96f6ac259b0c9a3c50`  
		Last Modified: Sat, 16 Dec 2023 10:50:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5e4f1485fcf74b20598addecf37e9e66ec66f6ad4c2b682e8b904e8218b0a8`  
		Last Modified: Sat, 16 Dec 2023 10:50:06 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73520c7490616d9f4bf9b9fb38028fdb28efb72fc023082b7c48251f19c33a3f`  
		Last Modified: Sat, 16 Dec 2023 10:50:06 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46da3311ce4ca4cd98cd531c8327e0f2a6b5c7ca076ac6fa5577745bd4150cbc`  
		Last Modified: Sat, 16 Dec 2023 10:50:11 GMT  
		Size: 139.3 MB (139274306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fcf08edb51dac3d4c000ac29a9e3a166ce348c0e9a46c6f105930b3233a783`  
		Last Modified: Sat, 16 Dec 2023 10:50:07 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:c095de4555021af7f44c15fc1192f53f471f7f0a5f0ea683a6b6c5ba0f89d8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53263295a079efebe4094c24f372b893df8bd18f7706ba0ab1172fba6c84238`

```dockerfile
```

-	Layers:
	-	`sha256:43d7f625249436af7191eb85c1fbfc18055bbf8d76e7b0c75e39a72a7fb1a37a`  
		Last Modified: Sat, 16 Dec 2023 10:50:06 GMT  
		Size: 2.7 MB (2723946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5063652e99622800e8bcd90633862da95d1e79760a0bb190e171de5720eac7e2`  
		Last Modified: Sat, 16 Dec 2023 10:50:05 GMT  
		Size: 28.0 KB (28044 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:73f5acb6281c74da4051325cb4bb263691f65979ebed395ac74393ff0ca29569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171506591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6c1472808c66d9a7be865b4a01ef23943c1f72bf2f256a5a942ad9cbfb2c63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Nov 2023 23:03:16 GMT
ARG RELEASE
# Mon, 27 Nov 2023 23:03:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Nov 2023 23:03:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Nov 2023 23:03:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Nov 2023 23:03:16 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Mon, 27 Nov 2023 23:03:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENV GOSU_VERSION=1.16
# Mon, 27 Nov 2023 23:03:16 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 27 Nov 2023 23:03:16 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_MAJOR=4.4
# Mon, 27 Nov 2023 23:03:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENV MONGO_VERSION=4.4.26
# Mon, 27 Nov 2023 23:03:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
VOLUME [/data/db /data/configdb]
# Mon, 27 Nov 2023 23:03:16 GMT
ENV HOME=/data/db
# Mon, 27 Nov 2023 23:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 27 Nov 2023 23:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Nov 2023 23:03:16 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 27 Nov 2023 23:03:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ba6b7451f9d95719ad43508919c914407cf286d0b7fb6e1ee9a02cd51b045`  
		Last Modified: Mon, 18 Dec 2023 19:51:47 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ded41913893fb2c19b7f6cb4b21f0e12639a543c69be1d62dbe3afdf3fbc42`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 8.2 MB (8200494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deddfd4aa405910f1def1dd6fb5da28c8c01831f20100c68ba672328228d629`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 1.0 MB (1031331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae6f8162365a2edd63c6252640611da17bb92f5172d0303262b4f9b68dd2c79`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d44bb34ad2e96a269000b39df9fd446d88b5053e7c0807719affad21b0679`  
		Last Modified: Mon, 18 Dec 2023 19:51:49 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240797f3b77993b21aab5895af98ba95e3d4daedf97a2abb4e5966cfc70fe93a`  
		Last Modified: Mon, 18 Dec 2023 19:51:49 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd611e2a8a7d1a271c170167ffc8b0d124e7c0007960fe008fa0545950475781`  
		Last Modified: Mon, 18 Dec 2023 19:51:54 GMT  
		Size: 136.3 MB (136291443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f08613babe22bc1ad31279c88ff461d3fa57f4ca2de2e1d6e6da1131c7221f`  
		Last Modified: Mon, 18 Dec 2023 19:51:50 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:53e4680211790eb8e1101d6dbfcd5e4e9a6563a9f3322cbfb5c7e173b8827355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d6cba73816742bff3c13a0467d1b9241a73771203ac868e601bd03bd12a657`

```dockerfile
```

-	Layers:
	-	`sha256:9c876eabfc58b400fc968bb3a780b22f756b348813c8fad51584d4f12bc99050`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 2.7 MB (2724284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e1c1732aeca2963e5d13eea48fe166ebf71db53b0c57a991ebedd0078f9944`  
		Last Modified: Mon, 18 Dec 2023 19:51:47 GMT  
		Size: 27.9 KB (27897 bytes)  
		MIME: application/vnd.in-toto+json
