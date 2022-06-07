## `mongo:focal`

```console
$ docker pull mongo@sha256:f1fa27e4f4535c391afe8250416cdd55893bbdd3979f921a150d26179cddc916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:focal` - linux; amd64

```console
$ docker pull mongo@sha256:f548240f5a61d1ecfe4c16cc73c8a12c1701bf9d47d0121f110dd5655ebefd55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245306167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3f6d5230f67503df7a474bc704166b0fb52792ed4d054f95297541778f30f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:32:20 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 07 Jun 2022 00:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:32:28 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jun 2022 00:32:28 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 07 Jun 2022 00:32:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jun 2022 00:32:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jun 2022 00:32:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 07 Jun 2022 00:32:45 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 07 Jun 2022 00:32:45 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 07 Jun 2022 00:32:45 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 07 Jun 2022 00:32:45 GMT
ENV MONGO_MAJOR=5.0
# Tue, 07 Jun 2022 00:32:46 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 07 Jun 2022 00:32:46 GMT
ENV MONGO_VERSION=5.0.9
# Tue, 07 Jun 2022 00:33:10 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 07 Jun 2022 00:33:12 GMT
VOLUME [/data/db /data/configdb]
# Tue, 07 Jun 2022 00:33:12 GMT
ENV HOME=/data/db
# Tue, 07 Jun 2022 00:33:12 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Tue, 07 Jun 2022 00:33:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:33:12 GMT
EXPOSE 27017
# Tue, 07 Jun 2022 00:33:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ef66a8492a7b4b656a9dddda9f1bfa3bd3213773c8449b68dadac55605c96f`  
		Last Modified: Tue, 07 Jun 2022 00:34:56 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cec14c8f9e0886403900a1569d2a6a4c33fa3b3984d7dc128eb71c437fe06d`  
		Last Modified: Tue, 07 Jun 2022 00:34:57 GMT  
		Size: 3.1 MB (3064245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c3018eb09a584362cfe9d340566fb755597b453ea58bf5c6c15c8e120efe44`  
		Last Modified: Tue, 07 Jun 2022 00:34:57 GMT  
		Size: 6.5 MB (6506121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc9e1c2556b202042e54ddafe2ae992d58cd462bd3a75ab2c55ccbc42c76dc9`  
		Last Modified: Tue, 07 Jun 2022 00:34:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c62d035322149352916a5f076138bc992cb1decf2017ac0143221c8d5afe2`  
		Last Modified: Tue, 07 Jun 2022 00:34:53 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a103a446c3f38697e880d478313e8128e54f3245c42f9e4e047d2f94476bfd0`  
		Last Modified: Tue, 07 Jun 2022 00:34:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6085016f3a0c6b14cdd29d6287e1745c48e6d43332da6be34795c6b8beb607`  
		Last Modified: Tue, 07 Jun 2022 00:35:22 GMT  
		Size: 207.2 MB (207154539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8109db46fca75b5f8e57f37f43d411a16dd24993d858e7153e451bd252bafa`  
		Last Modified: Tue, 07 Jun 2022 00:34:53 GMT  
		Size: 4.9 KB (4945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0ee764d498848174efae8b85289e71adaae5185463b9b8a7a65ebeb51d5cdb2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237800304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139e6a541a7923c8df93a81f527101c4dfe414cc8d6b22f9361218112d15d2a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Mon, 23 May 2022 23:58:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 23 May 2022 23:58:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2022 23:58:47 GMT
ENV GOSU_VERSION=1.12
# Mon, 23 May 2022 23:58:48 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 23 May 2022 23:59:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 23 May 2022 23:59:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 23 May 2022 23:59:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Mon, 23 May 2022 23:59:09 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 23 May 2022 23:59:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 23 May 2022 23:59:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 23 May 2022 23:59:12 GMT
ENV MONGO_MAJOR=5.0
# Mon, 23 May 2022 23:59:13 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 02 Jun 2022 18:00:35 GMT
ENV MONGO_VERSION=5.0.9
# Thu, 02 Jun 2022 18:00:59 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 02 Jun 2022 18:01:00 GMT
VOLUME [/data/db /data/configdb]
# Thu, 02 Jun 2022 18:01:00 GMT
ENV HOME=/data/db
# Thu, 02 Jun 2022 18:01:02 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Thu, 02 Jun 2022 18:01:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Jun 2022 18:01:03 GMT
EXPOSE 27017
# Thu, 02 Jun 2022 18:01:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0512bdaae73cf7907a5372e174d29934ef3d58b8c419189a40baf81b04f43a`  
		Last Modified: Tue, 24 May 2022 00:03:41 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51571d358e429281c0e3ed2ed7f53f21567aef6fe7532e2ec0b188209e61c8ca`  
		Last Modified: Tue, 24 May 2022 00:03:42 GMT  
		Size: 2.9 MB (2911511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa226bdd983047c6f94630a29b97dfac6379c6aab11572a84d338b40ae3635f6`  
		Last Modified: Tue, 24 May 2022 00:03:43 GMT  
		Size: 6.2 MB (6248132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0e3e44d3aceb5be4f15cafd160b7d54476229cb3d006f27cda634aef64be5e`  
		Last Modified: Tue, 24 May 2022 00:03:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106719865e3d888303573607c0a3e28219aa7b352067276bfb931eec1c45686`  
		Last Modified: Tue, 24 May 2022 00:03:39 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600ad43e7428f314f08b962d6543e2f4facea799bd703f6b6a383a19669bfef6`  
		Last Modified: Tue, 24 May 2022 00:03:39 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943041bc9b737c9be25a9769179bb1a62422adda25ff26541fd90416dc7c20f2`  
		Last Modified: Thu, 02 Jun 2022 18:02:34 GMT  
		Size: 201.5 MB (201462770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c0dd8839074bb1a604367fe8df3d162750e7f8814457531230766bcf15891b`  
		Last Modified: Thu, 02 Jun 2022 18:02:08 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
