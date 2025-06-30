## `mongo:latest`

```console
$ docker pull mongo@sha256:b2b90af3588fb4d71c341b1a9ce959e5ab55b3c34305130cfb88c157dac39ea8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:36b635a2c326c5ae9e8dadbc5ebc049e9cd558922ae917a01ce06e12e43ccd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294514885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c9136943ecb81c1544a4d3afef94443d65ab2d82a48b52cde58eeba5151ff5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 22:01:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 27 Jun 2025 22:01:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 27 Jun 2025 22:01:28 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 27 Jun 2025 22:01:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 27 Jun 2025 22:01:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 27 Jun 2025 22:01:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 27 Jun 2025 22:01:28 GMT
ENV MONGO_MAJOR=8.0
# Fri, 27 Jun 2025 22:01:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
ENV MONGO_VERSION=8.0.11
# Fri, 27 Jun 2025 22:01:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 27 Jun 2025 22:01:28 GMT
ENV HOME=/data/db
# Fri, 27 Jun 2025 22:01:28 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 27 Jun 2025 22:01:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jun 2025 22:01:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 27 Jun 2025 22:01:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4571ac1d3a10a6231ed52e953e938c11ad0253e459132d3432cfc2e16f8220a8`  
		Last Modified: Mon, 30 Jun 2025 17:28:53 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e425286ed2b102effaefdcc9012dc21225fe176aaddb1c143aad656d4fa2871`  
		Last Modified: Mon, 30 Jun 2025 17:28:53 GMT  
		Size: 1.5 MB (1508653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0c8fcacf7be71760be011d83bdd8d25cb12528ebb467c7959694ba2212db63`  
		Last Modified: Mon, 30 Jun 2025 17:28:53 GMT  
		Size: 1.1 MB (1131218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971fe30beb07288d0457e85a05c4a5efaaf287445016674213f6586efe8fbf1d`  
		Last Modified: Mon, 30 Jun 2025 17:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11a059ad1fb76bffe224c52609831f616b58070f812312a2a1efe7c156c8258`  
		Last Modified: Mon, 30 Jun 2025 17:28:55 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e3f4eaac3828763158c21300e6a7263ec5ee83b6ded9a7e9b09aeea8092d7`  
		Last Modified: Mon, 30 Jun 2025 19:07:54 GMT  
		Size: 262.2 MB (262153081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4599e773bec2626ccd156dd35edabe3f90b3daeb13c6bb8715bd88dc52e9100d`  
		Last Modified: Mon, 30 Jun 2025 17:28:53 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:b22cfc3a1b19da69473265960302c854c581c58bd5aecf4e131bedff80a90faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3e401a5959b0be184e8a462f6ee068a0e7c3229be4c73d69d1abe9de0aefbb`

```dockerfile
```

-	Layers:
	-	`sha256:d5272370c148bff30f48020879b87527786b7445245ac1347c6b439ef81bad92`  
		Last Modified: Mon, 30 Jun 2025 19:07:43 GMT  
		Size: 2.7 MB (2666250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21a697f0d6d502091e4f12ed07550b1340deced516a323035ea3b04744488724`  
		Last Modified: Mon, 30 Jun 2025 19:07:44 GMT  
		Size: 28.8 KB (28845 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:6fa3d345401315f447040b4c8a38f08b70c15817984c5dd1c993666f7a3356d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282527031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a0c3f910339ff6e459a4b02505e223ff4e58242b20e44bf887ec3556728b54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 22:01:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 27 Jun 2025 22:01:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 27 Jun 2025 22:01:28 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 27 Jun 2025 22:01:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 27 Jun 2025 22:01:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 27 Jun 2025 22:01:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 27 Jun 2025 22:01:28 GMT
ENV MONGO_MAJOR=8.0
# Fri, 27 Jun 2025 22:01:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
ENV MONGO_VERSION=8.0.11
# Fri, 27 Jun 2025 22:01:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 27 Jun 2025 22:01:28 GMT
ENV HOME=/data/db
# Fri, 27 Jun 2025 22:01:28 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 27 Jun 2025 22:01:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 27 Jun 2025 22:01:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jun 2025 22:01:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 27 Jun 2025 22:01:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aeb30c1936327beb2d8c7294c7af53522b6cc4b18535767d174b9b050ab8e0`  
		Last Modified: Mon, 30 Jun 2025 17:42:37 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a613b2781ab9da7f2ddde5c25713f8df062cb2d9ed7c694f0e50ea9e251fc58`  
		Last Modified: Mon, 30 Jun 2025 17:42:37 GMT  
		Size: 1.5 MB (1493064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb56e6628065442735aaa53e7e2cc2bc6f9e0b6fbfacf9e66c9493566d39386f`  
		Last Modified: Mon, 30 Jun 2025 17:42:37 GMT  
		Size: 1.1 MB (1061555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1749dfbe23dda937bf2a3a122d78c4db2782181533e2db08f9b99c8107e64f59`  
		Last Modified: Mon, 30 Jun 2025 17:42:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56db87df78269065c101337684e74cb4cda4eba27c8dd4c6c3b409bdb297a827`  
		Last Modified: Mon, 30 Jun 2025 17:42:37 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf7a6d1bde0e229e1d72d57456f27b146e41d3503376530aa66a159ac15c330`  
		Last Modified: Mon, 30 Jun 2025 18:10:55 GMT  
		Size: 251.1 MB (251113917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002d3ec25f05d3f0fcf757557c14614725ced80d598bc593c2550f1de1c5af73`  
		Last Modified: Mon, 30 Jun 2025 17:42:37 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:0b54bd61e62e5612c2dcb777ef23a471801ea389ee51534c09cb2239efecf5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5383cc6452031e1f296ab9ff370fdd1b4c92a22ffb87b2cba1d45f2cd4456694`

```dockerfile
```

-	Layers:
	-	`sha256:428ed3b2aa0a46847ada7778e6a465c612a01bf7f6d3a175c34bfbf12006ca7b`  
		Last Modified: Mon, 30 Jun 2025 19:07:48 GMT  
		Size: 2.7 MB (2667386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81602fd0a5f2a8645babb3767b7bf9994bd361fa5881593b5d898c2ec1a2b230`  
		Last Modified: Mon, 30 Jun 2025 19:07:49 GMT  
		Size: 29.1 KB (29072 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.4349; amd64

```console
$ docker pull mongo@sha256:2703cf0993abc144663c20313e88b33cf4e9e860c1e6fa4a4809f9a0d22c5ba6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 GB (4251851313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a52abbc57440e30a1b35f20b12b3830930ba0a3273e2fb0b0099c7fd66e3b8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 30 Jun 2025 17:33:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 30 Jun 2025 17:33:13 GMT
ENV MONGO_VERSION=8.0.11
# Mon, 30 Jun 2025 17:33:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.11-signed.msi
# Mon, 30 Jun 2025 17:33:15 GMT
ENV MONGO_DOWNLOAD_SHA256=887b2869804fec5f7412f4d848ab6bc587819fb2ee1ab49e2fac1538ccc53a91
# Mon, 30 Jun 2025 17:34:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 30 Jun 2025 17:34:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 30 Jun 2025 17:34:53 GMT
EXPOSE 27017
# Mon, 30 Jun 2025 17:34:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f289ccf36d787faff6667c77f87af5179c559808ee0632a728adf03d3454e4`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd1fe1d6af42cb0a7c67b8cf90ad69dd4d0ec9ff9ce5c26552108eb9bb34e7a`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9100df697eaac84a7d5d28c969859ca63dc83d83d4c7f902cf1fd01696e9f927`  
		Last Modified: Mon, 30 Jun 2025 17:38:30 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400bffd8dffbe95e8e2bb4f0cdfd27ed4da443c56ee97cf9033ebaefaa1089c6`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facf0f50a22d2f6ff761476fd2a884addc86e009f5986150bbec985aac93755c`  
		Last Modified: Mon, 30 Jun 2025 19:08:27 GMT  
		Size: 775.7 MB (775668039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6796d33b1d1578fd8e3b2279fd46f60b6f5a6f9b8704eee6f1e9e3155df8f0`  
		Last Modified: Mon, 30 Jun 2025 17:38:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046a4054c3279ed4cc552e15e60bb13fd8a26ea236cdacaee9ef2de8bd2ff950`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5798a3979f776055a136b6218d149825bd5cd50ccc2416f2f601a2d1f277f`  
		Last Modified: Mon, 30 Jun 2025 17:38:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.3807; amd64

```console
$ docker pull mongo@sha256:54d8bb048b8810ca92f8e4bced97a98382b3eeba4e67567af52624d29d5f18f8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3055879801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f455d0fc0b2bbe396880ecf71422304e0823db1cb60e098032ab6752319210`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Mon, 30 Jun 2025 17:27:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 30 Jun 2025 17:27:23 GMT
ENV MONGO_VERSION=8.0.11
# Mon, 30 Jun 2025 17:27:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.11-signed.msi
# Mon, 30 Jun 2025 17:27:24 GMT
ENV MONGO_DOWNLOAD_SHA256=887b2869804fec5f7412f4d848ab6bc587819fb2ee1ab49e2fac1538ccc53a91
# Mon, 30 Jun 2025 17:28:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 30 Jun 2025 17:28:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 30 Jun 2025 17:28:45 GMT
EXPOSE 27017
# Mon, 30 Jun 2025 17:28:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f719d54f40344d1f06ae72ea3d918295e9070130c07b6b67a23ecd457abcf2`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf5ac817fd80b4bcb5442cd3e27188a9709b7df446e510df175eaef0171333f`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8177af34a2a0a2735dc40be6a7189d5854c2e8be271550cabfbd3af50c2f9624`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcda42e73cbf2d3676f05a32d0b7e3fbeef49935203b6d3a8a2325d03e2bd4a3`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c18b7acfe7c9364937692224bdbf0bfe4f2e1611fb572e3c204b1325cb80e9`  
		Last Modified: Mon, 30 Jun 2025 17:36:53 GMT  
		Size: 775.6 MB (775619222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e69835ec0dff50ac4476db553949e116c13ec27a1499772ce18034ec2dd475`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c22e6b0a404b0082f6274e06fa0f4a8975e1a54bbbf32e0c07073769d3ce4e`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6526556be0e00104bb9641575b698a32747333be17472aba87d960e448201d0`  
		Last Modified: Mon, 30 Jun 2025 17:29:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
