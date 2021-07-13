## `mongo:latest`

```console
$ docker pull mongo@sha256:55220beeb465e818052d15413889ffaa19b680e8082ebbf34e5a68b61e53086e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1999; amd64
	-	windows version 10.0.14393.4467; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:2c2bb95b5fcd6f8a078c8a9aa52e91d1c734cbc95a9362b24f58fbc9f34c4ed7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244569769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5f1204a968489be896f41617231d8c8852140213ba948264f019d58680072f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:11:11 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 18 Jun 2021 01:11:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:11:21 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 01:11:21 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 18 Jun 2021 01:11:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 01:11:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 19:20:15 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 19:20:15 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 13 Jul 2021 19:20:15 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 13 Jul 2021 19:20:15 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 13 Jul 2021 19:20:15 GMT
ENV MONGO_MAJOR=5.0
# Tue, 13 Jul 2021 19:20:16 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 13 Jul 2021 19:20:17 GMT
ENV MONGO_VERSION=5.0.0
# Tue, 13 Jul 2021 19:20:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 13 Jul 2021 19:20:42 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 13 Jul 2021 19:20:42 GMT
VOLUME [/data/db /data/configdb]
# Tue, 13 Jul 2021 19:20:42 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Tue, 13 Jul 2021 19:20:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 19:20:43 GMT
EXPOSE 27017
# Tue, 13 Jul 2021 19:20:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd2834b286611cf1f7b102988029dd6b71c8d6f021ebf86e066cfbbeb67ebe1`  
		Last Modified: Fri, 18 Jun 2021 01:14:41 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543f5ecd43dfe5c6ecbe99383e8149ab0129ac243e2a73821e65bd535647ea02`  
		Last Modified: Fri, 18 Jun 2021 01:14:42 GMT  
		Size: 3.1 MB (3063707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b74f432c74dfb225aea390a227322a65b76b4b2c0a5ca1e7a49b25e1fcdd2b`  
		Last Modified: Fri, 18 Jun 2021 01:14:42 GMT  
		Size: 6.5 MB (6505809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c542e1d2f3bd9fe50a7c4f857ab0df85e03ac7ddf1a19d0990ab059f632d85`  
		Last Modified: Fri, 18 Jun 2021 01:14:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d89dbb44b51ef36053d8cd313316e8b0bfb18c1e15641e3e03f8ae2fce1166`  
		Last Modified: Tue, 13 Jul 2021 19:22:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f400ba5b942074978c01ee0d2aea07a0c314b07e855ab1082e9b2f6b4231657`  
		Last Modified: Tue, 13 Jul 2021 19:22:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3667e2928eef59051b7f8bc12b0e608545da981a6dc8baeefc69bb3fca763839`  
		Last Modified: Tue, 13 Jul 2021 19:22:47 GMT  
		Size: 206.4 MB (206438340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb66a26c2b9a3312a85c9275fcbb44a1b9e6e4146c221c5bb95aaecec848e597`  
		Last Modified: Tue, 13 Jul 2021 19:22:19 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e79c2e5ddbb7481decc5c944ad3cf60e4ac9ba4cc91188ef95e996dee08721c`  
		Last Modified: Tue, 13 Jul 2021 19:22:19 GMT  
		Size: 4.5 KB (4481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:908f9dd18fb8b5e4fc55faab7d584dbfc8d2579320490e33893aebaa6d4d7b07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237257090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b5ffc6e94809f5e2a03b6f363996bfd6347834d0ea70c84e31ba611db99ad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 17 Jun 2021 23:53:58 GMT
ADD file:9e94a579f0495fce8fac6889d0b9b2cd576d5b3ce9f18ff913ad99a503756769 in / 
# Thu, 17 Jun 2021 23:53:59 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:39:34 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 18 Jun 2021 00:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:39:42 GMT
ENV GOSU_VERSION=1.12
# Fri, 18 Jun 2021 00:39:42 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 18 Jun 2021 00:39:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Jun 2021 00:39:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jul 2021 19:40:07 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 13 Jul 2021 19:40:07 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 13 Jul 2021 19:40:07 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 13 Jul 2021 19:40:07 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 13 Jul 2021 19:40:08 GMT
ENV MONGO_MAJOR=5.0
# Tue, 13 Jul 2021 19:40:08 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 13 Jul 2021 19:40:09 GMT
ENV MONGO_VERSION=5.0.0
# Tue, 13 Jul 2021 19:40:35 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 13 Jul 2021 19:40:37 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 13 Jul 2021 19:40:37 GMT
VOLUME [/data/db /data/configdb]
# Tue, 13 Jul 2021 19:40:37 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Tue, 13 Jul 2021 19:40:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jul 2021 19:40:38 GMT
EXPOSE 27017
# Tue, 13 Jul 2021 19:40:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6f86eded34a1950318569803a7e0c689175ebd9d76faf08798f88ac133b98a11`  
		Last Modified: Thu, 17 Jun 2021 23:56:04 GMT  
		Size: 27.2 MB (27158803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4fb14df91e60b3139ee23202e7ab41ca6217f2cf29ac87dd6200c800da3721`  
		Last Modified: Fri, 18 Jun 2021 00:43:27 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd14a02c7a7db08374bfde8b40b03443a2773c9d38d8419b61467e6832288b54`  
		Last Modified: Fri, 18 Jun 2021 00:43:28 GMT  
		Size: 2.9 MB (2913160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8afab734ea82d28732dbe5cdf09476dbe66de7cf91c41bfffcbbe3b3ac7d62c`  
		Last Modified: Fri, 18 Jun 2021 00:43:28 GMT  
		Size: 6.4 MB (6406264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21e957a0820423b87f326efdc3d0fbaad0f8260f489dc441ba876a47642ca21`  
		Last Modified: Fri, 18 Jun 2021 00:43:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ddfbaa758abed1c731b41020002c0aa4b49e589689951514eac7c8fe83ea3a`  
		Last Modified: Tue, 13 Jul 2021 19:42:43 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e29875f0cbbbdde3ab9bddf68c8f5133dfa862ba9ca7afddafd0d4ac4f81fe`  
		Last Modified: Tue, 13 Jul 2021 19:42:43 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d078e63a1c3e8cb044382513e5363a6ce9550363fabdfc26e2b98b469eb3fe2`  
		Last Modified: Tue, 13 Jul 2021 19:43:14 GMT  
		Size: 200.8 MB (200770649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e13f255a9ef48842efed3dc779d13ed9a0f3e4bef9b2d7d9dc3040120c6b8a`  
		Last Modified: Tue, 13 Jul 2021 19:42:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172469d8bf9d4ef48fe1e94d7ddf86192b8ca66baff6284330793d11af84658f`  
		Last Modified: Tue, 13 Jul 2021 19:42:43 GMT  
		Size: 4.5 KB (4481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.1999; amd64

```console
$ docker pull mongo@sha256:f29cf811ea027d47b3f5340a1d5d63d782769c796c1c420995bfc841d1803c43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2873302372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec15f7149ae28b361ad54f2e2873c4e52589c9055d3a6c69ebae2ecf1fccc62`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 13:15:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 20:38:08 GMT
ENV MONGO_VERSION=4.4.6
# Wed, 09 Jun 2021 20:38:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.6-signed.msi
# Wed, 09 Jun 2021 20:38:14 GMT
ENV MONGO_DOWNLOAD_SHA256=ede50e8f8d8c9d23a8ca2cc1c96cdb9bcc1f617930e8bd1d46f21d95d0b555f8
# Wed, 09 Jun 2021 20:40:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Jun 2021 20:40:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Jun 2021 20:40:14 GMT
EXPOSE 27017
# Wed, 09 Jun 2021 20:40:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae7d2dc4b590128efeafd375d02122e65a2525623ac2be100c1a390caf8a4b49`  
		Last Modified: Wed, 09 Jun 2021 15:28:02 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ad0d495f3c090c8857d01c8c5c1d8808a0bd1ebe3acfc68cddc0518c316610`  
		Last Modified: Wed, 09 Jun 2021 21:05:12 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9348cb301dc54c9ee2b3f8272d11780555f985ea355cee0ce937d0cddaf45720`  
		Last Modified: Wed, 09 Jun 2021 21:05:11 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6903e6d82f07267bb25a20ef882109bed3163557a58cd437a2af16689aa9e5b1`  
		Last Modified: Wed, 09 Jun 2021 21:05:09 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecaf79bf9107c588c097d630b343f685f276e07697d8bb199cd470153d94239e`  
		Last Modified: Wed, 09 Jun 2021 21:06:01 GMT  
		Size: 231.7 MB (231707523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ff79e7a1c0d2cc43105f021997558851fa1b429b657840b2cb3fb7c94f9924`  
		Last Modified: Wed, 09 Jun 2021 21:05:09 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c487450715e390654352a901925f1db5f5892e3953b8ace13a9355a429e6f`  
		Last Modified: Wed, 09 Jun 2021 21:05:09 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5ec238c82175f83e27fc909d6ce4034997893f49209d2100d4225cb9acc2a1`  
		Last Modified: Wed, 09 Jun 2021 21:05:09 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.14393.4467; amd64

```console
$ docker pull mongo@sha256:b01b78e78ff15717c569d71b13f27bad07e0a54b9f22b7d338992aab78a52095
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6501876232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbf1160505acb0d2b0e89f9a079acda8bbcbedd1ce856ce14483d8e4e73a49f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 20:40:35 GMT
ENV MONGO_VERSION=4.4.6
# Wed, 09 Jun 2021 20:40:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.6-signed.msi
# Wed, 09 Jun 2021 20:40:39 GMT
ENV MONGO_DOWNLOAD_SHA256=ede50e8f8d8c9d23a8ca2cc1c96cdb9bcc1f617930e8bd1d46f21d95d0b555f8
# Wed, 09 Jun 2021 20:43:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Jun 2021 20:43:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Jun 2021 20:43:44 GMT
EXPOSE 27017
# Wed, 09 Jun 2021 20:43:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6562d39fa84cb30abdaf8ba85c49633fe3dbbbb574b420d3d6f0b6dcd84612c`  
		Last Modified: Wed, 09 Jun 2021 21:06:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632dffa8911cfd4ce0e581711217246f0acb2c9aa23c00d1665325ca9d01474d`  
		Last Modified: Wed, 09 Jun 2021 21:06:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d1a10881159fec53a734a20335f669c66ec8fad205ff18837714b08a2e57eb`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fea5282878f8bceeabdfa4eee9a3b15fa82046d07b73acc8bede72ed373e6eb`  
		Last Modified: Wed, 09 Jun 2021 21:10:53 GMT  
		Size: 236.1 MB (236139160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37d1edadef24c3d2d47473839335006c5e263b365ed3421f7da2ac8cf8d87db`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11529cee90aaa262ba14cbf27ff16a20766bacb7c7c673522446ebf8ae34b949`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c741f47ea5e251f30ac58630bf0c9d48dd7a1cc68e6394f1ad1c5dfe0aed50ed`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
