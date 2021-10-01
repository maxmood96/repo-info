## `mongo:4-focal`

```console
$ docker pull mongo@sha256:67ba3a64a39036ad18bb0706014dd93ad4867297dd4debe933ab99267177930d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:e3162aec7b6adc18c900e606053cddb4db4002190c63b788ec6a52adcfdc237a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171260128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c06b66248dbdf3932dafbb3101b2d01b9cac96752533ca29f75316b775bb02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:51:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 31 Aug 2021 03:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:51:15 GMT
ENV GOSU_VERSION=1.12
# Tue, 31 Aug 2021 03:51:15 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 31 Aug 2021 03:51:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 31 Aug 2021 03:51:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Aug 2021 03:52:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 31 Aug 2021 03:52:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 31 Aug 2021 03:52:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 31 Aug 2021 03:52:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 31 Aug 2021 03:52:21 GMT
ENV MONGO_MAJOR=4.4
# Tue, 31 Aug 2021 03:52:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Sep 2021 22:20:55 GMT
ENV MONGO_VERSION=4.4.9
# Mon, 20 Sep 2021 22:21:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Sep 2021 22:21:13 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Sep 2021 22:21:13 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Sep 2021 22:21:13 GMT
COPY file:df3353d9b2c25ef83b499ecae7fd5d611adb4a9462a577435178acaad3c8c695 in /usr/local/bin/ 
# Mon, 20 Sep 2021 22:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Sep 2021 22:21:14 GMT
EXPOSE 27017
# Mon, 20 Sep 2021 22:21:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664b0ebdcc074096f3cdb5767cd0679b6eb1b867cc4803caebc900c3a0e3cd7a`  
		Last Modified: Tue, 31 Aug 2021 03:54:55 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d598f4d3c08173a580ddfbc1aab7570a506bbe19ef2f760eef62bb18b0f2fe42`  
		Last Modified: Tue, 31 Aug 2021 03:54:56 GMT  
		Size: 3.1 MB (3064917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291455135b00f1125d53ec53b9bd1246a1a95c5289d78d52aeeebc2ca216e5ed`  
		Last Modified: Tue, 31 Aug 2021 03:54:56 GMT  
		Size: 6.5 MB (6506306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46409342f130fad45e914eb39eb6ff00f27268fb1b229f287a6b8102d7aa9bf`  
		Last Modified: Tue, 31 Aug 2021 03:54:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be18346a9b044d0826c950d4e78dc8966907454645dbbd8b72af3f8c91ff5bc5`  
		Last Modified: Tue, 31 Aug 2021 03:55:37 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13718f8ebc52752bb1764e12b1c7dbc900e89b47686bc8124cc6fdb6bfa5fb6`  
		Last Modified: Tue, 31 Aug 2021 03:55:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb9ead70d754b5b269f5204d4559cf2abbb736fb9df0a8e24d1b83164677cfb`  
		Last Modified: Mon, 20 Sep 2021 22:23:23 GMT  
		Size: 133.1 MB (133110397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc10997485bdc415e8bd3ad73a659daa6abd4924e7d8e644de1fb744766c909`  
		Last Modified: Mon, 20 Sep 2021 22:23:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaeb859ce86b08302618bdc4eceaa9d13cd6275c2531d06f5787ab2978ebc8f`  
		Last Modified: Mon, 20 Sep 2021 22:23:04 GMT  
		Size: 4.7 KB (4699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0837a92d01bcc8c750a8d692ed4df33f0befd07ef261b23e7d9feda04bacd3eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166510977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70bb32fa14171e1c73abc786f50a1c52f8db43511f55f1488f301d899829903e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:47:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Oct 2021 03:47:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:47:14 GMT
ENV GOSU_VERSION=1.12
# Fri, 01 Oct 2021 03:47:14 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 01 Oct 2021 03:47:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 03:47:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 03:48:25 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:48:26 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Oct 2021 03:48:26 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Oct 2021 03:48:26 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Oct 2021 03:48:26 GMT
ENV MONGO_MAJOR=4.4
# Fri, 01 Oct 2021 03:48:27 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Oct 2021 03:48:27 GMT
ENV MONGO_VERSION=4.4.9
# Fri, 01 Oct 2021 03:48:43 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Oct 2021 03:48:44 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Oct 2021 03:48:44 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Oct 2021 03:48:44 GMT
COPY file:df3353d9b2c25ef83b499ecae7fd5d611adb4a9462a577435178acaad3c8c695 in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:48:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:48:45 GMT
EXPOSE 27017
# Fri, 01 Oct 2021 03:48:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2d7ad0c540d3d6a3e1c2a1b6c954e66d6e6b6c75bf59c2104a92df0740cb53`  
		Last Modified: Fri, 01 Oct 2021 03:50:43 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfa2cc193b0006a873a273675ddb5c640b1fdd56d4ad78726a41aaa7b51a77d`  
		Last Modified: Fri, 01 Oct 2021 03:50:44 GMT  
		Size: 2.9 MB (2912520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d5b73fe1cd6faecdcb227db764498b01bfd441f3f96ed82407cc2b0192d557`  
		Last Modified: Fri, 01 Oct 2021 03:50:44 GMT  
		Size: 6.4 MB (6406199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b52226661184787da215a55f6b0a504f15f1663c47dddb8587a96466f893f88`  
		Last Modified: Fri, 01 Oct 2021 03:50:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac442448e9cf66535bba58c507118920f731f025366dc0179061d3df8d7499f`  
		Last Modified: Fri, 01 Oct 2021 03:51:28 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f509a2712f4ae4f567c0166a7fd3a878677d3f6ac00e48f18fbec865e8050`  
		Last Modified: Fri, 01 Oct 2021 03:51:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fc6a47fd05cec8009143360355f13d91a0077910d40abb4e2a9f803528eb2e`  
		Last Modified: Fri, 01 Oct 2021 03:51:46 GMT  
		Size: 130.0 MB (130011411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a2bee75686e6ff856f994e2ffc7bc58392ee56f8fc6fc398cd9e234419228a`  
		Last Modified: Fri, 01 Oct 2021 03:51:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a111e204e7cf0148df3e7aa4d5be1fb23a0c635b24bacfc6a7baba64c4e9c70e`  
		Last Modified: Fri, 01 Oct 2021 03:51:28 GMT  
		Size: 4.7 KB (4699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
