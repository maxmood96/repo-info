## `mongo:4-focal`

```console
$ docker pull mongo@sha256:7c5c6581217c4775518387ac211d010209668950120544fb340f5ea2edc493d4
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
