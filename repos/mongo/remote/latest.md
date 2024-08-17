## `mongo:latest`

```console
$ docker pull mongo@sha256:ae1cf99fa7bfb007db8416ad4f3980c46054d949fa55d28e6d301a813fee6c06
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
$ docker pull mongo@sha256:6d245af0e8dffc8771f3e734b4ee0bc7fcde48fcffe3bf2664592dfda8e9e6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258716192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2076a62a1ced8bc62d7963c2e04d7b5fdf3358503fd0daaa4688fb227c1ec35b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 28 Jun 2024 22:05:28 GMT
ARG RELEASE
# Fri, 28 Jun 2024 22:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Jun 2024 22:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Jun 2024 22:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Jun 2024 22:05:28 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Fri, 28 Jun 2024 22:05:28 GMT
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7a238bbe68584686a4ebcb3f11e2d5c8c482f89d9bc10bd3a1cc8d865ce2e`  
		Last Modified: Sat, 17 Aug 2024 02:05:52 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b2514837c958dcc097c5dd0234fc9c13927bfdffffbdf7c42ba698848a87d1`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 1.5 MB (1500849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22133372085a3b8bced4ea88fad92b9133bb845a5406ea0a9665765482f0513c`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 1.1 MB (1094738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dcbe55d7d81bb77a2097a01cf0b352928b24413bc00c910dfb8c641f290026`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8896cc7f272b5725dc5085436b3d6d2a87ff5222b0b2567f417a617549fc61`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21700c8b485401880278b1ceb01d37f902936ba1cbbe07ec4c426f54c3f36fe3`  
		Last Modified: Sat, 17 Aug 2024 02:05:56 GMT  
		Size: 226.6 MB (226577422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6268a37a75c7ce0206e22b8130d842787a1aad5a18afa44861d9d6fd9cda3cd`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 5.0 KB (4993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:547811295ce6ee3b6be4ba8084ac045d82214c317b3fd7cf2ceb5a5250cec3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba06afa1c71d48412bf99e98711bcbef7558ecf442468829d5f843db10f78dbf`

```dockerfile
```

-	Layers:
	-	`sha256:771bd0e9fdb41d0715e006a78edc27267223ef565234ec3f312eb9fbd3cb345d`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 3.0 MB (3029337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa424203b8eaa5e5a195192380be79ff983487fc4d661e5b3b696f1233a9763b`  
		Last Modified: Sat, 17 Aug 2024 02:05:53 GMT  
		Size: 27.6 KB (27635 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:5945eed557f9893a6cd97a5da1bf539d799e8f177f277ba9b8e9ca69fc31cf33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247410007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb433c5673fbd6b81f689c590d7c3e0f0f21605097c4284998bdd20a8df0bbd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 28 Jun 2024 22:05:28 GMT
ARG RELEASE
# Fri, 28 Jun 2024 22:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Jun 2024 22:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Jun 2024 22:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Jun 2024 22:05:28 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Fri, 28 Jun 2024 22:05:28 GMT
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5099c6f371c3636e69be7e06e54581f64b8c31de3c79ee2e511aab3b0621b`  
		Last Modified: Sat, 17 Aug 2024 03:19:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b46311ab598f2b54f733e70bf994f009a4d0e96b1ca8244fe0c81dfda8c066`  
		Last Modified: Sat, 17 Aug 2024 03:19:08 GMT  
		Size: 1.5 MB (1465923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9146fb61af94e0deb301e0cef12da9e4ffd3a8a431718e21541326216691a5f8`  
		Last Modified: Sat, 17 Aug 2024 03:20:37 GMT  
		Size: 1.0 MB (1027463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a0a89625025b9e7214ea8f6e2258c5b34df7da73eabffaa97ad0a07f7d59cd`  
		Last Modified: Sat, 17 Aug 2024 03:20:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c457f686dcebd7d60a3c49f6449d22c22689171d7fec907183e1eb96d549543`  
		Last Modified: Sat, 17 Aug 2024 03:20:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991699882dca0731dd619c9b68fe29365c3fb8e94f9b5fbee8e9947167be76a`  
		Last Modified: Sat, 17 Aug 2024 03:20:43 GMT  
		Size: 217.6 MB (217550774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aa7657b86eae87e89e02d2d473df09b73e9deb0439d2d03229ef427c455e4c`  
		Last Modified: Sat, 17 Aug 2024 03:20:37 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:b3fd758c14b60976ccae20eaca8d40c665b3a6293521f1c0e6a6cf46ec23d56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a18e7b4ad1b94e53ea3caae766ba66c45ad39ff5af8f91bd247902f18b88f4`

```dockerfile
```

-	Layers:
	-	`sha256:2adf976235c8a2ab881c511daf33547727025835b21f054be71edffb49f34cc9`  
		Last Modified: Sat, 17 Aug 2024 03:20:37 GMT  
		Size: 3.0 MB (3029679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004311c68a974e8ea16c29bef5c831266e0e759088878bca39d722b02042e548`  
		Last Modified: Sat, 17 Aug 2024 03:20:36 GMT  
		Size: 28.0 KB (27985 bytes)  
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
