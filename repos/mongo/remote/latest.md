## `mongo:latest`

```console
$ docker pull mongo@sha256:5a6889e9f5e0c71ad8d1cf94b6d83d38162ba198e6083371e5141fc38137a01a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:3a023748ee30e915dd51642f1ef430c73c4e54937060054ca84c70417f510cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258563022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79112eff9c89624d06e0506e6ae01b76c68ec9fdbe2eda0c6f7ae56dae725f41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:33:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:33:16 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:33:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:33:16 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:33:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:33:16 GMT
ENV MONGO_MAJOR=7.0
# Thu, 29 Feb 2024 23:33:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ENV MONGO_VERSION=7.0.6
# Thu, 29 Feb 2024 23:33:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:33:16 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:33:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:33:16 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:33:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f07c832c0f4445791104ec094d14aee6178875b308ba2695ff7bff1c4f2158`  
		Last Modified: Wed, 06 Mar 2024 02:57:04 GMT  
		Size: 1.8 KB (1774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab2da22865c99f9d744b57e79dc62e733f07acd1f37ec72c6e0b9d4fe358699`  
		Last Modified: Wed, 06 Mar 2024 02:57:05 GMT  
		Size: 1.5 MB (1500328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7ceac81d5bf87c9d8f3630efba2c60a13fd35ac9fb73d1cce0e2d192baaae5`  
		Last Modified: Wed, 06 Mar 2024 02:57:05 GMT  
		Size: 1.1 MB (1094183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e507bb35e3318cb80a6aebcc70a00f79bbf3fd9eaa4ddd987e0d7dd00058f3b`  
		Last Modified: Wed, 06 Mar 2024 02:57:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf53d03cb40edb33e759e0f5bf6bd2c621e9e25be56949d23c07866cea7cee80`  
		Last Modified: Wed, 06 Mar 2024 02:57:05 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc32baa6c25a9ff05d6bbb2640981f475c7493461a2b44fab8c4a9020b25722b`  
		Last Modified: Wed, 06 Mar 2024 02:57:12 GMT  
		Size: 226.4 MB (226422397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cbd27917486c36829d0b826a8dbf92c0af85c790b6c589422e2c51b659833e`  
		Last Modified: Wed, 06 Mar 2024 02:57:06 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:dc4c466c11c87676f9647edd8c8c944dd86ad6627cba9c095c9fbde7750d3241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f364603f6c81f491d9b178b0cdd54410649b32328bc083d66b8cb42b029f4195`

```dockerfile
```

-	Layers:
	-	`sha256:50d6bb8cba4b5104d3bfe24e25c09e707b2956ea1e688201935f2f714d588938`  
		Last Modified: Wed, 06 Mar 2024 02:57:05 GMT  
		Size: 3.0 MB (2999865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42e9666f40a147bd14e7e0b6bb7a4feb37b38c4c7cebbfe697707e47468e48e`  
		Last Modified: Wed, 06 Mar 2024 02:57:04 GMT  
		Size: 27.7 KB (27735 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:997b2d81860269d50e2f2c9cb8ab08f59c80f969fd4f4d8529df7d9b0935d556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250408655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e5c11c442d7945ae38f403a0a7b6446f9728c550f9d60e0ee24087afbdd443`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:33:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:33:16 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:33:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:33:16 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:33:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:33:16 GMT
ENV MONGO_MAJOR=7.0
# Thu, 29 Feb 2024 23:33:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ENV MONGO_VERSION=7.0.6
# Thu, 29 Feb 2024 23:33:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:33:16 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:33:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:33:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:33:16 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:33:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a4a2c7a57ed8b997579870d0927433b03cfd94f5dba2153bdbcd885b5d620035`  
		Last Modified: Tue, 13 Feb 2024 10:22:28 GMT  
		Size: 27.4 MB (27356877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354176b189db5e882e8695cd36475579099a8312ad5731dd9c9365249630636`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a94d566154f568d8d3806d6f82aeec09ecd0408a9db227eceeb6849c9ead90`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 1.5 MB (1465222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e46f202d7a90abe40c09f31f1cf2c48277023e1dd069bf9a2687256c1c5e7b`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 1.0 MB (1026758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d926c33a8021648a6ee91c79b9743e0c4b7824f0e4abfd2d086fa58e86b389`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d249179d7272d9abc175c7f3f633122bd78ebc02e3551c0af3316984232a74`  
		Last Modified: Fri, 16 Feb 2024 19:01:35 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52760e866f213e432188386f2152b688fc342c468fbc12396b4d0534c5f45a6a`  
		Last Modified: Fri, 01 Mar 2024 06:13:27 GMT  
		Size: 220.6 MB (220552635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a92ed7955e318faeddaab8caab2acfe12d9b31433f4dfd104f6ab3b71ad666`  
		Last Modified: Fri, 01 Mar 2024 06:13:23 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:9ec8b1c7b7460653f043b377a98aa1bfedeb21fe2aaa8ec193e4ecf62b715482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49db1682b06744267b312033264e4fbf54dc38102cc185b8f7b2febbd988d0b6`

```dockerfile
```

-	Layers:
	-	`sha256:a1c66b6611dfc1a687f394fe28a05e9ec43cfeac773a027e2f34bd8273bd6034`  
		Last Modified: Fri, 01 Mar 2024 06:13:23 GMT  
		Size: 3.0 MB (3000122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ba24002c6172814b1e3a478a8941616764c18a93d2fecf5d4c1903e2278848`  
		Last Modified: Fri, 01 Mar 2024 06:13:22 GMT  
		Size: 27.6 KB (27591 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:fe7bfeef166c55aa9f1469374efc137fd9b113c4885f07937491816aa422397a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2572515990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7546be7438a0a693c90ce8d5c0d78c601658b7b7b430479cf934e61b908fcf07`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:06:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 00:06:02 GMT
ENV MONGO_VERSION=7.0.6
# Wed, 13 Mar 2024 00:06:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.6-signed.msi
# Wed, 13 Mar 2024 00:06:04 GMT
ENV MONGO_DOWNLOAD_SHA256=29fb23ca36a9dd6fee2f6491a92392c404d544ffe38bfaf3d2467db0bd774fde
# Wed, 13 Mar 2024 00:07:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:07:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 00:07:26 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 00:07:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade502e1a89fb2443bcc162a89b3065bdac30aea1068de4ffbcfc9407a26090b`  
		Last Modified: Wed, 13 Mar 2024 00:07:35 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e3919bf1f8d3c03b3156433d174008c799ead72ed969884e13600f85e120b7`  
		Last Modified: Wed, 13 Mar 2024 00:07:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcccbbe6d271a50ec455c3cb2dec8a9077320b78c081bad2fea822235d4929e`  
		Last Modified: Wed, 13 Mar 2024 00:07:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2d620f976729f09d7bf0d234ccdd6b8b1b5cf773b75244c71db47767cddded`  
		Last Modified: Wed, 13 Mar 2024 00:07:33 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebe89dcfd388595ee07f3d1f83cebe4c97c69f0c1f26fdc35386dd0cbce7458`  
		Last Modified: Wed, 13 Mar 2024 00:08:27 GMT  
		Size: 615.0 MB (615047924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d658cfa62684f9a26031429cb663383c18774c5e2575413652ec7a7ea2e2f6e6`  
		Last Modified: Wed, 13 Mar 2024 00:07:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ad98ede4bd6d12d24e9c0e3665a84158374811392a5e351708f9375e84e508`  
		Last Modified: Wed, 13 Mar 2024 00:07:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2595f870981ce52aaa26c33d0392909e6c707a4744d5db3a33e1d78cc31c1c6b`  
		Last Modified: Wed, 13 Mar 2024 00:07:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:e33586e46d6f3d4ff1e2acd4110dccefb5ecf64eeeaa94a2c579c56f5fdbe836
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2740178450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269008d76ef15f43c02afbee5340bb2af74ff2f9100da4dfdbbb660b8bbc5aa8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:11:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 00:11:10 GMT
ENV MONGO_VERSION=7.0.6
# Wed, 13 Mar 2024 00:11:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.6-signed.msi
# Wed, 13 Mar 2024 00:11:12 GMT
ENV MONGO_DOWNLOAD_SHA256=29fb23ca36a9dd6fee2f6491a92392c404d544ffe38bfaf3d2467db0bd774fde
# Wed, 13 Mar 2024 00:13:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:13:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 00:13:05 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 00:13:06 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea5669a1d47bee0cad3bc12d112d15407834d74be94fde844fcb1b557df07dc`  
		Last Modified: Wed, 13 Mar 2024 00:13:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd9da2ef937bad385e61c3c822a904d5153167cc989d88e150c1adc8ac62e17`  
		Last Modified: Wed, 13 Mar 2024 00:13:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc369613e07c7bf115fee5312c93ab516d6374e4be5eaceb6e1f2ed4ee5f6a73`  
		Last Modified: Wed, 13 Mar 2024 00:13:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cb7b20405d03c13566fd844482aba9d725be706bf3186b3a481d82d112b87a`  
		Last Modified: Wed, 13 Mar 2024 00:13:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461b577490448d51894b30774a4d49b38d784814db41056fa09dec6afe995be`  
		Last Modified: Wed, 13 Mar 2024 00:14:00 GMT  
		Size: 615.1 MB (615069453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92d59d5ab1a57c78fd919f85c008b7f22dd6bd516566aa0800aded48700e52d`  
		Last Modified: Wed, 13 Mar 2024 00:13:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffac732649f4193ffc501bb8be4b13c492eb793049e174acf5061652d8b8965`  
		Last Modified: Wed, 13 Mar 2024 00:13:08 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97169a0cbdcaaf4786fb0462144034ef249955f7e737228f1dd880475b1722f2`  
		Last Modified: Wed, 13 Mar 2024 00:13:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
