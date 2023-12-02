## `mongo:jammy`

```console
$ docker pull mongo@sha256:c2875269a10fd0e2e57e2b989ef9409c5b72a7391cb6f714eb0d8199b6744051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:3ee80b67778b162efb3323c1f1539c573c9928c0540a567ebf5fec15d387327a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261144938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acb2131d51f8ae39cbf4360b2f3f3e6d78dd14797bea477e173bb3c0e1abca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:58:09 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 02 Dec 2023 04:58:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:58:18 GMT
ENV GOSU_VERSION=1.16
# Sat, 02 Dec 2023 04:58:18 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 02 Dec 2023 04:58:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 02 Dec 2023 04:58:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 02 Dec 2023 04:58:27 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 02 Dec 2023 04:58:27 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 02 Dec 2023 04:58:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 02 Dec 2023 04:58:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 02 Dec 2023 04:58:28 GMT
ENV MONGO_MAJOR=7.0
# Sat, 02 Dec 2023 04:58:28 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 02 Dec 2023 04:58:28 GMT
ENV MONGO_VERSION=7.0.4
# Sat, 02 Dec 2023 04:58:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 02 Dec 2023 04:58:54 GMT
VOLUME [/data/db /data/configdb]
# Sat, 02 Dec 2023 04:58:54 GMT
ENV HOME=/data/db
# Sat, 02 Dec 2023 04:58:54 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Sat, 02 Dec 2023 04:58:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Dec 2023 04:58:55 GMT
EXPOSE 27017
# Sat, 02 Dec 2023 04:58:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80d99d2ce19b0e9c589171dbac0eac60bc4b3943817938ecfed3a8bd220d50b`  
		Last Modified: Sat, 02 Dec 2023 05:01:35 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb44dc221f386a8d7be81b66776b629685dd3cd74c5d31f00ef0357e74f09d2`  
		Last Modified: Sat, 02 Dec 2023 05:01:36 GMT  
		Size: 5.1 MB (5050736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cece2eeeb646063bf149487118b7a1ea3ecf6c3f73c21c788fc4a7b1773494`  
		Last Modified: Sat, 02 Dec 2023 05:01:35 GMT  
		Size: 1.3 MB (1253151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9484737e86c40951589e2640a2f2210e5a7132e28618477889d94b5ebad6fa4d`  
		Last Modified: Sat, 02 Dec 2023 05:01:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ad935b75c0adbcb0eb26c035678f90309445dac9174d56c62b0847197ae180`  
		Last Modified: Sat, 02 Dec 2023 05:01:33 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ac6a8edff6b5e30bb7b32d2e4daaf7842dca49fd285553ce761bbdfba89220`  
		Last Modified: Sat, 02 Dec 2023 05:01:33 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90580617c703984ef681dfe4d159b7985600a8c042c8402ae3ce579ea47c3a80`  
		Last Modified: Sat, 02 Dec 2023 05:02:00 GMT  
		Size: 224.4 MB (224386050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c932f95934184a92c486807fcfe334b9b9a2bcdfdbd2ed4d42d2886e51d528c`  
		Last Modified: Sat, 02 Dec 2023 05:01:33 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:89b822fa227786c7562f033985301cc9748c7f73bb6e075faca98fcfa4d75dc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253153069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6718e817cdb7562f310a2a533dc92578c786b264039d3fa7bde1d2fe919e720`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:07:59 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 13 Oct 2023 05:08:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 05:08:12 GMT
ENV GOSU_VERSION=1.16
# Fri, 13 Oct 2023 05:08:12 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 13 Oct 2023 05:08:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 05:08:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 05:08:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 05:08:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 05:08:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:22 GMT
ENV MONGO_MAJOR=7.0
# Fri, 13 Oct 2023 05:08:22 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 29 Nov 2023 06:25:36 GMT
ENV MONGO_VERSION=7.0.4
# Wed, 29 Nov 2023 06:26:36 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 29 Nov 2023 06:26:40 GMT
VOLUME [/data/db /data/configdb]
# Wed, 29 Nov 2023 06:26:40 GMT
ENV HOME=/data/db
# Wed, 29 Nov 2023 06:26:41 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 29 Nov 2023 06:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Nov 2023 06:26:41 GMT
EXPOSE 27017
# Wed, 29 Nov 2023 06:26:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53942a81bbed58a041019d02afca8f39cb3b5fc0b340c05513ba233089ddaa64`  
		Last Modified: Fri, 13 Oct 2023 05:11:43 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c77c1ea6f8e184bfebf5bd44a67db789f6dda84d9e1765f88df461c6fc366ba`  
		Last Modified: Fri, 13 Oct 2023 05:11:44 GMT  
		Size: 5.0 MB (4993892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ffa19aee38fa5d40fbbb7ad0fed2cd802350b3e0859506d008678f433b01`  
		Last Modified: Fri, 13 Oct 2023 05:11:43 GMT  
		Size: 1.2 MB (1186372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae10bad01057285cb468c4b8ac16543be6f76dd7617e0a1dd477c7cab4e8265`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208482253dd3d9820726079a672df6e91e9b83c81c36d5554103f854670ccfc1`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beb4a4f2118534d26af685b92befcd861724f9f1ce3cd9a0cfabfecfe1452df`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea30ae4c939b9934695156460720f2ee94c990c9f4289e1d89736019b33c72fa`  
		Last Modified: Wed, 29 Nov 2023 06:29:02 GMT  
		Size: 218.6 MB (218572185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2e9e9c3b685819ab035fbbe9b88d2d3163f49098dfa1cbf4dac427732e056f`  
		Last Modified: Wed, 29 Nov 2023 06:28:43 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
