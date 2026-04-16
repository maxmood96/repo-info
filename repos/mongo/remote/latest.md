## `mongo:latest`

```console
$ docker pull mongo@sha256:9690b268c50317b2988a7f84f514a2cdcf4de6836e12c295b48f3a203731fce1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:9c97228da610a4a1a407e34fe790dcdf5a4273c1e84d1c74cd2231b72881ffca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337907815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9e92717f46eb666ce4d53f67d49b4550f64e95298a670f3df168ee29f64f15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:45:10 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 15 Apr 2026 20:45:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:45:32 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:45:32 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 15 Apr 2026 20:45:32 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 15 Apr 2026 20:45:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:45:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:45:32 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 15 Apr 2026 20:45:32 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 15 Apr 2026 20:45:32 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 15 Apr 2026 20:45:32 GMT
ENV MONGO_MAJOR=8.2
# Wed, 15 Apr 2026 20:45:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Wed, 15 Apr 2026 20:45:32 GMT
ENV MONGO_VERSION=8.2.6
# Wed, 15 Apr 2026 20:45:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 15 Apr 2026 20:45:50 GMT
VOLUME [/data/db /data/configdb]
# Wed, 15 Apr 2026 20:45:50 GMT
ENV HOME=/data/db
# Wed, 15 Apr 2026 20:45:50 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 15 Apr 2026 20:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:45:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:45:50 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 15 Apr 2026 20:45:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8492d04f645da2decadc32bc63c3fcd05d8f7c28553aadfe04e799ba45c29d8c`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e60aa43f91918a9a7a4df219bea9455874a63706a75cf32d58fb44d407bc8c`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 1.5 MB (1509470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4252558202f8120684a17557867dc1daa4b644a3a72f3e33ed80a552bdf8401`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 933.7 KB (933651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba13ae45bcfd5b436e368eeb596d4f68f12ca67d0744aa6640f8ef5eff144560`  
		Last Modified: Wed, 15 Apr 2026 20:46:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337e87e1b497771012cbdfffcf86b0d63ee602e27ea03395f3a6bc611e3860a4`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e136f956bcd522a73a0a5dc40ad53b3b1068f38e705aba7131797b3e08a6e961`  
		Last Modified: Wed, 15 Apr 2026 20:46:37 GMT  
		Size: 305.7 MB (305725123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c085ac393e2a8e2a0a4c6340147582e59210c6efad827487dc7b86c64f801c3a`  
		Last Modified: Wed, 15 Apr 2026 20:46:30 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:9d6266906b6434f5d65ca8288c95b4d9eb69a33b636d354478296aca90ea4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cf19a25a2732602b52b7b721e8342c98ed085ada8f13a4c7d355a11c08fabd`

```dockerfile
```

-	Layers:
	-	`sha256:65eb9fab83ebf4e1b40e3d79530a4a3c32e5753cc37230047a1393dfe7b544af`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 2.7 MB (2661252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea25dafc37e6814e4a727564960e3b363e702058c0f0a81794a3c8a94094d948`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 28.7 KB (28736 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:feaab4061b34d3c6eb97afa5d89c4aebfd74914744c4c2016bc6ca78303e27f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322604121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c89596a639978ad5954484e9bb812c9a937f16413b71e70dfd06b873697f6e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:45:10 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 15 Apr 2026 20:45:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:45:32 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:45:32 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 15 Apr 2026 20:45:32 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 15 Apr 2026 20:45:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:45:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:45:32 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 15 Apr 2026 20:45:32 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 15 Apr 2026 20:45:32 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 15 Apr 2026 20:45:32 GMT
ENV MONGO_MAJOR=8.2
# Wed, 15 Apr 2026 20:45:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Wed, 15 Apr 2026 20:45:32 GMT
ENV MONGO_VERSION=8.2.6
# Wed, 15 Apr 2026 20:45:55 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 15 Apr 2026 20:45:55 GMT
VOLUME [/data/db /data/configdb]
# Wed, 15 Apr 2026 20:45:55 GMT
ENV HOME=/data/db
# Wed, 15 Apr 2026 20:45:55 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 15 Apr 2026 20:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:45:55 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 15 Apr 2026 20:45:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63c163c3d5474b7e207b8fc413794164faf0a4b5ddc7bd71892e50f0302496b`  
		Last Modified: Wed, 15 Apr 2026 20:46:30 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c500879dd728a2e1abf3a592d0f242d6be5e802f68bd33c1ea4f42c618f82c9a`  
		Last Modified: Wed, 15 Apr 2026 20:46:30 GMT  
		Size: 1.5 MB (1494534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a47f4d9ec4c7c9c2c7befe4450766ff8594de808a4ea52f61d4ec1d6214c7e`  
		Last Modified: Wed, 15 Apr 2026 20:46:30 GMT  
		Size: 886.1 KB (886075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba13ae45bcfd5b436e368eeb596d4f68f12ca67d0744aa6640f8ef5eff144560`  
		Last Modified: Wed, 15 Apr 2026 20:46:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9577b2a99da2ce66f4631f0803a359ffa1b32d48b3c37905424e52896284433e`  
		Last Modified: Wed, 15 Apr 2026 20:46:31 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b748d04050ae5c0836680368d67a4ba07c83dc49c8b143ad43add65f3d1311b6`  
		Last Modified: Wed, 15 Apr 2026 20:46:39 GMT  
		Size: 291.3 MB (291341132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdb4b8bb08c66450956854a6e435e386bc9327023236cee2efd2ec608f4aee7`  
		Last Modified: Wed, 15 Apr 2026 20:46:32 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:af253f0c737450eb53c9257cdacc0765d9e3c7fcb1d3fae1c9cb70f4eb9373a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170792cd2e39c21e9b929ea5213952f9549d3a993f37b4f392bdb94cc3cef7d4`

```dockerfile
```

-	Layers:
	-	`sha256:43ef8e1546fc1d804c1e8bc970304643430e6e8a3f6e2be674b484d53a3a75b3`  
		Last Modified: Wed, 15 Apr 2026 20:46:30 GMT  
		Size: 2.7 MB (2662388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931a6c26e85e711a32d104f6f861f397101bb6ff1fb853ec7b913653a4766e17`  
		Last Modified: Wed, 15 Apr 2026 20:46:30 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.32690; amd64

```console
$ docker pull mongo@sha256:b04a31ee394275c9f2e3f1518353262f1a44d94e3ae91a6a1706a10219b7dc8b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2947256507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0fba07e02e8b0b97cf6a2cbf788c70aa200704cf84868410ba4d1eb45935f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:12:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:12:36 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 14 Apr 2026 21:12:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.6-signed.msi
# Tue, 14 Apr 2026 21:12:37 GMT
ENV MONGO_DOWNLOAD_SHA256=a6672561354b1bd37c5ba8d7dd76b66bfdbd28baec6fd8eb2b7eb2b32eaf344f
# Tue, 14 Apr 2026 21:14:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:14:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Apr 2026 21:14:32 GMT
EXPOSE 27017
# Tue, 14 Apr 2026 21:14:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93dfb163be42a2c9d7f691b0d7d60196bb56525fae130c10464d1aded18eff1`  
		Last Modified: Tue, 14 Apr 2026 21:14:45 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d691c6ce6102c38d975341234ae6cce051b08aee0c7e50e3d5e4304c17433d`  
		Last Modified: Tue, 14 Apr 2026 21:14:45 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f8948060fd5bbbaaa4091db122a4eed10081b8ffa59d0692071360897eeb9`  
		Last Modified: Tue, 14 Apr 2026 21:14:45 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44075d631fbf717ac1f0023d83380b72f98e0e34963c1361497a5bbe4af63db3`  
		Last Modified: Tue, 14 Apr 2026 21:14:43 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cb2d05daec8d7a4de15f5cc9083fe1bc10cacf395d30188ab506710fc1e6f8`  
		Last Modified: Tue, 14 Apr 2026 21:16:03 GMT  
		Size: 817.3 MB (817261289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a79e9aac3ae30da683c9b33ffb23c467909251c098570e0873cc998d29797e`  
		Last Modified: Tue, 14 Apr 2026 21:14:43 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6e28d8d2b34bf3f77d9475a73e83e675de2994ef9120ae0baaaad9e45a63d7`  
		Last Modified: Tue, 14 Apr 2026 21:14:43 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef20b7fbd97b9fdd9d51ccd1c8758618fae8e8f08312a28faa7a8d7a03996625`  
		Last Modified: Tue, 14 Apr 2026 21:14:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.5020; amd64

```console
$ docker pull mongo@sha256:3f96f8486bc6b643a5c4e76373a8cb43a9d5046daee6bbc26a20bf00d60ccdcb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2887469915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663bfc3bfc5206a1e842509e34dcdddfb69715fbb48e2e7ab6fcee0661393883`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:21:36 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 14 Apr 2026 21:21:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.6-signed.msi
# Tue, 14 Apr 2026 21:21:37 GMT
ENV MONGO_DOWNLOAD_SHA256=a6672561354b1bd37c5ba8d7dd76b66bfdbd28baec6fd8eb2b7eb2b32eaf344f
# Tue, 14 Apr 2026 21:23:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:23:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Apr 2026 21:23:19 GMT
EXPOSE 27017
# Tue, 14 Apr 2026 21:23:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2f0eb5446c500384b621e6e7e04325997102ef3e1039b7b7fef6b8f62f8a06`  
		Last Modified: Tue, 14 Apr 2026 21:23:33 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c088d5819c4520f394f081378a64a8dd28b441c64029ca053f982e9d9db4b3`  
		Last Modified: Tue, 14 Apr 2026 21:23:33 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11200cad54e65f431b5c6f487bfe512b713beb23a9fa386a2c6dc8faffbe4cb`  
		Last Modified: Tue, 14 Apr 2026 21:23:32 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6313fe9d921f5b93012deeca6ba6cc72f12f370c5d8c33bf630547672eea23`  
		Last Modified: Tue, 14 Apr 2026 21:24:44 GMT  
		Size: 817.2 MB (817249416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c67b2556d2cbde34b53db68053d78acf3aaac358426c656a9ab0a62efd77a81`  
		Last Modified: Tue, 14 Apr 2026 21:23:32 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adacb9155c7fb600f3deb90d72dbfa3e5ee722156790a43298e954360e1f943`  
		Last Modified: Tue, 14 Apr 2026 21:23:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec7350e308faad11933819e7ecfb30275d2f00ab577c6bf385a21c83b94b0be`  
		Last Modified: Tue, 14 Apr 2026 21:23:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
