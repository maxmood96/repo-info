## `mongo:4-focal`

```console
$ docker pull mongo@sha256:e1aff8b2f483d37bb2b18436900783df097031c20368eb6215944962537c4db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:24da9c8334e15ca4dc7683a579224d63fe771f7defb140149bfbe4480ee426d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172835652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfc933017699eda23d3f56a592b565de3368cd8caf4a3d56f8dbbb8f8247959`
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
# Fri, 02 Sep 2022 03:54:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Fri, 02 Sep 2022 03:54:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 02 Sep 2022 03:54:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 03:54:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 03:54:20 GMT
ENV MONGO_MAJOR=4.4
# Fri, 02 Sep 2022 03:54:21 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 29 Sep 2022 21:20:38 GMT
ENV MONGO_VERSION=4.4.17
# Thu, 29 Sep 2022 21:20:55 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 29 Sep 2022 21:20:56 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Sep 2022 21:20:56 GMT
ENV HOME=/data/db
# Thu, 29 Sep 2022 21:20:56 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Thu, 29 Sep 2022 21:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Sep 2022 21:20:57 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 21:20:57 GMT
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
	-	`sha256:595a03cbac5349ce9d03ba3bee9ebce578e6dd38d212e2d5e3799bbc3a7fcc97`  
		Last Modified: Fri, 02 Sep 2022 03:58:52 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc6ab7f7529889ad786429377cc5a92c9e5bc61ee6ad647d44aecfded1dda37`  
		Last Modified: Fri, 02 Sep 2022 03:58:52 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01715fba6c05b9c8c47ceb09346a09f7d4cea8217d3f78accab66d3e1593934d`  
		Last Modified: Thu, 29 Sep 2022 21:23:18 GMT  
		Size: 134.7 MB (134688577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d83897816d92569014214e3d09ca912f9e91cf655c7ec2380d607999db527e4`  
		Last Modified: Thu, 29 Sep 2022 21:23:01 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:eb01712b2774537f7a05fe988c34251e605876f20745a6886a376a617b91ac7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167672931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db3e8fc4f894f1c40de8a9a71f57c66c1cd79cc56e35ccb93e69ab11ce33f99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:38:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 02 Sep 2022 05:38:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:38:32 GMT
ENV GOSU_VERSION=1.12
# Fri, 02 Sep 2022 05:38:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 02 Sep 2022 05:38:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Sep 2022 05:38:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Sep 2022 05:40:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Fri, 02 Sep 2022 05:40:58 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 02 Sep 2022 05:40:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 05:41:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 05:41:01 GMT
ENV MONGO_MAJOR=4.4
# Fri, 02 Sep 2022 05:41:02 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 29 Sep 2022 21:33:51 GMT
ENV MONGO_VERSION=4.4.17
# Thu, 29 Sep 2022 21:34:08 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 29 Sep 2022 21:34:08 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Sep 2022 21:34:09 GMT
ENV HOME=/data/db
# Thu, 29 Sep 2022 21:34:11 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Thu, 29 Sep 2022 21:34:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Sep 2022 21:34:12 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 21:34:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe07d8ebcafb11d0bd133b24c0b609a2df7be61177317743622e25402fad20e5`  
		Last Modified: Fri, 02 Sep 2022 05:44:29 GMT  
		Size: 1.8 KB (1779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f116473d7043b4502e37137a97bd6e20142172dab16e6f88e497d3d33b0c78`  
		Last Modified: Fri, 02 Sep 2022 05:44:30 GMT  
		Size: 2.9 MB (2906991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed58e863f95532cf6247f0bc0953d63704dde8a89053df15b1712a2ec112d07`  
		Last Modified: Fri, 02 Sep 2022 05:44:30 GMT  
		Size: 6.2 MB (6249319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62274e6e1246430435b8017651d8588082af58d5faa6c59dd88c773c2825bc0c`  
		Last Modified: Fri, 02 Sep 2022 05:44:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d1b609eda28a773b91e6de02800c882c5dbe7d3f1503353520349642953da0`  
		Last Modified: Fri, 02 Sep 2022 05:46:28 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5edad46787e2c61fb20b77decc69eb7afa9da6eb1b47e4e2de956d1d532e2ef`  
		Last Modified: Fri, 02 Sep 2022 05:46:28 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a4fad532a064caecfc1ab54e6ae837aa3838b00a7ea0e8a493bcd08a8620f4`  
		Last Modified: Thu, 29 Sep 2022 21:37:08 GMT  
		Size: 131.3 MB (131316184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ffea987210dc23c8188db3f068f8ba7a5e954b2bca9fa2a9711f3a95b805f3`  
		Last Modified: Thu, 29 Sep 2022 21:36:51 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
