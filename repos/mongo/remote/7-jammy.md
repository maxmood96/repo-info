## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:050e37782ef658826e70b96760de66529b858b767aad668f49a368e974455d6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:7b651890ce6f3ead14e53250d32d8d1f0329faa321d7e178d6e5193c6e2fcc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265516880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b3ba6bed352dc1d776be4a63614c5f39d1b5e284b7515aab0d1646ffc92599`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 May 2024 22:01:34 GMT
ARG RELEASE
# Thu, 23 May 2024 22:01:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 22:01:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 22:01:34 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 23 May 2024 22:01:34 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 23 May 2024 22:01:34 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 May 2024 22:01:34 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_MAJOR=7.0
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_VERSION=7.0.11
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 23 May 2024 22:01:34 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 May 2024 22:01:34 GMT
ENV HOME=/data/db
# Thu, 23 May 2024 22:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 22:01:34 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 23 May 2024 22:01:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f24d0041302a7c0bf7459138b2ed35b7eeef7cba2355b83a6d8088ddc997b9`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfef8821fc6226d0bc344922b4ef14dd84a6c05d27159359a12b845a4df2998`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 1.5 MB (1500765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2b135d9110dce3bbc12911886244fc938c197984c2599a07df46102d4fd1a0`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 1.1 MB (1094590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76154bf34598c7e33d0b21ed9fd726deceb22016abbe63dd91919d70594da21b`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93134489020215d0914960ef5d143295c0186f2eaabf16ddf7d5d94b0bbd16e`  
		Last Modified: Wed, 05 Jun 2024 02:21:38 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1fa78ffcfb0678cf343c2f69625fe6d9285a9c872cb5b9fbbea9ed06391b1d`  
		Last Modified: Wed, 05 Jun 2024 02:21:41 GMT  
		Size: 233.4 MB (233380616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91b3273507c2e1fdd232b09697881d666b9dc9b71164793b9881ce1de4c52bc`  
		Last Modified: Wed, 05 Jun 2024 02:21:38 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:4ec8a4b06b0726e2fcd373b7f3802e0b8531876c0b25c9dceca84be4578e84b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09821ae91f4e4f84acb99b20aeea02f6121836975977b6f34e93a59233498f19`

```dockerfile
```

-	Layers:
	-	`sha256:9690e378086f3e5ae5d690e001383188fb3b45c9a20691043d0fff867c783b9c`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 3.0 MB (3001102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a083280b7900cdd63e9cc5b28b0d543626449bbb3bebc398e6126d2e34f8f3c`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 27.6 KB (27587 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b77b61b24371a890786159373b18172fac47d52a7bb6a41abef2735fec1660b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257368339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bb8ca2cb4faf3a73f048b635a079000ac0705744d7715b7d7e9c4f2f578ce1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 May 2024 22:01:34 GMT
ARG RELEASE
# Thu, 23 May 2024 22:01:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 22:01:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 22:01:34 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 23 May 2024 22:01:34 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 23 May 2024 22:01:34 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 May 2024 22:01:34 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_MAJOR=7.0
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_VERSION=7.0.11
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 23 May 2024 22:01:34 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 May 2024 22:01:34 GMT
ENV HOME=/data/db
# Thu, 23 May 2024 22:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 22:01:34 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 23 May 2024 22:01:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f33a3006c470fcf35e360ed94e30a65c5fe9f95ce0cf0c9ab2243273d4df519`  
		Last Modified: Wed, 05 Jun 2024 16:22:58 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedf0c2fd07791b0a7c85eaf3c323cc949fdc8675f41c70a6bfff588bab98d26`  
		Last Modified: Wed, 05 Jun 2024 16:22:58 GMT  
		Size: 1.5 MB (1467355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f46cd936f683cfcf794bf655b79598309e782291363b3cab7ec7b3abf637b0`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 1.0 MB (1028907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ec972210ed7a766b75b403456bf7587b4268fa84be43afcccc99ed64e028c0`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ba95ff848c1a743d24ad8a63dd57339dfb46e68a153aebc3e61dc2562c8198`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce2268597823db5b1f109875432d69361eed336dda14d2143b0d3ff5df0dcdd`  
		Last Modified: Wed, 05 Jun 2024 16:24:29 GMT  
		Size: 227.5 MB (227503125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b2690426673c98900ec241412a346b96c12b84ffa846cf0295430292553c6c`  
		Last Modified: Wed, 05 Jun 2024 16:24:24 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:10886ea40c504df8eefe844720edba4c31e284527e5c448775fb2344678286a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3029380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2814160134051b5ebfefede1f97df0253673e3d7c59e42fb98058c7e3f6e4405`

```dockerfile
```

-	Layers:
	-	`sha256:1e1e0731a6d932f8b6c94d6cee08bd69d2f7c025b4c1b3b4d3acd61741a587be`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 3.0 MB (3001444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:053ae8ba3f661051809e8ceb46ea28e4f038e9df5bd4c633cc396ee26a2dab89`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 27.9 KB (27936 bytes)  
		MIME: application/vnd.in-toto+json
