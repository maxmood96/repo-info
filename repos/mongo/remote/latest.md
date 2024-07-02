## `mongo:latest`

```console
$ docker pull mongo@sha256:d6bd5e1840b6cddcaecc7fd05a12cb6393c2ff18179bb003d151af8fdc9db2a8
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
$ docker pull mongo@sha256:3d592fc4805168a80600d0a2300344e4e1bbe2c18226a52d2e2645de777314fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257711695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1f209b12c1d2acfac2c4d063c093a39499e8db44475073cb7ab427b09012d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab0f54223e2f06694e8a32dd2a1455a1aad475c9840691a4c63598717de3e79`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a724e63221774b2fcd311f891451a83234f1132255c0cb67f896c6003002374`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 1.5 MB (1467365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901e602b71c88a0922aa0afe1382749fb3c4070e0c79651cac9fe65d6778ad4e`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 1.0 MB (1028915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c63a2c02eae273a52a4d55f6fa7b0d982f706f8f99e71cd69bf99945b6428`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858880bdbb3411d7854f42b9def8ad3f8ff990b580c831a982fb1ba42bb52150`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2386ab574158b740092de2f7a3fa9286ec1111fa7f54cb7661b17516f38ba70`  
		Last Modified: Fri, 28 Jun 2024 23:56:11 GMT  
		Size: 227.8 MB (227846475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c55327c92fc01d00693b43ee151a7b735c7b67149495b6e9cca2dbf13d091c8`  
		Last Modified: Fri, 28 Jun 2024 23:56:06 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:464a52b01648022052c0b917a7a03c504496029287b7ba963fb1c4287b1089a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3031553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a39d4eb9f91a7bf46e2bb2d3a3c00460fdf6c7189ce0b9e2045366214d68273`

```dockerfile
```

-	Layers:
	-	`sha256:8b00a0877469065b0f5a0266a5d333f8fc6ab0d47e5889be23860bccb215632b`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 3.0 MB (3003568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64bfae95b8bb5944c06f8ccf6dabff2197934b09c61b6929d761c351dc295e05`  
		Last Modified: Fri, 28 Jun 2024 23:56:05 GMT  
		Size: 28.0 KB (27985 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:77092b64be37f3b0b2892a11c4e70281578a829c79172dc497a1f12eca1528ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726989821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f9107bad946e6707f68e19347432e7f9a3f34ba715d2bca77ea11720cb9b7a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Fri, 28 Jun 2024 23:55:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 28 Jun 2024 23:55:24 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 23:55:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Fri, 28 Jun 2024 23:55:25 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Fri, 28 Jun 2024 23:57:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 28 Jun 2024 23:57:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 28 Jun 2024 23:57:58 GMT
EXPOSE 27017
# Fri, 28 Jun 2024 23:57:59 GMT
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
	-	`sha256:dd61208c16770e7b6f1086224d285df9a3d1bab3aed447de9e1841323d15fcf5`  
		Last Modified: Fri, 28 Jun 2024 23:58:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031a00c2645e9ff89d47241865b6b7778dc668b8e624e4c744000f5e0576190b`  
		Last Modified: Fri, 28 Jun 2024 23:58:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459ea13c8c965953637da85b0925c1b54941e60c3a6c859734e26351a1f7add`  
		Last Modified: Fri, 28 Jun 2024 23:58:02 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8306ad4975d367ff5d8cf1a2428fe9f3319e2d461aa7f12cd5aeccc35b6136c3`  
		Last Modified: Fri, 28 Jun 2024 23:58:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e99d8e789fede49ecf83c637d8065a9037f74d9286add5b654e658c41fe8c0c`  
		Last Modified: Fri, 28 Jun 2024 23:58:47 GMT  
		Size: 608.8 MB (608790545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a143d11fa7ed8bb9e89c28e4cdbc0064e5e69388ecaf8c5be628163e0718aca8`  
		Last Modified: Fri, 28 Jun 2024 23:58:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addc4658fc847cc75ef5ac76127b69d9c54c86a97d93c97f12fcca2cbc163a44`  
		Last Modified: Fri, 28 Jun 2024 23:58:01 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf82acf494a704f558c328bd607ea32faebbfd89079c2c4f117c58d11b7539e`  
		Last Modified: Fri, 28 Jun 2024 23:58:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:dd85cab6304c859a1f3cf4abfb6db529eb5673074fa2a9c4d139495fa21f5bc4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2829632641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4159ebc29a28c284d8cdbdccb1ab50c906be9868de42c920de637960d2064e92`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Fri, 28 Jun 2024 23:55:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 28 Jun 2024 23:55:17 GMT
ENV MONGO_VERSION=7.0.12
# Fri, 28 Jun 2024 23:55:17 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Fri, 28 Jun 2024 23:55:18 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Fri, 28 Jun 2024 23:58:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 28 Jun 2024 23:58:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 28 Jun 2024 23:58:27 GMT
EXPOSE 27017
# Fri, 28 Jun 2024 23:58:28 GMT
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
	-	`sha256:9a92aacc9f51ed7a59d66a611cef7bda8617d7cc761d89ab1e9c89b410c61a92`  
		Last Modified: Fri, 28 Jun 2024 23:58:31 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63f9f1cbd84670e9caf6a387e356fe324c705b811e2e390623904d66dd7b594`  
		Last Modified: Fri, 28 Jun 2024 23:58:31 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994df02ea50779784cbd775a9b5fbeff1732c4c9bea436bac2210057f1dd96f5`  
		Last Modified: Fri, 28 Jun 2024 23:58:32 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e402124f634bc0554258042bfc8a65d71901bdc716376522f51deca8c47b12c4`  
		Last Modified: Fri, 28 Jun 2024 23:58:30 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5365be088357d7a26961dee5e3b86fe62af0a3ba6ff68a30d8bbfb04bcb450ac`  
		Last Modified: Fri, 28 Jun 2024 23:59:17 GMT  
		Size: 608.9 MB (608942369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcf702b18dc66be12ef3d759932934431590cb15b91cb978aafda1827ea8df3`  
		Last Modified: Fri, 28 Jun 2024 23:58:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e85609069fc0d27983ce8cd12c3df256bc516272aa90c225abbb93d5382bd8`  
		Last Modified: Fri, 28 Jun 2024 23:58:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41328de76efdf9a8bcec7cf8e6004eb1ed8c5fd90d15eb388e1210a89f89add`  
		Last Modified: Fri, 28 Jun 2024 23:58:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
