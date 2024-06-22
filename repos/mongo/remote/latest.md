## `mongo:latest`

```console
$ docker pull mongo@sha256:bd38dc3d2895c7434b9b75c86525642efe3d65e4c6aadfe397486d7cc89406f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:7b651890ce6f3ead14e53250d32d8d1f0329faa321d7e178d6e5193c6e2fcc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265516880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b3ba6bed352dc1d776be4a63614c5f39d1b5e284b7515aab0d1646ffc92599`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 May 2024 22:01:34 GMT
ARG RELEASE
# Thu, 23 May 2024 22:01:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 22:01:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 22:01:34 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 23 May 2024 22:01:34 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 23 May 2024 22:01:34 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 May 2024 22:01:34 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_MAJOR=7.0
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_VERSION=7.0.11
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 23 May 2024 22:01:34 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 May 2024 22:01:34 GMT
ENV HOME=/data/db
# Thu, 23 May 2024 22:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 22:01:34 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 23 May 2024 22:01:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f24d0041302a7c0bf7459138b2ed35b7eeef7cba2355b83a6d8088ddc997b9`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfef8821fc6226d0bc344922b4ef14dd84a6c05d27159359a12b845a4df2998`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 1.5 MB (1500765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2b135d9110dce3bbc12911886244fc938c197984c2599a07df46102d4fd1a0`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 1.1 MB (1094590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76154bf34598c7e33d0b21ed9fd726deceb22016abbe63dd91919d70594da21b`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93134489020215d0914960ef5d143295c0186f2eaabf16ddf7d5d94b0bbd16e`  
		Last Modified: Wed, 05 Jun 2024 02:21:38 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1fa78ffcfb0678cf343c2f69625fe6d9285a9c872cb5b9fbbea9ed06391b1d`  
		Last Modified: Wed, 05 Jun 2024 02:21:41 GMT  
		Size: 233.4 MB (233380616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91b3273507c2e1fdd232b09697881d666b9dc9b71164793b9881ce1de4c52bc`  
		Last Modified: Wed, 05 Jun 2024 02:21:38 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:4ec8a4b06b0726e2fcd373b7f3802e0b8531876c0b25c9dceca84be4578e84b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09821ae91f4e4f84acb99b20aeea02f6121836975977b6f34e93a59233498f19`

```dockerfile
```

-	Layers:
	-	`sha256:9690e378086f3e5ae5d690e001383188fb3b45c9a20691043d0fff867c783b9c`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 3.0 MB (3001102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a083280b7900cdd63e9cc5b28b0d543626449bbb3bebc398e6126d2e34f8f3c`  
		Last Modified: Wed, 05 Jun 2024 02:21:37 GMT  
		Size: 27.6 KB (27587 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b77b61b24371a890786159373b18172fac47d52a7bb6a41abef2735fec1660b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257368339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bb8ca2cb4faf3a73f048b635a079000ac0705744d7715b7d7e9c4f2f578ce1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 May 2024 22:01:34 GMT
ARG RELEASE
# Thu, 23 May 2024 22:01:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 22:01:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 22:01:34 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 23 May 2024 22:01:34 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 23 May 2024 22:01:34 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 May 2024 22:01:34 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_MAJOR=7.0
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_VERSION=7.0.11
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 23 May 2024 22:01:34 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 May 2024 22:01:34 GMT
ENV HOME=/data/db
# Thu, 23 May 2024 22:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 22:01:34 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 23 May 2024 22:01:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f33a3006c470fcf35e360ed94e30a65c5fe9f95ce0cf0c9ab2243273d4df519`  
		Last Modified: Wed, 05 Jun 2024 16:22:58 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedf0c2fd07791b0a7c85eaf3c323cc949fdc8675f41c70a6bfff588bab98d26`  
		Last Modified: Wed, 05 Jun 2024 16:22:58 GMT  
		Size: 1.5 MB (1467355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f46cd936f683cfcf794bf655b79598309e782291363b3cab7ec7b3abf637b0`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 1.0 MB (1028907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ec972210ed7a766b75b403456bf7587b4268fa84be43afcccc99ed64e028c0`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ba95ff848c1a743d24ad8a63dd57339dfb46e68a153aebc3e61dc2562c8198`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce2268597823db5b1f109875432d69361eed336dda14d2143b0d3ff5df0dcdd`  
		Last Modified: Wed, 05 Jun 2024 16:24:29 GMT  
		Size: 227.5 MB (227503125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b2690426673c98900ec241412a346b96c12b84ffa846cf0295430292553c6c`  
		Last Modified: Wed, 05 Jun 2024 16:24:24 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:10886ea40c504df8eefe844720edba4c31e284527e5c448775fb2344678286a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3029380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2814160134051b5ebfefede1f97df0253673e3d7c59e42fb98058c7e3f6e4405`

```dockerfile
```

-	Layers:
	-	`sha256:1e1e0731a6d932f8b6c94d6cee08bd69d2f7c025b4c1b3b4d3acd61741a587be`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 3.0 MB (3001444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:053ae8ba3f661051809e8ceb46ea28e4f038e9df5bd4c633cc396ee26a2dab89`  
		Last Modified: Wed, 05 Jun 2024 16:24:23 GMT  
		Size: 27.9 KB (27936 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:f64ec448d8d61b13e1235657217b02b06e0d398b724fa100818a70930791d19a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737451302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbf814e45ab8f3d58d8e13dc2e33d18c94f4a3fa1c71a9c10b183eb65efd518`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Fri, 21 Jun 2024 23:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 21 Jun 2024 23:57:49 GMT
ENV MONGO_VERSION=7.0.11
# Fri, 21 Jun 2024 23:57:49 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.11-signed.msi
# Fri, 21 Jun 2024 23:57:50 GMT
ENV MONGO_DOWNLOAD_SHA256=80e1e9806e02a95c0365509ec3a4e83b8771da09a1c4df9f7d1dfbe4516a07f5
# Fri, 21 Jun 2024 23:58:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 21 Jun 2024 23:58:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 21 Jun 2024 23:58:53 GMT
EXPOSE 27017
# Fri, 21 Jun 2024 23:58:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626f975969eaf93cc62527c4fe329d3d400fd15c5ac8823308fa42153059d17e`  
		Last Modified: Fri, 21 Jun 2024 23:59:01 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3478b71875d3b6bd99d832b94b1fb6a08180de09c61f92b10b555e67e3297f`  
		Last Modified: Fri, 21 Jun 2024 23:59:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5063c6f55cab3de309215f53397c29d7c6dbc5b1cd4a3afe9b322839fccf3`  
		Last Modified: Fri, 21 Jun 2024 23:59:01 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030de6508246f8ed2f65eec99437bbca4e5b2931036ead8950591dca133d73ae`  
		Last Modified: Fri, 21 Jun 2024 23:58:59 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668c22fc5fe7bf8e22bc8a837dd3e8c6e7b98ba1a993582079c71f8849c67c0b`  
		Last Modified: Fri, 21 Jun 2024 23:59:49 GMT  
		Size: 619.3 MB (619251882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7dcc008a0d76ed9611fbb4469296b752e6e6651111be7bd97a390b81367960`  
		Last Modified: Fri, 21 Jun 2024 23:58:59 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de85be255f9ddcddbf07003d364ec02bc30616a9da59042ac32ba5d3bad11d9c`  
		Last Modified: Fri, 21 Jun 2024 23:58:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51434ec730555a658fba1d4e293c96f1acc4cf33400c7cf2c883d8990c0c1a2b`  
		Last Modified: Fri, 21 Jun 2024 23:58:58 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:9c5993594a0b95c6f3b7482d128db6d9fe8d359e4096d49f706340ae29d01b72
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2840056848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069746ca6e5ca1cab6a4d73bf34cbfc36749142b458ce9ab73a0820ffd4acbda`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:12:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:12:38 GMT
ENV MONGO_VERSION=7.0.11
# Wed, 12 Jun 2024 18:12:38 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.11-signed.msi
# Wed, 12 Jun 2024 18:12:39 GMT
ENV MONGO_DOWNLOAD_SHA256=80e1e9806e02a95c0365509ec3a4e83b8771da09a1c4df9f7d1dfbe4516a07f5
# Wed, 12 Jun 2024 18:15:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:15:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jun 2024 18:15:16 GMT
EXPOSE 27017
# Wed, 12 Jun 2024 18:15:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eeda944b1e59ee631ff37afe9229f7dc647c6e816d063a5bacf59c88ce1d276`  
		Last Modified: Wed, 12 Jun 2024 18:15:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d456b62a17a84d4f8a3224068c88b520290f4c36a8b60867def416983f2082`  
		Last Modified: Wed, 12 Jun 2024 18:15:21 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fe44d721820e708630910cfcf25bcc9af8abff2968c1ad59b5b3e5f482266d`  
		Last Modified: Wed, 12 Jun 2024 18:15:21 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6804744b6117f3ddfa362ede394df1fde63b8d816d7b98ee8726c115ba044ee6`  
		Last Modified: Wed, 12 Jun 2024 18:15:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9286690f3b7551208aa124931f97c81df466af93eae21988017dcdfede1adb17`  
		Last Modified: Wed, 12 Jun 2024 18:16:10 GMT  
		Size: 619.4 MB (619366551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982a3253ac8ca5a10d9ad11939bc6db5cdbfd7c5e0ccc77e4f4fcc85b011f385`  
		Last Modified: Wed, 12 Jun 2024 18:15:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf98e6905b7e4c6151e4288bf5ea689a2521e800f2b2625919a46ab278f2f7c0`  
		Last Modified: Wed, 12 Jun 2024 18:15:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63e8c7af8c9ac0d653a551b3431a46eae9238a4c2f898ee278fea559ee17f7`  
		Last Modified: Wed, 12 Jun 2024 18:15:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
