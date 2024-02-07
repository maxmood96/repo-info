## `mongo:jammy`

```console
$ docker pull mongo@sha256:766e7a263169ed1084dbefe70499cf4cb20f7d9636b0995e6a1b3052c7e74122
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:d593866fcb8872eb3021c55cb5739d12ce63efdde9f57a2c650118f0052cc5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261308905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50de30b43cadc17a46f655a0955942ab9790b7384dde444caba0f7072ec29625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 06 Jan 2024 05:07:23 GMT
ARG RELEASE
# Sat, 06 Jan 2024 05:07:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 06 Jan 2024 05:07:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 06 Jan 2024 05:07:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 06 Jan 2024 05:07:23 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Sat, 06 Jan 2024 05:07:23 GMT
CMD ["/bin/bash"]
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV GOSU_VERSION=1.16
# Sat, 06 Jan 2024 05:07:23 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_MAJOR=7.0
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_VERSION=7.0.5
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
VOLUME [/data/db /data/configdb]
# Sat, 06 Jan 2024 05:07:23 GMT
ENV HOME=/data/db
# Sat, 06 Jan 2024 05:07:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jan 2024 05:07:23 GMT
EXPOSE map[27017/tcp:{}]
# Sat, 06 Jan 2024 05:07:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ded68502327f9abc69bbb09354baed995ca81cc8bf775b89bd9a88a4b25c92d`  
		Last Modified: Fri, 02 Feb 2024 00:56:04 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b2700cb3f29336ae4b4d11ba84ba6b5b2ef17d898891cb9acd12237fb0a970`  
		Last Modified: Fri, 02 Feb 2024 00:56:05 GMT  
		Size: 5.0 MB (5049177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c78628995a6c3d2a6e1ac9450a4084d0ca3f902f13e4c0c71c5af071be315d`  
		Last Modified: Fri, 02 Feb 2024 00:56:04 GMT  
		Size: 1.1 MB (1100997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f3a3fe93a2f62de967eae39b837c72e9f8ae364c5a4d183edb85f7aa51cdfc`  
		Last Modified: Fri, 02 Feb 2024 00:56:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbdadf2860f385aa3ee9e7a6a21c995785542b611a806904a6a1b97b2a1cdb0`  
		Last Modified: Fri, 02 Feb 2024 00:56:05 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8050fbbed2fd73f9b8c9a53a714a5c0ecc3af0de284e91a62975f9c67b116b26`  
		Last Modified: Fri, 02 Feb 2024 00:56:05 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d012f43ecccabb6a6b619d6364a64bc6ed425d02afb9af4e3912d05646273de`  
		Last Modified: Fri, 02 Feb 2024 00:56:28 GMT  
		Size: 225.6 MB (225601238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80634cd52614de26770940f942f3a22a1ef7b4a11bbcb64162f957d4aa4f8015`  
		Last Modified: Fri, 02 Feb 2024 00:56:06 GMT  
		Size: 5.0 KB (4994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:128fe226b390477fa4a7bc7abb5b4a96d28494bebc70ac1b8fe083a24d70b8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f62b7386c4886868ab6657884adb137131e03acb20e998b1e075f5db1873d0`

```dockerfile
```

-	Layers:
	-	`sha256:a1a18860ab6e90b3af3c3461d8ecd172ee91d1315c702a39bf2d519219f442c6`  
		Last Modified: Fri, 02 Feb 2024 00:56:04 GMT  
		Size: 2.7 MB (2729173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556f9cf2e2f39270ab6f1c3a3a8d40a96b73e101cfaa665558d7946863a0b3ae`  
		Last Modified: Fri, 02 Feb 2024 00:56:04 GMT  
		Size: 29.5 KB (29526 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:7a6e1cc99026b31f259b243e60560dbc8eec1d66ddb884a35ad424896aaaa278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249956436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc88d61af2bb604e7349715b4189021c0cc0472190b0a3829d2b98daf78ca1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_MAJOR=7.0
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_VERSION=7.0.5
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
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
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3043a828317f90526bc796d34c21e5d39070ccd0952802b5ba3cec982df51912`  
		Last Modified: Mon, 05 Feb 2024 18:49:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62ab884678dcc6edb5b99b1a6ab0fd19682a78ab87ffefb11610f1fd8eaf7a5`  
		Last Modified: Wed, 07 Feb 2024 02:29:04 GMT  
		Size: 1.5 MB (1465198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec9ed1aa2368c185f2be61dc5fd92f17ac0bc9c827da8b419833999e1e63910`  
		Last Modified: Wed, 07 Feb 2024 02:29:04 GMT  
		Size: 1.0 MB (1026695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9624113956abcfd97a9cfc784ac2bc0f7f10b32317ebe04a95065b4f0dda44b4`  
		Last Modified: Wed, 07 Feb 2024 02:29:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58c3149c62807bf87af638fe4e6013d2cd10a1b821fd47d0a0ea822c903a794`  
		Last Modified: Wed, 07 Feb 2024 02:29:04 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a8880dddf521b53f316086d7f12128c376d1f7b65b568d4e745faa5bfd2940`  
		Last Modified: Wed, 07 Feb 2024 02:29:11 GMT  
		Size: 220.1 MB (220100834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe7ec2c07e60a83f4f129675e6df964fcc2f1aa68ebe7e43e81e2064306438d`  
		Last Modified: Wed, 07 Feb 2024 02:29:06 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:49b933e997e429cfbc70bc8098f2f1eb7a7ad349d52d53c15beae4d2faae47f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238f12b3911b044d943ac34b8786d1079cbefa1cac099170afced002dde18ccc`

```dockerfile
```

-	Layers:
	-	`sha256:79f254cd500f721ba14a11e682e76e164fb79fb3a34a909c75ff341c4304d967`  
		Last Modified: Wed, 07 Feb 2024 02:29:05 GMT  
		Size: 2.6 MB (2615387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e2ef33155a85c0595f7e8a4033efdb50cca5e64b75115d2f7bc8389a4e4d9f`  
		Last Modified: Wed, 07 Feb 2024 02:29:04 GMT  
		Size: 27.6 KB (27591 bytes)  
		MIME: application/vnd.in-toto+json
