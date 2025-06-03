## `mongo:8-noble`

```console
$ docker pull mongo@sha256:c62941346f86428a2ff60d0b77d1c400f5b78d19d519b88e6484930cb058782e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:7bedd3932a37cd38c056993a198f76ec5b674b9c82f908edc0b27a9a5a9899a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291355266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5625b96e2f902e639ace95673207cebf11e5f69cd8031451f023238339f64a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 01 May 2025 22:01:24 GMT
ARG RELEASE
# Thu, 01 May 2025 22:01:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 May 2025 22:01:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 May 2025 22:01:24 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 May 2025 22:01:24 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 01 May 2025 22:01:24 GMT
CMD ["/bin/bash"]
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 01 May 2025 22:01:24 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 01 May 2025 22:01:24 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 01 May 2025 22:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 01 May 2025 22:01:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_MAJOR=8.0
# Thu, 01 May 2025 22:01:24 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 22:01:24 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 01 May 2025 22:01:24 GMT
VOLUME [/data/db /data/configdb]
# Thu, 01 May 2025 22:01:24 GMT
ENV HOME=/data/db
# Thu, 01 May 2025 22:01:24 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Thu, 01 May 2025 22:01:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 22:01:24 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 01 May 2025 22:01:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886e2901cc3cfbfbe8e093367296824145b2848aed762000c7e06afc2abde6e9`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e5496c463cb192be03a1ee49eda03040673b46deb595b7aba648746df88da5`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 1.5 MB (1508664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ff3887af58c217a0686d810b0fd0fa00ef4078e49c25f94f8c12a30d7e04e6`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 1.1 MB (1131199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe348f35d71cdd1963a59603c3770ab49416d705b6459d6e922d10fcc4552fef`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370025c3b5a0f7549b4edc071f05b6f831b9401b02172e083a5e11002379ed24`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d10e96e8208cf658592312721ea11b65fd4319d9b0b0e7d5019868a312272b2`  
		Last Modified: Tue, 03 Jun 2025 13:32:01 GMT  
		Size: 259.0 MB (258993470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c414ac2a616f7b40de76022e3ed1dc0359f95761e1a76980ff5d5b8ceb035f7f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:cd9779e582499c104d1e9b455dd2a153ad7d5682b740594d8cad0dbed1bfc09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2577953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f88b681846b002f588f4f366b8b332fdfb42454f6ad513344f10de27478c5a3`

```dockerfile
```

-	Layers:
	-	`sha256:cb38c51e3dabe26c474dd4012ac8dc1cf4327e810ae0b226606acdfa11f8888a`  
		Last Modified: Tue, 03 Jun 2025 14:01:41 GMT  
		Size: 2.5 MB (2549114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fdd59aad38c0bc348dfd0ebb98278674a9ef2f683398dbeda4e42a22955e1b3`  
		Last Modified: Tue, 03 Jun 2025 14:01:42 GMT  
		Size: 28.8 KB (28839 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:3a3873e1e17a9bb86a95e93fe3cd70108cc0d21604221e129433ac83afc7278c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279373973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d10d3f771582209fd73129f4ac1e818157434d3758bdeefbec03b848ae9028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 01 May 2025 22:01:24 GMT
ARG RELEASE
# Thu, 01 May 2025 22:01:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 May 2025 22:01:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 May 2025 22:01:24 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 May 2025 22:01:24 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 01 May 2025 22:01:24 GMT
CMD ["/bin/bash"]
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 01 May 2025 22:01:24 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 01 May 2025 22:01:24 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 01 May 2025 22:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 01 May 2025 22:01:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_MAJOR=8.0
# Thu, 01 May 2025 22:01:24 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 22:01:24 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 01 May 2025 22:01:24 GMT
VOLUME [/data/db /data/configdb]
# Thu, 01 May 2025 22:01:24 GMT
ENV HOME=/data/db
# Thu, 01 May 2025 22:01:24 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Thu, 01 May 2025 22:01:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 22:01:24 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 01 May 2025 22:01:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74a1ae4187ca39441ce0280ed46f7e940011001904496c194c96afa952b28e8`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c2bac4974367e8dbec6564f432778bc4687507d85d598684d0ccf0728f8e73`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 1.5 MB (1493004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae5faba732408a4f893e98413513cfaf16ee8ff23809a49b06ce28fd1d392af`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 1.1 MB (1061543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f97c411657c7125b4349041cfa15b3cd2adb7f555f5f1a37b720b8cbd19ff26`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723d46de0012aa6f0ff8e889af05e7f7f5ba4bb4a3a83a3360bb8d08646ba7e9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28af5706c1aa16e6533679d84c8b9ae5ee8fde94ea73467e9b01eda592bf41ca`  
		Last Modified: Tue, 03 Jun 2025 13:32:38 GMT  
		Size: 248.0 MB (247960933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd2fb6560a5390d494487698c464bb05bd17e3d96574066457ec099de2f8ce6`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:3d8c56a1f26657f6895893466929285ef73bbf3f011c13f38a8d632a00ca5d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2579317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfcdb1a37979b3442a9631bf19bd08fef4af385b734a00f18eae1276115c3bc`

```dockerfile
```

-	Layers:
	-	`sha256:af8e1c07d63d1ab1de464f3ca7f120c602245e3570444deb2802e40765a6231b`  
		Last Modified: Tue, 03 Jun 2025 14:01:53 GMT  
		Size: 2.6 MB (2550250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5a9a4fc5750bba03291285f6bb9aff9fb6f43b154c6affbdef55a152e7c94f`  
		Last Modified: Tue, 03 Jun 2025 14:01:54 GMT  
		Size: 29.1 KB (29067 bytes)  
		MIME: application/vnd.in-toto+json
