## `mongo:latest`

```console
$ docker pull mongo@sha256:d08b45d6409f36e138c33a77a103152f9f72d225b6640e1fde943368177c45e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.2031; amd64
	-	windows version 10.0.17763.4974; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:238b1636bdd7820c752b91bec8a669f92568eb313ad89a1fc4a92903c1b40489
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261077393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021b676f1558d3c0000ae5bc21b1193f2de7fe3b16919b97cff760d9373ade82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:46:00 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 13 Oct 2023 04:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:46:11 GMT
ENV GOSU_VERSION=1.16
# Fri, 13 Oct 2023 04:46:11 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 13 Oct 2023 04:46:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 04:46:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 04:46:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 04:46:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 04:46:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 04:46:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 04:46:22 GMT
ENV MONGO_MAJOR=7.0
# Fri, 13 Oct 2023 04:46:22 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 15 Nov 2023 05:20:47 GMT
ENV MONGO_VERSION=7.0.3
# Wed, 15 Nov 2023 05:21:13 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 15 Nov 2023 05:21:15 GMT
VOLUME [/data/db /data/configdb]
# Wed, 15 Nov 2023 05:21:15 GMT
ENV HOME=/data/db
# Wed, 15 Nov 2023 05:21:15 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 15 Nov 2023 05:21:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Nov 2023 05:21:15 GMT
EXPOSE 27017
# Wed, 15 Nov 2023 05:21:15 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a7480baa9dd203af7b88b2fe7e6b4f81563a7ffb540e462456ae061accb837`  
		Last Modified: Fri, 13 Oct 2023 04:49:41 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9301fbd7df07e1041efa8f0b71daef6163a40cddd61abd63c7622c0031ee4c`  
		Last Modified: Fri, 13 Oct 2023 04:49:42 GMT  
		Size: 5.1 MB (5050516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4470f2e90f14923cd6b6c2b4c9482ab700e2ee6adb23b5509826a2994aec9c`  
		Last Modified: Fri, 13 Oct 2023 04:49:42 GMT  
		Size: 1.3 MB (1252869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d046ff8fd3271879d2f76a64b0ff765e3b484eb8c712dbab9ba3f3aae73de6`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e062d62b861ed7136f7640c09410c619e0b146c7ea00bbc076ede8ffe17a2428`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72919e34fde8aa9d4c9919b131ea251cd24f66df9b967a3e9a00fcb931a80f37`  
		Last Modified: Fri, 13 Oct 2023 04:49:39 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c3fb6d33e0d3552c64f0369b43a5459d9afa45d57adaec11a919809a0c6ee1`  
		Last Modified: Wed, 15 Nov 2023 05:24:51 GMT  
		Size: 224.3 MB (224326213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfd395e3ac5ef9e7ad6e42d7e4d603531282c6f1afc3cff39ba5d182560aefd`  
		Last Modified: Wed, 15 Nov 2023 05:24:25 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:993cce3158e7c2f302bf26e0153faccfaca5831c497e68a3813893b11f73c35a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253089652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203fb0aeb494164ffddb68e653e75a612132fefc3d901739a0e1cf57a68249ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:07:59 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 13 Oct 2023 05:08:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 05:08:12 GMT
ENV GOSU_VERSION=1.16
# Fri, 13 Oct 2023 05:08:12 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 13 Oct 2023 05:08:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 13 Oct 2023 05:08:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 13 Oct 2023 05:08:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 13 Oct 2023 05:08:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 13 Oct 2023 05:08:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 13 Oct 2023 05:08:22 GMT
ENV MONGO_MAJOR=7.0
# Fri, 13 Oct 2023 05:08:22 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 15 Nov 2023 01:48:15 GMT
ENV MONGO_VERSION=7.0.3
# Wed, 15 Nov 2023 01:48:37 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 15 Nov 2023 01:48:41 GMT
VOLUME [/data/db /data/configdb]
# Wed, 15 Nov 2023 01:48:41 GMT
ENV HOME=/data/db
# Wed, 15 Nov 2023 01:48:41 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 15 Nov 2023 01:48:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Nov 2023 01:48:41 GMT
EXPOSE 27017
# Wed, 15 Nov 2023 01:48:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53942a81bbed58a041019d02afca8f39cb3b5fc0b340c05513ba233089ddaa64`  
		Last Modified: Fri, 13 Oct 2023 05:11:43 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c77c1ea6f8e184bfebf5bd44a67db789f6dda84d9e1765f88df461c6fc366ba`  
		Last Modified: Fri, 13 Oct 2023 05:11:44 GMT  
		Size: 5.0 MB (4993892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9269ffa19aee38fa5d40fbbb7ad0fed2cd802350b3e0859506d008678f433b01`  
		Last Modified: Fri, 13 Oct 2023 05:11:43 GMT  
		Size: 1.2 MB (1186372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae10bad01057285cb468c4b8ac16543be6f76dd7617e0a1dd477c7cab4e8265`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208482253dd3d9820726079a672df6e91e9b83c81c36d5554103f854670ccfc1`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beb4a4f2118534d26af685b92befcd861724f9f1ce3cd9a0cfabfecfe1452df`  
		Last Modified: Fri, 13 Oct 2023 05:11:41 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d8399c849e346dacbd60cf9862e89c06e19511069a55d363ebf497b4196a9f`  
		Last Modified: Wed, 15 Nov 2023 01:51:50 GMT  
		Size: 218.5 MB (218508770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39807cb848fcdb56e57ffe59695facd1b5ea2316e587d2977e3df4826574df1`  
		Last Modified: Wed, 15 Nov 2023 01:51:31 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.2031; amd64

```console
$ docker pull mongo@sha256:b23f0f330b3d5d30ad39c5174003ca84f243e06ea13b07554eb9445821622b29
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472193755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8cc4abe576bee596834fb307d441369b384dba13fc5c8c20a76a4dffb6f058`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 02:54:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Nov 2023 02:25:52 GMT
ENV MONGO_VERSION=7.0.3
# Wed, 15 Nov 2023 02:25:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.3-signed.msi
# Wed, 15 Nov 2023 02:25:54 GMT
ENV MONGO_DOWNLOAD_SHA256=7ec97aa108c6af587e77a49479b4e7239da6ccac2903e163ae984797b3afea14
# Wed, 15 Nov 2023 02:28:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Nov 2023 02:28:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Nov 2023 02:28:24 GMT
EXPOSE 27017
# Wed, 15 Nov 2023 02:28:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c131d94d08cb023367d3fd8434c336e9d07495660367cc521ddff869fb44dc7d`  
		Last Modified: Wed, 11 Oct 2023 05:52:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9021d3f18c544462ba44d454c8e899c9e85e46c764c333f9b8282aefa37e804`  
		Last Modified: Wed, 15 Nov 2023 03:10:41 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bd86fbbe395214807b203a5894e8dc630e438309d319ff06357646c1ce74a3`  
		Last Modified: Wed, 15 Nov 2023 03:10:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447b3610a31003c67cfca7f209e9599e532bde8b4011866d6e15be71339fc1ba`  
		Last Modified: Wed, 15 Nov 2023 03:10:39 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392c63100c195055b8384d40e5b9a50b53ea32d015a8af77ca6ba3727e3fcfe3`  
		Last Modified: Wed, 15 Nov 2023 03:12:28 GMT  
		Size: 612.3 MB (612340679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f8e1c7b300cb23643b9439eb6cf46d36fb7aeeb1e6db58f072d7816aa284ca`  
		Last Modified: Wed, 15 Nov 2023 03:10:39 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aae3a12c8fc1f424608bad1bea4d02e38d70ea282746a22480dee5837be631`  
		Last Modified: Wed, 15 Nov 2023 03:10:39 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5847bea7c39edeb6d7828062029a9b7c222665024386c12233affca3384c0381`  
		Last Modified: Wed, 15 Nov 2023 03:10:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.4974; amd64

```console
$ docker pull mongo@sha256:f9a266f5dd083a659612b3ddae1d0ba57ecd8dd2caceff80bb2ce86ccaf330dd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2643981269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7da1c5fc060225b9ae1a5eef1ddb7f5d28c046c15a35dc2de196aaa90856a62`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Nov 2023 02:28:35 GMT
ENV MONGO_VERSION=7.0.3
# Wed, 15 Nov 2023 02:28:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.3-signed.msi
# Wed, 15 Nov 2023 02:28:37 GMT
ENV MONGO_DOWNLOAD_SHA256=7ec97aa108c6af587e77a49479b4e7239da6ccac2903e163ae984797b3afea14
# Wed, 15 Nov 2023 02:32:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Nov 2023 02:32:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Nov 2023 02:32:19 GMT
EXPOSE 27017
# Wed, 15 Nov 2023 02:32:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7e93b7ab1fcb2401675153bbb5e9cba8cbf2dab09628d41df888e30cc703c1`  
		Last Modified: Wed, 15 Nov 2023 03:12:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90151399a52e5b0f945c856cb634d1ab406c4e7a2c4f62c01e0ed50bb05b34de`  
		Last Modified: Wed, 15 Nov 2023 03:12:48 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d24900fb65faa9f4c9f0ff4fb614e8e7be8e5be6564593aaa5049d4b96e6331`  
		Last Modified: Wed, 15 Nov 2023 03:12:46 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcfaf21e9c7a45ca514db3921fc2dfca01ec692f9cd37791f72578adc2fca6e`  
		Last Modified: Wed, 15 Nov 2023 03:14:37 GMT  
		Size: 612.4 MB (612380773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97f639746dd64b3bce4df1f365382c354f265550f6b8db5193cfa33a094f7f1`  
		Last Modified: Wed, 15 Nov 2023 03:12:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b9e3c0fa0e5aaaa6afdb3cbc0a7f8dffa9f9c02cf14058bb5e8c221eec8d0c`  
		Last Modified: Wed, 15 Nov 2023 03:12:46 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706e46f7ce84f8429f8b571986afe09bb12c5c9da3d8d75e63894650e4b870ce`  
		Last Modified: Wed, 15 Nov 2023 03:12:46 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
