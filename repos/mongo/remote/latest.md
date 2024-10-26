## `mongo:latest`

```console
$ docker pull mongo@sha256:3984cf5a234e525253619060fcbff12449db0597d62a6d4e18991a18f2365c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

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

### `mongo:latest` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:06472eb9afce60b19596150621e877a47eb0667110b99f2e8977f49ac0542ccd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568049456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98efadaec49409b1d2089fd87677cf77990556f795ce1ec2000f3bd9c8fad0ef`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Fri, 25 Oct 2024 23:57:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Oct 2024 23:57:12 GMT
ENV MONGO_VERSION=8.0.3
# Fri, 25 Oct 2024 23:57:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.3-signed.msi
# Fri, 25 Oct 2024 23:57:13 GMT
ENV MONGO_DOWNLOAD_SHA256=f064b0d5096136a70edd9a4a1c17d23c78f62600ba860512523eee2206a018b9
# Fri, 25 Oct 2024 23:59:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 25 Oct 2024 23:59:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 25 Oct 2024 23:59:49 GMT
EXPOSE 27017
# Fri, 25 Oct 2024 23:59:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1199f3a042eeaf1554bf78a1a3b3e30ec6a6ba8371772feb2bd5552de7c4c09`  
		Last Modified: Fri, 25 Oct 2024 23:59:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58624da82b4c32ac0f2aa179f66eba0f192c1b7c5124d5cd5a7ed4c08a03a04`  
		Last Modified: Fri, 25 Oct 2024 23:59:53 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e612f83dec9fa8bd61af3574a8e8aad95bdbbdf2e60c83227042fa6ecc8d1d`  
		Last Modified: Fri, 25 Oct 2024 23:59:53 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4a723b0e20fa35f7e27b895d4ec554e1cc3b995f44b1b7b224c7e3764f28e5`  
		Last Modified: Fri, 25 Oct 2024 23:59:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598057ebd54e7d5789d7dab0c9c5d1a3481c0fa793550b5388ce1e45e6df1842`  
		Last Modified: Sat, 26 Oct 2024 00:00:51 GMT  
		Size: 768.7 MB (768698892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6538712d000ab89cfd995663aca54e24fe6b611a6d74ab61ed812eb91a7d09ca`  
		Last Modified: Fri, 25 Oct 2024 23:59:52 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4bf14a2a6ab78e4f0895573f09cd741cbcd535978e0c56a2b5ec2c9f0ab652`  
		Last Modified: Fri, 25 Oct 2024 23:59:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e79b0f655ce9b9961df283430428b764c3e76f44a14c7e2210e324ccbf2f54`  
		Last Modified: Fri, 25 Oct 2024 23:59:52 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:52a770a60dc2fe6710864c8d3f907b102eea04090994298b786a93318d43d313
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2670541584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f3bbc6251375d6e0e8bfc9567c3b1633afab0ce259dee23e4c5ba111378d75`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Fri, 25 Oct 2024 23:57:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Oct 2024 23:57:10 GMT
ENV MONGO_VERSION=8.0.3
# Fri, 25 Oct 2024 23:57:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.3-signed.msi
# Fri, 25 Oct 2024 23:57:11 GMT
ENV MONGO_DOWNLOAD_SHA256=f064b0d5096136a70edd9a4a1c17d23c78f62600ba860512523eee2206a018b9
# Fri, 25 Oct 2024 23:59:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 25 Oct 2024 23:59:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 25 Oct 2024 23:59:57 GMT
EXPOSE 27017
# Fri, 25 Oct 2024 23:59:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c93e022fd5b1459e2a0287132848ce0766c424dd1e488d7bbc93fb1fc98ade`  
		Last Modified: Sat, 26 Oct 2024 00:00:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d4e9c0880ba7f6fa2ba82ff317a53b7587d82aac46dba86c24b21784427a8d`  
		Last Modified: Sat, 26 Oct 2024 00:00:03 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9504ea41fe8eb79a354a741e534bb5d13a77c7289f196073039fd6931ee17455`  
		Last Modified: Sat, 26 Oct 2024 00:00:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b52bce99ca5ac3c9c4e430f8f9fda368da15464908ed9da4a6ba975deb58ad`  
		Last Modified: Sat, 26 Oct 2024 00:00:01 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192c9faefcffc6b2fac10996e6a79eb51ffac2e966da72d1c76e426de879b2eb`  
		Last Modified: Sat, 26 Oct 2024 00:01:00 GMT  
		Size: 768.7 MB (768707186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29126f60832e4ef19432321239aedbe553944a85ef71311c216070ae9375b9a2`  
		Last Modified: Sat, 26 Oct 2024 00:00:01 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b274bcbd39a27a8f3e7bd19451a9bed7744bbcc8dc2c19da6318283a654f8a9`  
		Last Modified: Sat, 26 Oct 2024 00:00:01 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f0b5c1b45d6b7b79cb03b2b30b9b22c83c29fdeb3a9e118bea0dac73ed98d`  
		Last Modified: Sat, 26 Oct 2024 00:00:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
