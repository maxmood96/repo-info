## `mongo:jammy`

```console
$ docker pull mongo@sha256:6cebec2ff800e0fb051f73a6c37feec1a17442a6222b9e0eaa7a20d1f4d4cf9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:6d245af0e8dffc8771f3e734b4ee0bc7fcde48fcffe3bf2664592dfda8e9e6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258716192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2076a62a1ced8bc62d7963c2e04d7b5fdf3358503fd0daaa4688fb227c1ec35b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 28 Jun 2024 22:05:28 GMT
ARG RELEASE
# Fri, 28 Jun 2024 22:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Jun 2024 22:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Jun 2024 22:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Jun 2024 22:05:28 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Fri, 28 Jun 2024 22:05:28 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 28 Jun 2024 22:05:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_MAJOR=7.0
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 28 Jun 2024 22:05:28 GMT
ENV HOME=/data/db
# Fri, 28 Jun 2024 22:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 22:05:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 28 Jun 2024 22:05:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7a238bbe68584686a4ebcb3f11e2d5c8c482f89d9bc10bd3a1cc8d865ce2e`  
		Last Modified: Sat, 17 Aug 2024 02:05:52 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b2514837c958dcc097c5dd0234fc9c13927bfdffffbdf7c42ba698848a87d1`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 1.5 MB (1500849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22133372085a3b8bced4ea88fad92b9133bb845a5406ea0a9665765482f0513c`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 1.1 MB (1094738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcbe55d7d81bb77a2097a01cf0b352928b24413bc00c910dfb8c641f290026`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8896cc7f272b5725dc5085436b3d6d2a87ff5222b0b2567f417a617549fc61`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21700c8b485401880278b1ceb01d37f902936ba1cbbe07ec4c426f54c3f36fe3`  
		Last Modified: Sat, 17 Aug 2024 02:05:56 GMT  
		Size: 226.6 MB (226577422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6268a37a75c7ce0206e22b8130d842787a1aad5a18afa44861d9d6fd9cda3cd`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 5.0 KB (4993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:547811295ce6ee3b6be4ba8084ac045d82214c317b3fd7cf2ceb5a5250cec3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba06afa1c71d48412bf99e98711bcbef7558ecf442468829d5f843db10f78dbf`

```dockerfile
```

-	Layers:
	-	`sha256:771bd0e9fdb41d0715e006a78edc27267223ef565234ec3f312eb9fbd3cb345d`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 3.0 MB (3029337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa424203b8eaa5e5a195192380be79ff983487fc4d661e5b3b696f1233a9763b`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 27.6 KB (27635 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:5945eed557f9893a6cd97a5da1bf539d799e8f177f277ba9b8e9ca69fc31cf33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247410007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb433c5673fbd6b81f689c590d7c3e0f0f21605097c4284998bdd20a8df0bbd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 28 Jun 2024 22:05:28 GMT
ARG RELEASE
# Fri, 28 Jun 2024 22:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Jun 2024 22:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Jun 2024 22:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Jun 2024 22:05:28 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Fri, 28 Jun 2024 22:05:28 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 28 Jun 2024 22:05:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_MAJOR=7.0
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 28 Jun 2024 22:05:28 GMT
ENV HOME=/data/db
# Fri, 28 Jun 2024 22:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 22:05:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 28 Jun 2024 22:05:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5099c6f371c3636e69be7e06e54581f64b8c31de3c79ee2e511aab3b0621b`  
		Last Modified: Sat, 17 Aug 2024 03:19:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b46311ab598f2b54f733e70bf994f009a4d0e96b1ca8244fe0c81dfda8c066`  
		Last Modified: Sat, 17 Aug 2024 03:19:08 GMT  
		Size: 1.5 MB (1465923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9146fb61af94e0deb301e0cef12da9e4ffd3a8a431718e21541326216691a5f8`  
		Last Modified: Sat, 17 Aug 2024 03:20:37 GMT  
		Size: 1.0 MB (1027463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a0a89625025b9e7214ea8f6e2258c5b34df7da73eabffaa97ad0a07f7d59cd`  
		Last Modified: Sat, 17 Aug 2024 03:20:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c457f686dcebd7d60a3c49f6449d22c22689171d7fec907183e1eb96d549543`  
		Last Modified: Sat, 17 Aug 2024 03:20:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991699882dca0731dd619c9b68fe29365c3fb8e94f9b5fbee8e9947167be76a`  
		Last Modified: Sat, 17 Aug 2024 03:20:43 GMT  
		Size: 217.6 MB (217550774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aa7657b86eae87e89e02d2d473df09b73e9deb0439d2d03229ef427c455e4c`  
		Last Modified: Sat, 17 Aug 2024 03:20:37 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:b3fd758c14b60976ccae20eaca8d40c665b3a6293521f1c0e6a6cf46ec23d56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a18e7b4ad1b94e53ea3caae766ba66c45ad39ff5af8f91bd247902f18b88f4`

```dockerfile
```

-	Layers:
	-	`sha256:2adf976235c8a2ab881c511daf33547727025835b21f054be71edffb49f34cc9`  
		Last Modified: Sat, 17 Aug 2024 03:20:37 GMT  
		Size: 3.0 MB (3029679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004311c68a974e8ea16c29bef5c831266e0e759088878bca39d722b02042e548`  
		Last Modified: Sat, 17 Aug 2024 03:20:36 GMT  
		Size: 28.0 KB (27985 bytes)  
		MIME: application/vnd.in-toto+json
