## `mongo:5-focal`

```console
$ docker pull mongo@sha256:cfc3b29c43d391da7c61c8b4e0fde46252311ff5b6ddb92966f63cd950b85ee1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:64c64522d822786ffc8189f34bc16ee3c874e1f8448735e05507f3575d085203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270121688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a49b822de3e60f7fc33f80e93da52929c37579f8d041171ce2a0d6bf28ff07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 22:01:15 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 06 Jun 2024 22:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 22:01:15 GMT
ENV GOSU_VERSION=1.17
# Thu, 06 Jun 2024 22:01:15 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 06 Jun 2024 22:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 06 Jun 2024 22:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 06 Jun 2024 22:01:15 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 06 Jun 2024 22:01:15 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 06 Jun 2024 22:01:15 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 06 Jun 2024 22:01:15 GMT
ENV MONGO_MAJOR=5.0
# Thu, 06 Jun 2024 22:01:15 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 06 Jun 2024 22:01:15 GMT
ENV MONGO_VERSION=5.0.27
# Thu, 06 Jun 2024 22:01:15 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 06 Jun 2024 22:01:15 GMT
VOLUME [/data/db /data/configdb]
# Thu, 06 Jun 2024 22:01:15 GMT
ENV HOME=/data/db
# Thu, 06 Jun 2024 22:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 22:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Jun 2024 22:01:15 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 06 Jun 2024 22:01:15 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756591a68cb141857cdf3f0ee22ddeb0219650d65351ca7f2627cd4aa830bcf9`  
		Last Modified: Fri, 07 Jun 2024 01:04:10 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3aac2d255ca63200a13e1d7c8b373790d15c22db29277f70d350a0b7d7c995`  
		Last Modified: Fri, 07 Jun 2024 01:04:10 GMT  
		Size: 3.1 MB (3076343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878eb11c8d5a181f4c1138caa1c639bab6e8798954be986b46e2ac12c4a77184`  
		Last Modified: Fri, 07 Jun 2024 01:04:10 GMT  
		Size: 1.1 MB (1091402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f4e181ac9aa70927fa96cb5ff28f1b4da11dac1171258e9b75811ea7c3d9c`  
		Last Modified: Fri, 07 Jun 2024 01:04:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c553592ce92a861407c5198a0dd2157846365789f95550ac83c4d8f502da2b`  
		Last Modified: Fri, 07 Jun 2024 01:04:11 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b9f9d712894756791c64e4c960e099d9810fdfa21c58518def56c9cca3e04c`  
		Last Modified: Fri, 07 Jun 2024 01:04:16 GMT  
		Size: 238.4 MB (238435017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a8cac0cc78cc5cc0def8700b8f348a523dad649eabd7fad7e5f07d99e5569c`  
		Last Modified: Fri, 07 Jun 2024 01:04:11 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:121bf4b9e0bbd29a7947f3bc7856ac1cbc083e16c3413ede08716f0086f7842b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015b302c6afb30f60c7fa95ed917e5bb8d07a6e64e4c68ed8a5352675d2a33d3`

```dockerfile
```

-	Layers:
	-	`sha256:0bd911b2e0f6096b29a6bdcdda9a965d5ab2f0aaa8829e72b5f0e6fcd2169d7b`  
		Last Modified: Fri, 07 Jun 2024 01:04:10 GMT  
		Size: 3.0 MB (2999993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c34c1697e6d002c36f08e6c9ea074f2a151df1bba5a26a2426875158cd442c28`  
		Last Modified: Fri, 07 Jun 2024 01:04:10 GMT  
		Size: 26.7 KB (26724 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ef6a478e3a268f41e658cb95d73d97525578285571b361225a0e21514b5625c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262473143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c10c541e00d8a09219eba9c71f16cb627e0a81304bd4f2fb2ba9465774d70a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Mar 2024 22:01:21 GMT
ARG RELEASE
# Tue, 26 Mar 2024 22:01:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 22:01:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 22:01:21 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 22:01:21 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 26 Mar 2024 22:01:21 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 22:01:21 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_MAJOR=5.0
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_VERSION=5.0.26
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
VOLUME [/data/db /data/configdb]
# Tue, 26 Mar 2024 22:01:21 GMT
ENV HOME=/data/db
# Tue, 26 Mar 2024 22:01:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 22:01:21 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 26 Mar 2024 22:01:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20de50c7979928f6a2ff806f22680e1b850947be04f26ec532650e2533a5856f`  
		Last Modified: Wed, 05 Jun 2024 16:28:25 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5ee07feb16ff247dd7feeaf66f29e96b390d7c169aca89ccd4136134770b2`  
		Last Modified: Wed, 05 Jun 2024 16:28:25 GMT  
		Size: 2.9 MB (2929661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de879c2bf4da5ec5aef915bbeb3d1dba7eec8995048bab32692b338b39cf5d8`  
		Last Modified: Wed, 05 Jun 2024 16:29:48 GMT  
		Size: 1.0 MB (1023643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5781815affea17824ad94bd1df13bba5371bc1e7e6330dde8a09223cfe7622`  
		Last Modified: Wed, 05 Jun 2024 16:29:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c315c03c35ff43f383a545113241c9be0fa20f2a08e191e88597d0a513971295`  
		Last Modified: Wed, 05 Jun 2024 16:29:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ec07ac8695ca59209d8db217b871639e109cc9a227bf3fda417222f3b79ddd`  
		Last Modified: Wed, 05 Jun 2024 16:29:57 GMT  
		Size: 232.5 MB (232538467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc1a48211252b64be155d47cc377b934fec8c0d8752c176fc24bd1764a73c80`  
		Last Modified: Wed, 05 Jun 2024 16:29:50 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:e3879f9d7e6839f79e55280de28b8eb6731a4a5138045763a7fa1b9029de2c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f35a609450f22acf388e4e882ceb42de33bf4913a47998db05ea61ce14014fe`

```dockerfile
```

-	Layers:
	-	`sha256:cbe564b3f8e5e2b41845e7b1e044dbcaf43707b3192e47aaac12927d2a571db9`  
		Last Modified: Wed, 05 Jun 2024 16:29:49 GMT  
		Size: 3.0 MB (3000291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b58478af2f3c1b3bdc529db5347986b9564d76cf2c1cb692feb4173f425d967`  
		Last Modified: Wed, 05 Jun 2024 16:29:48 GMT  
		Size: 27.0 KB (27000 bytes)  
		MIME: application/vnd.in-toto+json
