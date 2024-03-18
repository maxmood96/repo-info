## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:6ab153aafe3d6d9a1b7ab9162276bcfef52caf24b271a563695a6b0257f911e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:5af155ed5b41f856dc214e16fd30f666fc1a07ad8fed454b3e0f009b4bd49ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261522284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24041ceefc56c2a051bd3a9a8397b319f6bcd62fff796647f2c1da0a201ab792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 16:01:38 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 18 Mar 2024 16:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Mar 2024 16:01:38 GMT
ENV GOSU_VERSION=1.17
# Mon, 18 Mar 2024 16:01:38 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 18 Mar 2024 16:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 18 Mar 2024 16:01:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Mar 2024 16:01:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 18 Mar 2024 16:01:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 18 Mar 2024 16:01:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 18 Mar 2024 16:01:38 GMT
ENV MONGO_MAJOR=7.0
# Mon, 18 Mar 2024 16:01:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 18 Mar 2024 16:01:38 GMT
ENV MONGO_VERSION=7.0.7
# Mon, 18 Mar 2024 16:01:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 18 Mar 2024 16:01:38 GMT
VOLUME [/data/db /data/configdb]
# Mon, 18 Mar 2024 16:01:38 GMT
ENV HOME=/data/db
# Mon, 18 Mar 2024 16:01:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 16:01:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Mar 2024 16:01:38 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 18 Mar 2024 16:01:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00c7ff578b0f50502a55231572f62f8480405197f879b8dc4984b5164960f35`  
		Last Modified: Mon, 18 Mar 2024 18:49:14 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f43ab851519ac42130b6e1030d805dd26ca2f874537117b5dd87ea1ac4c48d`  
		Last Modified: Mon, 18 Mar 2024 18:49:14 GMT  
		Size: 1.5 MB (1500307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f6a5998ab06d09eb8b92b5244b4ed1fcbd8cd5c8b44171afb5542e27b984`  
		Last Modified: Mon, 18 Mar 2024 18:49:14 GMT  
		Size: 1.1 MB (1094167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8424336879e4960f5c1e39ee1406d6adfb841c1446adc56b782886ed1698f003`  
		Last Modified: Mon, 18 Mar 2024 18:49:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a6d3c2e6c8f25edb0b829f34434e5db0184545a43e035d32ae6f3b2035bc9b`  
		Last Modified: Mon, 18 Mar 2024 18:49:15 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c533c21e5fb8b41a6144ab7e498d522954e752c02af9c741d523073db4fc34d9`  
		Last Modified: Mon, 18 Mar 2024 18:49:18 GMT  
		Size: 229.4 MB (229381694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fddf702bb73fb7b0c74e9cc1518a67bffa49fe33091255b1f7291b9a185d956`  
		Last Modified: Mon, 18 Mar 2024 18:49:15 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:6b89b6389535ef63a7ca2107ea68ceec4d455df03a81f9250f846a1e6fa1ce30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e59e0605d7513f5f729bb453e48cc38018753535a6699ae10ef898f89c09aa7`

```dockerfile
```

-	Layers:
	-	`sha256:f97b7474055b810f39e1e8eba4afc0bebebdd3e0616bd366b18cfe472dcba4f8`  
		Last Modified: Mon, 18 Mar 2024 18:49:14 GMT  
		Size: 3.0 MB (2999865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13adf0ac94927b757a63cec5111dc17b4dafe54a27edc6e0edcd998b4aa4eac6`  
		Last Modified: Mon, 18 Mar 2024 18:49:14 GMT  
		Size: 27.7 KB (27735 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:406995896fd76614f36ee10cf92d5d7f1c5526de07561f3d599a89b39f49b55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250411010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4b09aafef7b3d4b99228fd0de0091d887a5c01362ea280541c12b9a5ab67b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:33:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:33:16 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:33:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:33:16 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:33:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:33:16 GMT
ENV MONGO_MAJOR=7.0
# Thu, 29 Feb 2024 23:33:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ENV MONGO_VERSION=7.0.6
# Thu, 29 Feb 2024 23:33:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:33:16 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:33:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:33:16 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:33:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bd89af55c0e4a026246b31bb0ead738f1dec86ed74f6cd61588112089ffdf`  
		Last Modified: Fri, 15 Mar 2024 19:53:26 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5eac8f7306550dc8afd92ed23b6cf11dd6ce96e577a15565b3b5af29aa2503f`  
		Last Modified: Fri, 15 Mar 2024 19:53:26 GMT  
		Size: 1.5 MB (1465421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d36aaec7660425fb0685d9180636a0948ec5c4eb1ff21b7bf6c02c611223429`  
		Last Modified: Fri, 15 Mar 2024 20:00:18 GMT  
		Size: 1.0 MB (1026952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36b91931846c4396113a1e263599671c5095101135c12af29df89f2d104b33d`  
		Last Modified: Fri, 15 Mar 2024 20:00:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b4c126fe09f5a308711b91a9c6708dd12a52ba68910097eda1633600b4ff6b`  
		Last Modified: Fri, 15 Mar 2024 20:00:17 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8079e24d3936e965c597eee2fb11fc4d74a10ad1fd55fc2e986ad26825cdbd7d`  
		Last Modified: Fri, 15 Mar 2024 20:00:22 GMT  
		Size: 220.6 MB (220552754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb93384cdee1ae0cb886ea1c67140fcc4beab9c5a320c112ad79a62f6eada01e`  
		Last Modified: Fri, 15 Mar 2024 20:00:18 GMT  
		Size: 5.0 KB (4994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:cd83e2d537a29e11bdddc38ac3c06406876de57c6ca75b304be6ce4c000e75ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da877cca864e4d658d1d8b9babd9b1eda43940fe64966ffdb842b18249298a4d`

```dockerfile
```

-	Layers:
	-	`sha256:23b152d5d1d1e1f512741eee513f998f912412a4729aa10774a1a035a86ec3c0`  
		Last Modified: Fri, 15 Mar 2024 20:00:18 GMT  
		Size: 3.0 MB (3000122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c8d9f409f68be3fabcd523c782e5def4ffc0734ab98485ee0ceebc6dbaf1189`  
		Last Modified: Fri, 15 Mar 2024 20:00:17 GMT  
		Size: 27.6 KB (27592 bytes)  
		MIME: application/vnd.in-toto+json
