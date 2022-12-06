## `mongo:6-focal`

```console
$ docker pull mongo@sha256:9b6f66c5107ab13bf5f800d433cdd3f0935414057c7f1a508c79e1cc651a7174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:6-focal` - linux; amd64

```console
$ docker pull mongo@sha256:7124b43eb6302e865671dd35f07ba343c42a16b4a0707c7007ddce5d9f24e530
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232484377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cefe1229065b580a534c422d46c205e596c8e4e2b45cd63f7283000afd1b733`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:37:18 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 06 Dec 2022 01:29:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 01:29:23 GMT
ENV GOSU_VERSION=1.12
# Tue, 06 Dec 2022 01:29:23 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 06 Dec 2022 01:29:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 06 Dec 2022 01:29:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 06 Dec 2022 01:29:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 06 Dec 2022 01:29:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 06 Dec 2022 01:29:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 06 Dec 2022 01:29:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 06 Dec 2022 01:29:34 GMT
ENV MONGO_MAJOR=6.0
# Tue, 06 Dec 2022 01:29:35 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 06 Dec 2022 01:29:35 GMT
ENV MONGO_VERSION=6.0.3
# Tue, 06 Dec 2022 01:30:01 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 06 Dec 2022 01:30:03 GMT
VOLUME [/data/db /data/configdb]
# Tue, 06 Dec 2022 01:30:03 GMT
ENV HOME=/data/db
# Tue, 06 Dec 2022 01:30:03 GMT
COPY file:679af4e310ab84df3ded97dcc73874df246621b7a2d482fe4f055c0176bfec37 in /usr/local/bin/ 
# Tue, 06 Dec 2022 01:30:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Dec 2022 01:30:03 GMT
EXPOSE 27017
# Tue, 06 Dec 2022 01:30:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a00eb9f68a0dcf2f4b6f3881376f35b2908e0ec03e0ba7b41dce5138a57017e`  
		Last Modified: Wed, 26 Oct 2022 16:14:33 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520612e53a012cdc246ac86453ed00490dcc1f6231ff791d7cbfc4252dd4686`  
		Last Modified: Tue, 06 Dec 2022 01:33:09 GMT  
		Size: 8.3 MB (8347534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a357eb129f55d827f44e96a7e4eecb6aabe6d6f0b85782082a841025a6371f`  
		Last Modified: Tue, 06 Dec 2022 01:33:08 GMT  
		Size: 1.2 MB (1235277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44e86010cfce519ebeabf17ad8c2437885f5a697c1d60ddbfbf2a1c87c6cb1b`  
		Last Modified: Tue, 06 Dec 2022 01:33:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d899e9427fa8b2a4d25138295eba374f2afebad52af675f17a10289765b6b`  
		Last Modified: Tue, 06 Dec 2022 01:33:06 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfecd4270f9ab85fb597eedb0a25fd63ea7d1182ecfbb03bfb727b548ae4ae7a`  
		Last Modified: Tue, 06 Dec 2022 01:33:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd246a7f5dd1ab6131bed0b2f48a5a160e7bba9ccd5023a22d67e53360c6afb`  
		Last Modified: Tue, 06 Dec 2022 01:33:33 GMT  
		Size: 194.3 MB (194315359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b962974cdbb0154bad0680cd24e26c076e0c961e8137424ee01a24cd29d34913`  
		Last Modified: Tue, 06 Dec 2022 01:33:06 GMT  
		Size: 4.7 KB (4685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:73bf63b9cb28133895c39ed645ccebb40e557765e4d193b0a1e05cd15ffd3377
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225839266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6b6c2c4a2635b26c5c221336b9fb57e64e05e0ec7dd5467df884cb375d190e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:12:08 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 06 Dec 2022 01:47:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 01:47:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 06 Dec 2022 01:47:59 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 06 Dec 2022 01:48:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 06 Dec 2022 01:48:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 06 Dec 2022 01:48:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 06 Dec 2022 01:48:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 06 Dec 2022 01:48:11 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 06 Dec 2022 01:48:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 06 Dec 2022 01:48:11 GMT
ENV MONGO_MAJOR=6.0
# Tue, 06 Dec 2022 01:48:11 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 06 Dec 2022 01:48:11 GMT
ENV MONGO_VERSION=6.0.3
# Tue, 06 Dec 2022 01:48:35 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 06 Dec 2022 01:48:39 GMT
VOLUME [/data/db /data/configdb]
# Tue, 06 Dec 2022 01:48:39 GMT
ENV HOME=/data/db
# Tue, 06 Dec 2022 01:48:39 GMT
COPY file:679af4e310ab84df3ded97dcc73874df246621b7a2d482fe4f055c0176bfec37 in /usr/local/bin/ 
# Tue, 06 Dec 2022 01:48:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Dec 2022 01:48:39 GMT
EXPOSE 27017
# Tue, 06 Dec 2022 01:48:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffac05d305dafc7bd6d968c4d611342ceb95a87494c361ab37718b188f02763`  
		Last Modified: Wed, 26 Oct 2022 02:16:20 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31398b3e1bf2974e53f1dcd4072b9393983bd39a468fe3f29d273bb393ab5cb`  
		Last Modified: Tue, 06 Dec 2022 01:51:31 GMT  
		Size: 8.2 MB (8178053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44094a1241c81ae235a0e5a6b2ffcab1fefae17787c403f6bd777af91ce91aeb`  
		Last Modified: Tue, 06 Dec 2022 01:51:30 GMT  
		Size: 1.2 MB (1171948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308106baa2a56617e15fb8f64a5d29a73adc29199d61ad858f1127f6b066eb8`  
		Last Modified: Tue, 06 Dec 2022 01:51:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a7685edfd30f419ede23e88dc1e8df523873f766bdabbe6b5f7d21a2a60aab`  
		Last Modified: Tue, 06 Dec 2022 01:51:28 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ec491990d778feb7b4fa7270f2777d755fb32f4080d38d854a741e488d2d4`  
		Last Modified: Tue, 06 Dec 2022 01:51:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3161135f32765a98977dc15d3adbb6b7f877faf9c8b10fa009ad3943ebdc90da`  
		Last Modified: Tue, 06 Dec 2022 01:51:48 GMT  
		Size: 189.3 MB (189284892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3f906d15078bb366e197ffc780abb0f062b91e0e3d419c4bfdf2e50718879e`  
		Last Modified: Tue, 06 Dec 2022 01:51:28 GMT  
		Size: 4.7 KB (4683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
