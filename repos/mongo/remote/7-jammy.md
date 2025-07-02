## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:4b2c99c4b4a3e70ee002fea3088c4b7302185f24b4891d85d8f065eb8fd29dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:ebbb6f6189a851083df17e2a8482a04f13cbf982baad29f5d421b680c233226f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278573357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3f2533ee90c1875e120ce0b3174433b1484893fab8b00cadfac0bf0d1d0ccc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 03 Jun 2025 22:06:20 GMT
ARG RELEASE
# Tue, 03 Jun 2025 22:06:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 22:06:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 22:06:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 22:06:20 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Tue, 03 Jun 2025 22:06:20 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 22:06:20 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Jun 2025 22:06:20 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 03 Jun 2025 22:06:20 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 03 Jun 2025 22:06:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 03 Jun 2025 22:06:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 03 Jun 2025 22:06:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 03 Jun 2025 22:06:20 GMT
ENV MONGO_MAJOR=7.0
# Tue, 03 Jun 2025 22:06:20 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
ENV MONGO_VERSION=7.0.21
# Tue, 03 Jun 2025 22:06:20 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Jun 2025 22:06:20 GMT
ENV HOME=/data/db
# Tue, 03 Jun 2025 22:06:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 22:06:20 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 03 Jun 2025 22:06:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5affe3fb7b03151b53e7c55bd2202efc3848cf44bd979841d457518e6bfea99d`  
		Last Modified: Wed, 02 Jul 2025 05:35:16 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f4843e1a040e86cd46a142ffc6ed1003c74578727a09432c4e25f26faf74b4`  
		Last Modified: Wed, 02 Jul 2025 05:35:16 GMT  
		Size: 1.5 MB (1513210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891a4204f7fe02d3f17e06eadb12c7e46987267f4a54c02135360ee9db3d5d7a`  
		Last Modified: Wed, 02 Jul 2025 05:35:16 GMT  
		Size: 1.1 MB (1095038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca8bb63c2934dfc0c5b37c2b2b7d112152d7037a7f49e943996334968496026`  
		Last Modified: Wed, 02 Jul 2025 05:35:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60770f14b2bd76b7e6122e21fae5598581b974cbd7578751a46421c8be770fcc`  
		Last Modified: Wed, 02 Jul 2025 05:35:16 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d17dc80cac05741b481ce95ee6bc75a2cec8c190d19e189af824140ff5434c`  
		Last Modified: Wed, 02 Jul 2025 05:35:39 GMT  
		Size: 246.4 MB (246422259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b66fa715a2b43294fe0102339dfa0f162ba357c6e24786f1bdc4e4f562e5269`  
		Last Modified: Wed, 02 Jul 2025 05:35:17 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:c68cb8b4c6fe21f8fee8746901d079903b02d1d73a55463c380fefda65700a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f64bb5abc4af20a52bcfd1cb78fc39fd50a7ac99bec07bdf311cb8acb06ae03`

```dockerfile
```

-	Layers:
	-	`sha256:73264a540b70e04046225df94390b19f9cb7ddeab1fb6eeb95a92998b8d1eabf`  
		Last Modified: Wed, 02 Jul 2025 07:07:41 GMT  
		Size: 3.2 MB (3223917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb7e5b7dba6535b36f20e9bcc32962c2bbd68f5d0aa092f83c42904a3f27ba3`  
		Last Modified: Wed, 02 Jul 2025 07:07:41 GMT  
		Size: 28.0 KB (27991 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:e8997ae5853a0b835732d9cde4c49ad4ae4458497f7aae0a533f7038de91039f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265994769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcdd01acba8d9a7b2d01b34292b257130a1fc373684e7be2da3a98aaf316758`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 03 Jun 2025 22:06:20 GMT
ARG RELEASE
# Tue, 03 Jun 2025 22:06:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 22:06:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 22:06:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 22:06:20 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Tue, 03 Jun 2025 22:06:20 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 22:06:20 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Jun 2025 22:06:20 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 03 Jun 2025 22:06:20 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 03 Jun 2025 22:06:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 03 Jun 2025 22:06:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 03 Jun 2025 22:06:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 03 Jun 2025 22:06:20 GMT
ENV MONGO_MAJOR=7.0
# Tue, 03 Jun 2025 22:06:20 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
ENV MONGO_VERSION=7.0.21
# Tue, 03 Jun 2025 22:06:20 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Jun 2025 22:06:20 GMT
ENV HOME=/data/db
# Tue, 03 Jun 2025 22:06:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 22:06:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 22:06:20 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 03 Jun 2025 22:06:20 GMT
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
	-	`sha256:8e28f5908b791ce1b8ca79c05544ffc8432972dd2465fe8dab06193ca8f48a52`  
		Last Modified: Wed, 02 Jul 2025 05:52:33 GMT  
		Size: 1.0 MB (1027757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8367c9ad25fec83777466d6adb92a3c561734898ed68494289e782da9c2c44`  
		Last Modified: Wed, 02 Jul 2025 05:52:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa21e664d043a2e5672e5e90c325a2aeb23ae66e0eec86ced9170048a573de8`  
		Last Modified: Wed, 02 Jul 2025 05:52:32 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e76236c132267af81ba5aab7dd80d728cd2a943393026606bc7c15b940bbe0`  
		Last Modified: Wed, 02 Jul 2025 06:17:25 GMT  
		Size: 236.1 MB (236118792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b819058544b823b95edd2f7d6687f8aceb0411827f44f196d1edff9221f057`  
		Last Modified: Wed, 02 Jul 2025 05:52:32 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:87b4f1cfa6d38a4010f96e4fe48ac946b03ca52a8008f1ed1d77fff8212a79db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60afdbbaa3bcd7bd9a02a0e701a189ddaa19b747aead41027490552628540b11`

```dockerfile
```

-	Layers:
	-	`sha256:9d0fe9d421f9554303350229dd272faff7cfa777f2f3d9321a53e321468e8b81`  
		Last Modified: Wed, 02 Jul 2025 07:07:46 GMT  
		Size: 3.2 MB (3224236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194a41c52ee09621875ccf7e3ad426d1406071ce30adb05e9783cd2572287eb8`  
		Last Modified: Wed, 02 Jul 2025 07:07:46 GMT  
		Size: 28.2 KB (28194 bytes)  
		MIME: application/vnd.in-toto+json
