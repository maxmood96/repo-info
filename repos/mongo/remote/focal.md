## `mongo:focal`

```console
$ docker pull mongo@sha256:7a34575d7c0c84cfe3a907073e7d4ecd631faa484878c4705f2c709c64279b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:focal` - linux; amd64

```console
$ docker pull mongo@sha256:0e0c67d4bb79dc1d20b3a6f2ecb93024bbbaa0e92311a12c6bd081ba24b81801
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231722030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70885e78ca893b5e53b9c8f0d0679ac828f4d8846ce144a8cbca60c001cfe91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:52:11 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 02 Sep 2022 03:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:52:19 GMT
ENV GOSU_VERSION=1.12
# Fri, 02 Sep 2022 03:52:20 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 02 Sep 2022 03:52:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Sep 2022 03:52:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Sep 2022 03:52:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Fri, 02 Sep 2022 03:52:33 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 02 Sep 2022 03:52:33 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 03:52:33 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 03:52:33 GMT
ENV MONGO_MAJOR=6.0
# Fri, 02 Sep 2022 03:52:34 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 29 Sep 2022 21:19:36 GMT
ENV MONGO_VERSION=6.0.2
# Thu, 29 Sep 2022 21:20:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 29 Sep 2022 21:20:03 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Sep 2022 21:20:03 GMT
ENV HOME=/data/db
# Thu, 29 Sep 2022 21:20:03 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Thu, 29 Sep 2022 21:20:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Sep 2022 21:20:04 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 21:20:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9c8c301e0f21d7d0b229b7ce3bf5f73a8032a77f1fd0ead5a40ae2904e7386`  
		Last Modified: Fri, 02 Sep 2022 03:57:03 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73738965c4ce390367a607807b960c2c4cd8aa410fc4b1bea6ce71263c6725a8`  
		Last Modified: Fri, 02 Sep 2022 03:57:04 GMT  
		Size: 3.1 MB (3059566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6635b9ddf662b5aad927979bc18877d5e93da5b68d0257bf589086be3fc24`  
		Last Modified: Fri, 02 Sep 2022 03:57:04 GMT  
		Size: 6.5 MB (6506072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a471eaa4ad67f863744ea2570d2995126f69ac4a5156455603a9308c2c915e`  
		Last Modified: Fri, 02 Sep 2022 03:57:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf274af89b0a0884f7e076b77aa392912a4199a2dc008ddcfce30b3dc843df5`  
		Last Modified: Fri, 02 Sep 2022 03:57:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fc489f2a3bae9cf2166f37d4fe0c5fcbfb452e62be136900d6695577033d3e`  
		Last Modified: Fri, 02 Sep 2022 03:57:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1abc36251b97103711f5db370c4431c08c6343c9e768cd7f1c4f30cd153cea2`  
		Last Modified: Thu, 29 Sep 2022 21:22:03 GMT  
		Size: 193.6 MB (193574960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396db6f4d8008af59305c514b2d28092e698960cb572c185839d7dfea6a90a7a`  
		Last Modified: Thu, 29 Sep 2022 21:21:36 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0a6f2b19ee2f8c5193fa286524aa9949c3a68af5b2e8440d2f593996376504c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224938630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa885bebec49cae70e782b1d0fcb92fccebfb386ccd76251ceb1b0f99e08bb04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:54:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 05 Oct 2022 16:54:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 16:54:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 05 Oct 2022 16:54:46 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 05 Oct 2022 16:55:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 16:55:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 16:55:05 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 05 Oct 2022 16:55:06 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 05 Oct 2022 16:55:07 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 16:55:08 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 16:55:09 GMT
ENV MONGO_MAJOR=6.0
# Wed, 05 Oct 2022 16:55:10 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 05 Oct 2022 16:55:11 GMT
ENV MONGO_VERSION=6.0.2
# Wed, 05 Oct 2022 16:55:34 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 05 Oct 2022 16:55:35 GMT
VOLUME [/data/db /data/configdb]
# Wed, 05 Oct 2022 16:55:35 GMT
ENV HOME=/data/db
# Wed, 05 Oct 2022 16:55:37 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Wed, 05 Oct 2022 16:55:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:55:38 GMT
EXPOSE 27017
# Wed, 05 Oct 2022 16:55:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808a7df5fbbc12c4cd8f740fabdbbe301d6a4efe1b81b3f196474a28d0322c92`  
		Last Modified: Wed, 05 Oct 2022 16:59:14 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5a5e151a7f04dcea23cd214c84a62e5c02bfd8bf21e50b6384cb32a7dac4ed`  
		Last Modified: Wed, 05 Oct 2022 16:59:14 GMT  
		Size: 2.9 MB (2905895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbed2c86a740691aafa2028087ed2a11f64352f3ab06a520efa22bc7c5246f03`  
		Last Modified: Wed, 05 Oct 2022 16:59:14 GMT  
		Size: 6.2 MB (6248099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c6dc442fc2aca80b585c0c229cf8addb668c43cb2b7b15193532981186e6d`  
		Last Modified: Wed, 05 Oct 2022 16:59:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d00e8640a3f0c64b7cd189730daacde9c594bf5850cda768e9e0f97bfbfbcc`  
		Last Modified: Wed, 05 Oct 2022 16:59:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11bc600eb8d283a1a0030c98e1856fd8b96b8f8c86fd7feb0cf74e710e168b4`  
		Last Modified: Wed, 05 Oct 2022 16:59:11 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b720c57555ba599236671087a8d9d0dae2da8d3677a9e9c240128242c28796`  
		Last Modified: Wed, 05 Oct 2022 16:59:37 GMT  
		Size: 188.6 MB (188584399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194b45d19c19e2b2b24ad7d9b21b2be0ad2e16c100733b8f0ce8ed73fae5873e`  
		Last Modified: Wed, 05 Oct 2022 16:59:11 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
