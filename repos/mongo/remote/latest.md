## `mongo:latest`

```console
$ docker pull mongo@sha256:8d618695cf4885846da876a07ab6f3c50858e93b74b82fab3413341c1bf41aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:15342c724bd7c4be9b329078040bdd1f6629eca737d64fb0e249a08a914b31d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246587169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4130848d45a9029621ebb788067479178f90f7cb2eadd23277cb1c056ddd3b7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:30:41 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 02 Aug 2022 20:30:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:30:50 GMT
ENV GOSU_VERSION=1.12
# Tue, 02 Aug 2022 20:30:50 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 02 Aug 2022 20:31:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 20:31:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 20:31:03 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 02 Aug 2022 20:31:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 02 Aug 2022 20:31:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 20:31:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 20:31:03 GMT
ENV MONGO_MAJOR=5.0
# Tue, 02 Aug 2022 20:31:04 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 20 Aug 2022 01:25:13 GMT
ENV MONGO_VERSION=5.0.11
# Sat, 20 Aug 2022 01:25:42 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 20 Aug 2022 01:25:43 GMT
VOLUME [/data/db /data/configdb]
# Sat, 20 Aug 2022 01:25:43 GMT
ENV HOME=/data/db
# Sat, 20 Aug 2022 01:25:44 GMT
COPY file:b7b44e96082c97da2e7f6248f8bbb2edd837542169af52bcc3f53a0cf8b74b7e in /usr/local/bin/ 
# Sat, 20 Aug 2022 01:25:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Aug 2022 01:25:44 GMT
EXPOSE 27017
# Sat, 20 Aug 2022 01:25:44 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016bc871e2b33f0e2a37272769ebd6defdb4b702f0d41ec1e685f0366b64e64a`  
		Last Modified: Tue, 02 Aug 2022 20:33:16 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd649edd82d79ffc6f573cd5da7909ae50596b95aca684a571aff6e36aa8cb`  
		Last Modified: Tue, 02 Aug 2022 20:33:17 GMT  
		Size: 3.1 MB (3059542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bf776c01e412c9cf35ea7a41f97370c486dee27a2aab228cf2e850a8863e8b`  
		Last Modified: Tue, 02 Aug 2022 20:33:17 GMT  
		Size: 6.5 MB (6506025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f0405a2fe343547a60a9d4182261ca02d70bb9e47d6cd248f3285d6b41e64c`  
		Last Modified: Tue, 02 Aug 2022 20:33:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417812e2676cfb1081230e71a277704bbeb9a058b34dc34fc1f83a874410d437`  
		Last Modified: Tue, 02 Aug 2022 20:33:14 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905384a6c9a925f65f24476b0520ff9fbb65badb483ce7d3ce01d837894f2cb8`  
		Last Modified: Tue, 02 Aug 2022 20:33:14 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768aa2a1becc4323abd25288f2eb8d4e60451fee416867061d3c5e867c80190e`  
		Last Modified: Sat, 20 Aug 2022 01:27:42 GMT  
		Size: 208.4 MB (208440363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623c0121bf78896bdced9f79b10ab231242be65940fa95b6d5b054902b1da0e7`  
		Last Modified: Sat, 20 Aug 2022 01:27:14 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:7229980e6be8d3605f74de9ac0a294e593d6edc9ec391bedc62ac846b666f2b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238850920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f91cb7f47f4afc438117f97816bc48767aa1277d2732664ea18e76d57311e39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:46:08 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 02 Aug 2022 18:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:46:42 GMT
ENV GOSU_VERSION=1.12
# Tue, 02 Aug 2022 18:46:43 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 02 Aug 2022 18:47:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 18:47:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 18:47:04 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 02 Aug 2022 18:47:05 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 02 Aug 2022 18:47:06 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 18:47:07 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 02 Aug 2022 18:47:08 GMT
ENV MONGO_MAJOR=5.0
# Tue, 02 Aug 2022 18:47:09 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 20 Aug 2022 01:45:51 GMT
ENV MONGO_VERSION=5.0.11
# Sat, 20 Aug 2022 01:46:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 20 Aug 2022 01:46:14 GMT
VOLUME [/data/db /data/configdb]
# Sat, 20 Aug 2022 01:46:15 GMT
ENV HOME=/data/db
# Sat, 20 Aug 2022 01:46:17 GMT
COPY file:b7b44e96082c97da2e7f6248f8bbb2edd837542169af52bcc3f53a0cf8b74b7e in /usr/local/bin/ 
# Sat, 20 Aug 2022 01:46:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Aug 2022 01:46:18 GMT
EXPOSE 27017
# Sat, 20 Aug 2022 01:46:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f92e7525120387a6bc9ec42b9ebfc8115309ab70f65a766e3fda1239d787f9`  
		Last Modified: Tue, 02 Aug 2022 18:51:20 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdda1347325980782ee9b7c6232d712c262b77bc097f712508cf17423dea0de`  
		Last Modified: Tue, 02 Aug 2022 18:51:21 GMT  
		Size: 2.9 MB (2907020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e02463a0f47d7c309281cbc5b4603815ec64c4653d4ed4ac37a06e6bb91b8e`  
		Last Modified: Tue, 02 Aug 2022 18:51:21 GMT  
		Size: 6.2 MB (6249317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9bc5b0968e9dc0079b9ed64930bcf14f8d69847b72f526a1dd1c8bd43df8cc`  
		Last Modified: Tue, 02 Aug 2022 18:51:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f0d07ad9ca0e23d2aa1f261353224866eb9e7e2aee1f1e0f55252f197a51a6`  
		Last Modified: Tue, 02 Aug 2022 18:51:18 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c25f5ea9839a3e6d5693d2a2ccb61e495710d2e0ae3523d52ab23a576c87a8`  
		Last Modified: Tue, 02 Aug 2022 18:51:18 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45978cf40df4c00556b647b2a43581b9da690cbba41ca80fff2dd2de68b5002`  
		Last Modified: Sat, 20 Aug 2022 01:48:35 GMT  
		Size: 202.5 MB (202494278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6707d110142a48fc3fd51f49cfb60012e05613bfa56486c826b718de684f8de`  
		Last Modified: Sat, 20 Aug 2022 01:48:07 GMT  
		Size: 5.0 KB (4953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.887; amd64

```console
$ docker pull mongo@sha256:eb780ace213935639b0c52fd1d0126a96baa7769980dd8874513551c194adc64
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2827459434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a068a5ef96ae377d29f507455d6d31d4be40947e02f02b57d5fae93ed56d8caa`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 13:33:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 24 Aug 2022 22:20:28 GMT
ENV MONGO_VERSION=6.0.1
# Wed, 24 Aug 2022 22:20:30 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.1-signed.msi
# Wed, 24 Aug 2022 22:20:33 GMT
ENV MONGO_DOWNLOAD_SHA256=999b39df67a77eda3198f8412dc159b0cd8aa6677b901a0cf287921884306ac3
# Wed, 24 Aug 2022 22:22:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 24 Aug 2022 22:22:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 Aug 2022 22:22:49 GMT
EXPOSE 27017
# Wed, 24 Aug 2022 22:22:51 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ff9b89cbdb5f88cb926263140643eb2bfad61fb092119830e290c8f8ff711c8f`  
		Last Modified: Wed, 10 Aug 2022 15:05:31 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd7efca209e774c4a36672309ba8ca7bfb3b19ff678b88b29e8ae6b4a4f6f1`  
		Last Modified: Wed, 24 Aug 2022 22:50:29 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f42c41de4d0146e05d2f121ae0d1f7dcf762c8693c19a905fb57aa4634f226d`  
		Last Modified: Wed, 24 Aug 2022 22:50:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3aa1a73ee48e9a6d45d98005c080b190c68e7bcc42f9f07a25113dced65f6c`  
		Last Modified: Wed, 24 Aug 2022 22:50:26 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8379514e18c1f59e19da84edc7704dd411bdb705b14b9921e1518a2bd6fa91e`  
		Last Modified: Wed, 24 Aug 2022 22:51:42 GMT  
		Size: 510.6 MB (510560384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619dcf50ea0c5d58a23998106214de32df475d2ef6effc1c7814401d0002063b`  
		Last Modified: Wed, 24 Aug 2022 22:50:26 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5583d44b6c97384a6373b070c5e5f20890efc1a546cf0d1c46bb3cde19b78`  
		Last Modified: Wed, 24 Aug 2022 22:50:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14524abd86317864e27bbf69b26825dae062a1b7c7989cb60339627c5e2d4c36`  
		Last Modified: Wed, 24 Aug 2022 22:50:26 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.3287; amd64

```console
$ docker pull mongo@sha256:4cdc1b42c969779aa235db37bd2032d4039bafe4873cd92815ff6da5fe6b174a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3188041560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff3f79430666efb79ad68d561dfc49d451739643832d5bb12078a697252376d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 24 Aug 2022 22:23:14 GMT
ENV MONGO_VERSION=6.0.1
# Wed, 24 Aug 2022 22:23:16 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.1-signed.msi
# Wed, 24 Aug 2022 22:23:18 GMT
ENV MONGO_DOWNLOAD_SHA256=999b39df67a77eda3198f8412dc159b0cd8aa6677b901a0cf287921884306ac3
# Wed, 24 Aug 2022 22:26:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 24 Aug 2022 22:26:09 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 Aug 2022 22:26:11 GMT
EXPOSE 27017
# Wed, 24 Aug 2022 22:26:14 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34716fa1da4761caaad6e9f10e85cc622d30700891d1b9bd5d4a423a40f8631d`  
		Last Modified: Wed, 24 Aug 2022 22:52:01 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d87db2a376c901b76b0863788cd1298471786b9d204bb55b99ed0f804c6958`  
		Last Modified: Wed, 24 Aug 2022 22:52:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4206639ce1c663688d04594a60ba96835f233d935d31464f1ec23036ae5931`  
		Last Modified: Wed, 24 Aug 2022 22:51:58 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140f1ef13fb603028e27e2b450ced77785ed3b92dc98d854a60570b79d7c47e0`  
		Last Modified: Wed, 24 Aug 2022 22:53:17 GMT  
		Size: 510.3 MB (510318914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ed0a278d09575040bcc31ebdc9bfab524cc363df32ebcb5663a77f3f18f92`  
		Last Modified: Wed, 24 Aug 2022 22:51:58 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59915d09f1fddc1c80a13998bfc256f358f566e16a84599f3b2deeaf52f0ca`  
		Last Modified: Wed, 24 Aug 2022 22:51:58 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b685ca4f8bfb31c6fa64a7f3333908590a5a64ee6f62595a87961256233da08`  
		Last Modified: Wed, 24 Aug 2022 22:51:58 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
