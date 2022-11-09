## `mongo:latest`

```console
$ docker pull mongo@sha256:71a63fc2438e45714f6c8a2505968ee0beeb94ec77a88ef12190f7cee9b95f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:53c4915c2c13524007a84b472f8c0b0a3c4f889afcb014306b628b2e82d0b658
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231730275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70536aeb2507ba0ea53767d15d836e140ccf3df74f2678f0cb5dd5c5e1d952c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:37:18 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 25 Oct 2022 17:37:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 17:37:28 GMT
ENV GOSU_VERSION=1.12
# Tue, 25 Oct 2022 17:37:28 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 25 Oct 2022 17:37:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 17:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 17:37:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 25 Oct 2022 17:37:45 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 25 Oct 2022 17:37:45 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 25 Oct 2022 17:37:45 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 25 Oct 2022 17:37:45 GMT
ENV MONGO_MAJOR=6.0
# Tue, 25 Oct 2022 17:37:46 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 25 Oct 2022 17:37:46 GMT
ENV MONGO_VERSION=6.0.2
# Tue, 25 Oct 2022 17:38:10 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 25 Oct 2022 17:38:11 GMT
VOLUME [/data/db /data/configdb]
# Tue, 25 Oct 2022 17:38:11 GMT
ENV HOME=/data/db
# Tue, 25 Oct 2022 17:38:12 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Tue, 25 Oct 2022 17:38:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 17:38:12 GMT
EXPOSE 27017
# Tue, 25 Oct 2022 17:38:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a00eb9f68a0dcf2f4b6f3881376f35b2908e0ec03e0ba7b41dce5138a57017e`  
		Last Modified: Wed, 26 Oct 2022 16:14:33 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f683956749c518e0ea925e30c0c5115c4ce12e827cd34bcf72ce2e9d750a2bb6`  
		Last Modified: Wed, 26 Oct 2022 16:14:35 GMT  
		Size: 3.1 MB (3059607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b2f05ea206b8ad00c6db544ddc80db3b9f6f9ea070867894eb83acdd9656c`  
		Last Modified: Tue, 25 Oct 2022 17:40:52 GMT  
		Size: 6.5 MB (6509130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a342bea915a9cfedf83084c321b2c1aae8bbfdc8aa1f0845669c4d325bff96d`  
		Last Modified: Tue, 25 Oct 2022 17:40:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa956ab1c2f09b41dec38b203cd914272b87e515a3658915e57f3a686382c261`  
		Last Modified: Tue, 25 Oct 2022 17:40:30 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a8542a62498c9e71e1778b9b0bfbf522b4e549b83a9b4f64f7c1b671ae7df`  
		Last Modified: Tue, 25 Oct 2022 17:40:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acab179a7f073886768651b76367c9845a10c2a53048b6c95f1b1424e86dea92`  
		Last Modified: Tue, 25 Oct 2022 17:40:57 GMT  
		Size: 193.6 MB (193574943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88335710e8418ba561f1d9505ee45125592f4f5d9ab248393041a53e3051f7a`  
		Last Modified: Tue, 25 Oct 2022 17:40:30 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b567c55036f586bc6cee739009fb81c144adf3806898a3d8910ff5d557d45a45
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225123999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5c8f74cf956d352341b9ec6530cc0341ffd4cd58cebde205ce254d2203b715`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:12:08 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 26 Oct 2022 02:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:12:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 26 Oct 2022 02:12:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 26 Oct 2022 02:12:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:12:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:12:28 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 26 Oct 2022 02:12:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 26 Oct 2022 02:12:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 26 Oct 2022 02:12:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 26 Oct 2022 02:12:28 GMT
ENV MONGO_MAJOR=6.0
# Wed, 26 Oct 2022 02:12:28 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 26 Oct 2022 02:12:28 GMT
ENV MONGO_VERSION=6.0.2
# Wed, 26 Oct 2022 02:12:47 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 26 Oct 2022 02:12:51 GMT
VOLUME [/data/db /data/configdb]
# Wed, 26 Oct 2022 02:12:51 GMT
ENV HOME=/data/db
# Wed, 26 Oct 2022 02:12:51 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:12:51 GMT
EXPOSE 27017
# Wed, 26 Oct 2022 02:12:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffac05d305dafc7bd6d968c4d611342ceb95a87494c361ab37718b188f02763`  
		Last Modified: Wed, 26 Oct 2022 02:16:20 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d44feb31079d0e2421a83a8dd5563d203ec1ff537396d3ed65dd35cdfed206f`  
		Last Modified: Wed, 26 Oct 2022 02:16:21 GMT  
		Size: 2.9 MB (2907461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd79df0bf56efa1ec22177052bd5d6e4feef423ad95176bd0f86a478f3f99d30`  
		Last Modified: Wed, 26 Oct 2022 02:16:21 GMT  
		Size: 6.4 MB (6425791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393c4defd29fb265c4d4794d5f008fbde7c8d9c4f91a7105e9cf2866a28df77a`  
		Last Modified: Wed, 26 Oct 2022 02:16:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2da71c1f524304c6fddcfd682ea28128baf5f08cadfbf5b9c0ad090af3831d`  
		Last Modified: Wed, 26 Oct 2022 02:16:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4c4322236bd8250387800e057c330d487ebf386f2d007d7ccb8bc9aabc13e1`  
		Last Modified: Wed, 26 Oct 2022 02:16:18 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4baaecdab319402fa206222759f080d7bd645002f9ad3a1ddb6b4e32204110`  
		Last Modified: Wed, 26 Oct 2022 02:16:38 GMT  
		Size: 188.6 MB (188585988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2076034e8003a37c5a97f6f6d582de741fd3a0b4a1f4dd671b148023f85c00e`  
		Last Modified: Wed, 26 Oct 2022 02:16:18 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.1249; amd64

```console
$ docker pull mongo@sha256:6c76367747757ba6897dca28ff0d3359c46216a0e5c9932efc5166bcf3aa8920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2994464371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f484e92419400ca1fe01c9b8d16981964fe62e9bffe5dd1736dd4b6898c8b9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Wed, 09 Nov 2022 14:41:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 18:22:00 GMT
ENV MONGO_VERSION=6.0.2
# Wed, 09 Nov 2022 18:22:01 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.2-signed.msi
# Wed, 09 Nov 2022 18:22:02 GMT
ENV MONGO_DOWNLOAD_SHA256=964a7e33927a8c01a6177daf0bf49f3ec17560b1b78f8be60ec641a03c55cb18
# Wed, 09 Nov 2022 18:24:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 18:24:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Nov 2022 18:24:15 GMT
EXPOSE 27017
# Wed, 09 Nov 2022 18:24:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcc0cd10e58716558145d847bcea390e3840d172df19b8d0f08a57dd985262d`  
		Last Modified: Wed, 09 Nov 2022 19:02:46 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2181e1adb6da783ef737efe46eb9aa253d785a46843f0b8a12301b7337d15c04`  
		Last Modified: Wed, 09 Nov 2022 19:02:46 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456decbcd5c74457855fbaf2b027f6819683fcb87441e6643f44542f9a5cdb56`  
		Last Modified: Wed, 09 Nov 2022 19:02:45 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d748c55105ec09d7403ba625dfe485918bbfec20a980bc1af45f3180a8dc909`  
		Last Modified: Wed, 09 Nov 2022 19:02:43 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a889f81d86650d9c1bae3ce2ed0287812fc0680d580bf549d0f4a43715d6c133`  
		Last Modified: Wed, 09 Nov 2022 19:04:11 GMT  
		Size: 512.7 MB (512685887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964d726a83c6a1293392e10654a23d7ef4998c6643bc87364213446e2904e5cd`  
		Last Modified: Wed, 09 Nov 2022 19:02:43 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244ae10be776babe53eef1e437574e8624aa0d9b7b3ea34386721d61af82ac7a`  
		Last Modified: Wed, 09 Nov 2022 19:02:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a8eed089b637c7348d6490113e5ed7391de0ecbda52eb9b92b869aa5a198c8`  
		Last Modified: Wed, 09 Nov 2022 19:02:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.3650; amd64

```console
$ docker pull mongo@sha256:78b2e7438587e7a5653fb03bb8a5c25d280e8597f02a25939de96e6921b697b7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3291082908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eecef695ec74bd59d29fd578d4be6f56a5fd070d32351df46f030ab2a53a807`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 18:24:30 GMT
ENV MONGO_VERSION=6.0.2
# Wed, 09 Nov 2022 18:24:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.2-signed.msi
# Wed, 09 Nov 2022 18:24:32 GMT
ENV MONGO_DOWNLOAD_SHA256=964a7e33927a8c01a6177daf0bf49f3ec17560b1b78f8be60ec641a03c55cb18
# Wed, 09 Nov 2022 18:28:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 18:28:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Nov 2022 18:28:03 GMT
EXPOSE 27017
# Wed, 09 Nov 2022 18:28:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fec38ff3c242baf141e10c6a5b81f008c9915acd4dd9cc327eaf296892c96`  
		Last Modified: Wed, 09 Nov 2022 19:04:32 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537c68971b182ddb518477c6993accb024778f71f16894ed90390301eb7a7dbb`  
		Last Modified: Wed, 09 Nov 2022 19:04:32 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f07b977aece83110fb1358d8b0863f8ae2635c61e505e11cbc078e175a12c50`  
		Last Modified: Wed, 09 Nov 2022 19:04:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17aef8040e1f6a5348317cc5430061159238fc4f6004b23714a8a5b6a5b50e91`  
		Last Modified: Wed, 09 Nov 2022 19:05:56 GMT  
		Size: 512.5 MB (512486276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7866b495e26e50fe549700b9f846f7f279dbd5e27aaa6901017e8a414412681`  
		Last Modified: Wed, 09 Nov 2022 19:04:29 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e8a72583964e2d9524c834c0288f7032834759c8d3f683776c31e66ab24423`  
		Last Modified: Wed, 09 Nov 2022 19:04:29 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b494701b847f8225f597c05baec6c20bcd3464f492576d85be3260aff75ec192`  
		Last Modified: Wed, 09 Nov 2022 19:04:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
