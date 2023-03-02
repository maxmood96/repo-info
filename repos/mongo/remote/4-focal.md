## `mongo:4-focal`

```console
$ docker pull mongo@sha256:47f220b859f55e8f9e018950f4d1e211a7da9468425fe5710a5f8218c8a30109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:e8f56e6aac5aa663383ca7f56e9b69bb30f9f8dce6d029b601d89f374816a366
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175742424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140bcf29d664210726360ba9b92b09c5eaa76853d5e02ff44d4402e76f88f2b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:53:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 02 Mar 2023 04:53:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:53:33 GMT
ENV GOSU_VERSION=1.16
# Thu, 02 Mar 2023 04:53:33 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 02 Mar 2023 04:53:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Mar 2023 04:53:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Mar 2023 04:54:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 02 Mar 2023 04:54:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 02 Mar 2023 04:54:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 02 Mar 2023 04:54:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 02 Mar 2023 04:54:21 GMT
ENV MONGO_MAJOR=4.4
# Thu, 02 Mar 2023 04:54:21 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 02 Mar 2023 04:54:21 GMT
ENV MONGO_VERSION=4.4.19
# Thu, 02 Mar 2023 04:54:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 02 Mar 2023 04:54:40 GMT
VOLUME [/data/db /data/configdb]
# Thu, 02 Mar 2023 04:54:41 GMT
ENV HOME=/data/db
# Thu, 02 Mar 2023 04:54:41 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Thu, 02 Mar 2023 04:54:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 04:54:41 GMT
EXPOSE 27017
# Thu, 02 Mar 2023 04:54:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33948e0c4f1ec3d7f1f88d15d9111d987047f05e35895547088a4366a369471a`  
		Last Modified: Thu, 02 Mar 2023 04:56:37 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6616e03404440290f2ddbbbc23d6b487c3a4ef918cdbb97114cd2e7906899249`  
		Last Modified: Thu, 02 Mar 2023 04:56:38 GMT  
		Size: 8.3 MB (8348515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06c1e4170036421e2a979769d225392876d3e1c8615333b42e4e7db0f980cc9`  
		Last Modified: Thu, 02 Mar 2023 04:56:37 GMT  
		Size: 1.3 MB (1255825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2c675591da5d5379f30c2e9170e83fcd789f3819e100dee451e1ffbd289a9c`  
		Last Modified: Thu, 02 Mar 2023 04:56:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63c078e02d81f142795d18ac39c360531efba53b1ba94ba699fe2b1caa97ad8`  
		Last Modified: Thu, 02 Mar 2023 04:57:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4788ef694503183cbdc94a2c8b80ab269b6c14873a13e98a17166bdee84b00b6`  
		Last Modified: Thu, 02 Mar 2023 04:57:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e060e8df80a6d5271a97fa86b5c3702fc60f2e8506a4117694e7fbe5c762a521`  
		Last Modified: Thu, 02 Mar 2023 04:57:28 GMT  
		Size: 137.6 MB (137551434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559b53d13b60759159eba6b216edf71a6f6ec68e046db6f049d2bad42e7d8e`  
		Last Modified: Thu, 02 Mar 2023 04:57:12 GMT  
		Size: 5.0 KB (4964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b8c075fddd6956e61e7a9241862301f6814d41e52f2e3f70b596ad7e511ed7f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171365325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721b48b27bc989bbf98f7540b548a027b4fa283fba45e66918ec0914b7e02cda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:08:35 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 02 Mar 2023 03:08:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:08:44 GMT
ENV GOSU_VERSION=1.16
# Thu, 02 Mar 2023 03:08:44 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 02 Mar 2023 03:08:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 02 Mar 2023 03:08:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 02 Mar 2023 03:09:24 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 02 Mar 2023 03:09:24 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 02 Mar 2023 03:09:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 02 Mar 2023 03:09:24 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 02 Mar 2023 03:09:24 GMT
ENV MONGO_MAJOR=4.4
# Thu, 02 Mar 2023 03:09:24 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 02 Mar 2023 03:09:24 GMT
ENV MONGO_VERSION=4.4.19
# Thu, 02 Mar 2023 03:09:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 02 Mar 2023 03:09:41 GMT
VOLUME [/data/db /data/configdb]
# Thu, 02 Mar 2023 03:09:41 GMT
ENV HOME=/data/db
# Thu, 02 Mar 2023 03:09:41 GMT
COPY file:82adc06ee9084caf92c64e3fbb536f06b2a724aa0c1f122d17c10c70a5a1b90e in /usr/local/bin/ 
# Thu, 02 Mar 2023 03:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:09:41 GMT
EXPOSE 27017
# Thu, 02 Mar 2023 03:09:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e28cabe5b8f281103472572c0e399c29fbf74223424938ede3ad075366c54a4`  
		Last Modified: Thu, 02 Mar 2023 03:11:41 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fe96ecdce59379bca8bb02a9459cf43ba1986a9088a6662eb99c7fec20edcd`  
		Last Modified: Thu, 02 Mar 2023 03:11:42 GMT  
		Size: 8.2 MB (8179205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ff04ba7a2ec5f3105430e627489f080663eda132ffbc69f28c76208b08392`  
		Last Modified: Thu, 02 Mar 2023 03:11:41 GMT  
		Size: 1.2 MB (1188294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81d49462d00fb935bb228aa8e73eb44f3b1a61118c624a67376a34e6b60201a`  
		Last Modified: Thu, 02 Mar 2023 03:11:39 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cd6c6905e6f5b2b8d048153bb24681da245bba04d31bdfa5144a56bfd90b7b`  
		Last Modified: Thu, 02 Mar 2023 03:12:08 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bafb6491217a7b2ecc2ac55e09f17120bd4c54cc16ddb10825909641d84455`  
		Last Modified: Thu, 02 Mar 2023 03:12:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a2923f5aa0b315f82107fbd4e24eb8e8e319bdac0221b846129055f30d82a`  
		Last Modified: Thu, 02 Mar 2023 03:12:21 GMT  
		Size: 134.8 MB (134794660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff4a9d0688d498a5c0daca8d978b2a58a20cb924533f8cfc2f74509915f0f45`  
		Last Modified: Thu, 02 Mar 2023 03:12:08 GMT  
		Size: 5.0 KB (4964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
