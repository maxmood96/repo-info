## `mongo:latest`

```console
$ docker pull mongo@sha256:2e018e386e891d2e4239aca6035fb7701dac51b72891247ecd2f95ff8a167859
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:c2c12cd59c8171f5723fad813b7fb92889b389aab166a4169d6b775ae09fdd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290969534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c5f35e6c6deae286b0d9bd65a093cd273858522f09e8b04ebb5585b7838628`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 01 May 2025 22:01:24 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 01 May 2025 22:01:24 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 01 May 2025 22:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 01 May 2025 22:01:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_MAJOR=8.0
# Thu, 01 May 2025 22:01:24 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 22:01:24 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 01 May 2025 22:01:24 GMT
VOLUME [/data/db /data/configdb]
# Thu, 01 May 2025 22:01:24 GMT
ENV HOME=/data/db
# Thu, 01 May 2025 22:01:24 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Thu, 01 May 2025 22:01:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 22:01:24 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 01 May 2025 22:01:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aa6a7c13c0ebacea1683a9d74eb974031e133db33b853d4d6e90a6cba422bf`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a30a2444162208d43e011acb1e3ea91c1f688435e01601830809d42186e830`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 1.5 MB (1508590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c82d0518f83718a3a081365cdd6358cad8379cddb067a7941260e8891ec9e7`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 1.1 MB (1131070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6be4e21c66f8533616a1432544e712a586c6c7840241f93c6cab31ef9276a8`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ae99607c30f6663c0ff4a573d36e511e5720f1c52efe9d47834566761109af`  
		Last Modified: Thu, 08 May 2025 17:04:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca015e545994e8a04048ac8dfdcf2775f35e97b645ed5004c3dbc88c08f5704d`  
		Last Modified: Thu, 08 May 2025 17:08:46 GMT  
		Size: 258.6 MB (258605741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54db8e3d8732559d77d5f452b6c59a60908e115273bb3e9bcb171c3490896797`  
		Last Modified: Thu, 08 May 2025 17:04:36 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:4e4935877960d7c52980c827a77909e76a0ddbd9a8d47a2f6d5b09b6f2dce59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9580f6a9d3681b773a1222088f844565d1c6109e9d6dced151cd73373c44f928`

```dockerfile
```

-	Layers:
	-	`sha256:02319a7e8ffe0e9aec60429fa691da079b86f16b2067f68a50c240338f6cfd7e`  
		Last Modified: Thu, 08 May 2025 17:19:49 GMT  
		Size: 2.5 MB (2524548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b06e114f492355ec830611b2bd349e04df8e43c790381b64b0d5df712c151e9`  
		Last Modified: Thu, 08 May 2025 17:19:48 GMT  
		Size: 28.8 KB (28840 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:1026d540a24df2d312d7d76e0d885f3fec4bc9fad0fbebc0e9793d6e4c914aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (278988268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c763bc4de8b048717ee40e9ee4a553fdaefd8fc907db4bdc6037e46c56ab95b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 01 May 2025 22:01:24 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 01 May 2025 22:01:24 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 01 May 2025 22:01:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 01 May 2025 22:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 01 May 2025 22:01:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_MAJOR=8.0
# Thu, 01 May 2025 22:01:24 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 22:01:24 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 01 May 2025 22:01:24 GMT
VOLUME [/data/db /data/configdb]
# Thu, 01 May 2025 22:01:24 GMT
ENV HOME=/data/db
# Thu, 01 May 2025 22:01:24 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Thu, 01 May 2025 22:01:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 May 2025 22:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 22:01:24 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 01 May 2025 22:01:24 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acccc25ace7a11227a26e9c62ac07b9390b376a47a7bdc13a2c1b37ff6be40c`  
		Last Modified: Thu, 08 May 2025 17:04:57 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147bb50d9e7b588cedf96637cba88d7c246a31e9fe72bf4d74e8b9463cbbee31`  
		Last Modified: Thu, 08 May 2025 17:04:57 GMT  
		Size: 1.5 MB (1492776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e47adbac281243f952c7f7a4fd73ca4d3e6d22a370d669145c7ea924e37ab`  
		Last Modified: Thu, 08 May 2025 17:04:57 GMT  
		Size: 1.1 MB (1061288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cf0e7472fcb7ce59cfe10a6068a83dd7b4f68969997a89b9cff5cc223fe173`  
		Last Modified: Thu, 08 May 2025 17:04:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e53c954a274fcc22852f68cd0907863a774a0f32f17951efa15be8b639c6eac`  
		Last Modified: Thu, 08 May 2025 17:04:57 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25ae28b38686475c7576e7df8a65632819de3d829604527af1ab8bbea69e2eb`  
		Last Modified: Thu, 08 May 2025 17:17:41 GMT  
		Size: 247.6 MB (247580724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d0024d7b7f6007ad00fd5a5338d6c50f2633fd98fe37cd2840697c5e1b6caf`  
		Last Modified: Thu, 08 May 2025 17:04:57 GMT  
		Size: 5.0 KB (5004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:4304005f29b0eb368def14e362cb66a13e7458121785ee9f4f493b7d8191e498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bcd33e5f7f637e38d46365e26ffef8c78bbee6548b5561d530222a15031734`

```dockerfile
```

-	Layers:
	-	`sha256:dc4e88a7c661c34c1653a23340f027d99cfbeff83083f4f52f3dfe173ce08a54`  
		Last Modified: Thu, 08 May 2025 17:20:09 GMT  
		Size: 2.5 MB (2525684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703396b7c208d599acf170d0654e4be1cf912f21fb21fd255fba315e545e0799`  
		Last Modified: Thu, 08 May 2025 17:20:09 GMT  
		Size: 29.1 KB (29066 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.3781; amd64

```console
$ docker pull mongo@sha256:00f8f358ef314ce2be6e32928c6554bc54a8ec4dbd893a50a118b4ef894bb8b3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 GB (4168665778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f16d10c0d1b205b99a5a55702806d21618f0fe8162261962f95abe15c01f41`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Thu, 01 May 2025 22:34:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 01 May 2025 22:34:03 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 22:34:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.9-signed.msi
# Thu, 01 May 2025 22:34:07 GMT
ENV MONGO_DOWNLOAD_SHA256=4acf24592a7658cc58b4293cbf0a3f42133c9c1d4f2234f1a249f74aa1c7d22a
# Thu, 01 May 2025 22:35:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 01 May 2025 22:35:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 01 May 2025 22:35:44 GMT
EXPOSE 27017
# Thu, 01 May 2025 22:35:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccd48a0c5377d8718cc8996cd030fd9c44f81f01d9504598f5ee454927c2cd8`  
		Last Modified: Thu, 08 May 2025 17:20:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a826a7710cded399ef84aab5bb14bc01889de49303b80d7071bbe9aba000896`  
		Last Modified: Thu, 08 May 2025 17:20:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a925c6773379e2dae97ed38f536d853c3a23162201fa809806cbfddd3620d4b0`  
		Last Modified: Thu, 08 May 2025 17:20:11 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8fff0c45fe72daf506ad5856321d9be8b230b23eb061168f1020fd1b51f35a`  
		Last Modified: Thu, 08 May 2025 17:20:12 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94408351b87f6142e2ebd794494d39694722c5c97d1d61ad723ed8e34cb7eaae`  
		Last Modified: Thu, 08 May 2025 17:42:26 GMT  
		Size: 773.5 MB (773495107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bec2fdd4f099de9a2221e4b099fb05296882765309313a8107735d19ef58951`  
		Last Modified: Thu, 08 May 2025 17:20:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42448f181bc1c424769ef68c122d219ca70d9078f5962198ae2e8438605685f`  
		Last Modified: Thu, 08 May 2025 17:20:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7db15666cfcc8ab8d39680f9ee967f342e0f19263efc4d3e1232ab46f73e87a`  
		Last Modified: Thu, 08 May 2025 17:20:13 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.3566; amd64

```console
$ docker pull mongo@sha256:b36cec1a504a8c20ddb6e352c0085f76842f76463a1a313f2ab19f0747f6a93a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3047015361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85e415623098257a3cfe3dc1eb7e31dbbfaa7b3a7febdd470ea26879907f941`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Thu, 01 May 2025 22:27:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 01 May 2025 22:27:44 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 22:27:45 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.9-signed.msi
# Thu, 01 May 2025 22:27:46 GMT
ENV MONGO_DOWNLOAD_SHA256=4acf24592a7658cc58b4293cbf0a3f42133c9c1d4f2234f1a249f74aa1c7d22a
# Thu, 01 May 2025 22:30:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 01 May 2025 22:30:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 01 May 2025 22:30:44 GMT
EXPOSE 27017
# Thu, 01 May 2025 22:30:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6e3fac54df010b5e00d50bb7603b498f9eb5a2d6a592e758c3e2afaed13049`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba627a58ad5f3b612159dabdd4ae608396b78c64ada934e306685f89056c9ef1`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f138553713491a85e2955d3dbf41bfc0d90054fa67cda24d8231bfde8d2571`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cab525b91f5d289114405733c8cd521aadea6b814b07830e74029619bb4e9a4`  
		Last Modified: Thu, 08 May 2025 17:14:50 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af3a4af14cf5b4f64298a12394bdb87ccba14d4bc3444ca02c7f782761d54a4`  
		Last Modified: Thu, 08 May 2025 17:37:29 GMT  
		Size: 773.4 MB (773423840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b86e650e9a6e4416bce15b927cfa5dc429cacbec623d35cd5bff9cbd7c67de`  
		Last Modified: Thu, 08 May 2025 17:17:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e8c12c43976ffadafca6c648cd95ea6c22787523c4aeb3f24bda9e3dc5ae49`  
		Last Modified: Thu, 08 May 2025 17:17:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ddf18c6c34734ab52c2be7030255a4c9824c008030f06493a673320f85fdd7`  
		Last Modified: Thu, 08 May 2025 17:17:18 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:ffd4fd8061fe7864dfb7af18a18a524a8079ac59fb2bf6c5575eedfdd6af8abd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2939031103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f07a1f6f17950ecfba01f2cc57df1e8e309047a4b1f4f445645b2c9708b6ff8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Thu, 01 May 2025 22:27:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 01 May 2025 22:27:47 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 22:27:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.9-signed.msi
# Thu, 01 May 2025 22:27:48 GMT
ENV MONGO_DOWNLOAD_SHA256=4acf24592a7658cc58b4293cbf0a3f42133c9c1d4f2234f1a249f74aa1c7d22a
# Thu, 01 May 2025 22:31:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 01 May 2025 22:31:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 01 May 2025 22:31:11 GMT
EXPOSE 27017
# Thu, 01 May 2025 22:31:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258de7be8acc97d1226a3162840f8a807fb62a678b7514644a54a4badcb97e38`  
		Last Modified: Thu, 08 May 2025 17:21:59 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c7dc57c27b6a4c68a74274af66a5c682ff5a8b320edc3a6b25769ba60974f`  
		Last Modified: Thu, 08 May 2025 17:22:00 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0798b44dadd77f2e5bb274203994fe57b21283891c7bdc7f6e0c3df6c7d5b098`  
		Last Modified: Thu, 08 May 2025 17:22:00 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c25021e3f57db7736128f272f1f529487909bd8709eebbdd8e630527839f1db`  
		Last Modified: Thu, 08 May 2025 17:21:59 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5fb2f7b46ba2ba952875271d296e67735ecb3de3e65d32af64cb93dd90ad78`  
		Last Modified: Thu, 08 May 2025 17:42:48 GMT  
		Size: 773.5 MB (773495787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc983a66680377183653e75011df2c811fbe0486ea51feaaba47aa1adc72ab7`  
		Last Modified: Thu, 08 May 2025 17:22:00 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e76ccfcca0c27cf3fb11d0c23be73c9b68519aa168c8848fd06191e39b518dd`  
		Last Modified: Thu, 08 May 2025 17:22:01 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a55f3f7d938f160731c9acb2f6ef87f0e4878cddc8f5aadb7cc0cc57ec9ea25`  
		Last Modified: Thu, 08 May 2025 17:22:01 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
