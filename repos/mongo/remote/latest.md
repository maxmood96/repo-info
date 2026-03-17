## `mongo:latest`

```console
$ docker pull mongo@sha256:d343c378b5c6e2fe373174abcf4a877be0dfc721b5d0b9d582204dccb1c00b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:3a48ba077bff43ff6f4affa874b03ef0c78be3a62db8a15fa7ea0e86918439a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.8 MB (337816942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fc3eda4f9a20a603760951ba923b2904f477a5e5efef1b220ac4b572b0f4ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 18:09:55 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 17 Mar 2026 18:10:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 18:10:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:10:16 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 17 Mar 2026 18:10:16 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 17 Mar 2026 18:10:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:10:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 18:10:16 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 17 Mar 2026 18:10:16 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 18:10:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 18:10:16 GMT
ENV MONGO_MAJOR=8.2
# Tue, 17 Mar 2026 18:10:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 17 Mar 2026 18:10:16 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 17 Mar 2026 18:10:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 17 Mar 2026 18:10:36 GMT
VOLUME [/data/db /data/configdb]
# Tue, 17 Mar 2026 18:10:36 GMT
ENV HOME=/data/db
# Tue, 17 Mar 2026 18:10:36 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 17 Mar 2026 18:10:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:10:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:10:36 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Mar 2026 18:10:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2605962b028632a0b8652d3e951ecf2798b46aba298b9b231198cc1451274ca1`  
		Last Modified: Tue, 17 Mar 2026 18:11:16 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c85015575adb6d73b0a3a5a8ab1890d21eb3a0627efcec8bbc9ac27eba8e34f`  
		Last Modified: Tue, 17 Mar 2026 18:11:16 GMT  
		Size: 1.5 MB (1509488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e41d5f93e35647acfe6e5a37c32e0604b100b762ff2f60bbea1e6115fd259b0`  
		Last Modified: Tue, 17 Mar 2026 18:11:16 GMT  
		Size: 933.6 KB (933635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5c9bc3c6a6835209525cea7214b2baecf3900303dfef0689bb7da9803d804d`  
		Last Modified: Tue, 17 Mar 2026 18:11:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8567d1c4785e4b28e757f24dd04b434ca8b494ad343c96254457928e5a19096`  
		Last Modified: Tue, 17 Mar 2026 18:11:16 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1d6859a473296343a8110c82d4e5cef2211efccfbec9295517a016e6899b83`  
		Last Modified: Tue, 17 Mar 2026 18:11:24 GMT  
		Size: 305.6 MB (305635227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a854eada6f0da6cce6acd66504d9683b6596b4adb7396bb95378f9606fbea9`  
		Last Modified: Tue, 17 Mar 2026 18:11:18 GMT  
		Size: 5.0 KB (5005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:cb1364c46755b2493d56da7de092cd31a1e7283bfb9b99cb50468257430dee1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2690044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afa7b7bd7e50c37ac5c4e322097d3f53ecd37bae6a886be497b16f36ea3fdd9`

```dockerfile
```

-	Layers:
	-	`sha256:51deed191cabc88b2eb5d20c01815d78c5dce48c51eb7646aaba4a5e326da0cf`  
		Last Modified: Tue, 17 Mar 2026 18:11:17 GMT  
		Size: 2.7 MB (2661252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee7db4c3583f71c4fc1b29f507d3709741ba47ee26ca8cde5c6437eab9282e3f`  
		Last Modified: Tue, 17 Mar 2026 18:11:16 GMT  
		Size: 28.8 KB (28792 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a9068ae2d236847d8865cc40f380ff4a75266fff743b4f9084d0f46cce72ac79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322506563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1c9ff2047611faa6561c94b3b4cfa7350dbbbda21aa86237fa353a07a35d25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 18:09:43 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 17 Mar 2026 18:09:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 18:10:09 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:10:09 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 17 Mar 2026 18:10:09 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 17 Mar 2026 18:10:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:10:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 18:10:09 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 17 Mar 2026 18:10:09 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 18:10:09 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 18:10:09 GMT
ENV MONGO_MAJOR=8.2
# Tue, 17 Mar 2026 18:10:09 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 17 Mar 2026 18:10:09 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 17 Mar 2026 18:10:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 17 Mar 2026 18:10:34 GMT
VOLUME [/data/db /data/configdb]
# Tue, 17 Mar 2026 18:10:34 GMT
ENV HOME=/data/db
# Tue, 17 Mar 2026 18:10:34 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 17 Mar 2026 18:10:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:10:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:10:34 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Mar 2026 18:10:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9554779821efefdc203308b5ebd89c0c4edbe971b9322f1fc10a5a6f6e4ac5a`  
		Last Modified: Tue, 17 Mar 2026 18:11:07 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525bed6c17aa5344e7a7230eaf25b05716c1b3a9c6e4eb6193a221e93059b8d7`  
		Last Modified: Tue, 17 Mar 2026 18:11:08 GMT  
		Size: 1.5 MB (1494487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2793ee0b560f12a2ab010a5a1a0cc17f050470da8ac021a6d18b8edc536f4d25`  
		Last Modified: Tue, 17 Mar 2026 18:11:08 GMT  
		Size: 886.0 KB (886001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86297d6e55b16c11e793c5070d1bac2aca0adef7e27a65818fdb1f5ebef55e03`  
		Last Modified: Tue, 17 Mar 2026 18:11:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104c4a307f09ca69d35fa437feb29ac4b20f475698dac7946f2325112e7d723`  
		Last Modified: Tue, 17 Mar 2026 18:11:09 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95d86c562cdcd18dca07d363a1955dcb68cdf8d7ea6d1f0679e8d773ad7dee8`  
		Last Modified: Tue, 17 Mar 2026 18:11:14 GMT  
		Size: 291.2 MB (291249771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88d203c09f08dc14f6f70cf1faef5e71e937710b1dc7d043882315a80ea343f`  
		Last Modified: Tue, 17 Mar 2026 18:11:09 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:f863cd915191889471145df7b5122b2d84f1651c2070c4027ba8e7ce755200ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ce654df9a572062ef22558b63b07f9eb55e664dfeae4261325706223986e3b`

```dockerfile
```

-	Layers:
	-	`sha256:5d9cae264b1ba6e77898e410f7569c70d3cb2b6aca7e83058751c0fab8c9275f`  
		Last Modified: Tue, 17 Mar 2026 18:11:08 GMT  
		Size: 2.7 MB (2662388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d4ad92f8657743ce9f65011e922a36eaf0124b51bbecb40597476eb29165c8`  
		Last Modified: Tue, 17 Mar 2026 18:11:08 GMT  
		Size: 29.0 KB (29019 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.32522; amd64

```console
$ docker pull mongo@sha256:47d17995cd74ba4db09c71ea0c6144ff25ec0b4fbf8c0fdae2fb7ee16842fef4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2898502252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3f98054d71b96c28f56a20ac59b99885eb6e1a464478e3c16690385d505307`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 17 Mar 2026 18:05:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Mar 2026 18:05:28 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 17 Mar 2026 18:05:28 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.6-signed.msi
# Tue, 17 Mar 2026 18:05:29 GMT
ENV MONGO_DOWNLOAD_SHA256=a6672561354b1bd37c5ba8d7dd76b66bfdbd28baec6fd8eb2b7eb2b32eaf344f
# Tue, 17 Mar 2026 18:07:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 17 Mar 2026 18:07:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 17 Mar 2026 18:07:32 GMT
EXPOSE 27017
# Tue, 17 Mar 2026 18:07:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2666b4db1bf612509a1a01c4481b3ab7958c6fd378398d17a1e776283513656b`  
		Last Modified: Tue, 17 Mar 2026 18:07:43 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1938b67d91f4951956a41d6518581fd9734a9472cc05182ad63d4c400082ec4`  
		Last Modified: Tue, 17 Mar 2026 18:07:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53dc785b70d4cbb8ce765821bee64d36e6eb9e9bae0c9f48a7b44b55ad6ef5d`  
		Last Modified: Tue, 17 Mar 2026 18:07:44 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1c54015a5565ef3b7d1963f81083feb67659679ac5592972d974c3114ace07`  
		Last Modified: Tue, 17 Mar 2026 18:07:42 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852b2cbab53aafe24e1b523e10cfd38eed2dbd7e7ab567097615e1e4b841f188`  
		Last Modified: Tue, 17 Mar 2026 18:09:01 GMT  
		Size: 817.3 MB (817297063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547260cd6673b450a86b8ff29adddbdee61c57b393366cb5b07fe63c3a9b9f4`  
		Last Modified: Tue, 17 Mar 2026 18:07:42 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0526c8497d92dcf7e8eecfe402d085ae08b1098880e5d12bb74fcc5597fc6665`  
		Last Modified: Tue, 17 Mar 2026 18:07:42 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a056fd3a0d06f58a25fbf7bf34eea77471f7f51b7cb805170990748c80a7b05c`  
		Last Modified: Tue, 17 Mar 2026 18:07:42 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.4893; amd64

```console
$ docker pull mongo@sha256:2bddc1202f7d5f0275bcc884ad482372b715e56161b168477fceb1e131f402bb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2799555230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9b72ee36ebeaea5b4e62e3d0ad20db9134ddca2ab092f09333952d6243e6d9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 17 Mar 2026 18:05:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Mar 2026 18:05:32 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 17 Mar 2026 18:05:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.6-signed.msi
# Tue, 17 Mar 2026 18:05:33 GMT
ENV MONGO_DOWNLOAD_SHA256=a6672561354b1bd37c5ba8d7dd76b66bfdbd28baec6fd8eb2b7eb2b32eaf344f
# Tue, 17 Mar 2026 18:07:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 17 Mar 2026 18:07:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 17 Mar 2026 18:07:58 GMT
EXPOSE 27017
# Tue, 17 Mar 2026 18:07:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62430fe0975ecfdad77ac0cf66b918cd69edc36a8b48e0bbed20b0a612b2cf35`  
		Last Modified: Tue, 17 Mar 2026 18:08:13 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e551441cbadd370dd75ab0f9e96a3ba577871c0d919aec1f92880588c48c8ca0`  
		Last Modified: Tue, 17 Mar 2026 18:08:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404a5794660fbb5b6d7af22cd39d2d70fb8d7704ca52ad286e5eb70c192045f3`  
		Last Modified: Tue, 17 Mar 2026 18:08:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff55011c515d23bc6eb501efe52e72b599716ed0bc6b049667d25a614104caeb`  
		Last Modified: Tue, 17 Mar 2026 18:08:11 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4074d47cb546f2a399f03a0489132de7160f4aa8cca8c529b4981f5dcd0e80`  
		Last Modified: Tue, 17 Mar 2026 18:09:31 GMT  
		Size: 817.3 MB (817264643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86dbb13ac1d3e15b791132a7470f6578826f8fb2a5b2cf59b0d4310c11373e`  
		Last Modified: Tue, 17 Mar 2026 18:08:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4519129b8b4a6fc4078f8a2189660ca379ccf761a45f886509f806bf8dc99993`  
		Last Modified: Tue, 17 Mar 2026 18:08:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1492217039ef3d5728ef075dbe9713f8bd05833a9a6bc54b0b8f76f6938c935f`  
		Last Modified: Tue, 17 Mar 2026 18:08:11 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
