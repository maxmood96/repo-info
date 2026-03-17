## `mongo:latest`

```console
$ docker pull mongo@sha256:b80abaeb88da051d51f51a138d6c1a0c72bb39f88a7492d7e88a458dae7e80b5
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
$ docker pull mongo@sha256:3c615e75a6c37cdf38c4cf5690834f302813f4b4edcf25620960159d0dbec93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.3 MB (335306722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0286cc181898f3800665c63e6c51638a308d8ba97ed1c199e8ffa79db122780`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:24 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 17 Feb 2026 20:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 20:28:44 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 17 Feb 2026 20:28:44 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 17 Feb 2026 20:28:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 20:28:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:28:44 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 17 Feb 2026 20:28:44 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 17 Feb 2026 20:28:44 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 17 Feb 2026 20:28:44 GMT
ENV MONGO_MAJOR=8.2
# Tue, 17 Feb 2026 20:28:45 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 17 Feb 2026 20:28:45 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 17 Feb 2026 20:29:04 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 17 Feb 2026 20:29:04 GMT
VOLUME [/data/db /data/configdb]
# Tue, 17 Feb 2026 20:29:04 GMT
ENV HOME=/data/db
# Tue, 17 Feb 2026 20:29:04 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 17 Feb 2026 20:29:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:29:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:29:04 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Feb 2026 20:29:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79e499203c9cf152c5bc6f038864c8785d3bacb24b4ae97001ad0614e9dd487`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46eb2190ffc37d34bd6051d25cb4a73f4384442ee145609df2fd4e97b065729`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 1.5 MB (1509524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427c118b20797fcc39d562bb8290341651e5b31524cead45eea3d36f774c64fc`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 933.7 KB (933728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfd783f7a597bbb7d6eb1383ebdbbd9a0f413f175bbdc38b74ef123eabe184f`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea2e6a72e6bef5c958a79ccaa672d231f05a40baa2000d690fb554d0abdf2a5`  
		Last Modified: Tue, 17 Feb 2026 20:29:42 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b55066391c2657b7fc353f59ac462e607e3be45af587fa3699aac5a8f609f`  
		Last Modified: Tue, 17 Feb 2026 20:29:48 GMT  
		Size: 303.1 MB (303129259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d23bbf2b2165d0729765a06f400db5f7a9583d60bf1fb848098d8187a813aa2`  
		Last Modified: Tue, 17 Feb 2026 20:29:42 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:b2d948e0d71df0606c8245d92f31c23bb452b975904115fdadc03b48d89e0d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9666c8b0c3de9d7efc891d9db60777c5fc54df39e739aa74167b3a1a170798`

```dockerfile
```

-	Layers:
	-	`sha256:bae1425230be09820e17d4685d782ea5ce48279512df9f9cf628d547d9df58a0`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 2.7 MB (2668919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eeb70347fbd8068cd83426d0d25bba2d3dca4dc008bcbba698cbfe8f37851cb`  
		Last Modified: Tue, 17 Feb 2026 20:29:41 GMT  
		Size: 28.8 KB (28792 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:85f531df10086bcb4a5c36b8f6a62c39358bea0a6e67f4c9bb23e4c69d6c20c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322303489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a04f4f50c0bc9cac053c8e90d1e68d36d35a6d5e31dbfd201044e8845f3b41`
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
# Tue, 17 Mar 2026 01:43:02 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 17 Mar 2026 01:43:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:43:28 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 17 Mar 2026 01:43:28 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 17 Mar 2026 01:43:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:43:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:43:29 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 17 Mar 2026 01:43:29 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 01:43:29 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 01:43:29 GMT
ENV MONGO_MAJOR=8.2
# Tue, 17 Mar 2026 01:43:29 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 17 Mar 2026 01:43:29 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 17 Mar 2026 01:43:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 17 Mar 2026 01:43:50 GMT
VOLUME [/data/db /data/configdb]
# Tue, 17 Mar 2026 01:43:50 GMT
ENV HOME=/data/db
# Tue, 17 Mar 2026 01:43:50 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 17 Mar 2026 01:43:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:43:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:43:50 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Mar 2026 01:43:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e359c1269ef0a0f50006c700a84cc9e21c909d01288500ea418b5e9bb4f0035`  
		Last Modified: Tue, 17 Mar 2026 01:44:24 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13d771a2470e3bdf2d286c6484fc2fe9d97d347c358c6498a64088ea417c9b0`  
		Last Modified: Tue, 17 Mar 2026 01:44:24 GMT  
		Size: 1.5 MB (1494438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dfe56cec2a17eaa90d20f641c7b615c8422cc641bfdac8d6db8310a766a998`  
		Last Modified: Tue, 17 Mar 2026 01:44:24 GMT  
		Size: 886.0 KB (886004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc10438b058c90eff9a6d991fe918ebb5e6d6e15d3945d4a21064002bc72d8e`  
		Last Modified: Tue, 17 Mar 2026 01:44:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11255fa494856dc28a1be9a64bd321a040f4c8c6644e9d67faf2642ac75a4be`  
		Last Modified: Tue, 17 Mar 2026 01:44:25 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b7656913df1d091368cc385524aef00966bad70d931dedf4cd4221a03be1c5`  
		Last Modified: Tue, 17 Mar 2026 01:44:31 GMT  
		Size: 291.0 MB (291046738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220142f2d9dee9c792298467d91dc0b74d4f4b1d5e29a8eef8cb39b73f47edf0`  
		Last Modified: Tue, 17 Mar 2026 01:44:26 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:94bf17daf5503fbf7cbb3457880ba1b9fb11e4ad14829997772aadd9ce5a86ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439faa9e386146d5b6b153cd3072a61bccf675145f7a95778c46b3ec9596028`

```dockerfile
```

-	Layers:
	-	`sha256:d17ecbbdca7e71fd23c7948159e2c595bacd14abe08c1043e8125307b023d37f`  
		Last Modified: Tue, 17 Mar 2026 01:44:25 GMT  
		Size: 2.7 MB (2662388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda6c72856edfd6f2fb7620ead2f5525a7ae2977390bedf947cbc23a50301a75`  
		Last Modified: Tue, 17 Mar 2026 01:44:24 GMT  
		Size: 29.0 KB (29018 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.32522; amd64

```console
$ docker pull mongo@sha256:3204cc69c577d2baaac34a72f9157c953c0f3868974a192c7a563b1d93184da3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2896855749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76be2efeea61115d3cc764af6eb2396c570708194572351b6f6cdab185606f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 22:06:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 22:06:02 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Mar 2026 22:06:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Mar 2026 22:06:04 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Mar 2026 22:08:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:08:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Mar 2026 22:08:06 GMT
EXPOSE 27017
# Tue, 10 Mar 2026 22:08:06 GMT
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
	-	`sha256:4d0ecf41559df61247aa99121106588c7bd8133fd5ca3eb5f0e11d7e10364714`  
		Last Modified: Tue, 10 Mar 2026 22:08:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9699db20dbc71231d41a6fe8de88a9bcc647aeceaae843a5439a9045af49ee47`  
		Last Modified: Tue, 10 Mar 2026 22:08:23 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567a8c0273ee13e49c4dd4f1c65a04d4271f5befa11f150e85b278eea2bc459e`  
		Last Modified: Tue, 10 Mar 2026 22:08:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c00da52a9c16e3a235e7ed24f6ec80170deb3ba8ff8fb38be4766cb133d139`  
		Last Modified: Tue, 10 Mar 2026 22:08:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfa1ceb8f1ba5bdb79de11862752366ff6bcfbef13f98e3707e9e801cd3cc00`  
		Last Modified: Tue, 10 Mar 2026 22:09:39 GMT  
		Size: 815.7 MB (815650484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9001a4eefdfc8174fc09c0caa404a4d80f9eec24bcbc3e2d4f6ed940be24bf4`  
		Last Modified: Tue, 10 Mar 2026 22:08:22 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebaea12e708b7610da7975067b5a903426108e9d5973ef0ffdb40b46728d392`  
		Last Modified: Tue, 10 Mar 2026 22:08:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d187e65a211430393432b9e4a7769cc0722abcb2e0b1bffb097ac5fc7f5664e6`  
		Last Modified: Tue, 10 Mar 2026 22:08:22 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.4893; amd64

```console
$ docker pull mongo@sha256:57ca68b4c13cc2137fe699c9e1c99c64ef4767d8d73dbda84f28d01eaa4ad77d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2797930393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa592677550dc8f3745c4ccfd0941d90b94badac863878b730d601198dafb18`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 22:08:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 22:11:17 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Mar 2026 22:11:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Mar 2026 22:11:18 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Mar 2026 22:12:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:13:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Mar 2026 22:13:02 GMT
EXPOSE 27017
# Tue, 10 Mar 2026 22:13:02 GMT
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
	-	`sha256:c7844febc2b3fc230db18cb213fc8393b6e366b0df81fa90676409b67dd0c203`  
		Last Modified: Tue, 10 Mar 2026 22:11:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f108226ea6de24bdbbf312738f16cc310896fdd798863c92a05b7fae14d7adcb`  
		Last Modified: Tue, 10 Mar 2026 22:13:16 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2656a028d718ce2f9cb83ccadf96306625cbd90d2b3895686c224034736e86e2`  
		Last Modified: Tue, 10 Mar 2026 22:13:16 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f022db29ffdb891255f7215ba57b95819445dee96e0238450411e8052ca4b6c2`  
		Last Modified: Tue, 10 Mar 2026 22:13:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb695cf5356292eb6d8e85928094844b3b956355636d411e82dafeb315cf19a8`  
		Last Modified: Tue, 10 Mar 2026 22:14:32 GMT  
		Size: 815.6 MB (815639834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6151f826a95d1c0d56289a6a08b6f82e231dbc90867bf024fb86d3d1143bcb`  
		Last Modified: Tue, 10 Mar 2026 22:13:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c748d3175b6620afafe10a51b08c289298cf11bed8e7bbde3d0012fa29a5f99`  
		Last Modified: Tue, 10 Mar 2026 22:13:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2c67705fb982354c7f5773644772e8d86416efba04a1f7e1fb3e88f0a2c7c8`  
		Last Modified: Tue, 10 Mar 2026 22:13:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
