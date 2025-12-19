## `mongo:8-noble`

```console
$ docker pull mongo@sha256:d775d416112201f006871dd792dc0917eec9aa566b327611b1ca52397e79bf03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:6738383868377b1ccc6762a3f008c553d4ddb21e3430b2729814c0692ed35c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326990250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252af33466de8a9b9528dc7265331a25ba054d6a7f19172eba96f33b905b96aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 19 Dec 2025 18:52:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 19 Dec 2025 18:52:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 18:52:59 GMT
ENV GOSU_VERSION=1.19
# Fri, 19 Dec 2025 18:52:59 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 19 Dec 2025 18:52:59 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 19 Dec 2025 18:52:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 19 Dec 2025 18:52:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 19 Dec 2025 18:52:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 19 Dec 2025 18:52:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 19 Dec 2025 18:52:59 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 19 Dec 2025 18:52:59 GMT
ENV MONGO_MAJOR=8.2
# Fri, 19 Dec 2025 18:52:59 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 19 Dec 2025 18:52:59 GMT
ENV MONGO_VERSION=8.2.3
# Fri, 19 Dec 2025 18:53:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 19 Dec 2025 18:53:16 GMT
VOLUME [/data/db /data/configdb]
# Fri, 19 Dec 2025 18:53:16 GMT
ENV HOME=/data/db
# Fri, 19 Dec 2025 18:53:16 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 19 Dec 2025 18:53:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:53:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:53:16 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 19 Dec 2025 18:53:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348649c4494ee19c9c75e6b46903f30b777acc8607bf2ab3f4a3e22eea7f9e78`  
		Last Modified: Fri, 19 Dec 2025 18:54:20 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cfba47b77776b350b8d1446c56f901b226863d1bb7f2155d2bb7800186c5c8`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 1.5 MB (1509246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13b06a365c8f8066d701d49908d22a72e5f1e39a846cd44ca3ed974429bb0b6`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 933.7 KB (933721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376ac72e170c6ee7e294e6b516620f76917a93a67ef0705aa9351f96dd8e08d4`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ced2b1d3306d87cd62cec65e18dba5064386d5b20d78aa834138b493ccae3ac`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e5d4f0408a6e94afd9cb9285d74583a29287d726b226e2818f4d8181a82be`  
		Last Modified: Fri, 19 Dec 2025 18:54:33 GMT  
		Size: 294.8 MB (294815995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f31927b28a041a22e274a675ad6c346e1918a7b6c0f9ff56774d8fe6e6a7cb`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 5.0 KB (5005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:f7c968b45502d0c39d85b2be2a2af321f4c0db48f36c5333f84cfda4892bc2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7806f7be971b81eb6bd00255af9488fdedf2b84af6aec7cf7b42852851eefb1`

```dockerfile
```

-	Layers:
	-	`sha256:5eb8e9025022d723d2d32617658c24f97b8eb6b312f229d4294fc5ab0a3db053`  
		Last Modified: Fri, 19 Dec 2025 20:07:53 GMT  
		Size: 2.7 MB (2668873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c714cb47e7a45d2c5af645eb5778d6bad96ffa0fc8e8d9e71e855e55a0748a`  
		Last Modified: Fri, 19 Dec 2025 20:07:54 GMT  
		Size: 28.8 KB (28792 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:41d3045f9b8575dd5070cc760db5da659067747ff782e55284cfefac449db519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312538494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8879c0828d78dc79a36a09e861928116e5485e1d41fdbb1dc0c57329d16e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 19 Dec 2025 18:53:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 19 Dec 2025 18:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 18:53:39 GMT
ENV GOSU_VERSION=1.19
# Fri, 19 Dec 2025 18:53:39 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 19 Dec 2025 18:53:39 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 19 Dec 2025 18:53:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 19 Dec 2025 18:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 19 Dec 2025 18:53:39 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 19 Dec 2025 18:53:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 19 Dec 2025 18:53:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 19 Dec 2025 18:53:39 GMT
ENV MONGO_MAJOR=8.2
# Fri, 19 Dec 2025 18:53:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 19 Dec 2025 18:53:39 GMT
ENV MONGO_VERSION=8.2.3
# Fri, 19 Dec 2025 18:54:00 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 19 Dec 2025 18:54:00 GMT
VOLUME [/data/db /data/configdb]
# Fri, 19 Dec 2025 18:54:00 GMT
ENV HOME=/data/db
# Fri, 19 Dec 2025 18:54:00 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 19 Dec 2025 18:54:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:54:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:54:00 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 19 Dec 2025 18:54:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6c93d4528b48d6009b14db5449fe1ab781c036306d04878e97ff8058714e3c`  
		Last Modified: Fri, 19 Dec 2025 18:54:51 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1d960a65675ebd01b7aec52ad60a9d58ca1b5930d084aa65df2d4d26a4cfa0`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 1.5 MB (1494212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90aac4a84565e81d1b2a7ba73cbff2f51e631226c6c23e4c3ff179a3028087e6`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 886.0 KB (885960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab1583455871f1b05a4c17d88636ffef27673934cc53fb5da576c4887b5e5fb`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb9ad4997b8b44ddda18e96138e6c3f131c4ed90582aca8b019c91fdab28950`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec3fd50f49f6d11df2c4b35e8d33499da45d2dc6b9048b832ae1d144c0858ac`  
		Last Modified: Fri, 19 Dec 2025 18:57:29 GMT  
		Size: 281.3 MB (281289763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ff4183d3969317eca4a5acdd02023d9fe6ce73e76ead2a28e6529644f429e5`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 5.0 KB (5006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:838ada4774c3a1bbc381db4bd63a76bdc700f9e3214794bd4ca85c88ab6da4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adcdbf59af9672e6899427cc2961b26b9018698320d175ca0bfc4dd2008ca00`

```dockerfile
```

-	Layers:
	-	`sha256:2ce8f7b034ed5c1a73b6170b912dff4cf7cfbe4b67a078a65a5c8f9ad7555d37`  
		Last Modified: Fri, 19 Dec 2025 20:07:50 GMT  
		Size: 2.7 MB (2670009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fce2d6033e186ab239a07846bc3904696bd9570943af23b63779dbb6c79870d5`  
		Last Modified: Fri, 19 Dec 2025 20:07:49 GMT  
		Size: 29.0 KB (29019 bytes)  
		MIME: application/vnd.in-toto+json
