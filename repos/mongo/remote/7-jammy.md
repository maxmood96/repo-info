## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:314a1242a514ccfc6fedd97d8426cdd57555d3e9aa03cc6764edab99d4eec3aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:3e94e41213f2942963eb834940dbc78654754908593cd26f33df8f51553344ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279784538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d200c8650208b87e833e43bc2c8b029a92adc296f1d467c8604b81f3dddff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:30:56 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 13 Nov 2025 23:31:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 23:31:17 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 13 Nov 2025 23:31:17 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 13 Nov 2025 23:31:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 13 Nov 2025 23:31:17 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 13 Nov 2025 23:31:17 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 13 Nov 2025 23:31:17 GMT
ENV MONGO_MAJOR=7.0
# Thu, 13 Nov 2025 23:31:17 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
ENV MONGO_VERSION=7.0.25
# Thu, 13 Nov 2025 23:31:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 13 Nov 2025 23:31:38 GMT
VOLUME [/data/db /data/configdb]
# Thu, 13 Nov 2025 23:31:38 GMT
ENV HOME=/data/db
# Thu, 13 Nov 2025 23:31:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:31:38 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 13 Nov 2025 23:31:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febe548a5fe0d7482ee1e9649f09d3116e6f8f2c536d8996fa7e9c3f2529ea0e`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0577f0c5ac79e75e27bdcbae088ee808a14f5177c64faa693c0d450d88cfe`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 1.5 MB (1513900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bb42539a6eecc3312b4dff7426141ad0800c712ad8f7dfcd6601b89cdbc300`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 898.1 KB (898129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2f7dfc9d56fd0d33ab3003de2002af9ef9a4cf1938b023f29e426a7adddef`  
		Last Modified: Thu, 13 Nov 2025 23:32:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3370660e379324a2ef299dee8cf9cd94b20cd745f41a300900e22e3ca082fe81`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423feecba649506af1ed9d63501b66ea6b446b1dbbe9afc9ae734e9d582dd2fd`  
		Last Modified: Fri, 14 Nov 2025 00:33:18 GMT  
		Size: 247.8 MB (247828545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213a7d95f2f6b458bb809edc19804ae91797aa954d68234046f0f2efc319f05a`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:8bcef27b041d824418b7f6348469304bcbb2b2a30f17108326b76ff7dc6349ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e500947796962cd809bd43dcf8a8789e75a1611cec4e52dadc439338a36a6040`

```dockerfile
```

-	Layers:
	-	`sha256:2c6fdcfc318cc26678a9435258bcfa31c0f620df45195b413d5f0ec867ad3bad`  
		Last Modified: Fri, 14 Nov 2025 02:07:35 GMT  
		Size: 3.2 MB (3223939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d0e52bc181844ae7d2b0f5270c66342ebb98ece96c6476c752c65365f78420`  
		Last Modified: Fri, 14 Nov 2025 02:07:36 GMT  
		Size: 27.9 KB (27943 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4ee06b29399f0d093a0f8c222193d614f75626d33086ae9e0c78e4facf7bf013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.0 MB (267045294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c253d4ebb32e2b91250e087ad3c225c7977870dcd66afe47e07165b8d4daed2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:30:19 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 13 Nov 2025 23:30:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:30:41 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 23:30:41 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 13 Nov 2025 23:30:41 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 13 Nov 2025 23:30:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 23:30:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:30:41 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 13 Nov 2025 23:30:41 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 13 Nov 2025 23:30:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 13 Nov 2025 23:30:41 GMT
ENV MONGO_MAJOR=7.0
# Thu, 13 Nov 2025 23:30:41 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 13 Nov 2025 23:30:41 GMT
ENV MONGO_VERSION=7.0.25
# Thu, 13 Nov 2025 23:31:02 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 13 Nov 2025 23:31:02 GMT
VOLUME [/data/db /data/configdb]
# Thu, 13 Nov 2025 23:31:02 GMT
ENV HOME=/data/db
# Thu, 13 Nov 2025 23:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:31:02 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 13 Nov 2025 23:31:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941627ca1bf46d45e6ac4eabf60f7d339ab9de264fcaf29a1d59e1d81e002a89`  
		Last Modified: Thu, 13 Nov 2025 23:31:41 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2afca6323317f0195e21065525b277f638b62bd351def2b3c50c6ca8cb019`  
		Last Modified: Thu, 13 Nov 2025 23:31:41 GMT  
		Size: 1.5 MB (1482424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3ea6d00797e54807253c64f0be47d9115e0efe1d8525a2fb5d82becb1d11a0`  
		Last Modified: Thu, 13 Nov 2025 23:31:41 GMT  
		Size: 850.5 KB (850513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a60032d5848e99ddd0ddfcab78f5d5d86a418a97a690ec7bcc4710d9c51e6d6`  
		Last Modified: Thu, 13 Nov 2025 23:31:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63d4d0d884d4f04ae597de49694d125a6caf4ac47aeb79cccf5af79db5da320`  
		Last Modified: Thu, 13 Nov 2025 23:31:41 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8892c2f68a49f7f6809a1dc39efef0957eb1c5ea5be7214710b6cfc0f8b182`  
		Last Modified: Fri, 14 Nov 2025 00:32:40 GMT  
		Size: 237.3 MB (237321309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ef8391cb7dcfd51cdfb21cfe7ee5c9b556bbbfe0ab055c5e8ba7b25ccff2e`  
		Last Modified: Thu, 13 Nov 2025 23:31:41 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:a10877131ef9e66a227703a0bf255464c5bdba03e8074644cb08719de8f15e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40b59da2fbccb8f3ecd1f6ecd9b26e3b12e810e28f65438af00375d93deea43`

```dockerfile
```

-	Layers:
	-	`sha256:2a13190a037fcb1e19a84d9d6759905976eeb38df3f9cf668a249612cdbb10f3`  
		Last Modified: Fri, 14 Nov 2025 00:32:33 GMT  
		Size: 3.2 MB (3224258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a15a811e389c2b07fb014505face381090cc288003124672709c79e9ca7b22`  
		Last Modified: Fri, 14 Nov 2025 00:32:32 GMT  
		Size: 28.1 KB (28146 bytes)  
		MIME: application/vnd.in-toto+json
