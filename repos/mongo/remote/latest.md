## `mongo:latest`

```console
$ docker pull mongo@sha256:c57e511ce78d6847e2605db8e374611492f588e24f93c80e0c6baba9d6c029c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:0e0c67d4bb79dc1d20b3a6f2ecb93024bbbaa0e92311a12c6bd081ba24b81801
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231722030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70885e78ca893b5e53b9c8f0d0679ac828f4d8846ce144a8cbca60c001cfe91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:52:11 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 02 Sep 2022 03:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:52:19 GMT
ENV GOSU_VERSION=1.12
# Fri, 02 Sep 2022 03:52:20 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 02 Sep 2022 03:52:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Sep 2022 03:52:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Sep 2022 03:52:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Fri, 02 Sep 2022 03:52:33 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 02 Sep 2022 03:52:33 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 03:52:33 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 03:52:33 GMT
ENV MONGO_MAJOR=6.0
# Fri, 02 Sep 2022 03:52:34 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 29 Sep 2022 21:19:36 GMT
ENV MONGO_VERSION=6.0.2
# Thu, 29 Sep 2022 21:20:02 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 29 Sep 2022 21:20:03 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Sep 2022 21:20:03 GMT
ENV HOME=/data/db
# Thu, 29 Sep 2022 21:20:03 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Thu, 29 Sep 2022 21:20:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Sep 2022 21:20:04 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 21:20:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9c8c301e0f21d7d0b229b7ce3bf5f73a8032a77f1fd0ead5a40ae2904e7386`  
		Last Modified: Fri, 02 Sep 2022 03:57:03 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73738965c4ce390367a607807b960c2c4cd8aa410fc4b1bea6ce71263c6725a8`  
		Last Modified: Fri, 02 Sep 2022 03:57:04 GMT  
		Size: 3.1 MB (3059566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6635b9ddf662b5aad927979bc18877d5e93da5b68d0257bf589086be3fc24`  
		Last Modified: Fri, 02 Sep 2022 03:57:04 GMT  
		Size: 6.5 MB (6506072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a471eaa4ad67f863744ea2570d2995126f69ac4a5156455603a9308c2c915e`  
		Last Modified: Fri, 02 Sep 2022 03:57:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf274af89b0a0884f7e076b77aa392912a4199a2dc008ddcfce30b3dc843df5`  
		Last Modified: Fri, 02 Sep 2022 03:57:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fc489f2a3bae9cf2166f37d4fe0c5fcbfb452e62be136900d6695577033d3e`  
		Last Modified: Fri, 02 Sep 2022 03:57:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1abc36251b97103711f5db370c4431c08c6343c9e768cd7f1c4f30cd153cea2`  
		Last Modified: Thu, 29 Sep 2022 21:22:03 GMT  
		Size: 193.6 MB (193574960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396db6f4d8008af59305c514b2d28092e698960cb572c185839d7dfea6a90a7a`  
		Last Modified: Thu, 29 Sep 2022 21:21:36 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:30bb3d2e33bc569e68290ec019cdf4506e77d3f62fe97dc1bc5761028c29f062
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224942277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36734b2913a4c0687b760fc838e8bc970e3520931bd5be743fca4ffb91d2694`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:38:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 02 Sep 2022 05:38:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:38:32 GMT
ENV GOSU_VERSION=1.12
# Fri, 02 Sep 2022 05:38:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 02 Sep 2022 05:38:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Sep 2022 05:38:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Sep 2022 05:38:51 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Fri, 02 Sep 2022 05:38:52 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 02 Sep 2022 05:38:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 05:38:54 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 05:38:55 GMT
ENV MONGO_MAJOR=6.0
# Fri, 02 Sep 2022 05:38:56 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 29 Sep 2022 21:32:38 GMT
ENV MONGO_VERSION=6.0.2
# Thu, 29 Sep 2022 21:33:00 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 29 Sep 2022 21:33:00 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Sep 2022 21:33:01 GMT
ENV HOME=/data/db
# Thu, 29 Sep 2022 21:33:03 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Thu, 29 Sep 2022 21:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Sep 2022 21:33:04 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 21:33:05 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe07d8ebcafb11d0bd133b24c0b609a2df7be61177317743622e25402fad20e5`  
		Last Modified: Fri, 02 Sep 2022 05:44:29 GMT  
		Size: 1.8 KB (1779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f116473d7043b4502e37137a97bd6e20142172dab16e6f88e497d3d33b0c78`  
		Last Modified: Fri, 02 Sep 2022 05:44:30 GMT  
		Size: 2.9 MB (2906991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed58e863f95532cf6247f0bc0953d63704dde8a89053df15b1712a2ec112d07`  
		Last Modified: Fri, 02 Sep 2022 05:44:30 GMT  
		Size: 6.2 MB (6249319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62274e6e1246430435b8017651d8588082af58d5faa6c59dd88c773c2825bc0c`  
		Last Modified: Fri, 02 Sep 2022 05:44:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe64d6112f448ead4c422bec13b68fe02c890c9ba1b5cdbae6844d91b583a27a`  
		Last Modified: Fri, 02 Sep 2022 05:44:27 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baed58b8554979b78c7358f439e6e15515a7e798171a6c48ace5b737c9883d52`  
		Last Modified: Fri, 02 Sep 2022 05:44:27 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebc944f33dc8e50004ba539f200d20f8d219debd5580020ee42d8024075dd7f`  
		Last Modified: Thu, 29 Sep 2022 21:35:53 GMT  
		Size: 188.6 MB (188585530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3a9f6b549cab0e99ee66aeda84963f49bbe201b4f3c5ce524fcbd0a5c93fc`  
		Last Modified: Thu, 29 Sep 2022 21:35:27 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.1006; amd64

```console
$ docker pull mongo@sha256:4970e2730c531e3244ce2dfea104a3f527287faed45294d3b1f41ca751ca885d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2859647357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776205d7096dcc9eea9d0c94d1759da4c19d8208529eda2fc597a931bfb8e60a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 13:31:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 29 Sep 2022 20:16:03 GMT
ENV MONGO_VERSION=6.0.2
# Thu, 29 Sep 2022 20:16:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.2-signed.msi
# Thu, 29 Sep 2022 20:16:05 GMT
ENV MONGO_DOWNLOAD_SHA256=964a7e33927a8c01a6177daf0bf49f3ec17560b1b78f8be60ec641a03c55cb18
# Thu, 29 Sep 2022 20:18:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 29 Sep 2022 20:18:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Sep 2022 20:18:15 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 20:18:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a16438b2cffe7980c606769d49003f7f1c4d27549445f824511a81834513616a`  
		Last Modified: Wed, 14 Sep 2022 18:58:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dfc797ce3690758c479c00b9ca3298b1c93eb7668d80d214fe17d060571387`  
		Last Modified: Thu, 29 Sep 2022 20:40:27 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee2a0d4d13d2cb0cf5c46f4c883feccb59d8d9889d0851d6146f6bdef7ee551`  
		Last Modified: Thu, 29 Sep 2022 20:40:28 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dde840cd7adf6220569e0d770f78d653a42a5d03943b05bd40fa7cc8307f91`  
		Last Modified: Thu, 29 Sep 2022 20:40:25 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb5d662739157bf74d34795da8f255ed1e3cde59d7bca6b800ce7da45f48a12`  
		Last Modified: Thu, 29 Sep 2022 20:41:59 GMT  
		Size: 512.7 MB (512687831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168959b80726fdfa9c12b7f47042c772f5adebba338a68196d2b180129139f98`  
		Last Modified: Thu, 29 Sep 2022 20:40:25 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8f546d2d42ad044020845ce8da5db56893975b45daa98dedbb21cd79f80f42`  
		Last Modified: Thu, 29 Sep 2022 20:40:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c147588fb9862ba6185fab13b7b1416d092a1510dc8b7a1be01853b714eb2a54`  
		Last Modified: Thu, 29 Sep 2022 20:40:25 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.3406; amd64

```console
$ docker pull mongo@sha256:6e40569802588196bbaaef26b3abf496c0c3f7334ee4ce1345f04a80cf38540a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3216045919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d5d056f6533cf8bae8619fe0ac89ba2248f998d1320ec139be1c93b0de2a34`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 29 Sep 2022 20:18:30 GMT
ENV MONGO_VERSION=6.0.2
# Thu, 29 Sep 2022 20:18:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.2-signed.msi
# Thu, 29 Sep 2022 20:18:32 GMT
ENV MONGO_DOWNLOAD_SHA256=964a7e33927a8c01a6177daf0bf49f3ec17560b1b78f8be60ec641a03c55cb18
# Thu, 29 Sep 2022 20:21:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 29 Sep 2022 20:21:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Sep 2022 20:21:26 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 20:21:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa66d188ef46de08ce4a0b12ac6d3bbd8b0bd2fdc177291872b15b4b539a8ae1`  
		Last Modified: Thu, 29 Sep 2022 20:42:17 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26c9569da32bffd522bb0dc969a1d77d8240bc47cb78420f516a38d7a0b9805`  
		Last Modified: Thu, 29 Sep 2022 20:42:17 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1543ccd01c84b8b79fef6f476c55f9ec2d09f801ed323be1ee96eabf9dcb0411`  
		Last Modified: Thu, 29 Sep 2022 20:42:15 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa80cb09530d62bc969d1b1a903b1d0f179234a5f3cea3e2d136b6875e6c2572`  
		Last Modified: Thu, 29 Sep 2022 20:43:33 GMT  
		Size: 512.5 MB (512471333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e001b0294952432610d53c39b2fdda3f557e8b21c7a442d925ebce8b7eeed1`  
		Last Modified: Thu, 29 Sep 2022 20:42:15 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be420c4cbe76ee34aa21f3151fd2e7082794ba065930b079b700bbb53ace5e11`  
		Last Modified: Thu, 29 Sep 2022 20:42:15 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5046bf8c1b461cb39e40a60fceed4b9b77a80e27855140250e8d7be25462de2`  
		Last Modified: Thu, 29 Sep 2022 20:42:15 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
