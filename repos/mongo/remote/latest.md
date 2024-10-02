## `mongo:latest`

```console
$ docker pull mongo@sha256:0c17421487ae4a5cae88e7652a26ef72a8162adbc599a0730805526f5ff5ee83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:b07755058fd9ee3478bdef0a2614e51f7b73a91c85e221233444456e4ad9671e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274325363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72576a3db0329e0a60aae2259e2c9e26aff5ee3296a43100cb77e53062fae2db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENV GOSU_VERSION=1.17
# Wed, 18 Sep 2024 22:02:51 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 18 Sep 2024 22:02:51 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_MAJOR=8.0
# Wed, 18 Sep 2024 22:02:51 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_VERSION=8.0.0
# Wed, 18 Sep 2024 22:02:51 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
VOLUME [/data/db /data/configdb]
# Wed, 18 Sep 2024 22:02:51 GMT
ENV HOME=/data/db
# Wed, 18 Sep 2024 22:02:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 22:02:51 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 18 Sep 2024 22:02:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2843f0424c9344edf24ab2b082e0db21487318b0ae337a6454823b3dcc7ec002`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a7a845331184c79fd0b6c2e978d9d9211da333f5cb9a85c280f4a7669a87c`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 1.8 MB (1819214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923fbc5d75e9896b4dde2dc1a6da962d656f88966bb945925dc1df1881fa39a5`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 1.1 MB (1129336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c9b75dcd29b36886e7bced4e2ec1122a4025f7c7ce3688b4606d9508a26e77`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3df91fefa244f2b7c08700a1864a6f84a5349164a9bed97b52128807ecb3f2`  
		Last Modified: Wed, 02 Oct 2024 01:58:54 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d7cdcf0d099dc078c04879f432e3ae704bfecad9e19f02a70b9227cb371216`  
		Last Modified: Wed, 02 Oct 2024 01:58:58 GMT  
		Size: 241.6 MB (241620364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26443d53f1837b2e304d0e1a22296d172190a44f4979bf2fb18e4a7dd849395f`  
		Last Modified: Wed, 02 Oct 2024 01:58:54 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:0462ccb311c105b57b1f038d62694ea681d76a28b407441a910a8681c32b6f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b0f9f9b733ffe95652e2c9f908484bbcc686cda9c42ac3f719924f172b786f`

```dockerfile
```

-	Layers:
	-	`sha256:10d2c2a1b23757434b4525efadbcdb6eac00b1a2f97142f3d5f2545995fe632e`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 2.5 MB (2480732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b59d9e314bcef24b14104fffec77b700563d83ea83e506581f022c5a26323745`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 27.6 KB (27632 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:43cf5020e2aa0267ec342160a79b98403b757ba3efa26f9be48b0bc10c78eb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263603857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba14bdfa6ab04c0645a5b1db40e6bf9ffaab2e847ad046ac4150ad9a772eaadd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENV GOSU_VERSION=1.17
# Wed, 18 Sep 2024 22:02:51 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 18 Sep 2024 22:02:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 18 Sep 2024 22:02:51 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_MAJOR=8.0
# Wed, 18 Sep 2024 22:02:51 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENV MONGO_VERSION=8.0.0
# Wed, 18 Sep 2024 22:02:51 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
VOLUME [/data/db /data/configdb]
# Wed, 18 Sep 2024 22:02:51 GMT
ENV HOME=/data/db
# Wed, 18 Sep 2024 22:02:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 18 Sep 2024 22:02:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Sep 2024 22:02:51 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 18 Sep 2024 22:02:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0c4d5193bdabc1cc1473967db2645224cbad2e95a841621c02c179750a0061`  
		Last Modified: Wed, 02 Oct 2024 03:16:42 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b745a2d75ed5e1081baf2a9b8e3ed414025313a4dc8b07c93b43b4c8794e4d`  
		Last Modified: Wed, 02 Oct 2024 03:16:42 GMT  
		Size: 1.8 MB (1817032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69382d493b48d52426f0ac15b51261019b7e0fd8f186e8a4106c323ea60585e9`  
		Last Modified: Wed, 02 Oct 2024 03:18:11 GMT  
		Size: 1.1 MB (1059590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ff0a1a4e92c458c86eac4702a9da7f1aa880b1bd0e24df632a0d1e6db50cde`  
		Last Modified: Wed, 02 Oct 2024 03:18:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292d57a1df0782b2c3ec64e6aae541ef0903e05ee7f9f2a60ad1365d1d6fa896`  
		Last Modified: Wed, 02 Oct 2024 03:18:11 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6f8dd708478c10bf72cb36437a7c7f175349a291e8bbd7dc5ac53102ccab24`  
		Last Modified: Wed, 02 Oct 2024 03:18:16 GMT  
		Size: 231.8 MB (231835214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cabcda262baac7761e7b502a6d8f923dde9ff68a6d070f61884b9e30e2edeb`  
		Last Modified: Wed, 02 Oct 2024 03:18:11 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:61c85a52a6eed4f1b12e50a9805793b502b49d1f26fa199ca96ad733ce4a4602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3bc44ceddcbd2e1d777aa3a5707f0d2ebffe3edda69ea64b514e904d2caa8f`

```dockerfile
```

-	Layers:
	-	`sha256:5ca9f472d706f11ed8c7f6f8413aea01def21283fdd46945b6d701464b2aa2a6`  
		Last Modified: Wed, 02 Oct 2024 03:18:11 GMT  
		Size: 2.5 MB (2481868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e3da140cf51fd77bc804c1b96bc7ae70b6ecfff48e8f0785a0ed6bc6fb13b7b`  
		Last Modified: Wed, 02 Oct 2024 03:18:10 GMT  
		Size: 27.9 KB (27853 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.20348.2700; amd64

```console
$ docker pull mongo@sha256:7fa429881eb8d35500efb41ccfbf6f3b7fea6440755288db76b3e5d815e5f8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227212387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f1fb75e7c0e04bb4f779d5c953cedc0171dd18435913e6ae1f6cb2fb077293`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 18:57:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 19 Sep 2024 18:57:30 GMT
ENV MONGO_VERSION=8.0.0
# Thu, 19 Sep 2024 18:57:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.0-signed.msi
# Thu, 19 Sep 2024 18:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=778f03552b6638822c18a9a2e8996d31cf12e4c9b87ffc73be8ce71e0a8465e9
# Thu, 19 Sep 2024 19:00:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 19:00:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 19 Sep 2024 19:00:17 GMT
EXPOSE 27017
# Thu, 19 Sep 2024 19:00:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc256b237a6e28c22f04564693f63cfa0f2060260ab54382bb4b656c8e49368`  
		Last Modified: Thu, 19 Sep 2024 19:00:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449d832e3eee20ab426b6c85c9704bd7e621dc6b27bc41040328761d69517a70`  
		Last Modified: Thu, 19 Sep 2024 19:00:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a1fc04a3d3809ee94bb395eec8d781067b83ae5b7d956dd486cbecf5a0910f`  
		Last Modified: Thu, 19 Sep 2024 19:00:21 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1171bb8ab5212218b0ac3be3e5d4fa8e98f0d1a2fa4b16917aa0c7e7014ef0b`  
		Last Modified: Thu, 19 Sep 2024 19:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6408a9294c2da888498c3e5c90c2951be1c9c6c7fb15de86379d95c0478bb696`  
		Last Modified: Thu, 19 Sep 2024 19:01:17 GMT  
		Size: 765.0 MB (765010998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af615893a2fe9ef06c601cc1bc06e47c0c27822d1c122fd780f20f9ca89e539c`  
		Last Modified: Thu, 19 Sep 2024 19:00:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aefb28914c3e0c610f914be046997b5918a67cf2295acc2facb714cb0b88fb9`  
		Last Modified: Thu, 19 Sep 2024 19:00:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae5ac6efc4f7187bc4eb8ffefcc218153c2956f4087f3231642be7967128d2`  
		Last Modified: Thu, 19 Sep 2024 19:00:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.6293; amd64

```console
$ docker pull mongo@sha256:9e43383e6ca1d3be2c128d5670b51977100e8c1ccd84a438fda2b0c603148012
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485285280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c36268ecd0496d2b6679c40c246a11137301cc7d674be17d4b1c3f709729fb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 18:57:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 19 Sep 2024 18:57:22 GMT
ENV MONGO_VERSION=8.0.0
# Thu, 19 Sep 2024 18:57:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.0-signed.msi
# Thu, 19 Sep 2024 18:57:23 GMT
ENV MONGO_DOWNLOAD_SHA256=778f03552b6638822c18a9a2e8996d31cf12e4c9b87ffc73be8ce71e0a8465e9
# Thu, 19 Sep 2024 18:59:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 18:59:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 19 Sep 2024 18:59:18 GMT
EXPOSE 27017
# Thu, 19 Sep 2024 18:59:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdd9502c4b68024084c88d0782929ee759f273a442011b2bcf833b576b6fa4e`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e243d7a17956bf9424e764cc4d3ab4f359cfd3c8643dfa3ac7ce8a0dd76485`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c28e73026a011b1c1e665a2e2f6f4ede28c39beaee51aea83a19cac01bb063`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caddb3e1dbaea7dbd32889ca53f8123d94ce1d02b49d569f5ce0211530f8685`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53023350b6c4c96532a470d5cbe3468d5127c46484dca0358ff81360ee552448`  
		Last Modified: Thu, 19 Sep 2024 19:00:21 GMT  
		Size: 765.0 MB (765007868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f2ec306c60dc1b0e9d515dc0e6cfb63a3b0658ddd93e856d8c8325d2ec1563`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d3324a0b94a41ea65e391cbfb1fa48f604f3baa86f3c0b08175d1b097c8dd5`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1344664231c31c2007cc360a73163229ce210ef226379e6fda9fd10c56b0d2`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
