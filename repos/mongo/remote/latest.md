## `mongo:latest`

```console
$ docker pull mongo@sha256:b0abf19259902648be5ac17479dd4c65e037c3292c9eb09181f087687bca5102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:d1e3b724d514ed8df7f73ee175057160bde1c9cf3a85536e5e96161f40e8cf63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248870002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2388d1f0a57b9111045828faffacb618474b114e12c1de67f96f2bbd97ebe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:57:21 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 03 Mar 2022 21:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:57:29 GMT
ENV GOSU_VERSION=1.12
# Thu, 03 Mar 2022 21:57:29 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 03 Mar 2022 21:57:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 03 Mar 2022 21:57:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 03 Mar 2022 21:58:22 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Thu, 03 Mar 2022 21:58:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 03 Mar 2022 21:58:23 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 03 Mar 2022 21:58:23 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 03 Mar 2022 21:58:23 GMT
ENV MONGO_MAJOR=5.0
# Thu, 03 Mar 2022 21:58:23 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 03 Mar 2022 21:58:23 GMT
ENV MONGO_VERSION=5.0.6
# Thu, 03 Mar 2022 21:58:49 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 03 Mar 2022 21:58:51 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 03 Mar 2022 21:58:51 GMT
VOLUME [/data/db /data/configdb]
# Thu, 03 Mar 2022 21:58:51 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:58:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Mar 2022 21:58:51 GMT
EXPOSE 27017
# Thu, 03 Mar 2022 21:58:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a403577c28fafaf89a46590d69c237ae9fd5e576f96bf984e45ead657a3ef3`  
		Last Modified: Thu, 03 Mar 2022 22:07:07 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bbb7dc901383749cee88f0d357711cf7059ef51211c4725d60127a431d2844`  
		Last Modified: Thu, 03 Mar 2022 22:07:08 GMT  
		Size: 3.1 MB (3064492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81b1e5a386bad953e0fc4c4625bb63aea27c931f575e665730eea7fd4f373ad`  
		Last Modified: Thu, 03 Mar 2022 22:07:08 GMT  
		Size: 6.5 MB (6505604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdc1db49ec948ae1977bbbf82bca00efce13bebbaf1aabbe5ec24e1b3c268db`  
		Last Modified: Thu, 03 Mar 2022 22:07:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2f602f894c906b6b36c7b1fff4333658756e4f4837e21ded39c2d244c49405`  
		Last Modified: Thu, 03 Mar 2022 22:07:05 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627a84bea5f4b8ca8fe1ec90c21ac1946afa459fef7530bc9c674a4a3078308f`  
		Last Modified: Thu, 03 Mar 2022 22:07:05 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc06fa2a9f52c275570ed1ba6e5d3ab70a0a7f7c99ec7b328048a13afde1394f`  
		Last Modified: Thu, 03 Mar 2022 22:07:34 GMT  
		Size: 210.7 MB (210725432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0133c89ee92bf3428f2584f62b0d138cf4d6d1930c9a1426d20a4107f064fe79`  
		Last Modified: Thu, 03 Mar 2022 22:07:05 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e990167b745c8c6acbe9e08774be8420a7da623527573a2b7a767db9bd80d87`  
		Last Modified: Thu, 03 Mar 2022 22:07:05 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:16c7c417c0f803e2012d123c54b8479f733c6f902768494617f8a2f0fb515ed9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241079914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4c92fc145cd21d7af328656bbdf08a6039e2d58f31f89777fd9a6f976f59f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:50:47 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 03 Mar 2022 20:50:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:50:58 GMT
ENV GOSU_VERSION=1.12
# Thu, 03 Mar 2022 20:50:59 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 03 Mar 2022 20:51:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 03 Mar 2022 20:51:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 03 Mar 2022 20:51:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Thu, 03 Mar 2022 20:51:54 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 03 Mar 2022 20:51:55 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 03 Mar 2022 20:51:56 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 03 Mar 2022 20:51:57 GMT
ENV MONGO_MAJOR=5.0
# Thu, 03 Mar 2022 20:51:58 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 03 Mar 2022 20:51:59 GMT
ENV MONGO_VERSION=5.0.6
# Thu, 03 Mar 2022 20:52:25 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 03 Mar 2022 20:52:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 03 Mar 2022 20:52:27 GMT
VOLUME [/data/db /data/configdb]
# Thu, 03 Mar 2022 20:52:29 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Thu, 03 Mar 2022 20:52:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Mar 2022 20:52:30 GMT
EXPOSE 27017
# Thu, 03 Mar 2022 20:52:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93835005f83fca8d11e84de6d362cbdac541df8362e80c6a0172100f8b8a27ea`  
		Last Modified: Thu, 03 Mar 2022 21:02:38 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b1c8f1aa262a4f9ecfc4a311235d079693056c9b47ac47c30478ac25c87e36`  
		Last Modified: Thu, 03 Mar 2022 21:02:36 GMT  
		Size: 2.9 MB (2912105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9207ce7ec0ce748a22c1074f1471f694ca5a46ba77f3cb86f7485a9df75f492`  
		Last Modified: Thu, 03 Mar 2022 21:02:36 GMT  
		Size: 6.2 MB (6248075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98a90fbda7bccfa543c5d402318d145dc64f2d3be60275c04a10ede986569ca`  
		Last Modified: Thu, 03 Mar 2022 21:02:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ca3d6b9bafb90b33e2e2d4651318004e2bc74d76aaa8502aff9e78b134589f`  
		Last Modified: Thu, 03 Mar 2022 21:02:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e915500804c314c72f7e604e9cd17e410eb3a9d186b1cdf94cdad32add6e750`  
		Last Modified: Thu, 03 Mar 2022 21:02:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289a3a230e1df28826d50ce17e1c042aeaecf7f6045713355263ab2a3f717e9`  
		Last Modified: Thu, 03 Mar 2022 21:03:01 GMT  
		Size: 204.7 MB (204741520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e9aa7f19e73d27fbbffb762b8499cbec2c6d4e11a988d0cd4ebced973f6b04`  
		Last Modified: Thu, 03 Mar 2022 21:02:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dce2383b1d022163ec8099933f09fae45c32b13a97f3508bec941859a641b2`  
		Last Modified: Thu, 03 Mar 2022 21:02:33 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.524; amd64

```console
$ docker pull mongo@sha256:2e33c72be9c2dfd405570da7c568ce40b5ff928a348c37dc77d038ed702d3900
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2518632952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4656a0a7e2a7ebb27306e0593af491f1907c749dd6cceb37f825dd042e6221`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Tue, 01 Feb 2022 02:49:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 09 Feb 2022 14:56:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 16:52:33 GMT
ENV MONGO_VERSION=5.0.6
# Wed, 09 Feb 2022 16:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.6-signed.msi
# Wed, 09 Feb 2022 16:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=f6e2bc600b2b8b0251a9e99d84fefc43c66e45deb5793ed8e65cd12a318c76ee
# Wed, 09 Feb 2022 16:54:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Feb 2022 16:54:53 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Feb 2022 16:54:54 GMT
EXPOSE 27017
# Wed, 09 Feb 2022 16:54:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:898469748ff68223ab87b654b29fb366c1f4f2b7cfad7a37426346ea16db8dfa`  
		Size: 963.2 MB (963225591 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ff78097ae7bacc8d0990c9620bbe5ddc9639d4f309f097c6cdd3cc7a68e56aad`  
		Last Modified: Wed, 09 Feb 2022 16:39:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1720968c024a720137a114fface1f915ba0fd85e0492c4f3def0f09bfe86ed8`  
		Last Modified: Wed, 09 Feb 2022 17:31:41 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb8650848e898ae4b21e6c9ef08a95cb44f793d969d0c53682ea9d5b0d6c232`  
		Last Modified: Wed, 09 Feb 2022 17:31:40 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cad2d5bbcf613034086611ba95509bd31a44c30ede6b2e89c18af4a30aac76`  
		Last Modified: Wed, 09 Feb 2022 17:31:38 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608f023e48193be3f253098749dfd4aaab573ce855a4ae54f1e896ec40165278`  
		Last Modified: Wed, 09 Feb 2022 17:36:58 GMT  
		Size: 303.7 MB (303698411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d57e1670d94bfce2a3d7cbc6039f4c3a0656d378b4539814336634aad541d5`  
		Last Modified: Wed, 09 Feb 2022 17:31:38 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ece5446a3ae673f58e817aa5bd340179373c2339627916fdd5cb85d5a22aff`  
		Last Modified: Wed, 09 Feb 2022 17:31:38 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd24f43a8325a63ed3a6f78a304bab36493f5a650df8b8d727999007b5acf40`  
		Last Modified: Wed, 09 Feb 2022 17:31:38 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.2565; amd64

```console
$ docker pull mongo@sha256:fe6606626eff67e03aae4ff876e0aa01c6fe632da83c3459a1b8c322de6d184b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3017197463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6897ba10a4e96c672a21cc22a603a0f4ae5f0d6c090bf37dbffd58925ad87d48`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 16:55:15 GMT
ENV MONGO_VERSION=5.0.6
# Wed, 09 Feb 2022 16:55:16 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.6-signed.msi
# Wed, 09 Feb 2022 16:55:17 GMT
ENV MONGO_DOWNLOAD_SHA256=f6e2bc600b2b8b0251a9e99d84fefc43c66e45deb5793ed8e65cd12a318c76ee
# Wed, 09 Feb 2022 16:58:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Feb 2022 16:58:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Feb 2022 16:58:16 GMT
EXPOSE 27017
# Wed, 09 Feb 2022 16:58:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c519ba05cc7100838acc148104c8a33bfaec5446aa2c9a10f16d6e85b11ea7fd`  
		Last Modified: Wed, 09 Feb 2022 17:37:16 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250fe36d1564a90d3a9bdcb5577f8f9ab60a3160122f6a73862cd76fa69c7a2d`  
		Last Modified: Wed, 09 Feb 2022 17:37:16 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360e0458d5c65d58709df9d76da6ddae568e3f109612eadbdc5b26baaa5372b5`  
		Last Modified: Wed, 09 Feb 2022 17:37:13 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b225fde6eacdc36e0ec64d139536923a38be57b7a5acca7352ccf61a5dfc52`  
		Last Modified: Wed, 09 Feb 2022 17:38:07 GMT  
		Size: 303.5 MB (303472777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9f467c6a2d07347e18eacb36da020e1392114dc0ba7fafa64ac0372812e4fe`  
		Last Modified: Wed, 09 Feb 2022 17:37:13 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142de3b921be3ef8da67ccdeda6db94ff58916785a9d4eed8a55c768b1e51c49`  
		Last Modified: Wed, 09 Feb 2022 17:37:13 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ee4171601008010af5ae4b655173c7e1e2c5554f540be43c1d73044f44cec`  
		Last Modified: Wed, 09 Feb 2022 17:37:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
