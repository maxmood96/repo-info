## `mongo:focal`

```console
$ docker pull mongo@sha256:ad99ee7785dcf50dc6ddbdac5e134da3ee2ffa610fc5c8af6a5a7e16760bb802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:focal` - linux; amd64

```console
$ docker pull mongo@sha256:ec63238cfff22866241104a425892204c2eb76fe4eed53661b24db9bacbdf446
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248164536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfda7a2cf27349457de1696cb5c97b422a4292af17a7ef3b7032348b5e6ff1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:04:13 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 16 Oct 2021 03:04:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:04:21 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 Oct 2021 03:04:21 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 16 Oct 2021 03:04:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 Oct 2021 03:04:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 16 Oct 2021 03:04:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 16 Oct 2021 03:04:41 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 16 Oct 2021 03:04:41 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 16 Oct 2021 03:04:42 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 16 Oct 2021 03:04:42 GMT
ENV MONGO_MAJOR=5.0
# Sat, 16 Oct 2021 03:04:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 08 Dec 2021 00:24:19 GMT
ENV MONGO_VERSION=5.0.5
# Wed, 08 Dec 2021 00:24:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 08 Dec 2021 00:25:01 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 08 Dec 2021 00:25:01 GMT
VOLUME [/data/db /data/configdb]
# Wed, 08 Dec 2021 00:25:01 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Wed, 08 Dec 2021 00:25:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Dec 2021 00:25:01 GMT
EXPOSE 27017
# Wed, 08 Dec 2021 00:25:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90eb44ebc60bb16588c109f5262f2e1ddf21b139ded13daaa291f02dd3f2289e`  
		Last Modified: Sat, 16 Oct 2021 03:06:23 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5085b59f2efb7e626508e23c85e6ef162ba3fa1e69c4c3bf1a69ffc10dee0586`  
		Last Modified: Sat, 16 Oct 2021 03:06:23 GMT  
		Size: 3.1 MB (3064302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7499923d022b687faac3ecd024ab159a472120a06d0df1583b035f6adf2dbd8`  
		Last Modified: Sat, 16 Oct 2021 03:06:24 GMT  
		Size: 6.5 MB (6506381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019496b6c44a3bff7c252b5ea300acbb686bedaf7834036cfaa66c4b56097394`  
		Last Modified: Sat, 16 Oct 2021 03:06:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0df4f407f693c30a6a5431eb968f6f7a7311337611a86ec63e9ab346719baa3`  
		Last Modified: Sat, 16 Oct 2021 03:06:20 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351daa315b6c1d66ece665ede381cb48d62d33ff7094565926020c8313d9b3ab`  
		Last Modified: Sat, 16 Oct 2021 03:06:20 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a233e6240acc3bfa50b1b65db8a990f3be800681ec0d5996d8e52a085d11ee2a`  
		Last Modified: Wed, 08 Dec 2021 00:26:13 GMT  
		Size: 210.0 MB (210018055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f57d6be64f36f1c01f3067d72702e57ac0bf807724f97f1dbfbe5072a897cf`  
		Last Modified: Wed, 08 Dec 2021 00:25:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1b5b3453232ba5d764e65b4182a47de0e2f950aa37bd0acd18618e95b922c9`  
		Last Modified: Wed, 08 Dec 2021 00:25:44 GMT  
		Size: 5.0 KB (4954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8a823923d80e819e21ee6c179eabf42460b6b7d8ac3dd5f35b59419ae5413640
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240584346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427dd68dd642a1b4527c2e8e48f16cb2a117c4429b854e64d42f2749ec961bc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:54:22 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 07 Jan 2022 02:54:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:54:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 07 Jan 2022 02:54:34 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 07 Jan 2022 02:54:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 02:54:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 02:55:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 02:55:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 07 Jan 2022 02:55:04 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 07 Jan 2022 02:55:05 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 07 Jan 2022 02:55:06 GMT
ENV MONGO_MAJOR=5.0
# Fri, 07 Jan 2022 02:55:07 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 07 Jan 2022 02:55:08 GMT
ENV MONGO_VERSION=5.0.5
# Fri, 07 Jan 2022 02:55:34 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 07 Jan 2022 02:55:35 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 07 Jan 2022 02:55:36 GMT
VOLUME [/data/db /data/configdb]
# Fri, 07 Jan 2022 02:55:38 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 02:55:39 GMT
EXPOSE 27017
# Fri, 07 Jan 2022 02:55:40 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85128fd0bdbd21eacb87b1a9d4b89432feab85c9332caa3b4d5372ea6aae020`  
		Last Modified: Fri, 07 Jan 2022 02:59:54 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d0b1d6186796e8e37d6f6e96c650c8d9ed7d0b75f8f1c9bd997d16fcc8e218`  
		Last Modified: Fri, 07 Jan 2022 02:59:54 GMT  
		Size: 2.9 MB (2912276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2fd1a09846b8f4ba763c5295f435ae4b8fb3fc2801fd9a7feb992bcfa1eb95`  
		Last Modified: Fri, 07 Jan 2022 02:59:55 GMT  
		Size: 6.2 MB (6248505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff66d32779057b30050b5c6425df611781d393b6e7622a89f49b6d021c17a3e`  
		Last Modified: Fri, 07 Jan 2022 02:59:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc46a45cd078966114ea7cd56294805286147b732252f9c3e0f6704934ad24b8`  
		Last Modified: Fri, 07 Jan 2022 02:59:52 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0433167df8ee88bc1760ceaabcc69ed8ca06b2f7d945d724c5a8881273ca7e9`  
		Last Modified: Fri, 07 Jan 2022 02:59:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95b813873f03aa1adcfbb99d6c7ff34d318f849243b84d6b1f01b6a2e3ceb3c`  
		Last Modified: Fri, 07 Jan 2022 03:00:19 GMT  
		Size: 204.2 MB (204243922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67186c7ba8dd2bb1978c6e6081db9df5c26ca51e89897cc3af679706d64cc13`  
		Last Modified: Fri, 07 Jan 2022 02:59:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da11637980f1913055a137dbab35bdaaff220d44aeacab914649f0c63f262759`  
		Last Modified: Fri, 07 Jan 2022 02:59:52 GMT  
		Size: 4.9 KB (4945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
