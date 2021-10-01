## `mongo:focal`

```console
$ docker pull mongo@sha256:7b5279b8eb13a83f04d86674cb14f03317ac36d32a02fcd3f2c345ca452b9ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:focal` - linux; amd64

```console
$ docker pull mongo@sha256:87ae78e36c0234dd0ef3c03a65d06353ffac67eb7b22c411cff960f134806642
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248813510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf4b4ee3beead6425ed92e6ae915bd0a5da899bd43e2722a756eceb579aa5d4`
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
# Tue, 31 Aug 2021 03:51:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 31 Aug 2021 03:51:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 31 Aug 2021 03:51:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 31 Aug 2021 03:51:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 31 Aug 2021 03:51:35 GMT
ENV MONGO_MAJOR=5.0
# Tue, 31 Aug 2021 03:51:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Sep 2021 22:20:11 GMT
ENV MONGO_VERSION=5.0.3
# Mon, 20 Sep 2021 22:20:45 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Sep 2021 22:20:47 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Sep 2021 22:20:48 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Sep 2021 22:20:48 GMT
COPY file:df3353d9b2c25ef83b499ecae7fd5d611adb4a9462a577435178acaad3c8c695 in /usr/local/bin/ 
# Mon, 20 Sep 2021 22:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Sep 2021 22:20:48 GMT
EXPOSE 27017
# Mon, 20 Sep 2021 22:20:48 GMT
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
	-	`sha256:ff2b9c6e6f3a34b81bff9c8e5cca15de3929bb9eaac42390afe055c4fb1dead8`  
		Last Modified: Tue, 31 Aug 2021 03:54:53 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149f6335fc27dbe4a0d20cedeadb246cd0527052841f69e697ecf1dc3e5345cf`  
		Last Modified: Tue, 31 Aug 2021 03:54:53 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0adda745823b05b58810f001e2b9c63d7c51d9bef9508d80d3f5d0fafe62aa`  
		Last Modified: Mon, 20 Sep 2021 22:22:49 GMT  
		Size: 210.7 MB (210663765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170bad7cd6cb209d04013bdd2899703d7b499e4bc21699f97e7bf86f6048af57`  
		Last Modified: Mon, 20 Sep 2021 22:22:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7fd7a769b4bc7b673d2aca605c010f13f8cd5ebc222d0940a9449a3d1ec94f`  
		Last Modified: Mon, 20 Sep 2021 22:22:21 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:22fe59c3baf283535fcd6daa5a496779a8ad9dbd1ccaddcdd34d0074a87169aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238946746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d77cdc4a135468349305a7788be24a3e64abf0046ab48e69e12d40bdfc4246`
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
# Fri, 01 Oct 2021 03:47:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 03:47:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Oct 2021 03:47:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Oct 2021 03:47:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Oct 2021 03:47:38 GMT
ENV MONGO_MAJOR=5.0
# Fri, 01 Oct 2021 03:47:39 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Oct 2021 03:47:39 GMT
ENV MONGO_VERSION=5.0.3
# Fri, 01 Oct 2021 03:48:04 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Oct 2021 03:48:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Oct 2021 03:48:06 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Oct 2021 03:48:06 GMT
COPY file:df3353d9b2c25ef83b499ecae7fd5d611adb4a9462a577435178acaad3c8c695 in /usr/local/bin/ 
# Fri, 01 Oct 2021 03:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 03:48:07 GMT
EXPOSE 27017
# Fri, 01 Oct 2021 03:48:07 GMT
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
	-	`sha256:10b8e6103dc39531c96089f285b6a91a574d84dcafd43f37848397091829ed47`  
		Last Modified: Fri, 01 Oct 2021 03:50:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e26edf56c5d0ae1b907038ce4526de78efa8d7da79d2ef754f348635568ff83`  
		Last Modified: Fri, 01 Oct 2021 03:50:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29473489a1ae2215f37ddf52cc7b5eb760eeff978f2877d8b2ee31d8838bb2fa`  
		Last Modified: Fri, 01 Oct 2021 03:51:10 GMT  
		Size: 202.4 MB (202447174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02075687f04886eee4859dfc3e42c5c6a145f465f331f79f94025a3ee46618`  
		Last Modified: Fri, 01 Oct 2021 03:50:41 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94e6498398ee71c5ffc5021c6a99721c469444ccc19bd1fde3933e5dd8cbbdd`  
		Last Modified: Fri, 01 Oct 2021 03:50:41 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
