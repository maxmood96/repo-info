## `mongo:latest`

```console
$ docker pull mongo@sha256:95a98776f273721a295b03098578b06bc10281bb56aa828c77e9f60ecc70b150
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:108c3c1646aa75e8f75361024ae3f90b2ba9d2ad6d442d042bdeb269ef8d15bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295931157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dcc14380635cc7184b14c4839d0e4cbb98ecc1ba92558b531dec565d8772df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 23 Jul 2025 22:01:30 GMT
ARG RELEASE
# Wed, 23 Jul 2025 22:01:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Jul 2025 22:01:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Jul 2025 22:01:30 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Jul 2025 22:01:30 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 23 Jul 2025 22:01:30 GMT
CMD ["/bin/bash"]
# Wed, 23 Jul 2025 22:01:30 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Jul 2025 22:01:30 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 23 Jul 2025 22:01:30 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 23 Jul 2025 22:01:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 23 Jul 2025 22:01:30 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 23 Jul 2025 22:01:30 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 23 Jul 2025 22:01:30 GMT
ENV MONGO_MAJOR=8.0
# Wed, 23 Jul 2025 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
ENV MONGO_VERSION=8.0.12
# Wed, 23 Jul 2025 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
VOLUME [/data/db /data/configdb]
# Wed, 23 Jul 2025 22:01:30 GMT
ENV HOME=/data/db
# Wed, 23 Jul 2025 22:01:30 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 23 Jul 2025 22:01:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Jul 2025 22:01:30 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 23 Jul 2025 22:01:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e701e7c9324a0124dc4823f24c7ddfde225cf284cc1a4152b88a0ed4431c8cb7`  
		Last Modified: Tue, 12 Aug 2025 18:05:57 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1102db351d8ce4cf36dd598fa2876e74a0c8814e9f46fde8f7da29598d1cf51`  
		Last Modified: Tue, 12 Aug 2025 18:05:59 GMT  
		Size: 1.5 MB (1509114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d713d16a80436e61f471b2e3c4b33bbf5bd0b8cf3a1c24bb86813cae6b13b5b6`  
		Last Modified: Tue, 12 Aug 2025 18:06:00 GMT  
		Size: 1.1 MB (1131121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb52df844465653688678819be18831e154979a82f93aca3bea1699f4a74f5eb`  
		Last Modified: Tue, 12 Aug 2025 18:06:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578438e6cda545166661671ecfc24cc00d347012024cf112eb1b041f3f93be8a`  
		Last Modified: Tue, 12 Aug 2025 18:06:02 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a07b2b41243745a63426dfa0a2ec13e851b21cdd3dba0aa06f549f28ee2e598`  
		Last Modified: Tue, 12 Aug 2025 19:08:15 GMT  
		Size: 263.6 MB (263561109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91469349d2c256e9813bd4b9f4ff42b0bfbdb3388115be1b1ae6dcccd9ba016b`  
		Last Modified: Tue, 12 Aug 2025 18:05:56 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:a71d89ae00b65c3d89790ec85015b1bd24c2c4560ee1248a88958a8606ceaa97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a357c75289581583504c155e137b260f5e6ee9601af8945d3d4ef436b81c0350`

```dockerfile
```

-	Layers:
	-	`sha256:fcd5c905ac2ba560858f43a2815024a347f9a1c5803d3d2bdbe50d9874a13723`  
		Last Modified: Tue, 12 Aug 2025 19:08:09 GMT  
		Size: 2.7 MB (2666308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e7f9f139310a270c084095df832c03f7d515daa94008a564a7dc30e291b8b7`  
		Last Modified: Tue, 12 Aug 2025 19:08:10 GMT  
		Size: 28.8 KB (28845 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:52aa5caf8fa42792565bd7d10054aadbedc52c9974212816fc3d95b2086fdd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283898863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94477dcb333ec0d48e8d388ca683fafbd6a3b647b9ee849d9fa898d9789ae7fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 23 Jul 2025 22:01:30 GMT
ARG RELEASE
# Wed, 23 Jul 2025 22:01:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Jul 2025 22:01:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Jul 2025 22:01:30 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Jul 2025 22:01:30 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 23 Jul 2025 22:01:30 GMT
CMD ["/bin/bash"]
# Wed, 23 Jul 2025 22:01:30 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Jul 2025 22:01:30 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 23 Jul 2025 22:01:30 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 23 Jul 2025 22:01:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 23 Jul 2025 22:01:30 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 23 Jul 2025 22:01:30 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 23 Jul 2025 22:01:30 GMT
ENV MONGO_MAJOR=8.0
# Wed, 23 Jul 2025 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
ENV MONGO_VERSION=8.0.12
# Wed, 23 Jul 2025 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
VOLUME [/data/db /data/configdb]
# Wed, 23 Jul 2025 22:01:30 GMT
ENV HOME=/data/db
# Wed, 23 Jul 2025 22:01:30 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 23 Jul 2025 22:01:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 23 Jul 2025 22:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Jul 2025 22:01:30 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 23 Jul 2025 22:01:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770deb42eab21b27bbb55cc4cf29322634354ac2d2aa894794837b4011cbd98e`  
		Last Modified: Tue, 12 Aug 2025 20:28:10 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c37b4f106e3f27dfb0117d7f1f102aa507166042a05403fbab1e8b11c56e019`  
		Last Modified: Tue, 12 Aug 2025 20:28:16 GMT  
		Size: 1.5 MB (1494192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14af82ae345a340900c1587be538f9b72898fec7c154b2b2f4350c413fe5f1fd`  
		Last Modified: Tue, 12 Aug 2025 20:28:15 GMT  
		Size: 1.1 MB (1061482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b52914487467c91827ca1bfefe91cf07e18c8868adefc001f3ea87f193cab1`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2de875d5692997b1b716526fce081e00d4d60b2d7e819d0a7821fe96d3af560`  
		Last Modified: Tue, 12 Aug 2025 20:28:15 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c5eb12939de42adae87d00c3820d375078f1c825caff7c825a4146a8fce1e`  
		Last Modified: Tue, 12 Aug 2025 20:48:36 GMT  
		Size: 252.5 MB (252476210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4891da281115109e76136851d45005db441dc9fddcceecc7bf7c3ed4c0907529`  
		Last Modified: Tue, 12 Aug 2025 20:28:15 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:1c23ee132fc2bfd27dc76caf3f045f0792a45dc0db1de92501b429ecd0c9f113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362147e9edea62fc9949594215a00270939e8e048f884eede4ed49a72fb55a30`

```dockerfile
```

-	Layers:
	-	`sha256:ad358d188cefbfb622b888fa9cba9057a3140c2e1636ece25088fe04edf64a2e`  
		Last Modified: Tue, 12 Aug 2025 22:08:55 GMT  
		Size: 2.7 MB (2667444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70847f99aa901698f6de062df68a8b9b9be3aed6d58a54ca3b94d8b40afdb2c7`  
		Last Modified: Tue, 12 Aug 2025 22:08:55 GMT  
		Size: 29.1 KB (29072 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.4946; amd64

```console
$ docker pull mongo@sha256:9559700aa5023d07104d2d75dafc7c566cd7eb048618a1c128d864e3dd7c43c1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 GB (4276638366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85353faeaa4db214a5c390f901fb3897aaf7ab2efdc9836114b2b03e99b5f923`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:59 GMT
ENV MONGO_VERSION=8.0.12
# Tue, 12 Aug 2025 20:28:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.12-signed.msi
# Tue, 12 Aug 2025 20:28:00 GMT
ENV MONGO_DOWNLOAD_SHA256=19d8820364f55dfde5724b2d99520be8aadb62d15486a71295457ff071565d80
# Tue, 12 Aug 2025 20:29:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:29:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 Aug 2025 20:29:01 GMT
EXPOSE 27017
# Tue, 12 Aug 2025 20:29:01 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f3c18358d440940935dae03d80a368bb02a6119703702b547e204ae36c27de`  
		Last Modified: Tue, 12 Aug 2025 20:56:46 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa149a3e25d7c087c46afb7ee19527b7ee779218b193f3cdafdeed8d4b5e878`  
		Last Modified: Tue, 12 Aug 2025 20:56:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16894e7775d0a35ed307a9ab6bfefcd3024f1d52823fdc23484182158f632637`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4cc0084928bc6300be0b4aba74ecdfa5807b70420b64b3c5bd3d7ced0d2249`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036f82926034406f23fa96ef6f2dbd1d93b4526d1d90b64d11a0bc68e80b7a4c`  
		Last Modified: Tue, 12 Aug 2025 22:10:03 GMT  
		Size: 777.8 MB (777798694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267346b8dbdf8c7445884a8e1ed23c828a22eb0081858392c09cb8bda5fff50b`  
		Last Modified: Tue, 12 Aug 2025 20:56:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbf2542c25e605c70d304cadf9bcaedb29335a25ab53bac5631418f5f487bc4`  
		Last Modified: Tue, 12 Aug 2025 20:57:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ccaf0ff385a09da18f6a5e9424312ca4a11e30397e6693bcb005f05d1e551b`  
		Last Modified: Tue, 12 Aug 2025 20:57:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.4052; amd64

```console
$ docker pull mongo@sha256:8036c766cb5e63777a8bc8a37dc00309ea7a44f7d13c14c3d1e0aa05376ec0a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3059536716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ea3e6b7f695600bb28c794c1b19f4a138c20648e01d9538f3c02ceee41eb24`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:27:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:22 GMT
ENV MONGO_VERSION=8.0.12
# Tue, 12 Aug 2025 20:27:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.12-signed.msi
# Tue, 12 Aug 2025 20:27:24 GMT
ENV MONGO_DOWNLOAD_SHA256=19d8820364f55dfde5724b2d99520be8aadb62d15486a71295457ff071565d80
# Tue, 12 Aug 2025 20:28:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:28:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 Aug 2025 20:28:34 GMT
EXPOSE 27017
# Tue, 12 Aug 2025 20:28:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4535cb6567046f6692dd2ddb6e91a32b70370f5732e7cb7bdf6cf698ac6573c7`  
		Last Modified: Tue, 12 Aug 2025 20:30:11 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fee7bb3c3e8b641d8dc88237b0f370188d595b2617ad35654bb263e8e1f869f`  
		Last Modified: Tue, 12 Aug 2025 20:30:10 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51be72a6173875ab91192e4b7992fa2e06b2fba88115393408335a5c18926eb7`  
		Last Modified: Tue, 12 Aug 2025 20:30:10 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4380aeb953ae1e8abd721eb16328f2a962254b6e7873ca9ef4fb82311af0b91`  
		Last Modified: Tue, 12 Aug 2025 20:30:02 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4d07a5cfa1f25f486ff5c28726e73e6f432f398f87c36469d0eb235290e98d`  
		Last Modified: Tue, 12 Aug 2025 20:45:31 GMT  
		Size: 777.8 MB (777835516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c23f55f453346fb227106c4263761fd8016aaf0f73b8dfa31af0e3637f518ef`  
		Last Modified: Tue, 12 Aug 2025 20:30:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92edad597286f386feb17c0dd3eba9cace21a996dab8c4bca0d8583b3b97741c`  
		Last Modified: Tue, 12 Aug 2025 20:30:02 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0f899b7f265c367aea22006826848401ecbdaeee2e9cff6a8ca7799ae5691a`  
		Last Modified: Tue, 12 Aug 2025 20:30:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
