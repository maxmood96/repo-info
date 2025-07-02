## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:a0a716283fbf7f7352660d65507461a655b1cb29ae3c4f11cab63b6c05b02707
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:6a57102d5cc5d6caa4fadebf7a49e974274808e229b12cca6442b5f05a496c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 MB (265686508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba17b94771eda2188e34be52b441df9a836f882b7591875bd731d118568fe1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 03 Jun 2025 22:01:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 22:01:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 22:01:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 22:01:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 22:01:14 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Tue, 03 Jun 2025 22:01:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 22:01:14 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Jun 2025 22:01:14 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 03 Jun 2025 22:01:14 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 03 Jun 2025 22:01:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 03 Jun 2025 22:01:14 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 03 Jun 2025 22:01:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 03 Jun 2025 22:01:14 GMT
ENV MONGO_MAJOR=6.0
# Tue, 03 Jun 2025 22:01:14 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
ENV MONGO_VERSION=6.0.24
# Tue, 03 Jun 2025 22:01:14 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Jun 2025 22:01:14 GMT
ENV HOME=/data/db
# Tue, 03 Jun 2025 22:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 22:01:14 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 03 Jun 2025 22:01:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a764c7a5cbf4b6e563aa7d2cad316c51dc201ca222a73089caf372429e997d8a`  
		Last Modified: Wed, 02 Jul 2025 05:34:30 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa3a52c924b062b905c90ef6a653e91bdf8a2430c66b28bcb0a9e9177b8c7ad`  
		Last Modified: Wed, 02 Jul 2025 05:34:35 GMT  
		Size: 1.5 MB (1513216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7dee31a653d1140b55667e4ef8a73907490ae174cd32037a01da6ead6b9ca`  
		Last Modified: Wed, 02 Jul 2025 05:34:44 GMT  
		Size: 1.1 MB (1095064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94512df871076177f715da34c927f1c72b07a7c716b1dac494411386f31e9cb`  
		Last Modified: Wed, 02 Jul 2025 05:34:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974b590250fcfaaa37965d3000c543412c3215164a015f423a5354c5638d8ac`  
		Last Modified: Wed, 02 Jul 2025 05:34:50 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0272ef2abd88b38fbe616f525ca3a32db80c9ac0629f34b00ceed7b30e7d144a`  
		Last Modified: Wed, 02 Jul 2025 07:07:31 GMT  
		Size: 233.5 MB (233535377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440c965ca82b6a4bb2b0c6afdeb0a9c0bf24a1b1a9b27f48032edfc4ae17804`  
		Last Modified: Wed, 02 Jul 2025 05:34:52 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:f8d3275f84519e0c80046650c938718222c9a92feb23b967f63e193b01ee7f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754f1a539830669b2086ad4d6925fc8983cc03e5378621a8114d82ab20aea5b3`

```dockerfile
```

-	Layers:
	-	`sha256:0f199f4618eaf1f778e87d6e35e668fc26e60ea40ea544e518cee1e3b1190345`  
		Last Modified: Wed, 02 Jul 2025 07:07:21 GMT  
		Size: 3.2 MB (3223917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d04a852ab3112079a246d87561272f331b5442dc5981e0721820c42f803b4e9c`  
		Last Modified: Wed, 02 Jul 2025 07:07:21 GMT  
		Size: 28.0 KB (27990 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:590d4dd863b8d987c703b0e6e6cf21e78fb580f7e312ae26ad448c87cde1b121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254629767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9774f436eeec8b64414fa5a9fe42aefbc19d0c12dea491e078608017289bb8e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 03 Jun 2025 22:01:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 22:01:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 22:01:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 22:01:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 22:01:14 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Tue, 03 Jun 2025 22:01:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 22:01:14 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Jun 2025 22:01:14 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 03 Jun 2025 22:01:14 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 03 Jun 2025 22:01:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 03 Jun 2025 22:01:14 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 03 Jun 2025 22:01:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 03 Jun 2025 22:01:14 GMT
ENV MONGO_MAJOR=6.0
# Tue, 03 Jun 2025 22:01:14 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
ENV MONGO_VERSION=6.0.24
# Tue, 03 Jun 2025 22:01:14 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Jun 2025 22:01:14 GMT
ENV HOME=/data/db
# Tue, 03 Jun 2025 22:01:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 22:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 22:01:14 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 03 Jun 2025 22:01:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42ab8cf783c92ac7f341c96dc6aa61dd153c8a66a6f0ab53e13c8d8f9ba277`  
		Last Modified: Wed, 02 Jul 2025 05:52:42 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a769382f90da32facf6337ff2e50cc6c2ad0b081c018d33d2d0d35691cab1e7d`  
		Last Modified: Wed, 02 Jul 2025 05:52:33 GMT  
		Size: 1.5 MB (1481784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9441df986cba6234e26ae924d9606b137eefd661891d05c26c765968d39f3fc`  
		Last Modified: Wed, 02 Jul 2025 05:53:42 GMT  
		Size: 1.0 MB (1027767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d240b1b97515307e579faaacee22a37ad40da30b96bea9132efdfde411e9970`  
		Last Modified: Wed, 02 Jul 2025 05:53:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1aabdec83e6b10b3cffd86e9b520213f4e537d37c5f417ec45ec706337b96a`  
		Last Modified: Wed, 02 Jul 2025 05:53:41 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1804d396a9bfefa6c049aaeaddb4184cf87239d19852be9d1dd3a3f920ace4ce`  
		Last Modified: Wed, 02 Jul 2025 07:07:38 GMT  
		Size: 224.8 MB (224753775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90da739a32f7ee91af295b67f1509284bde88062b812f382fedc211186eaf6b0`  
		Last Modified: Wed, 02 Jul 2025 05:53:41 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:7d81cbcaba6fb0f50015fb3ea3ae04fbd5f3188632e6046c805885a65be8ff20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2481c27faf284c32f3ba32354b69a2c991bbc09304ede38da73ac8b903f41b40`

```dockerfile
```

-	Layers:
	-	`sha256:e6cc58e2616549610c5e75071d8bccca172194f7c8cfb2079a37acc6c826aaf8`  
		Last Modified: Wed, 02 Jul 2025 07:07:25 GMT  
		Size: 3.2 MB (3224236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf2c7fbf43f97cc6497438e04293866818f8d1ce71065d6ea8023f05b2b0730`  
		Last Modified: Wed, 02 Jul 2025 07:07:26 GMT  
		Size: 28.2 KB (28194 bytes)  
		MIME: application/vnd.in-toto+json
