## `mongo:noble`

```console
$ docker pull mongo@sha256:6458b950c6340fb522868118b5cd31b52dad4e2fc7bf341e5732babebc9ae005
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:3c615e75a6c37cdf38c4cf5690834f302813f4b4edcf25620960159d0dbec93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.3 MB (335306722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0286cc181898f3800665c63e6c51638a308d8ba97ed1c199e8ffa79db122780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:24 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 17 Feb 2026 20:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 20:28:44 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 17 Feb 2026 20:28:44 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 17 Feb 2026 20:28:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 20:28:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:28:44 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 17 Feb 2026 20:28:44 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 17 Feb 2026 20:28:44 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 17 Feb 2026 20:28:44 GMT
ENV MONGO_MAJOR=8.2
# Tue, 17 Feb 2026 20:28:45 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 17 Feb 2026 20:28:45 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 17 Feb 2026 20:29:04 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 17 Feb 2026 20:29:04 GMT
VOLUME [/data/db /data/configdb]
# Tue, 17 Feb 2026 20:29:04 GMT
ENV HOME=/data/db
# Tue, 17 Feb 2026 20:29:04 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 17 Feb 2026 20:29:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:29:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:29:04 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Feb 2026 20:29:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79e499203c9cf152c5bc6f038864c8785d3bacb24b4ae97001ad0614e9dd487`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46eb2190ffc37d34bd6051d25cb4a73f4384442ee145609df2fd4e97b065729`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 1.5 MB (1509524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427c118b20797fcc39d562bb8290341651e5b31524cead45eea3d36f774c64fc`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 933.7 KB (933728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfd783f7a597bbb7d6eb1383ebdbbd9a0f413f175bbdc38b74ef123eabe184f`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea2e6a72e6bef5c958a79ccaa672d231f05a40baa2000d690fb554d0abdf2a5`  
		Last Modified: Tue, 17 Feb 2026 20:29:42 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b55066391c2657b7fc353f59ac462e607e3be45af587fa3699aac5a8f609f`  
		Last Modified: Tue, 17 Feb 2026 20:29:48 GMT  
		Size: 303.1 MB (303129259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d23bbf2b2165d0729765a06f400db5f7a9583d60bf1fb848098d8187a813aa2`  
		Last Modified: Tue, 17 Feb 2026 20:29:42 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:b2d948e0d71df0606c8245d92f31c23bb452b975904115fdadc03b48d89e0d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9666c8b0c3de9d7efc891d9db60777c5fc54df39e739aa74167b3a1a170798`

```dockerfile
```

-	Layers:
	-	`sha256:bae1425230be09820e17d4685d782ea5ce48279512df9f9cf628d547d9df58a0`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 2.7 MB (2668919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eeb70347fbd8068cd83426d0d25bba2d3dca4dc008bcbba698cbfe8f37851cb`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 28.8 KB (28792 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:870518acf2c2317f420810ec89afa6d5c733e79024252e6c410a6519a98a3bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320024005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8e0edc0030cc55428dfa46573846489ed56ce9dd3a985ae09a9a19640a5a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:06 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 17 Feb 2026 20:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:27:26 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 20:27:26 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 17 Feb 2026 20:27:26 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 17 Feb 2026 20:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 20:27:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:27:26 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 17 Feb 2026 20:27:26 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 17 Feb 2026 20:27:26 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 17 Feb 2026 20:27:26 GMT
ENV MONGO_MAJOR=8.2
# Tue, 17 Feb 2026 20:27:26 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 17 Feb 2026 20:27:26 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 17 Feb 2026 20:27:46 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 17 Feb 2026 20:27:46 GMT
VOLUME [/data/db /data/configdb]
# Tue, 17 Feb 2026 20:27:46 GMT
ENV HOME=/data/db
# Tue, 17 Feb 2026 20:27:46 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 17 Feb 2026 20:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:46 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Feb 2026 20:27:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f5cdbb159932848ccefb5074604621aff1e35e38f9139ab694f9ec085c3f07`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaee3f82e804503eab8d9d24299fa1c3dc140422e9a67bcb53082a4530dcf99b`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 1.5 MB (1494496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc0f1d374f5f0b098144592f053f6881b0705d02e2d984462cf7b0f202e175c`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 886.0 KB (886024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3cff213b9bb8afad7c3dbfe99a8b6394ed7085a0beb0e50dc44e4c8e6dd927`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7a0fd6d2b7d16debb4272be3cd687c7bd7986de94e31ae959418da75756e3`  
		Last Modified: Tue, 17 Feb 2026 20:28:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a1f3f71824f982bcf786b69dc31db90ee336cf081c90dfaf81ad5eb90459e7`  
		Last Modified: Tue, 17 Feb 2026 20:28:27 GMT  
		Size: 288.8 MB (288771770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5f049ccdd6eeaf83bc8f0ee42929386f93f3e898dc6c8a991ab8664c215652`  
		Last Modified: Tue, 17 Feb 2026 20:28:22 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:c083321a003de0eb5943dcbd889863e80e2b26e337ee62c3e60590a8928d6cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8fa3258980d4b51c1a54269b4e71dd41a3510ee843e3cf75d248a163d80fac`

```dockerfile
```

-	Layers:
	-	`sha256:531bae2495406a855f24e03fe93706aecf263f3886bfaeaa75facb5ad13d7350`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 2.7 MB (2670055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50a2880e8bc8d9aef74d840e85a8d681f3762a2ff0a4f5009eeefb6b035a24c5`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 29.0 KB (29019 bytes)  
		MIME: application/vnd.in-toto+json
