## `mongo:latest`

```console
$ docker pull mongo@sha256:474f5c3bf0e355bb97dafda730e725169a4d51c5578abf7be9ec7ad3fdee4481
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

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
$ docker pull mongo@sha256:870518acf2c2317f420810ec89afa6d5c733e79024252e6c410a6519a98a3bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320024005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8e0edc0030cc55428dfa46573846489ed56ce9dd3a985ae09a9a19640a5a69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:06 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 17 Feb 2026 20:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:27:26 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 20:27:26 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 17 Feb 2026 20:27:26 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 17 Feb 2026 20:27:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 20:27:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:27:26 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 17 Feb 2026 20:27:26 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 17 Feb 2026 20:27:26 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 17 Feb 2026 20:27:26 GMT
ENV MONGO_MAJOR=8.2
# Tue, 17 Feb 2026 20:27:26 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 17 Feb 2026 20:27:26 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 17 Feb 2026 20:27:46 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 17 Feb 2026 20:27:46 GMT
VOLUME [/data/db /data/configdb]
# Tue, 17 Feb 2026 20:27:46 GMT
ENV HOME=/data/db
# Tue, 17 Feb 2026 20:27:46 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 17 Feb 2026 20:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:46 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Feb 2026 20:27:46 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f5cdbb159932848ccefb5074604621aff1e35e38f9139ab694f9ec085c3f07`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaee3f82e804503eab8d9d24299fa1c3dc140422e9a67bcb53082a4530dcf99b`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 1.5 MB (1494496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc0f1d374f5f0b098144592f053f6881b0705d02e2d984462cf7b0f202e175c`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 886.0 KB (886024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3cff213b9bb8afad7c3dbfe99a8b6394ed7085a0beb0e50dc44e4c8e6dd927`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7a0fd6d2b7d16debb4272be3cd687c7bd7986de94e31ae959418da75756e3`  
		Last Modified: Tue, 17 Feb 2026 20:28:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a1f3f71824f982bcf786b69dc31db90ee336cf081c90dfaf81ad5eb90459e7`  
		Last Modified: Tue, 17 Feb 2026 20:28:27 GMT  
		Size: 288.8 MB (288771770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5f049ccdd6eeaf83bc8f0ee42929386f93f3e898dc6c8a991ab8664c215652`  
		Last Modified: Tue, 17 Feb 2026 20:28:22 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:c083321a003de0eb5943dcbd889863e80e2b26e337ee62c3e60590a8928d6cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8fa3258980d4b51c1a54269b4e71dd41a3510ee843e3cf75d248a163d80fac`

```dockerfile
```

-	Layers:
	-	`sha256:531bae2495406a855f24e03fe93706aecf263f3886bfaeaa75facb5ad13d7350`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 2.7 MB (2670055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50a2880e8bc8d9aef74d840e85a8d681f3762a2ff0a4f5009eeefb6b035a24c5`  
		Last Modified: Tue, 17 Feb 2026 20:28:20 GMT  
		Size: 29.0 KB (29019 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.32370; amd64

```console
$ docker pull mongo@sha256:3996669790c1847bbbdfcf636a24a6dccc5da6ac8dba75eab4c9746ac6ce3c81
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2780408960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddc79181f4ac354719d422e7f048b6930a4bad0d133b11f309f3753e952a9d8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:58:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 22:58:18 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Feb 2026 22:58:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Feb 2026 22:58:19 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Feb 2026 23:00:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 23:00:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 23:00:11 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 23:00:12 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a34ca08cf4aba145005c8c79ba38ccd008fc1424e50063c0de853b0dbf7a2a7`  
		Last Modified: Tue, 10 Feb 2026 23:00:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bae381db804c298e3d75193342e61c35c5d56cbc8f2796d4c63df00fff1970d`  
		Last Modified: Tue, 10 Feb 2026 23:00:18 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665308e4f8dc2612c4d59b4f775cc4630be5040610bb17a70a2e6e2dd682e0b3`  
		Last Modified: Tue, 10 Feb 2026 23:00:18 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e159c4826cd06e2bce1648c6dc57bfc8ccc9726e3eb3d4a485af6c91d4c58a5`  
		Last Modified: Tue, 10 Feb 2026 23:00:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58eb441c92b2889a2363e5bf3476a3756cb922542668fbbd4d0be6d4d3a196f`  
		Last Modified: Tue, 10 Feb 2026 23:01:31 GMT  
		Size: 815.6 MB (815639857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e994b54fa6a439cd8ea3386d09d5457187005af669142938669f0374c17ac8a`  
		Last Modified: Tue, 10 Feb 2026 23:00:18 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f50c4703f341ea70eb818ee86b051fe6e560e90618e797614981cb72673f59`  
		Last Modified: Tue, 10 Feb 2026 23:00:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9cdc6fcb58650d9d2a40ed6c2e1f7d9312b9e6ad3f6bc87b7a95d78c5fecf1`  
		Last Modified: Tue, 10 Feb 2026 23:00:17 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.4773; amd64

```console
$ docker pull mongo@sha256:59a5d1c65a6f2564cdc9ff9a34cf01a2aa55deeee8e0254564d3c105b55b689b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2678305709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d13c4504a0cd5f83fdba4b9e07a6d44befdc196e93fd501ec7d482511cf51a6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 23:03:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 23:06:23 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Feb 2026 23:06:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Feb 2026 23:06:25 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Feb 2026 23:08:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 23:08:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 23:08:04 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 23:08:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a9fd4b568d862245d76458065007c3dc78714ecd05e3b55812aa67f53958c6`  
		Last Modified: Tue, 10 Feb 2026 23:06:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8d8780e082cb147d57a8572b30936a4bbf2bab316ff68242bb1a67e917647d`  
		Last Modified: Tue, 10 Feb 2026 23:08:17 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e253cd6218c68c25cb58dc412bacd4a430646baceee15837e11ae37a37bffe92`  
		Last Modified: Tue, 10 Feb 2026 23:08:17 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f6df2e24a9d52d00afa6ac5a58b121e11361dbbe8640646d3f16d2082061f6`  
		Last Modified: Tue, 10 Feb 2026 23:08:15 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb8171f0ec86a0073fac030c3cb1ea87a9477fdb93a6ff4034ae4445ac94dda`  
		Last Modified: Tue, 10 Feb 2026 23:09:27 GMT  
		Size: 815.6 MB (815639387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f2b50415a3a09980803374be2d489ee239676006b3be98c5cb2c90c8918189`  
		Last Modified: Tue, 10 Feb 2026 23:08:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517a7ea87f02095a60cce615c3f9012673565f27f5863001ad8217bd746644c4`  
		Last Modified: Tue, 10 Feb 2026 23:08:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0a9bd398ba9ccbbd7613aceae8a3e957de54318158fae73470de2dde92fd2e`  
		Last Modified: Tue, 10 Feb 2026 23:08:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
