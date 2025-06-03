## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:8c8b41baaf6ba6edbeea4ebcfca6c813e0fc24e95a0fe9e35833e0d5a6586de0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:365a07aaeb5a54719a162709ca53475b3eeb5e93fe58f69cd6e604bcca26aa6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275587281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e49b827123ebec885233ecfc54a2467871141a6118768018179c2d0f1634f24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 29 Apr 2025 22:05:39 GMT
ARG RELEASE
# Tue, 29 Apr 2025 22:05:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 29 Apr 2025 22:05:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 29 Apr 2025 22:05:39 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 29 Apr 2025 22:05:39 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Tue, 29 Apr 2025 22:05:39 GMT
CMD ["/bin/bash"]
# Tue, 29 Apr 2025 22:05:39 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
ENV GOSU_VERSION=1.17
# Tue, 29 Apr 2025 22:05:39 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 29 Apr 2025 22:05:39 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 29 Apr 2025 22:05:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 29 Apr 2025 22:05:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 29 Apr 2025 22:05:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 29 Apr 2025 22:05:39 GMT
ENV MONGO_MAJOR=7.0
# Tue, 29 Apr 2025 22:05:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
ENV MONGO_VERSION=7.0.20
# Tue, 29 Apr 2025 22:05:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
VOLUME [/data/db /data/configdb]
# Tue, 29 Apr 2025 22:05:39 GMT
ENV HOME=/data/db
# Tue, 29 Apr 2025 22:05:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Apr 2025 22:05:39 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Apr 2025 22:05:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa68417c814d1d44110d1668b617f214e88ddf91ffd5dc6e9f986e7959be1d4`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 1.8 KB (1779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e5047c19850c5adddfca334978be020c0df7542c192100d8eaf496d4c92b3c`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 1.5 MB (1513246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a7b7ec93277085b8984e4e2fd680adffc2c34317c83220b4a294b51e848618`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 1.1 MB (1095084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1209b3d78c260aed41c795b62e38b1c49eb9129461036831eb94139da138b74a`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c88c0b185c7b11846d707791c9c778595511c19f6acecdb150278204409f0d`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbe65cc525ab976d51f6c1427f8e38618a2f5a7697f910f5db902e55f6ce47a`  
		Last Modified: Tue, 03 Jun 2025 13:32:09 GMT  
		Size: 243.4 MB (243438789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b12a794baed4dbbf921551b9b7536ef60944ca88225e52daf3518177869d8a`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:9db4c29e4049f66ff3cb5e69ebc737ab8b85b170cd852c254fc8526a4188b217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66465c4db12ed4ffce62a3a468a1fa157bc59d5d0a1b2e4e4cfd082cbc252a26`

```dockerfile
```

-	Layers:
	-	`sha256:38ab2d0c49cf76053b7b026ba4a89da99785f85d065573df695463ab1a957976`  
		Last Modified: Tue, 03 Jun 2025 13:44:02 GMT  
		Size: 3.1 MB (3101615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6fe946a3de96f8ae0c3ed1a5cdee26af6b0f6d6fd13f183396a6639628540a`  
		Last Modified: Tue, 03 Jun 2025 13:44:06 GMT  
		Size: 28.0 KB (27991 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:203e9fc7734fc45ac3bd4c9ddfc577e3af21af75dad5e25c101539a84b68e4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263018851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee873021ae9b3654ffadf9b581a16654eade20af58814b22b2f56595c3d0181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 29 Apr 2025 22:05:39 GMT
ARG RELEASE
# Tue, 29 Apr 2025 22:05:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 29 Apr 2025 22:05:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 29 Apr 2025 22:05:39 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 29 Apr 2025 22:05:39 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Tue, 29 Apr 2025 22:05:39 GMT
CMD ["/bin/bash"]
# Tue, 29 Apr 2025 22:05:39 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
ENV GOSU_VERSION=1.17
# Tue, 29 Apr 2025 22:05:39 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 29 Apr 2025 22:05:39 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 29 Apr 2025 22:05:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 29 Apr 2025 22:05:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 29 Apr 2025 22:05:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 29 Apr 2025 22:05:39 GMT
ENV MONGO_MAJOR=7.0
# Tue, 29 Apr 2025 22:05:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
ENV MONGO_VERSION=7.0.20
# Tue, 29 Apr 2025 22:05:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
VOLUME [/data/db /data/configdb]
# Tue, 29 Apr 2025 22:05:39 GMT
ENV HOME=/data/db
# Tue, 29 Apr 2025 22:05:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Apr 2025 22:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Apr 2025 22:05:39 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 29 Apr 2025 22:05:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb248b6ddf1eadf7eaca9b867b48d2fb358bd5fc7dfc92e87380a22b8b17059`  
		Last Modified: Tue, 03 Jun 2025 13:31:06 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc77ea490de9f702ea64bc43eb81ee198becae77e86919b49e883735ad25f0b`  
		Last Modified: Tue, 03 Jun 2025 13:31:06 GMT  
		Size: 1.5 MB (1481679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3158b1c1e6c9cc737ff7f08bbdcbc3347ae2cee597bf6dfa7cf477f9222afa4a`  
		Last Modified: Tue, 03 Jun 2025 13:32:17 GMT  
		Size: 1.0 MB (1027660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713746464844a161951ac8fb95333403ed5084a9f98a472f288b7f9319ff2753`  
		Last Modified: Tue, 03 Jun 2025 13:32:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e05c0f84fef18b087bc441264e6c079bc15949819f18fe0c869220cf3e30521`  
		Last Modified: Tue, 03 Jun 2025 13:32:26 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf42c4df4e972f6ac96194cc866db9ce146829346ac34585f664df177161ded`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 233.1 MB (233146765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d21942fc386424b65f61f273f3a43b1c57a01e54ea39f636afebfd5b1be0ac9`  
		Last Modified: Tue, 03 Jun 2025 13:32:29 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:4f66e2be888e9ed03c1e72bb2555a86e627e811b04fda6e351f3526f0173026a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee96f0eb121f8a5e344ad9025b3a3f2b2609bc051c8f68c0047044ef53c06522`

```dockerfile
```

-	Layers:
	-	`sha256:1e86c33286d139347ec3f52ca5842724d8029c15cb93820366db4dd7c9d9b2e4`  
		Last Modified: Tue, 03 Jun 2025 13:44:14 GMT  
		Size: 3.1 MB (3101934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a469d60864e49bc7b7de8c2287d9da1eb01d91ab09ae0e7dbf39186b5ac2ea8`  
		Last Modified: Tue, 03 Jun 2025 13:44:01 GMT  
		Size: 28.2 KB (28193 bytes)  
		MIME: application/vnd.in-toto+json
