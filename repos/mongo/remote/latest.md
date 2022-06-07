## `mongo:latest`

```console
$ docker pull mongo@sha256:94cd91589ff66a7cc7eb6f794f254522c1587457d46f94e0cb1c460e73498255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.707; amd64
	-	windows version 10.0.17763.2928; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:f548240f5a61d1ecfe4c16cc73c8a12c1701bf9d47d0121f110dd5655ebefd55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245306167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3f6d5230f67503df7a474bc704166b0fb52792ed4d054f95297541778f30f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:32:20 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 07 Jun 2022 00:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:32:28 GMT
ENV GOSU_VERSION=1.12
# Tue, 07 Jun 2022 00:32:28 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 07 Jun 2022 00:32:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 07 Jun 2022 00:32:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Jun 2022 00:32:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Tue, 07 Jun 2022 00:32:45 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 07 Jun 2022 00:32:45 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 07 Jun 2022 00:32:45 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 07 Jun 2022 00:32:45 GMT
ENV MONGO_MAJOR=5.0
# Tue, 07 Jun 2022 00:32:46 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 07 Jun 2022 00:32:46 GMT
ENV MONGO_VERSION=5.0.9
# Tue, 07 Jun 2022 00:33:10 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 07 Jun 2022 00:33:12 GMT
VOLUME [/data/db /data/configdb]
# Tue, 07 Jun 2022 00:33:12 GMT
ENV HOME=/data/db
# Tue, 07 Jun 2022 00:33:12 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Tue, 07 Jun 2022 00:33:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:33:12 GMT
EXPOSE 27017
# Tue, 07 Jun 2022 00:33:13 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ef66a8492a7b4b656a9dddda9f1bfa3bd3213773c8449b68dadac55605c96f`  
		Last Modified: Tue, 07 Jun 2022 00:34:56 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cec14c8f9e0886403900a1569d2a6a4c33fa3b3984d7dc128eb71c437fe06d`  
		Last Modified: Tue, 07 Jun 2022 00:34:57 GMT  
		Size: 3.1 MB (3064245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c3018eb09a584362cfe9d340566fb755597b453ea58bf5c6c15c8e120efe44`  
		Last Modified: Tue, 07 Jun 2022 00:34:57 GMT  
		Size: 6.5 MB (6506121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc9e1c2556b202042e54ddafe2ae992d58cd462bd3a75ab2c55ccbc42c76dc9`  
		Last Modified: Tue, 07 Jun 2022 00:34:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c62d035322149352916a5f076138bc992cb1decf2017ac0143221c8d5afe2`  
		Last Modified: Tue, 07 Jun 2022 00:34:53 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a103a446c3f38697e880d478313e8128e54f3245c42f9e4e047d2f94476bfd0`  
		Last Modified: Tue, 07 Jun 2022 00:34:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6085016f3a0c6b14cdd29d6287e1745c48e6d43332da6be34795c6b8beb607`  
		Last Modified: Tue, 07 Jun 2022 00:35:22 GMT  
		Size: 207.2 MB (207154539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8109db46fca75b5f8e57f37f43d411a16dd24993d858e7153e451bd252bafa`  
		Last Modified: Tue, 07 Jun 2022 00:34:53 GMT  
		Size: 4.9 KB (4945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0ee764d498848174efae8b85289e71adaae5185463b9b8a7a65ebeb51d5cdb2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237800304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139e6a541a7923c8df93a81f527101c4dfe414cc8d6b22f9361218112d15d2a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Mon, 23 May 2022 23:58:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 23 May 2022 23:58:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2022 23:58:47 GMT
ENV GOSU_VERSION=1.12
# Mon, 23 May 2022 23:58:48 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 23 May 2022 23:59:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 23 May 2022 23:59:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 23 May 2022 23:59:08 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Mon, 23 May 2022 23:59:09 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 23 May 2022 23:59:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 23 May 2022 23:59:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 23 May 2022 23:59:12 GMT
ENV MONGO_MAJOR=5.0
# Mon, 23 May 2022 23:59:13 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 02 Jun 2022 18:00:35 GMT
ENV MONGO_VERSION=5.0.9
# Thu, 02 Jun 2022 18:00:59 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 02 Jun 2022 18:01:00 GMT
VOLUME [/data/db /data/configdb]
# Thu, 02 Jun 2022 18:01:00 GMT
ENV HOME=/data/db
# Thu, 02 Jun 2022 18:01:02 GMT
COPY file:ff519c7454e20e6f14c42932b8d6eaee066ed739bfbbd2a6e884d0a7ffeead38 in /usr/local/bin/ 
# Thu, 02 Jun 2022 18:01:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Jun 2022 18:01:03 GMT
EXPOSE 27017
# Thu, 02 Jun 2022 18:01:04 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0512bdaae73cf7907a5372e174d29934ef3d58b8c419189a40baf81b04f43a`  
		Last Modified: Tue, 24 May 2022 00:03:41 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51571d358e429281c0e3ed2ed7f53f21567aef6fe7532e2ec0b188209e61c8ca`  
		Last Modified: Tue, 24 May 2022 00:03:42 GMT  
		Size: 2.9 MB (2911511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa226bdd983047c6f94630a29b97dfac6379c6aab11572a84d338b40ae3635f6`  
		Last Modified: Tue, 24 May 2022 00:03:43 GMT  
		Size: 6.2 MB (6248132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0e3e44d3aceb5be4f15cafd160b7d54476229cb3d006f27cda634aef64be5e`  
		Last Modified: Tue, 24 May 2022 00:03:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106719865e3d888303573607c0a3e28219aa7b352067276bfb931eec1c45686`  
		Last Modified: Tue, 24 May 2022 00:03:39 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600ad43e7428f314f08b962d6543e2f4facea799bd703f6b6a383a19669bfef6`  
		Last Modified: Tue, 24 May 2022 00:03:39 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943041bc9b737c9be25a9769179bb1a62422adda25ff26541fd90416dc7c20f2`  
		Last Modified: Thu, 02 Jun 2022 18:02:34 GMT  
		Size: 201.5 MB (201462770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c0dd8839074bb1a604367fe8df3d162750e7f8814457531230766bcf15891b`  
		Last Modified: Thu, 02 Jun 2022 18:02:08 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.707; amd64

```console
$ docker pull mongo@sha256:f08802d4acc1f73f153cac588a57f3190dc6e502b493861d063ea7c6a7264414
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2544945709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31df9ead91400f87b9b851bf148cd0e0fd5f38ed3ed549988028f1e7982e8ab4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Wed, 11 May 2022 12:34:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 02 Jun 2022 18:28:05 GMT
ENV MONGO_VERSION=5.0.9
# Thu, 02 Jun 2022 18:28:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.9-signed.msi
# Thu, 02 Jun 2022 18:28:07 GMT
ENV MONGO_DOWNLOAD_SHA256=0e8032c352253173e9d1683ac7b39c79a4eaed0682e8c0655ca0b3ebd6b11d74
# Thu, 02 Jun 2022 18:29:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 02 Jun 2022 18:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 02 Jun 2022 18:29:38 GMT
EXPOSE 27017
# Thu, 02 Jun 2022 18:29:39 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:52d280e9bf32da92b07a144022b757d7e39ac8039e166551ad32f8ee416bb55f`  
		Last Modified: Wed, 11 May 2022 14:06:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c0f0504bdcc7d14695ec71affd0ac13439dc4adc306b60c45538c694ef61cf`  
		Last Modified: Thu, 02 Jun 2022 18:37:00 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5c77de9d2465724d32abbce6b880ad7d389b8b2efe935a9b81b11047c2882e`  
		Last Modified: Thu, 02 Jun 2022 18:37:00 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1150524d75bcc937dd61ca154d9e217ac5429337aecb4947e066d75c308851ec`  
		Last Modified: Thu, 02 Jun 2022 18:36:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e77b31619d8ab0ba8045fd24c02e5b0a5fbe4a7d1e7a73d951f6c05e0a05fc`  
		Last Modified: Thu, 02 Jun 2022 18:42:25 GMT  
		Size: 307.4 MB (307400603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c1a54ada8b1ac7df4df3db1987fb17080a0f8557482502194990b49c09421c`  
		Last Modified: Thu, 02 Jun 2022 18:36:58 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f88c8f5eeab5df5e780cbbd9b122374326c07c11195d556776c1b537276280`  
		Last Modified: Thu, 02 Jun 2022 18:36:58 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f2b9ca35f4b5dfcaa5ed1f56d8a4122e7549cd62e4c9b5f8c1d815cc0b8e9d`  
		Last Modified: Thu, 02 Jun 2022 18:36:58 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.2928; amd64

```console
$ docker pull mongo@sha256:f5314a98f9b2abf45c5d0e66109dc7d5132f19a0ef707608a14f37fa419c07c7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2811380540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731fd22444d0d651b0bda4a2a858f2d132df3d3dd2c1418cbeff4775ba841b30`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 02 Jun 2022 18:29:47 GMT
ENV MONGO_VERSION=5.0.9
# Thu, 02 Jun 2022 18:29:49 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.9-signed.msi
# Thu, 02 Jun 2022 18:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=0e8032c352253173e9d1683ac7b39c79a4eaed0682e8c0655ca0b3ebd6b11d74
# Thu, 02 Jun 2022 18:31:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 02 Jun 2022 18:31:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 02 Jun 2022 18:31:57 GMT
EXPOSE 27017
# Thu, 02 Jun 2022 18:31:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25af2be13e0b425b1ab63d2f9bb381390bcfc2596383b2e16713ebf2a1fd30be`  
		Last Modified: Thu, 02 Jun 2022 18:42:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd685396f479c961130078fa61a9b0641d89ecdf9a1de4f4bf7b59b7ea45e2f9`  
		Last Modified: Thu, 02 Jun 2022 18:42:46 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092e8c3b76716c39e2e0918bcd60337757f72fa9be1e5b4089edb012fedb6934`  
		Last Modified: Thu, 02 Jun 2022 18:42:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b5892d41d9f4320bd09865818751271bc1e6cf894c51faf1eb9cb64c12f35f`  
		Last Modified: Thu, 02 Jun 2022 18:48:13 GMT  
		Size: 307.3 MB (307314841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f1dcc78a9ea8b74096eb4e5a145c0a7ad9e8c620f421251aab48f9bc72443e`  
		Last Modified: Thu, 02 Jun 2022 18:42:43 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e56b378fc81a6f3f26351d7a96b07ee8b81eddff5c2b4a245569fbd30ec9dc3`  
		Last Modified: Thu, 02 Jun 2022 18:42:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a89ed2188e369be934d0616b7f79ccb18750405d0e822e459bcf048881ecd5`  
		Last Modified: Thu, 02 Jun 2022 18:42:43 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
