## `mongo:5-focal`

```console
$ docker pull mongo@sha256:b45c136860fe7bb4fff32e8425457e01c3c8ee22e7e57d1b5d928243d4b6b1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:4897d6662abfbefef888ff25d1bea5e6443501bdc299af6aa1c6944a65d1794a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248523666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee13a1eacac90d5d727748ea5c2a8bfaf8b52393f0b12891d349cfb19c7060d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:38:41 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 07 Jan 2022 03:38:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:38:49 GMT
ENV GOSU_VERSION=1.12
# Fri, 07 Jan 2022 03:38:49 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 07 Jan 2022 03:39:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 07 Jan 2022 03:39:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 07 Jan 2022 03:39:11 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 07 Jan 2022 03:39:11 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 07 Jan 2022 03:39:11 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 07 Jan 2022 03:39:12 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 07 Jan 2022 03:39:12 GMT
ENV MONGO_MAJOR=5.0
# Fri, 07 Jan 2022 03:39:13 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 07 Jan 2022 03:39:13 GMT
ENV MONGO_VERSION=5.0.5
# Fri, 07 Jan 2022 03:39:36 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 07 Jan 2022 03:39:38 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 07 Jan 2022 03:39:39 GMT
VOLUME [/data/db /data/configdb]
# Fri, 07 Jan 2022 03:39:39 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Fri, 07 Jan 2022 03:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jan 2022 03:39:39 GMT
EXPOSE 27017
# Fri, 07 Jan 2022 03:39:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecab26900ceb816ecb13be911f506dc9970c103504a0402a110bed8a09354422`  
		Last Modified: Fri, 07 Jan 2022 03:42:40 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1847fcb70562b1afc3c3cfea06e6a0a50be8dd739b65569a72853340aa913e65`  
		Last Modified: Fri, 07 Jan 2022 03:42:39 GMT  
		Size: 3.1 MB (3064538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7de23811c0dc3af5c7a2fef91300b3ef7d56335b5b5300498f40edb2e51dbab`  
		Last Modified: Fri, 07 Jan 2022 03:42:39 GMT  
		Size: 6.5 MB (6505849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd51833fb97f2e1d80ffb59154f237b2f37bf64ee02de32618dde36be05019`  
		Last Modified: Fri, 07 Jan 2022 03:42:38 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eccd2be8afb9e1a8ca7224d9994a41ab0dd4b64ae4712a08d8019c23c69ced9`  
		Last Modified: Fri, 07 Jan 2022 03:42:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8a8cd6879ff4231cc3b9fcd9196649f42012767a6d17b91fc792f1df009880`  
		Last Modified: Fri, 07 Jan 2022 03:42:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ca3abc397d6acbcdca76fb68c367bdfc7cb1cc038f81bb54bf5cee47f5a7bc`  
		Last Modified: Fri, 07 Jan 2022 03:43:04 GMT  
		Size: 210.4 MB (210378179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7481c3682d3c9839e362d26e7215415155645fdf3b9c51eb8938fe33919dc785`  
		Last Modified: Fri, 07 Jan 2022 03:42:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af377cb9eb7df03e9be661ab4f27dcffb67faab7023c66c9a4f2ee6998ff2c81`  
		Last Modified: Fri, 07 Jan 2022 03:42:36 GMT  
		Size: 4.9 KB (4946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-focal` - linux; arm64 variant v8

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
