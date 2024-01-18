## `mongo:latest`

```console
$ docker pull mongo@sha256:192e2724093257a7db12db6cbafd92e3e5d51937f13846d49ea555cea85787ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:61ac9ef01392b2456212965eb36564a9500f22d00e19bfe13f80382155f329f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260100649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee26c8012dae78cacf5c81a2fc459263f9c952cc69644bf6fdd218eaba85485`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 06 Jan 2024 05:07:23 GMT
ARG RELEASE
# Sat, 06 Jan 2024 05:07:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 06 Jan 2024 05:07:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 06 Jan 2024 05:07:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 06 Jan 2024 05:07:23 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Sat, 06 Jan 2024 05:07:23 GMT
CMD ["/bin/bash"]
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV GOSU_VERSION=1.16
# Sat, 06 Jan 2024 05:07:23 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_MAJOR=7.0
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_VERSION=7.0.5
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
VOLUME [/data/db /data/configdb]
# Sat, 06 Jan 2024 05:07:23 GMT
ENV HOME=/data/db
# Sat, 06 Jan 2024 05:07:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jan 2024 05:07:23 GMT
EXPOSE map[27017/tcp:{}]
# Sat, 06 Jan 2024 05:07:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:29202e855b2021a2d7f92800619ed5f5e8ac402e267cfbb3d29a791feb13c1ee`  
		Last Modified: Thu, 11 Jan 2024 17:48:58 GMT  
		Size: 29.5 MB (29546295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7513301b17d707b2712858ea235b7cb644e763aba3502ede146b4530cd539be8`  
		Last Modified: Wed, 17 Jan 2024 03:48:46 GMT  
		Size: 1.8 KB (1779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8584f3ef30488c3659e70547d39f970c24f7af2c27c384cc77a05688b4021aec`  
		Last Modified: Wed, 17 Jan 2024 03:48:50 GMT  
		Size: 5.0 MB (5049507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7464f50635759ce2374c44fff3c033ed21e69b1994c5f72784638046b09fa7`  
		Last Modified: Wed, 17 Jan 2024 03:48:50 GMT  
		Size: 1.1 MB (1101009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ff633f781cb7118b4b43c4ea2c3df16167721c924118244518d8a448a3f0dc`  
		Last Modified: Wed, 17 Jan 2024 03:48:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644f6e5c0e6e9b58a0f3e5c9ce4d2bb8f6f29f5faa4dc3083f09f842f1ca1bd`  
		Last Modified: Wed, 17 Jan 2024 03:48:50 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930da07d87dd16c3cc6828713317ceebf52bd5cb40d5a91766daf01f280071d`  
		Last Modified: Wed, 17 Jan 2024 03:48:51 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fc900f7e64c6f8af34f6cf0a7b990afe6db47b1255ce24ccf8b0dc09ee6a23`  
		Last Modified: Wed, 17 Jan 2024 03:48:56 GMT  
		Size: 224.4 MB (224395273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4f29a303b4d5b087a526e6c511bd824a6c75e75b93774b1ee90d64ee46513`  
		Last Modified: Wed, 17 Jan 2024 03:48:51 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:b0fe3dba5e682bafb67584da4c858b15ff68bdf2e458ff7df36fea8d053e9125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9237b7acafa58732b5c5f34dd1ec2eb45a1db485d831dcfd5fea43c1d45e0f`

```dockerfile
```

-	Layers:
	-	`sha256:f41980d4b62f4152b693d59be71b492997a82c5c6d384377471109e3ee120aa3`  
		Last Modified: Wed, 17 Jan 2024 03:48:50 GMT  
		Size: 2.7 MB (2729173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937ebc520434fcdcc552ddaeb3139a4d5fda143438080aabf04169a195482386`  
		Last Modified: Wed, 17 Jan 2024 03:48:50 GMT  
		Size: 29.5 KB (29526 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:e887440265148070320613c057020143cec609780f6635d68c857482570b749e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251972412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545fe6e3d65b82c33aa0306dfff90887f239f4f884ad98209407dd086c78ebed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 06 Jan 2024 05:07:23 GMT
ARG RELEASE
# Sat, 06 Jan 2024 05:07:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 06 Jan 2024 05:07:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 06 Jan 2024 05:07:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 06 Jan 2024 05:07:23 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Sat, 06 Jan 2024 05:07:23 GMT
CMD ["/bin/bash"]
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV GOSU_VERSION=1.16
# Sat, 06 Jan 2024 05:07:23 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'E58830201F7DD82CD808AA84160D26BB1785BA38'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 06 Jan 2024 05:07:23 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_MAJOR=7.0
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENV MONGO_VERSION=7.0.5
# Sat, 06 Jan 2024 05:07:23 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
VOLUME [/data/db /data/configdb]
# Sat, 06 Jan 2024 05:07:23 GMT
ENV HOME=/data/db
# Sat, 06 Jan 2024 05:07:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Jan 2024 05:07:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jan 2024 05:07:23 GMT
EXPOSE map[27017/tcp:{}]
# Sat, 06 Jan 2024 05:07:23 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ce9ebea987c26664d067f7e14c93231c6d303e4acb322f15ddbf05b414646d64`  
		Last Modified: Thu, 11 Jan 2024 17:49:04 GMT  
		Size: 27.4 MB (27356849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bff83b454cc4ba45c11a9ab7b50b075c4ebb4cdd441d079c096276cdf568b53`  
		Last Modified: Thu, 18 Jan 2024 17:29:34 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea2c80cbb3b35f304679783e06b6220e9620dba964cb97800f786ef04696945`  
		Last Modified: Thu, 18 Jan 2024 17:29:35 GMT  
		Size: 5.0 MB (4990764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6467c6c2b6cab5d20978a2a487a45c7addfcb07b71b83ef5eb096bee090becfb`  
		Last Modified: Thu, 18 Jan 2024 17:29:35 GMT  
		Size: 1.0 MB (1032939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46127fbd2d5e71bd51881fac2905f1e939d37284cc95e56fb886e09eed183ecf`  
		Last Modified: Thu, 18 Jan 2024 17:29:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797b0c4aa8c6cf5b15268437cc6643b3e2ab17faad7f40e0ba09ae0a7f335153`  
		Last Modified: Thu, 18 Jan 2024 17:29:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c47dab697f3d38ea5a277b654f425ba5600b152eb4844186817272d90a3c2e5`  
		Last Modified: Thu, 18 Jan 2024 17:29:36 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79ccbb5da7205965ef7663539e1896cb60036f9ae7964ef269d07e113203d9`  
		Last Modified: Thu, 18 Jan 2024 17:29:42 GMT  
		Size: 218.6 MB (218583287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9abc8ba685ebfe2adf9b6fba30517e4a4a44ccc551530ab6517e10773a2d01`  
		Last Modified: Thu, 18 Jan 2024 17:29:36 GMT  
		Size: 5.0 KB (4994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:2fdb5b08211eff683278ec973f91bce6bce3a7c121411ceed2cf8dea93dd2bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13812cc41f158c395c6f18e2447bcdb91f6400548d43283b4e6ae88d7b4b38fd`

```dockerfile
```

-	Layers:
	-	`sha256:134c0b1420d88158228a8af68251392e5b0f93d828349f2a0e634f5701998150`  
		Last Modified: Thu, 18 Jan 2024 17:29:35 GMT  
		Size: 2.7 MB (2729535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc91d6ca96e42d06fb174b3503251e1776979bd417da1fd772f43d4215ceb77`  
		Last Modified: Thu, 18 Jan 2024 17:29:35 GMT  
		Size: 29.4 KB (29383 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:f6e3f95455279cff22b21bbd8e34f8b891c39b22cd795bda3ea4d2cd3a4ea665
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2513074958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6094f7ea2a542c5d94f12af1c92eebbccfe0ff1b0174d0c747961290d4a6700`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:08:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:08:13 GMT
ENV MONGO_VERSION=7.0.5
# Thu, 11 Jan 2024 00:08:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.5-signed.msi
# Thu, 11 Jan 2024 00:08:15 GMT
ENV MONGO_DOWNLOAD_SHA256=96441addde451b9d81dfaa10aca9678ada35d17d02a9a07481c6137d3df55e2b
# Thu, 11 Jan 2024 00:09:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:09:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:09:53 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:09:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a6ec03c2a160ba4b038ddae483ec907f1d72e641ae96db10132cd265b8341f`  
		Last Modified: Thu, 11 Jan 2024 00:10:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead4f04e23ba3df03b8407f5af834ecd48b89240e35e0bfd35a395bf5fb730f7`  
		Last Modified: Thu, 11 Jan 2024 00:10:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187c8c1e4e77012d4d3c4269ba2d3c0f277fc3243676da8d948ad3b3504f9c51`  
		Last Modified: Thu, 11 Jan 2024 00:10:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72b64df9937ffdab47c1c017459a0e37a7f555bdc2e73b618f6d09369a4429a`  
		Last Modified: Thu, 11 Jan 2024 00:09:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bc67b2fbe2158d8a244db4c307638df622abbaf6d5114ae6e87a7c84683ee0`  
		Last Modified: Thu, 11 Jan 2024 00:10:52 GMT  
		Size: 612.9 MB (612853259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a185ce32d5e0f6fcf2e1a8741e70092ba0ff337858530fc67c1533a219f2f`  
		Last Modified: Thu, 11 Jan 2024 00:09:58 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00cfce2f9415941a60e5433f970a60f76c2a8737d4a5bd19c0592786fbca5f7`  
		Last Modified: Thu, 11 Jan 2024 00:09:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7f9045d893218c6eb72f02afde0edfd960a6fdb99bd93f38ac9be07dbc6f0`  
		Last Modified: Thu, 11 Jan 2024 00:09:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.5329; amd64

```console
$ docker pull mongo@sha256:21fc83617f144fd02e75248cfd719cb35c29f6afe919ba90e5d5b5ac8d297212
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2682620480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392b169b51b5b37137b5e19368fefa41183b12169bebc1baa5254419b8132247`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:07:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:07:04 GMT
ENV MONGO_VERSION=7.0.5
# Thu, 11 Jan 2024 00:07:05 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.5-signed.msi
# Thu, 11 Jan 2024 00:07:06 GMT
ENV MONGO_DOWNLOAD_SHA256=96441addde451b9d81dfaa10aca9678ada35d17d02a9a07481c6137d3df55e2b
# Thu, 11 Jan 2024 00:09:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:09:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:09:16 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:09:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85e3bf0e1e89d472c51a19154545fe43b3b8535f977d49101631a43f7339dda`  
		Last Modified: Thu, 11 Jan 2024 00:09:20 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6299919dfce03153edaff39adfc587d95e483ab8ef8743e6d37a96431c8e9159`  
		Last Modified: Thu, 11 Jan 2024 00:09:20 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fa0ec5af138cc6bc01ab789af210dc923c7768d322c905f2f5ed1e9587af33`  
		Last Modified: Thu, 11 Jan 2024 00:09:20 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a084487c755a1874dc6ada94dca3386593ff8bd1aa6fcc6f9a53104823302a`  
		Last Modified: Thu, 11 Jan 2024 00:09:19 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aef0e486a4ba2f3c45a9d28c8b7032287426ccc588ad6d873b62bf4c7215b56`  
		Last Modified: Thu, 11 Jan 2024 00:10:12 GMT  
		Size: 612.9 MB (612888369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d78d70afe1792be7c15bce64e98b0eeb464955fcd8d7b12021c3a28cf873b7`  
		Last Modified: Thu, 11 Jan 2024 00:09:19 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa8ba30e61f085ecc3fe1a24cb9641d88864f1b10225cfccf4da90df2e7eb50`  
		Last Modified: Thu, 11 Jan 2024 00:09:19 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae185eb9d60f2343b7020feada8ce8172cf4c9aae88cc7b9d0ad065757cbb2f9`  
		Last Modified: Thu, 11 Jan 2024 00:09:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
