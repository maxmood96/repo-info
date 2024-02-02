## `mongo:4-focal`

```console
$ docker pull mongo@sha256:e4c02e1e840cbd0413b9cd3d7ef11c38cb6f25dbe4e2f97d3fb069960c80ebf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:32f68f7c95cfd33025f72caf3ebbd394b6ca7f396e5c968095480e7e173f5107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176314071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71014c81a0f9f5bc180319a274539a2c2131156f255a2eeff8357138e638eab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Jan 2024 17:01:11 GMT
ARG RELEASE
# Thu, 18 Jan 2024 17:01:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 17:01:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 17:01:11 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jan 2024 17:01:11 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Thu, 18 Jan 2024 17:01:11 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:01:11 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:01:11 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 18 Jan 2024 17:01:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 18 Jan 2024 17:01:11 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 18 Jan 2024 17:01:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 18 Jan 2024 17:01:11 GMT
ENV MONGO_MAJOR=4.4
# Thu, 18 Jan 2024 17:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
ENV MONGO_VERSION=4.4.28
# Thu, 18 Jan 2024 17:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
VOLUME [/data/db /data/configdb]
# Thu, 18 Jan 2024 17:01:11 GMT
ENV HOME=/data/db
# Thu, 18 Jan 2024 17:01:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:01:11 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 18 Jan 2024 17:01:11 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87203314cdf36368ed667d992a18920aa7c8a3b43bb2b9b513670c77101a6cd`  
		Last Modified: Fri, 02 Feb 2024 00:55:55 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fd0cd199eca5a990b5d0bbce440f102c2c48544acfb3423bfd5fe4db303fc5`  
		Last Modified: Fri, 02 Feb 2024 00:55:56 GMT  
		Size: 8.4 MB (8373012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d94a571dac1fe660f074d2fc21f8952e4dc8a7f6706417af1317200752b92b`  
		Last Modified: Fri, 02 Feb 2024 00:55:56 GMT  
		Size: 1.1 MB (1100467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5bacd0f7147199d140b0a05fdf0689548e17b2fb09842bc452a95ee865c764`  
		Last Modified: Fri, 02 Feb 2024 00:55:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c90867523a4883310b760fe4cf9c7385cffbdcf8efa76700094fd631ce406c`  
		Last Modified: Fri, 02 Feb 2024 00:55:56 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ef68f8c101d07735e4679b60316d11885c27e7b958b2814b606447c1f20c23`  
		Last Modified: Fri, 02 Feb 2024 00:55:56 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23cdbba0406a20d42f5578ef85a1e8d070e419ebbcf49e2cb0abaaab8b0b733`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 139.3 MB (139317120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac227d2d3299da47887af09df60fc47e312fdd4ebb7c8628273c2bb5b95caa3c`  
		Last Modified: Fri, 02 Feb 2024 00:55:57 GMT  
		Size: 5.0 KB (4993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:15856ce2d0c4a7239300f4cc66ce5f9f9ab70ba4ecdde9533def4910635ff83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e32e23712143592f02531fbad8dd586ad161337810d78033986e4c9fa3593`

```dockerfile
```

-	Layers:
	-	`sha256:acf74df03bf6052a33b3da1005d35a3ef261954c51b001f0afc80391c6cd71c4`  
		Last Modified: Fri, 02 Feb 2024 00:55:56 GMT  
		Size: 2.7 MB (2723468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:179768c53dae9cdab08b0f70b0acb2b3c47d515f2909bbc77e2440530789773e`  
		Last Modified: Fri, 02 Feb 2024 00:55:55 GMT  
		Size: 28.6 KB (28619 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f72a72df1b8acedbdfb39f8848b8f99af38ecbb85256febf0f7bd1c54ae69cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171549426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fcefaa9eaffcd70a6dc697a06b3df3df9337c45d07ccbd6375f65a774e0a997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:01:11 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:01:11 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 18 Jan 2024 17:01:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 18 Jan 2024 17:01:11 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 18 Jan 2024 17:01:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 18 Jan 2024 17:01:11 GMT
ENV MONGO_MAJOR=4.4
# Thu, 18 Jan 2024 17:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
ENV MONGO_VERSION=4.4.28
# Thu, 18 Jan 2024 17:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
VOLUME [/data/db /data/configdb]
# Thu, 18 Jan 2024 17:01:11 GMT
ENV HOME=/data/db
# Thu, 18 Jan 2024 17:01:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:01:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:01:11 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 18 Jan 2024 17:01:11 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ba6b7451f9d95719ad43508919c914407cf286d0b7fb6e1ee9a02cd51b045`  
		Last Modified: Mon, 18 Dec 2023 19:51:47 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ded41913893fb2c19b7f6cb4b21f0e12639a543c69be1d62dbe3afdf3fbc42`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 8.2 MB (8200494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ab25682bfe74e5ec2f8feaf928bbba54d7139f2c30e2ee063f5b347f288996`  
		Last Modified: Wed, 20 Dec 2023 22:10:12 GMT  
		Size: 1.0 MB (1032196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb81d91cc097017e7f7b40df750f78372e32354fd7495c225c4ffbbd8eab22f8`  
		Last Modified: Wed, 20 Dec 2023 22:10:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8819c2b7ec12b47e18ecfce95bfc0805a0eacf86c83cec477eb62b88084fa3`  
		Last Modified: Wed, 20 Dec 2023 22:33:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d757d8e05c23f189f9807127980ded661aaacb60460df561c074202ca66dd2`  
		Last Modified: Wed, 20 Dec 2023 22:33:16 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3edf585167c0071f493308cdf8f46528ba052351ef82d66a57aa838e2ba6c4`  
		Last Modified: Fri, 19 Jan 2024 04:21:10 GMT  
		Size: 136.3 MB (136333412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304d69c595fa88892be0de1ba0370c7cb9ae94fc6f8227f5f94f003b3f64f799`  
		Last Modified: Fri, 19 Jan 2024 04:21:06 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:21794359f426aecd5df4366f0c4dc24ea2487b4b6bb0f4a462d5c1086af83364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8d5e6b6dd2a12686d708c581dfddf93b0a2d4fb4dc50cf3fc8e3c14fbe8e04`

```dockerfile
```

-	Layers:
	-	`sha256:c9c213ff31e810c7881562e4a2783c4d9db9a5ab8d02fb1bf474254636cc0715`  
		Last Modified: Fri, 19 Jan 2024 04:21:06 GMT  
		Size: 2.7 MB (2723796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27250cf0077ed54c1ce66cc1816b7c30874f65a21b89a95505947943a791676`  
		Last Modified: Fri, 19 Jan 2024 04:21:06 GMT  
		Size: 28.5 KB (28471 bytes)  
		MIME: application/vnd.in-toto+json
