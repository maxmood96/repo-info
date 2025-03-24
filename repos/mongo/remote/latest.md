## `mongo:latest`

```console
$ docker pull mongo@sha256:1cb283500219e8fc0b61b328ea5a199a395a753d88b17351c58874fb425223cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:0fbe569f105156a412dd7383afdc9d6a784c9acea1367663c384e5e98b2ecc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288469640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d4ab2a034263b0e2306e41be1a596bd8600fb6fadef145a9088791c8d7c4b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Mar 2025 22:06:21 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 21 Mar 2025 22:06:21 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Mar 2025 22:06:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_MAJOR=8.0
# Fri, 21 Mar 2025 22:06:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_VERSION=8.0.6
# Fri, 21 Mar 2025 22:06:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Mar 2025 22:06:21 GMT
ENV HOME=/data/db
# Fri, 21 Mar 2025 22:06:21 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 21 Mar 2025 22:06:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Mar 2025 22:06:21 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 21 Mar 2025 22:06:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12757b6444c4bf8265b616857e2a81e055bf662038771fc2aeb2ef7a19944d`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cfb5e922d1078b85377cbdaa154d2b25f67fb5664a2907edd1a2b75d50f9cc`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 3.9 MB (3911303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11968535d8a0c360571f9996ad96877a29684239f55c1918206ae5d70f49fbb`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 1.1 MB (1130254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c711ee204b1d1383a860f114449a82e983ee41956d7c746e8791b53f066c3a82`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc65ca4253fd123c695b1b74bff2d7a8cdc2771a1a5d9da1668105079e175ec`  
		Last Modified: Mon, 24 Mar 2025 21:19:16 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacd77ad2ef6c5625e09b751626186b53d4e8662f79bd9253755f474fc22ac87`  
		Last Modified: Mon, 24 Mar 2025 21:19:20 GMT  
		Size: 253.7 MB (253667204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa69bd3db1e4fcd13568432e190d90762be307687b8e8405d90181f579b5ca6`  
		Last Modified: Mon, 24 Mar 2025 21:19:16 GMT  
		Size: 5.0 KB (4993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:6b2ee100d267caee895a5a955b799f40e276bd304c913dd12521f7a4262bba72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e6dad2596c599d3c33e66d26462bbd65aacb0b1ab8de023a01d42cd29a60ca`

```dockerfile
```

-	Layers:
	-	`sha256:d0bb38821262eef175d02bdb58df3c3808f21aea6994e542e4cf6e6a7e0d5f2e`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 2.5 MB (2524379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b1c498653910899b1790231eef60783e70932dc161bd544b2bf1647e17b749`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 28.8 KB (28839 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:433198e0a19aa4736f93862df15f4a75e74e6d9ffc540e9272f517e43e441f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276701240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c72c5f78fefe289d17c049f20c0e2bfbbe35607440da0175260737b1e5359b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Mar 2025 22:06:21 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 21 Mar 2025 22:06:21 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Mar 2025 22:06:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_MAJOR=8.0
# Fri, 21 Mar 2025 22:06:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_VERSION=8.0.6
# Fri, 21 Mar 2025 22:06:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Mar 2025 22:06:21 GMT
ENV HOME=/data/db
# Fri, 21 Mar 2025 22:06:21 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 21 Mar 2025 22:06:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Mar 2025 22:06:21 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 21 Mar 2025 22:06:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9286380517d7f8cc870c4ed63cf865809fb11d80de82513ae1ca35a9a0e0d744`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfd86d7f81de6a750a0de0b1865a6ec47f99950c02e29b090d62e56b64c4ed`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 3.7 MB (3707246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306fcfa15fb1fcf4f3393be0773933cce9ad962d35e156ec0fd6fcc5b243ed28`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 1.1 MB (1060641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568f73da14f2eb4f5eec89c2821555092eeb688d5acc72553f1b4981afcc2875`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c5ca75dbfb7148dbb6f65679d41cb4365f652921c0f00cba8ea31ec25fdfc9`  
		Last Modified: Mon, 24 Mar 2025 21:19:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f4766d11003e4c990338dfa942bd9d1228dfafb95088d4c6224daa75cb805`  
		Last Modified: Mon, 24 Mar 2025 21:19:43 GMT  
		Size: 243.0 MB (243033160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fcbf4e159abb793949f8eb8820658207317922226c0a9f07b3fd6fcebd5269`  
		Last Modified: Mon, 24 Mar 2025 21:19:37 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:d043a66b332d88d6c5b954f2c05715c8531c14cd2710a8f7d155aa7f057d6df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f79ee6278a5079672aff231f032d4b3ed1cf264dce59abd6e7753f60806104`

```dockerfile
```

-	Layers:
	-	`sha256:1fca4dee06fb75fbdf6a8b004297a4fb3356ace3664d35b0a07e854974daa083`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 2.5 MB (2525515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9150e3fbf9463c25fd0dc740e72e308b30b36bba5b8a95ac928b2620fcaeb960`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 29.1 KB (29067 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.3476; amd64

```console
$ docker pull mongo@sha256:c263b3d94ad1c1e74a8bd44eeabe56a209642ceb5314ee7eef4b8a294d1d4791
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3679074633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6f2929c22adcf653c9e56b98abc9d801e7bffd1b7c63724aca774f6fae01dc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Mon, 24 Mar 2025 21:24:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Mar 2025 21:24:17 GMT
ENV MONGO_VERSION=8.0.6
# Mon, 24 Mar 2025 21:24:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.6-signed.msi
# Mon, 24 Mar 2025 21:24:20 GMT
ENV MONGO_DOWNLOAD_SHA256=c90e72bd480ba96934708a90e456080732b473665abc8bfbe828b33b833f8a70
# Mon, 24 Mar 2025 21:26:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Mar 2025 21:26:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:26:08 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:26:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54af8826fa64a9c953680a6b5c0c1aef0b78403ea3149a869d494c91a6f2ca13`  
		Last Modified: Mon, 24 Mar 2025 21:26:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40d11d9fc599751a469127968294547e31fbcebbb9267c06e6fbdb1b1548ef4`  
		Last Modified: Mon, 24 Mar 2025 21:26:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f85b56d3ed5f1ebe85821643be91a39ce9f691ab47da22a88341ba6e00ea30`  
		Last Modified: Mon, 24 Mar 2025 21:26:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e881b1751d9778aa20fbf698c622765c6f24ccfa978f108fe6c0efc934b2246d`  
		Last Modified: Mon, 24 Mar 2025 21:26:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1110df54ac5651bb4810899a8b7b8a184277883ee438f279c5436752647da4a1`  
		Last Modified: Mon, 24 Mar 2025 21:27:53 GMT  
		Size: 770.4 MB (770417781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da05d198dc87e70ea2c3d961e16ff1b6285b096303075232a956bc215d0d378d`  
		Last Modified: Mon, 24 Mar 2025 21:26:38 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30516b9535b67a38df329f66d508e22e5b85d4268507a93e74bd9ed48438e270`  
		Last Modified: Mon, 24 Mar 2025 21:26:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c914fe91de6291781e82309c714b6d8023e13ed46e5b106c48fa640795c3ee48`  
		Last Modified: Mon, 24 Mar 2025 21:26:38 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:36e0e5b794722c6aad1b4661374699f5c1831806d4c97442605f0a061fd65d17
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3040364366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0da48b0ebfbc58eb16ed3b5c6d92dfdb7e865db279095d3bfc63433a570a78`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Mon, 24 Mar 2025 21:28:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Mar 2025 21:28:41 GMT
ENV MONGO_VERSION=8.0.6
# Mon, 24 Mar 2025 21:28:42 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.6-signed.msi
# Mon, 24 Mar 2025 21:28:43 GMT
ENV MONGO_DOWNLOAD_SHA256=c90e72bd480ba96934708a90e456080732b473665abc8bfbe828b33b833f8a70
# Mon, 24 Mar 2025 21:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Mar 2025 21:30:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:30:17 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:30:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a3ddef7178c76c59c2960849c42cf63ac8bc2f5dedcf45040900b586d6987e`  
		Last Modified: Mon, 24 Mar 2025 21:30:24 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3328750bfc1a085d46c100c13f977b43d4635da8107a14f77af009155275ab2`  
		Last Modified: Mon, 24 Mar 2025 21:30:24 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c43c3f8bf35ee6c3c6c2a099a16d257fe4054f4b12eb7d37ba07d967e7fbb1`  
		Last Modified: Mon, 24 Mar 2025 21:30:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb754facd294cfcaa50ed074ecec1c92d1b1f4d3064528d423329f6b1b3c7d6`  
		Last Modified: Mon, 24 Mar 2025 21:30:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975e213ba2e61ab3b1bcb490e9bf4ce6c04663ed8c44502d70d6b8bf6a565fc4`  
		Last Modified: Mon, 24 Mar 2025 21:31:25 GMT  
		Size: 770.4 MB (770414139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3ea3e63d2ec6eab99419dde5399b19c78dcd0928a9f9d1b1566a964d78fa47`  
		Last Modified: Mon, 24 Mar 2025 21:30:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be91c6d431a1a040502b1d15ac77edad453ab3391d1db47c31294b39179a97eb`  
		Last Modified: Mon, 24 Mar 2025 21:30:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd243a482faec97b8ebb4e6becd4a8658f9b76996b264db690b5dca163fe7251`  
		Last Modified: Mon, 24 Mar 2025 21:30:22 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.7009; amd64

```console
$ docker pull mongo@sha256:039a471b7601389c1f5a25efee6d1690868906fec0903befd87ef3bfd84e82dc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2922070021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e8c894d45aa438f706b8b9b0658873126a9b27d9a306a2b6701f2a6779c994`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 24 Mar 2025 21:25:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Mar 2025 21:25:15 GMT
ENV MONGO_VERSION=8.0.6
# Mon, 24 Mar 2025 21:25:15 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.6-signed.msi
# Mon, 24 Mar 2025 21:25:16 GMT
ENV MONGO_DOWNLOAD_SHA256=c90e72bd480ba96934708a90e456080732b473665abc8bfbe828b33b833f8a70
# Mon, 24 Mar 2025 21:27:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Mar 2025 21:27:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:27:20 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:27:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d405227af210997c952bf003172546fa6341a7e2accbc514dd40ee2cfedddcf`  
		Last Modified: Mon, 24 Mar 2025 21:27:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69604b53a834b69eee2511f513b0b185a098f3de0b4eeed21b1d6a7743cd5c06`  
		Last Modified: Mon, 24 Mar 2025 21:27:26 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fb0dc7d481797663eca991488c6ca2dce3a0d72d67d127e7727dcb20ab638a`  
		Last Modified: Mon, 24 Mar 2025 21:27:26 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4437b2984cd6098ec4757bf1ae5f092494ace3003268bea2f618084a89ec307c`  
		Last Modified: Mon, 24 Mar 2025 21:27:24 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6e9f19f76dd7bb70829a821f8812c8f14cd68fd7a75006dce6b2548caff719`  
		Last Modified: Mon, 24 Mar 2025 21:28:26 GMT  
		Size: 770.4 MB (770425908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbc3c0426f772a5c95eb13b4e9afc4d973c97917479874faf1a0f53ed4d0acf`  
		Last Modified: Mon, 24 Mar 2025 21:27:24 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d80e15692828d56aae021e857e8eae960749d5d884762784b94ea95b557f555`  
		Last Modified: Mon, 24 Mar 2025 21:27:24 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98774f721d3ddab9b8bcdd0936f9df3106846b097c79f8f6610cf3982c3df5c9`  
		Last Modified: Mon, 24 Mar 2025 21:27:24 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
