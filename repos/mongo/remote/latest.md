## `mongo:latest`

```console
$ docker pull mongo@sha256:5505a38a8c6044ace154376dfe4c94ac85f01c22585547efdd9483c4922dfa37
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
$ docker pull mongo@sha256:655bf6f8d962f008d00b31cf75634b529f72701acc652ba0b45cf99fd5303851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262224912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4debd652389d87df781cd0da313bef78f90ed1dca45f3409b58364503e32d0`
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
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Apr 2024 16:02:10 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_MAJOR=7.0
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
VOLUME [/data/db /data/configdb]
# Wed, 03 Apr 2024 16:02:10 GMT
ENV HOME=/data/db
# Wed, 03 Apr 2024 16:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Apr 2024 16:02:10 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 03 Apr 2024 16:02:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9fc3f4b6e2b228fce2f21406cb0138cc1c0e55455ab5835530249cf828cf46`  
		Last Modified: Wed, 03 Apr 2024 20:51:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7f3ab58bb1c13ba4b34967e87c4a1e1fbb4eaec0ed0c4d052c9617586cb859`  
		Last Modified: Wed, 03 Apr 2024 20:51:34 GMT  
		Size: 1.5 MB (1500351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d33d2943ba1ba716cecdc61d15c75610907682efec6a1306dfbbec21f3b38d`  
		Last Modified: Wed, 03 Apr 2024 20:51:34 GMT  
		Size: 1.1 MB (1094187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72665428d050d4486b678464ca2431ad72b46ff829cb68bca682b3e8f587fa6e`  
		Last Modified: Wed, 03 Apr 2024 20:51:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d2ccdf8e0a9e51092a8f860a64fe34dae149bb21e2d3cef7afa059563e7042`  
		Last Modified: Wed, 03 Apr 2024 20:51:35 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caa80570a18827f64180d0060e3a8524d4e58ac5c5be0a6189f23542be2a31d`  
		Last Modified: Wed, 03 Apr 2024 20:51:38 GMT  
		Size: 230.1 MB (230084253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24ae4ef8206e377695b7d95e4d6dfc0b9264ad5977b18ab82a7fbe56a697c65`  
		Last Modified: Wed, 03 Apr 2024 20:51:35 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:b6a2f92217b348ffbbcc3e9433e75f2a064c7e91ad8c887a186f9723344e42f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48351e09668a6cbf4234367bb21c764be430a5f1ab769a978e9b17ff8ab31a0`

```dockerfile
```

-	Layers:
	-	`sha256:3f3c3166f8f66026f4b166ba53907d108bbd3f5642107d665111be3967598bd8`  
		Last Modified: Wed, 03 Apr 2024 20:51:34 GMT  
		Size: 3.0 MB (3001013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc77db970580e4198cbfcddd04993b8be89958cdeb023c5ead66d09c0b40bcff`  
		Last Modified: Wed, 03 Apr 2024 20:51:34 GMT  
		Size: 27.7 KB (27735 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d21bcd02f2c5f50b862436ebb55c8c07f1782b4e6cb909ba87b0dbee72293217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254038304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372eb238b2a053d7bd28d06b67544050d4bd99a8a5f29553e8bc4547472c1039`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Apr 2024 16:02:10 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_MAJOR=7.0
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
VOLUME [/data/db /data/configdb]
# Wed, 03 Apr 2024 16:02:10 GMT
ENV HOME=/data/db
# Wed, 03 Apr 2024 16:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Apr 2024 16:02:10 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 03 Apr 2024 16:02:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52b73deb9edc3115af86e72d5e6b01b7580448fe8f2bad37252f1c6d6e47fab`  
		Last Modified: Tue, 19 Mar 2024 23:51:02 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310f328ae06be202e6c074df5e8ccf467ef34a7167b47f0d408d0ea70b6a44`  
		Last Modified: Tue, 19 Mar 2024 23:51:03 GMT  
		Size: 1.5 MB (1465416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6688fa40c23ff36e90f3fc306fbd3b7a6c9ab594bef76fd7b2a7b95b73202df`  
		Last Modified: Tue, 19 Mar 2024 23:51:03 GMT  
		Size: 1.0 MB (1026959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed5465e8998f674efa29cb64907336cd6669dc7c8468953e3d2b59cabf59a7e`  
		Last Modified: Tue, 19 Mar 2024 23:51:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaefe376ac3e126cd19d0b24976dcceb6f13ce301e1ed1029a293f44152c5983`  
		Last Modified: Tue, 19 Mar 2024 23:51:04 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd67cbaf0950c8a8192b42f1d3bad362b58d0fac767e58bae988f0cf0a62368`  
		Last Modified: Wed, 03 Apr 2024 20:59:46 GMT  
		Size: 224.2 MB (224180046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dbc7944e9af83852ad093fce6890e0574eca59af4f7ad7ddab55f723fa361a`  
		Last Modified: Wed, 03 Apr 2024 20:59:40 GMT  
		Size: 5.0 KB (4992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:1c1a761dbab4cbeb7c7dbae9752fc02ddb9e557648a08bbe692a35717300927b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1235223d2819f4775b0f2f285bc77019fb91557fe0917e1d77e0db0b08e7d7`

```dockerfile
```

-	Layers:
	-	`sha256:9e71c61c72eacebc24f2bb170cb9c0081afa1c4f6c75c5d2329ca9df5683030c`  
		Last Modified: Wed, 03 Apr 2024 20:59:41 GMT  
		Size: 3.0 MB (3001270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18dd4f1f79ae2953f56a4c5469da97744f4feddcba8693fc39d4fd9bd08f7205`  
		Last Modified: Wed, 03 Apr 2024 20:59:40 GMT  
		Size: 27.6 KB (27592 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:fdc6a0fcd9a88fbba815f88e0215dc76a4261dc9db2eeac728927d54766d29dc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2575271386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45bd006bceeb7043bbcc9af8c3ed2ab8c6a4ee991871f46a9720bfdcbf759a0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 03 Apr 2024 20:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 03 Apr 2024 20:50:59 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 20:51:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.8-signed.msi
# Wed, 03 Apr 2024 20:51:00 GMT
ENV MONGO_DOWNLOAD_SHA256=30b8b6a96c5887a49e671ba72a7995279be7f232a666acd6717a59f7c68295f3
# Wed, 03 Apr 2024 20:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 20:53:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 03 Apr 2024 20:53:58 GMT
EXPOSE 27017
# Wed, 03 Apr 2024 20:53:59 GMT
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
	-	`sha256:21fe8c3ef5dccf9800806f8d1d87830423bc307fff4e627cb559d0484193df53`  
		Last Modified: Wed, 03 Apr 2024 20:54:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e092c7571913f13aec1194969aee04dadff963062f701d6116ad8d4e0e483f`  
		Last Modified: Wed, 03 Apr 2024 20:54:03 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c9c15d7e0ab1082478292cf30e74f6571da8a69162c4cc6bc0602b09011673`  
		Last Modified: Wed, 03 Apr 2024 20:54:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c98984540c816dea737902e6aeed9239f35110f142be39804f76ca9b99ddb2`  
		Last Modified: Wed, 03 Apr 2024 20:54:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54358aa94e42a912d0c3b869eec605b696a279c761d1dcfdce0e2a836afe8e73`  
		Last Modified: Wed, 03 Apr 2024 20:54:50 GMT  
		Size: 617.8 MB (617803326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6fab670b98dd35c8b1d342ddc7d805ac7419afcd4931abac175ea563caa8d5`  
		Last Modified: Wed, 03 Apr 2024 20:54:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ce08824d37fa9b3e26429c6c5895515068449816b46d9ab35627fac8914f4e`  
		Last Modified: Wed, 03 Apr 2024 20:54:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb84c6b69455ef0a02b98f17a73859922fe85893e032dfcc02bd5fc826a888ce`  
		Last Modified: Wed, 03 Apr 2024 20:54:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:c733e3f586805b743de93415751d05476cf4774d7920a2410b0b3f3d75e4acb7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742931240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f91f8f54005112d08501e8ab5a1fa92bf20c6672feb1bf4316eb0c2948fa984`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 03 Apr 2024 20:50:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 03 Apr 2024 20:50:42 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 20:50:43 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.8-signed.msi
# Wed, 03 Apr 2024 20:50:43 GMT
ENV MONGO_DOWNLOAD_SHA256=30b8b6a96c5887a49e671ba72a7995279be7f232a666acd6717a59f7c68295f3
# Wed, 03 Apr 2024 20:53:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 20:53:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 03 Apr 2024 20:53:41 GMT
EXPOSE 27017
# Wed, 03 Apr 2024 20:53:42 GMT
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
	-	`sha256:eb384dd8863bb8e53edc5f1eb3d055fbf49fa9ee7622e6810e6cade5f0e9cd71`  
		Last Modified: Wed, 03 Apr 2024 20:53:49 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac0c2616d487e053941cad8127cba515be05e6f18910cfcd3f30d2b6179e267`  
		Last Modified: Wed, 03 Apr 2024 20:53:48 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c2ae6268c784e84ba943eaa7db3855dda12e7f9d95f42a32eaabef3824d755`  
		Last Modified: Wed, 03 Apr 2024 20:53:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0747ad2e967ed5093458c8932cb60eb63a10e2766d8a07f34d39d17c48b770af`  
		Last Modified: Wed, 03 Apr 2024 20:53:47 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65637511f404d3f40e02fd43da6a37d09582671d447febfa8fc10730d6b8190f`  
		Last Modified: Wed, 03 Apr 2024 20:54:35 GMT  
		Size: 617.8 MB (617822220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b33ecd0b48db67ded84b873323913fccda83011b0c34fc4e066f6ea083f6b1e`  
		Last Modified: Wed, 03 Apr 2024 20:53:46 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a56aae43123da1756386320c375245ef1493f70ab480a390ae020c87fcfc57`  
		Last Modified: Wed, 03 Apr 2024 20:53:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34481543ba043e652772ba34870cb002fcc6ba96c6c2faf5fd2f117efb15c45c`  
		Last Modified: Wed, 03 Apr 2024 20:53:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
