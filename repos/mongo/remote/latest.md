## `mongo:latest`

```console
$ docker pull mongo@sha256:dfa32f68d02281185978619aac453896c85c46ee4911c93b8e5a5d2167af4856
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:6738383868377b1ccc6762a3f008c553d4ddb21e3430b2729814c0692ed35c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326990250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252af33466de8a9b9528dc7265331a25ba054d6a7f19172eba96f33b905b96aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 19 Dec 2025 18:52:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 19 Dec 2025 18:52:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 18:52:59 GMT
ENV GOSU_VERSION=1.19
# Fri, 19 Dec 2025 18:52:59 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 19 Dec 2025 18:52:59 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 19 Dec 2025 18:52:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 19 Dec 2025 18:52:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 19 Dec 2025 18:52:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 19 Dec 2025 18:52:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 19 Dec 2025 18:52:59 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 19 Dec 2025 18:52:59 GMT
ENV MONGO_MAJOR=8.2
# Fri, 19 Dec 2025 18:52:59 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 19 Dec 2025 18:52:59 GMT
ENV MONGO_VERSION=8.2.3
# Fri, 19 Dec 2025 18:53:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 19 Dec 2025 18:53:16 GMT
VOLUME [/data/db /data/configdb]
# Fri, 19 Dec 2025 18:53:16 GMT
ENV HOME=/data/db
# Fri, 19 Dec 2025 18:53:16 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 19 Dec 2025 18:53:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:53:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:53:16 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 19 Dec 2025 18:53:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348649c4494ee19c9c75e6b46903f30b777acc8607bf2ab3f4a3e22eea7f9e78`  
		Last Modified: Fri, 19 Dec 2025 18:54:20 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cfba47b77776b350b8d1446c56f901b226863d1bb7f2155d2bb7800186c5c8`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 1.5 MB (1509246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13b06a365c8f8066d701d49908d22a72e5f1e39a846cd44ca3ed974429bb0b6`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 933.7 KB (933721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376ac72e170c6ee7e294e6b516620f76917a93a67ef0705aa9351f96dd8e08d4`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ced2b1d3306d87cd62cec65e18dba5064386d5b20d78aa834138b493ccae3ac`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e5d4f0408a6e94afd9cb9285d74583a29287d726b226e2818f4d8181a82be`  
		Last Modified: Fri, 19 Dec 2025 18:54:33 GMT  
		Size: 294.8 MB (294815995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f31927b28a041a22e274a675ad6c346e1918a7b6c0f9ff56774d8fe6e6a7cb`  
		Last Modified: Fri, 19 Dec 2025 18:54:14 GMT  
		Size: 5.0 KB (5005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:f7c968b45502d0c39d85b2be2a2af321f4c0db48f36c5333f84cfda4892bc2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7806f7be971b81eb6bd00255af9488fdedf2b84af6aec7cf7b42852851eefb1`

```dockerfile
```

-	Layers:
	-	`sha256:5eb8e9025022d723d2d32617658c24f97b8eb6b312f229d4294fc5ab0a3db053`  
		Last Modified: Fri, 19 Dec 2025 20:07:53 GMT  
		Size: 2.7 MB (2668873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c714cb47e7a45d2c5af645eb5778d6bad96ffa0fc8e8d9e71e855e55a0748a`  
		Last Modified: Fri, 19 Dec 2025 20:07:54 GMT  
		Size: 28.8 KB (28792 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:41d3045f9b8575dd5070cc760db5da659067747ff782e55284cfefac449db519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312538494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8879c0828d78dc79a36a09e861928116e5485e1d41fdbb1dc0c57329d16e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Fri, 19 Dec 2025 18:53:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 19 Dec 2025 18:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 18:53:39 GMT
ENV GOSU_VERSION=1.19
# Fri, 19 Dec 2025 18:53:39 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 19 Dec 2025 18:53:39 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 19 Dec 2025 18:53:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 19 Dec 2025 18:53:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 19 Dec 2025 18:53:39 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 19 Dec 2025 18:53:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 19 Dec 2025 18:53:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 19 Dec 2025 18:53:39 GMT
ENV MONGO_MAJOR=8.2
# Fri, 19 Dec 2025 18:53:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 19 Dec 2025 18:53:39 GMT
ENV MONGO_VERSION=8.2.3
# Fri, 19 Dec 2025 18:54:00 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 19 Dec 2025 18:54:00 GMT
VOLUME [/data/db /data/configdb]
# Fri, 19 Dec 2025 18:54:00 GMT
ENV HOME=/data/db
# Fri, 19 Dec 2025 18:54:00 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 19 Dec 2025 18:54:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:54:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:54:00 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 19 Dec 2025 18:54:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6c93d4528b48d6009b14db5449fe1ab781c036306d04878e97ff8058714e3c`  
		Last Modified: Fri, 19 Dec 2025 18:54:51 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1d960a65675ebd01b7aec52ad60a9d58ca1b5930d084aa65df2d4d26a4cfa0`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 1.5 MB (1494212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90aac4a84565e81d1b2a7ba73cbff2f51e631226c6c23e4c3ff179a3028087e6`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 886.0 KB (885960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab1583455871f1b05a4c17d88636ffef27673934cc53fb5da576c4887b5e5fb`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb9ad4997b8b44ddda18e96138e6c3f131c4ed90582aca8b019c91fdab28950`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec3fd50f49f6d11df2c4b35e8d33499da45d2dc6b9048b832ae1d144c0858ac`  
		Last Modified: Fri, 19 Dec 2025 18:57:29 GMT  
		Size: 281.3 MB (281289763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ff4183d3969317eca4a5acdd02023d9fe6ce73e76ead2a28e6529644f429e5`  
		Last Modified: Fri, 19 Dec 2025 18:54:50 GMT  
		Size: 5.0 KB (5006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:838ada4774c3a1bbc381db4bd63a76bdc700f9e3214794bd4ca85c88ab6da4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adcdbf59af9672e6899427cc2961b26b9018698320d175ca0bfc4dd2008ca00`

```dockerfile
```

-	Layers:
	-	`sha256:2ce8f7b034ed5c1a73b6170b912dff4cf7cfbe4b67a078a65a5c8f9ad7555d37`  
		Last Modified: Fri, 19 Dec 2025 20:07:50 GMT  
		Size: 2.7 MB (2670009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fce2d6033e186ab239a07846bc3904696bd9570943af23b63779dbb6c79870d5`  
		Last Modified: Fri, 19 Dec 2025 20:07:49 GMT  
		Size: 29.0 KB (29019 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.32230; amd64

```console
$ docker pull mongo@sha256:034f8b53d853553c0b73c053d6c40d6146068b50064534cff2b03015c98285fa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311040729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e747dede8516fe895982f98a417c98582db4a230a01b4221a6621e8e857d1d99`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 22:58:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Jan 2026 22:58:56 GMT
ENV MONGO_VERSION=8.2.3
# Tue, 13 Jan 2026 22:58:56 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.3-signed.msi
# Tue, 13 Jan 2026 22:58:57 GMT
ENV MONGO_DOWNLOAD_SHA256=dbad91532fd5f5bb5b42818ce7a644dd603a388926303b306e23ef29a640e849
# Tue, 13 Jan 2026 23:00:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 23:00:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Jan 2026 23:00:48 GMT
EXPOSE 27017
# Tue, 13 Jan 2026 23:00:49 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:56:33 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360b252c290b93ec41216f7dc46e4be66a0311063648c653fe191c345018fc7d`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be0589b24cd7e89b2d23e0010f876e83d5d84aa2e4c8fa1a7b94c34c000648a`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca321270f88713686ee5f8096d24db0c4f8ba5e6215a904800537d74cddecdb`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5dd864a30d14de5d6657733765e260f4f2ac28be4d180961bf278a74188e55`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc81f7eb21062c507514bbcf5226bc99bef4f91e5f305df02ecedab64b91ee3`  
		Last Modified: Tue, 13 Jan 2026 23:02:36 GMT  
		Size: 815.3 MB (815271256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32078f0c6fc72400232579f98fa85408ad8d6bbdff9f56da238ee70e9cdda01`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa8e4a5de20e8f54a754473a766b2323530f0a1e79c9b36f24cdefd43a17a9a`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13abaf697bd6b19a8b43b767f8b5cc60657c9540c47d1267d5dc526f1f39c1f3`  
		Last Modified: Tue, 13 Jan 2026 23:02:21 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:93ce3b5baa83a3540431ea264d54fd3a3d0aa239e99337a4ed99402060d3364d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2651085957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e6ae4bfa0cf66ee4be5875ff9ae90c6343cf8a31aa9e6dc8b6906007e93fb7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 23:01:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Jan 2026 23:08:57 GMT
ENV MONGO_VERSION=8.2.3
# Tue, 13 Jan 2026 23:08:58 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.3-signed.msi
# Tue, 13 Jan 2026 23:08:59 GMT
ENV MONGO_DOWNLOAD_SHA256=dbad91532fd5f5bb5b42818ce7a644dd603a388926303b306e23ef29a640e849
# Tue, 13 Jan 2026 23:10:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 23:10:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Jan 2026 23:10:40 GMT
EXPOSE 27017
# Tue, 13 Jan 2026 23:10:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0fce413876f886fb2250022b76f87a9e023cf582c638600a9fba8ca303bfd0`  
		Last Modified: Tue, 13 Jan 2026 23:02:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed1abd2a4a299d7ac78676b336899c0d5f82d3d058c2edad872c1eb1ef5d1`  
		Last Modified: Tue, 13 Jan 2026 23:12:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923f341d81286bf509bf5a571863ded6e1f90cb6d4898147afae5059549f5ee6`  
		Last Modified: Tue, 13 Jan 2026 23:12:11 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e21bf43bc0fdc9427abe81ff4f1387f2f043a3d3693215e1285c270af04ae32`  
		Last Modified: Tue, 13 Jan 2026 23:12:11 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438cf0b92e60792107bfcc7cdaa7ec529fe7490ab9eab13dcf423e721ccd85ee`  
		Last Modified: Tue, 13 Jan 2026 23:12:37 GMT  
		Size: 815.4 MB (815417561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14293688d6163c0d8e82c30e9fef412146cdd07daf95c72bd5a54b2f829710dc`  
		Last Modified: Tue, 13 Jan 2026 23:12:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18d32e4c0de7c773be3cc9dc0097c7ee4ed66d7651e7e490e0e4e0aab39dab2`  
		Last Modified: Tue, 13 Jan 2026 23:12:11 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67ef6346c36bd59d48ae769839e6ad4d3cdb078d6575a51712246fb545a933c`  
		Last Modified: Tue, 13 Jan 2026 23:12:11 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
