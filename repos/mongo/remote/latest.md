## `mongo:latest`

```console
$ docker pull mongo@sha256:05aeeb4cb12639aa6244eaecbfff6745a40ac564af58e6e9f4ea1b178a1daf2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:38f6ec342d336ff2551eccb9eb94e54d9b3d5f7ee1d4d723279469c97654f1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c59b6384122cf12efabd7a6ba739f2f18c4eed6632a8029715dc0323c7f0f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:15:38 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 25 Oct 2024 04:15:38 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 25 Oct 2024 04:15:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_MAJOR=8.0
# Fri, 25 Oct 2024 04:15:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_VERSION=8.0.3
# Fri, 25 Oct 2024 04:15:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 25 Oct 2024 04:15:38 GMT
ENV HOME=/data/db
# Fri, 25 Oct 2024 04:15:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 04:15:38 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 25 Oct 2024 04:15:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458feb30708281c7ce3b1d95b4da1022e55bef0539958ffa8311b03b60300d4a`  
		Last Modified: Fri, 25 Oct 2024 23:58:00 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59af5df8253c55a9c6d4753579e06d1cda407350cbf090e122c99cad7ff849f`  
		Last Modified: Fri, 25 Oct 2024 23:58:00 GMT  
		Size: 1.5 MB (1507180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145c7b6ccdb90c66352544d8d8f627f6366d02914298e260295c8e116c728d46`  
		Last Modified: Fri, 25 Oct 2024 23:58:00 GMT  
		Size: 1.1 MB (1129638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc527541fcbf62f2adee1fd7258cb41d512cac21755c83b47befc7b6308292`  
		Last Modified: Fri, 25 Oct 2024 23:58:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076d157aff577b86cdb929fa6c18538667be99f0b0cb13f70511b4f6eef2d08b`  
		Last Modified: Fri, 25 Oct 2024 23:58:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a304803279c07bab4705464de5db1a3de1c83fab7cc3744eb2afadbcda910`  
		Last Modified: Fri, 25 Oct 2024 23:58:04 GMT  
		Size: 242.2 MB (242202902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3736af050cc0475b998773af4ab378284de090f8a56f2995e5b041fd3bd47846`  
		Last Modified: Fri, 25 Oct 2024 23:58:01 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:606b2967930b4108cf7ed5610c37f9486a3923ee89c119ba2bd769d08d59351b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbece44ead317a9812fcece5729cfd75aa43a893b30db6bbdb0fdb60b74ae0fa`

```dockerfile
```

-	Layers:
	-	`sha256:1cbad80c38242ee76b3ba6d133561169cfb37a25859f73cf5c4364d3bef8bece`  
		Last Modified: Fri, 25 Oct 2024 23:58:00 GMT  
		Size: 2.5 MB (2497797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d945b3fe845f8d736e111b96884e794de978f7ae6b7b5c707570cc23e4d747a`  
		Last Modified: Fri, 25 Oct 2024 23:58:00 GMT  
		Size: 28.6 KB (28572 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:655e6de68371569a08b85e50507c6b05f31b6fd97d9eace28d25a80ef11e713c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263729841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc96b7a9c69b1df5c2409cab336b328fbf15fa8620423eabb5962221d3ace842`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:15:38 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 25 Oct 2024 04:15:38 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 25 Oct 2024 04:15:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_MAJOR=8.0
# Fri, 25 Oct 2024 04:15:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_VERSION=8.0.3
# Fri, 25 Oct 2024 04:15:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 25 Oct 2024 04:15:38 GMT
ENV HOME=/data/db
# Fri, 25 Oct 2024 04:15:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 04:15:38 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 25 Oct 2024 04:15:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387205ff5518f92532224e42a7c8df498c61705b1fc546e64d3c600986d9538c`  
		Last Modified: Fri, 25 Oct 2024 23:58:17 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc24964b1fbe73e9ce15686b931ad6e8977c60ccaaa5d39224b3bda2f4aa8a31`  
		Last Modified: Fri, 25 Oct 2024 23:58:17 GMT  
		Size: 1.5 MB (1491363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d01e0cfce8aeeb508c479736f394221fa1806a202363eac9c3de51cc91711bf`  
		Last Modified: Fri, 25 Oct 2024 23:58:17 GMT  
		Size: 1.1 MB (1059837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef73545efdd05a4e2600e0620e5bc714f5e2e6c56dcb488c9459636a25ff3d`  
		Last Modified: Fri, 25 Oct 2024 23:58:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3823d21067795852682aec94e4a1895b9630b60942525898dabaf01d185bcd5e`  
		Last Modified: Fri, 25 Oct 2024 23:58:17 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4887f19096e9b3daa3a53172802421c0cb0ce47206d6e22bc9ee1b4f6ec55448`  
		Last Modified: Fri, 25 Oct 2024 23:58:23 GMT  
		Size: 232.3 MB (232286211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c9d877e5da996cdb8a92120fd97b00a766fa2ff5d0fa4502169da3723da40`  
		Last Modified: Fri, 25 Oct 2024 23:58:18 GMT  
		Size: 5.0 KB (4993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:4af9df76c77611fbcd9b58a40b2f0447efc60f54dfabfeee3367e550017277f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfd2b267e5551512e60ee63289cf16b868d82cb4bb877ed99fd40d5504d76f6`

```dockerfile
```

-	Layers:
	-	`sha256:3ba65a46ca563f81b90761dbfca68d92a663a784e2ee10560179dbe579c5eb6c`  
		Last Modified: Fri, 25 Oct 2024 23:58:17 GMT  
		Size: 2.5 MB (2498933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fd0b121510d89bdaf8e5d5a909b2e0556dd0b39d3c1f51f1657f7e9d0bd0718`  
		Last Modified: Fri, 25 Oct 2024 23:58:17 GMT  
		Size: 28.8 KB (28799 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.20348.2849; amd64

```console
$ docker pull mongo@sha256:104bef9082ca209689a1d468b5bdf7531ece4c00e818bcc1123f8f097b18e059
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3021036863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be99c0d705f7f6bd64fc9f17fe77f2148a31274dac120acc07a83c91599d64a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:12:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:32 GMT
ENV MONGO_VERSION=8.0.3
# Thu, 14 Nov 2024 20:12:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.3-signed.msi
# Thu, 14 Nov 2024 20:12:33 GMT
ENV MONGO_DOWNLOAD_SHA256=f064b0d5096136a70edd9a4a1c17d23c78f62600ba860512523eee2206a018b9
# Thu, 14 Nov 2024 20:14:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:14:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Nov 2024 20:14:10 GMT
EXPOSE 27017
# Thu, 14 Nov 2024 20:14:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68965c48940231b5fb626c18bdcfa23bcdb6201b17b9cf8c79eb16e5011f7e70`  
		Last Modified: Thu, 14 Nov 2024 20:14:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceabd9f0091214a0700edd3df213158a29848e9b55147182420d1dfd11701db2`  
		Last Modified: Thu, 14 Nov 2024 20:14:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad13e9dd64be6b7347bd9706951c1adf27948e0308f1693de3cd7ec75a33c3da`  
		Last Modified: Thu, 14 Nov 2024 20:14:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877e0fd228bf732c0fd742ee177791132fb4b0d480178a6094cbfa5a191621ee`  
		Last Modified: Thu, 14 Nov 2024 20:14:14 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61ad68908d8e5a905dcb3749b11b5a83be1b4b823b37f91b2e6c1732071998f`  
		Last Modified: Thu, 14 Nov 2024 20:15:16 GMT  
		Size: 768.5 MB (768543629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0fb8b87d0f7b44e606fbedc4350de4d668e238c9f2f3455072dc767961f1c3`  
		Last Modified: Thu, 14 Nov 2024 20:14:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e66cda621851460f482cd961a8af19d43c214c15ecd10fd6eab020e9f27825c`  
		Last Modified: Thu, 14 Nov 2024 20:14:14 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d48e718d980129dc3e71d1aa7e599f20df110740ea665461fbb22ae8439ef1`  
		Last Modified: Thu, 14 Nov 2024 20:14:14 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.6532; amd64

```console
$ docker pull mongo@sha256:af01383bc3156dd397ca26b305957a9e521dd1fc5e7c0132e3ee18387526d6c0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779384978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c85a89a43b38c2ecd716664c2ceff5687a6f83dff7f92308373034129b1a87`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:25:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:25:54 GMT
ENV MONGO_VERSION=8.0.3
# Thu, 14 Nov 2024 20:25:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.3-signed.msi
# Thu, 14 Nov 2024 20:25:56 GMT
ENV MONGO_DOWNLOAD_SHA256=f064b0d5096136a70edd9a4a1c17d23c78f62600ba860512523eee2206a018b9
# Thu, 14 Nov 2024 20:28:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:28:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Nov 2024 20:28:26 GMT
EXPOSE 27017
# Thu, 14 Nov 2024 20:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8653d9fb91fed5131758cd8fa5736b0636e6ca1d07e98372e780ffb26150131`  
		Last Modified: Thu, 14 Nov 2024 20:28:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e2176c7c569a6f805807243a2c820d0460d7e162940b9013372a4dcbcd3046`  
		Last Modified: Thu, 14 Nov 2024 20:28:30 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2709433b292de808d3a0e8d8f79110c8287c3cc5e5cf5f30841f5b3f278ee68`  
		Last Modified: Thu, 14 Nov 2024 20:28:30 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0504601ed14fc7b3b472c306f8bb5f9541059faddb66163164d196e11e5ed5`  
		Last Modified: Thu, 14 Nov 2024 20:28:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9161f8003ed23645026859344b4facce849c94133846a59bc436ed5f7bc4f3b`  
		Last Modified: Thu, 14 Nov 2024 20:29:29 GMT  
		Size: 768.7 MB (768722121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14215beb02f69f878b04567a6b8afc3d974b3105ee152d6142756bbbf08bc038`  
		Last Modified: Thu, 14 Nov 2024 20:28:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04d67552305f8bd3f419d76bc3f02ead5ae1b7462a71f9d83c28bae86149d33`  
		Last Modified: Thu, 14 Nov 2024 20:28:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7ed86a558de63dd532ee970a41dd9a5ca534c668b3a977057d8c8270d77ad`  
		Last Modified: Thu, 14 Nov 2024 20:28:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
