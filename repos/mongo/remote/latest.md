## `mongo:latest`

```console
$ docker pull mongo@sha256:d672a079266a48faee269e6b5c6b1c7b9d9de3ddd8a1d5097a0881e15576bbb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:24ecfe95bbb98cd49e1d968c204515d4033ef86621e68ce148cf1d0a5a0f8a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (266032684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31b196b207d768e78f2af331869e91d13443f691080d3b93e8009a53391eeaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 28 Jun 2024 22:05:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_MAJOR=7.0
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 28 Jun 2024 22:05:28 GMT
ENV HOME=/data/db
# Fri, 28 Jun 2024 22:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 22:05:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 28 Jun 2024 22:05:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bdcacccd9761e2d61780030bcd45f245b518b8a809ce4c4c9482a0c55e7538`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b691142508b5c91753247cacfc5c7510117a337334137fe5b218e7840ebc15`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 1.5 MB (1500843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc1924dee6dc5e546ac00dd4882faa4d15b1b0801f7473d0bb2724ea2b51dc8`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 1.1 MB (1094666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a7990873d9ed83419722cfd149480ba8e3594e67fd3570bea80e7b7d08705`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e5254f6ae82e6ba705687e57f0f00d08f71e5aa27b0b9f9751c56e0591f681`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f753f5920b37b6dbad685fec1c4fe36da1716c33d050dad2a0a1289655dfa`  
		Last Modified: Tue, 02 Jul 2024 03:04:34 GMT  
		Size: 233.9 MB (233895960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cd53ea307cf86c5f6dc6be61ec92146c1b1d8dc0e86430ad1ed5eea3b6c06d`  
		Last Modified: Tue, 02 Jul 2024 03:04:31 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:df188eaf6293052ea19cd9f241d95188b7874029311548533bf603faa6e78726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3029117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b158c3805fcdf1eb2472d2eed370424252603d31bbf90f98f5dc84261262c0`

```dockerfile
```

-	Layers:
	-	`sha256:e800034b7bc03f34d08465829d2dec7812b1dad55bf724794a2fed0cc82954ba`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 3.0 MB (3001481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4673448c7bbb6b0d6d02fa9b6849a7ab18436af966f652b1bb2f8aef663e16db`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 27.6 KB (27636 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:3392526162619b2879841de68549cdaf68a9397dd0dda190f338c07f52894c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257705566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b372541400c4f030ccf979c9fbb53708c2ef6d705f60353f4f6e82c2dc91a06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 28 Jun 2024 22:05:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 28 Jun 2024 22:05:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 28 Jun 2024 22:05:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_MAJOR=7.0
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 22:05:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 28 Jun 2024 22:05:28 GMT
ENV HOME=/data/db
# Fri, 28 Jun 2024 22:05:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 28 Jun 2024 22:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jun 2024 22:05:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 28 Jun 2024 22:05:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31884fd206c88e23f26415a3b42f7eb8bb3f077ab4a83c263894fc97c742f601`  
		Last Modified: Tue, 02 Jul 2024 15:51:38 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a322bad11a3dfbe5821d19f93c35cf813768e29029b4a58a359b6e0f552c72`  
		Last Modified: Tue, 02 Jul 2024 15:51:38 GMT  
		Size: 1.5 MB (1465959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726cb38e7eb88a4d67d7bcaedef1167045524d6689c4f678ae455692447ffdcd`  
		Last Modified: Tue, 02 Jul 2024 15:52:56 GMT  
		Size: 1.0 MB (1027430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b21775af30ad56d650238ed7459a38221ff5584157532d845d860809382db8`  
		Last Modified: Tue, 02 Jul 2024 15:52:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b5d5657fe3976931b9c892b0c9dca1e54d47d1066356e12fddd94bffe198ce`  
		Last Modified: Tue, 02 Jul 2024 15:52:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30714bc85fb6d5700da2996397578d8b2246598a1c8b6ea8ecd021a1f399d008`  
		Last Modified: Tue, 02 Jul 2024 15:53:00 GMT  
		Size: 227.8 MB (227844992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba57d7527510ee11a45ecb15b8f084303ff00b0fef5ebe979380312a327afb51`  
		Last Modified: Tue, 02 Jul 2024 15:52:57 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:13272ba436be12a2b5271f941725502f238b08fe57a550f75b57c69c2f3b6054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3029807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfd698af09a9d19f068399a48545e28cf742f25a30f7814135c8fefa72722e2`

```dockerfile
```

-	Layers:
	-	`sha256:dbb4b08745d6f579d50d93ef5defe7ed3461a88c5fa8db2253131166b62d7961`  
		Last Modified: Tue, 02 Jul 2024 15:52:56 GMT  
		Size: 3.0 MB (3001823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8af7213b79bcdec3ea920fae58d04e65d3d423e029ce0911e2d7834b42a2307`  
		Last Modified: Tue, 02 Jul 2024 15:52:55 GMT  
		Size: 28.0 KB (27984 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.20348.2655; amd64

```console
$ docker pull mongo@sha256:09f7458917dfa6cb05f39ad6630fb8a1c7c9f3e1a8d3bd400e629db35adf9266
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2750562909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312a825e0fc0adc403a982ef1763ccc2fec51df69d2a46179ca61d180cdac5c3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:15:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:15:02 GMT
ENV MONGO_VERSION=7.0.12
# Tue, 13 Aug 2024 20:15:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Tue, 13 Aug 2024 20:15:04 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Tue, 13 Aug 2024 20:16:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:16:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 20:16:24 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 20:16:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304371999569501d22285076d583445ae9a71dbc9bbc8794422c2172c0f4c730`  
		Last Modified: Tue, 13 Aug 2024 20:16:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef456b8e36791a63aebfd02aa1457364b236b1e2d2ee28217313ef896cfe0fd`  
		Last Modified: Tue, 13 Aug 2024 20:16:28 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a1faaf446fba34c83978864b5b7d75a38c16fbfdd6843bb2b84eabdd57c842`  
		Last Modified: Tue, 13 Aug 2024 20:16:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a13aa819105bd796037c014ef879e4bcd9dd5c8d3824b8a2250c14dc5818a2`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffee34de017a49064632da5d7e1030bfc31a5105652f49a2ee08474a7f5960f`  
		Last Modified: Tue, 13 Aug 2024 20:17:19 GMT  
		Size: 608.8 MB (608788900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddbae91ab071def197c99a0c9b02d0b1e796e34cc04132d24c6d91d8b7cd3c0`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42165731c8550589c978e9d836425f3d687ae47963aa87ce4541efa9d5d993b0`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4299b8be79063f08fb975a723b9b4ec3315a2ea1ccd398081fbf8462cb5c816e`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:fc96eee784925b76ce9af670d74128c8ccff576ee3a3d27b9a64aa42c95e6c98
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2854123657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f451edc685259979df504d45c5b187af7161679a1db62ae1443dd069b198468`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:16:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:16:09 GMT
ENV MONGO_VERSION=7.0.12
# Tue, 13 Aug 2024 20:16:10 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Tue, 13 Aug 2024 20:16:10 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Tue, 13 Aug 2024 20:18:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:18:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 20:18:14 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 20:18:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5fad384d45d89607211110ce60951115ac0f9fa8c606bffead989f6ecb382f`  
		Last Modified: Tue, 13 Aug 2024 20:18:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329a398fe85cf030807bf41b6720420793c696816ff23d58b45e5dc94e047664`  
		Last Modified: Tue, 13 Aug 2024 20:18:19 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ad1c05d571d3c52fbc4399b2bc09aeff40e8e66d6b73df1ab1f8b32a43bfa3`  
		Last Modified: Tue, 13 Aug 2024 20:18:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb14bd68fa1091de79c25fd53310d1a26b9af0620acaf272acab1545d098080f`  
		Last Modified: Tue, 13 Aug 2024 20:18:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f62e7b296004c7b66b7189017ec56ce147da7cf67c97b1abccbde13d38bb13`  
		Last Modified: Tue, 13 Aug 2024 20:19:08 GMT  
		Size: 608.9 MB (608911360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203cecf2f6ff03f104829de0b7eb36097193eb3d346f139226f6200e0138645d`  
		Last Modified: Tue, 13 Aug 2024 20:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e3863f3b50c73c620154f9e2c45a0940958ed3683e41aa3e8599bbc347b53b`  
		Last Modified: Tue, 13 Aug 2024 20:18:18 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda7a1fc8e14d4dde60bbece6f2c67d59cd77234a64f8fe82cb876f222e181fe`  
		Last Modified: Tue, 13 Aug 2024 20:18:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
