## `mongo:jammy`

```console
$ docker pull mongo@sha256:a3b0264080e8fb5aa4e02bc0af3734340f11a0fd3a85d6122b2281aa6b9a3a3a
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
$ docker pull mongo@sha256:a05983f0fed3fefb07bfd8a4944661d5082e0f7a0c5c7ebb99eb66309a568896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253131560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba30a929272d9e89bf1a2c03962c4b48dde15ff5debfd29c4f886db972009e4a`
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
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
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
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3043a828317f90526bc796d34c21e5d39070ccd0952802b5ba3cec982df51912`  
		Last Modified: Mon, 05 Feb 2024 18:49:25 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db79f36a996fde9fb2962fadff36f849a3f3636e81465a8b9feb46970ed2410`  
		Last Modified: Mon, 05 Feb 2024 18:49:25 GMT  
		Size: 5.0 MB (4990340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bf25247bb52286fb0887a98122b321e7dfd501f756d57b42a95bf47bb8bc6f`  
		Last Modified: Mon, 05 Feb 2024 18:49:25 GMT  
		Size: 1.0 MB (1032808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e4aff435a6c8bdd0861d80a5b150525e6f5cee8e0b46fa9d5c4ed3c36200e0`  
		Last Modified: Mon, 05 Feb 2024 18:49:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750a9cdaae9af2387a63de016fc7289142d18dd13244ddcf9fbc31767c414ba8`  
		Last Modified: Mon, 05 Feb 2024 18:49:26 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc4e110b18ab96e2eaf30cf4815923ea13b7ca808d061ddb6a048c3066e24d8`  
		Last Modified: Mon, 05 Feb 2024 18:49:26 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50bd2c08235f936b5e83c9cf8d703c573c5c72a61b4c6a9ce27eb632c3d814e`  
		Last Modified: Mon, 05 Feb 2024 18:49:31 GMT  
		Size: 219.7 MB (219743298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26b9ad81480983379e3f4e2e34d6dd583a7be549c4782a5bbf200c5ec12436f`  
		Last Modified: Mon, 05 Feb 2024 18:49:26 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:7c19c8bd4a52533470669154cd60550b1120e9d4104909b8dfb78c9027778400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564d270c96e44d51cb4d13ad5615ceed0c2cbdf6d2120b4ff8053f07fbefb983`

```dockerfile
```

-	Layers:
	-	`sha256:c322c132aadb7eacbe1af33bcf6213b7cbe53952968d9b72a715154a8576caf1`  
		Last Modified: Mon, 05 Feb 2024 18:49:25 GMT  
		Size: 2.7 MB (2728793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3310231345bda3197e7f18c5dfd9aaf04abc1c3d76658e9ec5404cefea46f6`  
		Last Modified: Mon, 05 Feb 2024 18:49:25 GMT  
		Size: 29.4 KB (29383 bytes)  
		MIME: application/vnd.in-toto+json
