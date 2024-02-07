## `mongo:4-focal`

```console
$ docker pull mongo@sha256:f451397e6aa3750ce166397302feeec2e52fdfe38842844da0a9cb01f7decc6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:c3b2171beb51b5767403521feee4c36a3b6b59ceacedcc8044c1c447e8fbd67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173025912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bb05499e92192be1d12a960b027d7a1e7efe60c8a442282cd3d3ce83f55b58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV GOSU_VERSION=1.17
# Wed, 07 Feb 2024 00:59:03 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-4.4.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '20691EEC35216C63CAF66CE1656408E390CFB1F5' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_MAJOR=4.4
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_VERSION=4.4.28
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
VOLUME [/data/db /data/configdb]
# Wed, 07 Feb 2024 00:59:03 GMT
ENV HOME=/data/db
# Wed, 07 Feb 2024 00:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 00:59:03 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1cda98b0ec65f8a47123d1d130ea7c51f19a46aad5e97763e78b5cb73c69b1`  
		Last Modified: Wed, 07 Feb 2024 01:51:01 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f754b81d9887cc9a528e0dd86cbc62c0aac55f1edafa1bd784409d2d877bb4`  
		Last Modified: Wed, 07 Feb 2024 01:51:01 GMT  
		Size: 3.1 MB (3074617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd491944c4ca0bffb9540690a44398ff51fc9953c854392e38d730117f2fd45`  
		Last Modified: Wed, 07 Feb 2024 01:51:01 GMT  
		Size: 1.1 MB (1091408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dc08aa9dbdf21eca5f597ac9e5d1552f1b34db92d52068fd4e78bebb9dea13`  
		Last Modified: Wed, 07 Feb 2024 01:51:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660d7f0909715a48a6477369882de11d710f68785fcfe9fafac288a2c47c794`  
		Last Modified: Wed, 07 Feb 2024 01:51:02 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faffbc42b330659c18a8ed931bc3773c08f68a860775abeda41e53f5375ba96f`  
		Last Modified: Wed, 07 Feb 2024 01:51:04 GMT  
		Size: 141.3 MB (141337805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2051c8ea4db54896434b5ed1068f5b98800d246988c4181615626651a153e51d`  
		Last Modified: Wed, 07 Feb 2024 01:51:02 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:52f8a4a3c7ff7143c087c7bd7a60b8d68168d588f42626cb0f059732335a2945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567eff1acadc182131003e9dccaa67479e56b2c355c2efb960956a3b5dfd24f4`

```dockerfile
```

-	Layers:
	-	`sha256:3dd46f89c4edea37745b7479d0fd57c69db666bee7299fcdff2894c1498955a4`  
		Last Modified: Wed, 07 Feb 2024 01:51:01 GMT  
		Size: 2.6 MB (2607053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb2daed77d2f98071281bc7a2ae98df533018d05172b758dfa434d86b69d6ce`  
		Last Modified: Wed, 07 Feb 2024 01:51:01 GMT  
		Size: 26.8 KB (26832 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:7819de335de513e81a8afc63a7f3fa86d4bbae7c30f8e0940d72ae9b924c10f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168272549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7d3ae76c8b76750903a9e2885b43b1ca547dbaf7a0fd7521842484248bacaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV GOSU_VERSION=1.17
# Wed, 07 Feb 2024 00:59:03 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-4.4.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '20691EEC35216C63CAF66CE1656408E390CFB1F5' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_MAJOR=4.4
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_VERSION=4.4.28
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
VOLUME [/data/db /data/configdb]
# Wed, 07 Feb 2024 00:59:03 GMT
ENV HOME=/data/db
# Wed, 07 Feb 2024 00:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 00:59:03 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234fb188b2907c9715c7137a90acbfd86a567df40cb64cba4347f0e70b62bf32`  
		Last Modified: Sat, 03 Feb 2024 08:43:47 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3e56574048716548ffedbd95cd3f241e84077f8afa6862852f8eebe3c60a9f`  
		Last Modified: Wed, 07 Feb 2024 02:31:59 GMT  
		Size: 2.9 MB (2927602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adda3404e07ff98ab203ee0e2081cc749594009b960611c735ecb1189f6fb9f2`  
		Last Modified: Wed, 07 Feb 2024 02:33:24 GMT  
		Size: 1.0 MB (1023724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a8b8a8e02ee59dc295f023a3bbccb9e76025c101bcfc5c0a86fa00ba0560c`  
		Last Modified: Wed, 07 Feb 2024 02:33:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4c3428fb423dffd3be491a8912830972e23e616ae7c9a358a8c776be3f97d4`  
		Last Modified: Wed, 07 Feb 2024 02:33:24 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974e917490b6a3b8e8237fdbd46521727560c201e90e2400335ff78a0033cb5c`  
		Last Modified: Wed, 07 Feb 2024 02:33:28 GMT  
		Size: 138.3 MB (138338469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0bd6199d1a2df88838a9f056b844f4e9f4a5457b77685a3ab4eecf45c070bb`  
		Last Modified: Wed, 07 Feb 2024 02:33:25 GMT  
		Size: 5.0 KB (4994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:01fb5a073ed17f76ab5de8bd3cd6f7d880bbe03168b4946cef729f3af9b93894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5639d4f917ddbe63673eafbb9a215d64ba537a6861bc2d0f9807a77fbefa5146`

```dockerfile
```

-	Layers:
	-	`sha256:dcbac06ebae23a68d6af195b5fe9779965046580911e701378d3cf35426a429b`  
		Last Modified: Wed, 07 Feb 2024 02:33:24 GMT  
		Size: 2.6 MB (2607392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d243558cd28d3ef664fbac134eb937d261c300c0d0a01adcaf1cf8d75cd3d48`  
		Last Modified: Wed, 07 Feb 2024 02:33:24 GMT  
		Size: 26.7 KB (26684 bytes)  
		MIME: application/vnd.in-toto+json
