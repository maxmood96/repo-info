## `mongo:4-focal`

```console
$ docker pull mongo@sha256:3a5a916a1e24d355c731deaeadcc5d8373349d132ae40536ca6d9938df8de821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:ce0e402ef7626c21087142bab1cf387e54f671e7a1044efb45c5e74bc4bd83d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171688644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143c893415c04a28b523fbfdbc4e298aa4c3f863106e80619431bfd1c939b125`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Mon, 23 May 2022 23:31:01 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 23 May 2022 23:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2022 23:31:11 GMT
ENV GOSU_VERSION=1.12
# Mon, 23 May 2022 23:31:11 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 23 May 2022 23:31:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 23 May 2022 23:31:29 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 23 May 2022 23:32:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Mon, 23 May 2022 23:32:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 23 May 2022 23:32:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 23 May 2022 23:32:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 23 May 2022 23:32:10 GMT
ENV MONGO_MAJOR=4.4
# Mon, 23 May 2022 23:32:11 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 23 May 2022 23:32:11 GMT
ENV MONGO_VERSION=4.4.14
# Mon, 23 May 2022 23:32:26 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 23 May 2022 23:32:27 GMT
VOLUME [/data/db /data/configdb]
# Mon, 23 May 2022 23:32:27 GMT
ENV HOME=/data/db
# Mon, 23 May 2022 23:32:27 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Mon, 23 May 2022 23:32:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 23:32:28 GMT
EXPOSE 27017
# Mon, 23 May 2022 23:32:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d1e6b0e1ffe42821814ccdbc8ef5a82b419b7a1dcc6c6aa02a0fa3de1ab7bf`  
		Last Modified: Mon, 23 May 2022 23:35:14 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015ccc3eeca855fb936e2159d1daaa6f67b426d845f51cf5f0b4096c3429f523`  
		Last Modified: Mon, 23 May 2022 23:35:14 GMT  
		Size: 3.1 MB (3063970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0129deec1aaf785650249a55f1d7bac4a95e7b18f8ed660a457f6de21f9d4ca5`  
		Last Modified: Mon, 23 May 2022 23:35:15 GMT  
		Size: 6.5 MB (6505826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9522656704457d67a8a3fbd7d890bd495e5bafbfda575955c2eaa93d7ca141`  
		Last Modified: Mon, 23 May 2022 23:35:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3ef9bcc94eb9ad48fd9349a1a501e19e0a5ccc2e80725666dd27a66697269b`  
		Last Modified: Mon, 23 May 2022 23:36:00 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8222248b71f678e36f0838aaf16de556181bbb63b6f6364cddca739b750d688f`  
		Last Modified: Mon, 23 May 2022 23:36:00 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3bc88a39253883210505e0aca9aa70c82aa5e887a0fa18b53560b3a2d5dd52`  
		Last Modified: Mon, 23 May 2022 23:36:18 GMT  
		Size: 133.5 MB (133543984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d1c9f975d7561d4d3368d3276a696d31a8336c9b4f78d0c56f7a75bffa9648`  
		Last Modified: Mon, 23 May 2022 23:36:00 GMT  
		Size: 4.9 KB (4949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0e5c0cbb558d042a1d17450e4905b0c9b0917c70206c4ef2965a27cdbffc0889
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166761681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d0240bc8a555e5bef090bf229e07a4735165e5d1ba96659922ea32ef3ace12`
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
# Mon, 23 May 2022 23:59:51 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Mon, 23 May 2022 23:59:52 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 23 May 2022 23:59:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 23 May 2022 23:59:54 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 23 May 2022 23:59:55 GMT
ENV MONGO_MAJOR=4.4
# Mon, 23 May 2022 23:59:56 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 23 May 2022 23:59:57 GMT
ENV MONGO_VERSION=4.4.14
# Tue, 24 May 2022 00:00:17 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 24 May 2022 00:00:17 GMT
VOLUME [/data/db /data/configdb]
# Tue, 24 May 2022 00:00:18 GMT
ENV HOME=/data/db
# Tue, 24 May 2022 00:00:20 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Tue, 24 May 2022 00:00:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 May 2022 00:00:21 GMT
EXPOSE 27017
# Tue, 24 May 2022 00:00:22 GMT
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
	-	`sha256:c62259096f46cc79a253a4953eaafef8109b172e0dc5e7a656b1008ad7ff7445`  
		Last Modified: Tue, 24 May 2022 00:04:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa26079d5f72532ca0f769b367af3fb6e5b05cec0930815aa81219f89cda3af1`  
		Last Modified: Tue, 24 May 2022 00:04:25 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf244e9b1c9e808194ffbdce02be2ef595f7fb4be032aa900bed4090c72d117`  
		Last Modified: Tue, 24 May 2022 00:04:42 GMT  
		Size: 130.4 MB (130424147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe73ee32f125c927c114420c6703f0e7584ce8dbfc8dc38679ef506fc97eb09`  
		Last Modified: Tue, 24 May 2022 00:04:25 GMT  
		Size: 4.9 KB (4949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
