## `mongo:latest`

```console
$ docker pull mongo@sha256:e64f27edef80b41715e5830312da25ea5e6874a2b62ed1adb3e8f74bde7475a6
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
$ docker pull mongo@sha256:24c904ccff05dcd659aae47af9bf7c8ffeba84b62099f5cd8ca10327665cc1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258781872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a05b7283523bfe55eb2a90a39789c1bb3bbe95c14efcb4b014ef3e35a5e95e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENV GOSU_VERSION=1.17
# Mon, 26 Aug 2024 16:01:29 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 26 Aug 2024 16:01:29 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_MAJOR=7.0
# Mon, 26 Aug 2024 16:01:29 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_VERSION=7.0.14
# Mon, 26 Aug 2024 16:01:29 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
VOLUME [/data/db /data/configdb]
# Mon, 26 Aug 2024 16:01:29 GMT
ENV HOME=/data/db
# Mon, 26 Aug 2024 16:01:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 16:01:29 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 26 Aug 2024 16:01:29 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54f12bd58198590bc17d166d7e9d42dd34d95532894806656c46185c46c4d2d`  
		Last Modified: Mon, 26 Aug 2024 22:56:43 GMT  
		Size: 1.8 KB (1775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95b02a6236d79e0c6666e918812b1faf12db63bcea429a89d49082f91babf3d`  
		Last Modified: Mon, 26 Aug 2024 22:56:43 GMT  
		Size: 1.5 MB (1500964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d20d29fe9caa158e5e6612c0d7b28d1e19ab9c93d2401ec91f7eecb767d73a6`  
		Last Modified: Mon, 26 Aug 2024 22:56:43 GMT  
		Size: 1.1 MB (1094776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2382733f40de4cefce4aa72d34f893fad4a58907272dd73f9b4c3c7c60dae828`  
		Last Modified: Mon, 26 Aug 2024 22:56:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1458145b657ba68d3a0fed527b5b947771999ab5996b7ea2cd178261800c833`  
		Last Modified: Mon, 26 Aug 2024 22:56:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee77be417658c5caa35d1d096088fbbbafca3831b0541df1b69485d49a32fdd`  
		Last Modified: Mon, 26 Aug 2024 22:56:46 GMT  
		Size: 226.6 MB (226642954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4a4cbb623f6224bf010a7ed79f2197d59740f37575011bebd6c7546cbcd3d0`  
		Last Modified: Mon, 26 Aug 2024 22:56:44 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:fa4573c33fb811f47bf2b693a87eae15c331078e091c0825a9974168e8c27d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1512fc4a88599d984377df850e041e292addb224de0bb8e7417c49b58a5718c`

```dockerfile
```

-	Layers:
	-	`sha256:e1f5d4ecb98a9bb29f601f3de9b19519bf89817b4d035c5ecfc7ca2ba597b2d9`  
		Last Modified: Mon, 26 Aug 2024 22:56:43 GMT  
		Size: 3.0 MB (3029337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83fb5b7897fa69b3f78ef32445af4af2f4fad44fcaeccd4c9e8b5a84def98066`  
		Last Modified: Mon, 26 Aug 2024 22:56:43 GMT  
		Size: 27.6 KB (27636 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:102aae4108502c1ba4d176f1952095e754f22f264d0ecc581d4d34dc93ec170e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247466854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da14d7a14a17789c1392f4a5dea8273acadc0e0e71c80def82d826331a57310`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENV GOSU_VERSION=1.17
# Mon, 26 Aug 2024 16:01:29 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 26 Aug 2024 16:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 26 Aug 2024 16:01:29 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_MAJOR=7.0
# Mon, 26 Aug 2024 16:01:29 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENV MONGO_VERSION=7.0.14
# Mon, 26 Aug 2024 16:01:29 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
VOLUME [/data/db /data/configdb]
# Mon, 26 Aug 2024 16:01:29 GMT
ENV HOME=/data/db
# Mon, 26 Aug 2024 16:01:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Aug 2024 16:01:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Aug 2024 16:01:29 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 26 Aug 2024 16:01:29 GMT
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
	-	`sha256:6938b4cd751880fadd3be41c18dd62939dddcff1d4cbe06c26b05cce71ec8116`  
		Last Modified: Mon, 26 Aug 2024 22:59:34 GMT  
		Size: 217.6 MB (217607621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2db3ac0ac1117e12722f0991731345c490b0bd51f60bed70e8ff8ff89ba336`  
		Last Modified: Mon, 26 Aug 2024 22:59:27 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:15f60e1c9cfef7c22eb5ce983d5eb98db3717ead6a9c120728cd482182d57115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c60e77a3b3dc9a591f59c3164c70c6e71acc41dc1544197b0d5e51642663dd5`

```dockerfile
```

-	Layers:
	-	`sha256:5858beebfabaaff4d7c721551aebda4836862a814cb6f9b39d542dd829c7cd91`  
		Last Modified: Mon, 26 Aug 2024 22:59:27 GMT  
		Size: 3.0 MB (3029679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14a93a09806fea86b924512090741ff46a324c71dc9270f04d3c18999f9a0c37`  
		Last Modified: Mon, 26 Aug 2024 22:59:27 GMT  
		Size: 28.0 KB (27983 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.20348.2655; amd64

```console
$ docker pull mongo@sha256:5782ad461946662c7108502563a23055b911e0c88fd4cd82a920c264dc8009fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2751294982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f9693322db0dfe889937c15c9fc4c39ba82d77a7455878135debd66aacac80`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Mon, 26 Aug 2024 23:04:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 26 Aug 2024 23:04:33 GMT
ENV MONGO_VERSION=7.0.14
# Mon, 26 Aug 2024 23:04:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.14-signed.msi
# Mon, 26 Aug 2024 23:04:34 GMT
ENV MONGO_DOWNLOAD_SHA256=8916397b35f2b6b42241ef1625e5c75ba7ad10ad75072cf377450f6f0bdf254c
# Mon, 26 Aug 2024 23:05:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 26 Aug 2024 23:05:53 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 26 Aug 2024 23:05:53 GMT
EXPOSE 27017
# Mon, 26 Aug 2024 23:05:54 GMT
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
	-	`sha256:e3e3fd2ee4d5a6012f4b3000bbb36f1d579d52711b5232000e3dc225ee75736f`  
		Last Modified: Mon, 26 Aug 2024 23:05:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d117f6ae18dd48074cf6fed6dcfae15828ae9fb9f418ab6b2655df48abef373e`  
		Last Modified: Mon, 26 Aug 2024 23:05:59 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff9960bb95f21accbc9773bdcf8529928ed64a789e741b9cde91e5ddb2854f9`  
		Last Modified: Mon, 26 Aug 2024 23:05:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6580a2f7e3e77df85b650ab19d49478cf0b42dfa3af86b2a17248a9e8aee1`  
		Last Modified: Mon, 26 Aug 2024 23:05:58 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a7839a2cbb430345696bd7bc46a31d5aac724e2ddbcb0a163dec6797475079`  
		Last Modified: Mon, 26 Aug 2024 23:06:49 GMT  
		Size: 609.5 MB (609520983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b0806deff299d5769073c7a9b98569379b1e6dd22c7ed7aa14a152cb79fd2c`  
		Last Modified: Mon, 26 Aug 2024 23:05:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0880183e6463f8476567c2defe08a5c5d301ad341c7ec0fe1d26240dc57c4f`  
		Last Modified: Mon, 26 Aug 2024 23:05:58 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc8e75acfea6a485f86fb69b30197fcec0413258248f4431ae509c012e668e0`  
		Last Modified: Mon, 26 Aug 2024 23:05:58 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:b11f4e7fa642dba9418544a3f9d392fec257eb5b4322059164e288d2850d99d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2854921419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cb306282371ae1c22c6cd735a55bd9e8ca329b11b9318f9a5e867236b0fda4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Mon, 26 Aug 2024 22:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 26 Aug 2024 22:55:47 GMT
ENV MONGO_VERSION=7.0.14
# Mon, 26 Aug 2024 22:55:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.14-signed.msi
# Mon, 26 Aug 2024 22:55:49 GMT
ENV MONGO_DOWNLOAD_SHA256=8916397b35f2b6b42241ef1625e5c75ba7ad10ad75072cf377450f6f0bdf254c
# Mon, 26 Aug 2024 22:58:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 26 Aug 2024 22:58:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 26 Aug 2024 22:58:41 GMT
EXPOSE 27017
# Mon, 26 Aug 2024 22:58:42 GMT
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
	-	`sha256:426ba3cbf779c29063646390e2920f16d65c396af1f72f2dc4e5b4d811ad8177`  
		Last Modified: Mon, 26 Aug 2024 22:58:45 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85581ed0a705e2953dc01caf000485162ac3ff208f1482ce32f135436b25f465`  
		Last Modified: Mon, 26 Aug 2024 22:58:45 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597e761832c450162e922f32808f815ce2ec986f7dd7bc2e726cc6f32e73223d`  
		Last Modified: Mon, 26 Aug 2024 22:58:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213755ad8daacaba8b937bd2b7873bb5da7d29c8745c25da8c92fdda0f8c4c0a`  
		Last Modified: Mon, 26 Aug 2024 22:58:44 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd73cb761835860fd24006bb0554e3e4cd440c468e7c48adc258c972f95599d`  
		Last Modified: Mon, 26 Aug 2024 22:59:30 GMT  
		Size: 609.7 MB (609709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae5832247bf9fb4cb0f646d14538c266b3ad7dd05f5cf1a371884ca2169dc44`  
		Last Modified: Mon, 26 Aug 2024 22:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820397eeedc6daf8ec59dc3751c65c21b0e054241e4e5f091ef015988456288e`  
		Last Modified: Mon, 26 Aug 2024 22:58:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e114ad3497cbe1f1556a043aa7ce451911deb4b6ce2c149342919638f9976fab`  
		Last Modified: Mon, 26 Aug 2024 22:58:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
