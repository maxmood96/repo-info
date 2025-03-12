## `mongo:latest`

```console
$ docker pull mongo@sha256:36f9c7390e7fdc734501d7797a88b9b661c1f0d1d2a64a1706dfb6ae3ffcef04
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
$ docker pull mongo@sha256:90bf5066fed8a3cd59345d963922bc5cb557d4b4b2a0e38dfd9ee299c405741b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288216075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6551ff2e441be3fc2daa18db66670724e9e822ca116dd3af668a6a9f44c30126`
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
# Fri, 21 Feb 2025 23:01:38 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 23:01:38 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 21 Feb 2025 23:01:38 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 21 Feb 2025 23:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2025 23:01:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2025 23:01:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2025 23:01:38 GMT
ENV MONGO_MAJOR=8.0
# Fri, 21 Feb 2025 23:01:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
ENV MONGO_VERSION=8.0.5
# Fri, 21 Feb 2025 23:01:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2025 23:01:38 GMT
ENV HOME=/data/db
# Fri, 21 Feb 2025 23:01:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 23:01:38 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 21 Feb 2025 23:01:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073d1958f55c99f79f29d0193ba093f3829cd589ed174eea074fae0da55adb1a`  
		Last Modified: Mon, 24 Feb 2025 21:28:22 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25459f85dd50ffcefede34e1369c35dbb79a245515f35c76403f38fe2543d197`  
		Last Modified: Mon, 24 Feb 2025 21:28:22 GMT  
		Size: 3.9 MB (3911238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9aeb311ccdaa6051cf33564184ee80f4ca83873fde648d891de8da0e587705`  
		Last Modified: Mon, 24 Feb 2025 21:28:22 GMT  
		Size: 1.1 MB (1130250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8760a65b52ab4bfb2315899f6a6928ab94ba5be96489cc90297efae76061d5f`  
		Last Modified: Mon, 24 Feb 2025 21:28:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39481ab08cccae3501eefdef6129194e805d9c95a07e2c310718322c876334`  
		Last Modified: Mon, 24 Feb 2025 21:28:23 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f86bfbfe73e1a83803225ea0a49a345bc2cdb8eeb69cb588f7ff10bf421acc`  
		Last Modified: Mon, 24 Feb 2025 21:28:26 GMT  
		Size: 253.4 MB (253413705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47c58be646c2b27e1e3a24bf3cdc6ee1ad5b2f846703554db240e2890073c87`  
		Last Modified: Mon, 24 Feb 2025 21:28:23 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:e25e0fa7d00c64399ae581db9ce2fde1454326457ed2ec4b36f58816f4b58d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4825f18c2885c288cb5707124f52cdd8a2b33979a9d2147bcb609953e0497325`

```dockerfile
```

-	Layers:
	-	`sha256:94a60faa6acfc7f092d3ce9f411bea81588591046755c39200aac25033fe4f4d`  
		Last Modified: Mon, 24 Feb 2025 21:28:22 GMT  
		Size: 2.5 MB (2524379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba76b1787c994d0ecb7c95f41a7314d12ee9ae222467f376bb820b5ef0bcacb0`  
		Last Modified: Mon, 24 Feb 2025 21:28:22 GMT  
		Size: 28.6 KB (28572 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:c5d1e8db534ca5dea22c809589714f738a384f8a2dbf0469a77342288876175c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274238555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6d86eb68b25c724e795b32bc341fb5643be4a7963d7ea442c34cbbc1b5cbfa`
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
# Fri, 21 Feb 2025 23:01:38 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Feb 2025 23:01:38 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 21 Feb 2025 23:01:38 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 21 Feb 2025 23:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2025 23:01:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2025 23:01:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2025 23:01:38 GMT
ENV MONGO_MAJOR=8.0
# Fri, 21 Feb 2025 23:01:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
ENV MONGO_VERSION=8.0.5
# Fri, 21 Feb 2025 23:01:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2025 23:01:38 GMT
ENV HOME=/data/db
# Fri, 21 Feb 2025 23:01:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Feb 2025 23:01:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2025 23:01:38 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 21 Feb 2025 23:01:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce75871616d1f040379b78f076d89ecfea3f19b84e1ba96411ee0e9088684dec`  
		Last Modified: Fri, 07 Feb 2025 02:36:53 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ba4872ad7795f2c8f784298bdb31c787b73e30b1fdc5d581adc5b5f1dca61`  
		Last Modified: Fri, 07 Feb 2025 02:36:53 GMT  
		Size: 1.5 MB (1492039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e9bd428fd6ae2addcf889b66fd8b4864dcfaffe9c610cb1605901c11af0a40`  
		Last Modified: Mon, 24 Feb 2025 21:28:35 GMT  
		Size: 1.1 MB (1060554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e25f36ba94aaca670f9bffd49034edbae656d38e4a99ff7208f9a63409c794`  
		Last Modified: Mon, 24 Feb 2025 21:28:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7f6a3c999cf94263c5e9f1be3811066f672ba3ede5591f53a03ed15bec066e`  
		Last Modified: Mon, 24 Feb 2025 21:28:35 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fa30252f0cba92fdc3c1b408e5ecffcde538a42fc7bc12a8f6aa2593f2b6a8`  
		Last Modified: Mon, 24 Feb 2025 21:28:40 GMT  
		Size: 242.8 MB (242785767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d3e5e25e5ec02676f30d3b24522a6a8f902f3b0f5d00b7c518a05db616848`  
		Last Modified: Mon, 24 Feb 2025 21:28:36 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:2c7214e9c1a3abd63c3bbc9c49e92091ffad827932fafe2dfab14e57797d71c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4195549986751826af020b09db49af439e742e05a60275c57d41ab7e5144a026`

```dockerfile
```

-	Layers:
	-	`sha256:58f58badef43a381bf76e3c2a62269fa65ca10627c3b5f6a62e2f82dde5e1cb8`  
		Last Modified: Mon, 24 Feb 2025 21:28:35 GMT  
		Size: 2.5 MB (2525515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb90724356d2dd4d408bb04f0c9328e49185b118fed43391add6194b753349c6`  
		Last Modified: Mon, 24 Feb 2025 21:28:35 GMT  
		Size: 28.8 KB (28799 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - windows version 10.0.26100.3476; amd64

```console
$ docker pull mongo@sha256:bcbdfaa4aa89b79f70dc3b42ef6a5baa7f83e0aa81e5c0ffe88f69a729969c7a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3679590024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5f3c80ca136fe41cfbdec9af0fd64c85f69f7330a966568ab0941a4c64fca1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:55:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Mar 2025 18:55:52 GMT
ENV MONGO_VERSION=8.0.5
# Wed, 12 Mar 2025 18:55:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Wed, 12 Mar 2025 18:55:54 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Wed, 12 Mar 2025 18:57:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:57:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 18:57:30 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 18:57:31 GMT
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
	-	`sha256:6d8689654cd3363bfdbdeaaef6e0306180d3288489791eb3e70f46d8cc14296e`  
		Last Modified: Wed, 12 Mar 2025 18:57:38 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0519fb0ad7c5515d2ac0f10143923eb12fe3b4bf58495d925dd96816d15e1ee3`  
		Last Modified: Wed, 12 Mar 2025 18:57:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f593b27298c702e7baf4b46edd22b4dfc8678001e639bf19ab41bd646a4f7e4f`  
		Last Modified: Wed, 12 Mar 2025 18:57:38 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4247a1ea48f875cc1eba636038bfc127dd01d930b48684c926fe4f775e008e48`  
		Last Modified: Wed, 12 Mar 2025 18:57:36 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c750098b5feeda305cee71dc09614cd442610f08c1194357da29a88526bfdb`  
		Last Modified: Wed, 12 Mar 2025 18:58:49 GMT  
		Size: 770.9 MB (770933175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5cac45a1670d173e29fb6bf00c9176375175b75e2b63823f9f0971299274c2`  
		Last Modified: Wed, 12 Mar 2025 18:57:36 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2614739c08b40cfda11aa3e87ad499a32aaf3db3b72e0cc1264e17d4d400e4`  
		Last Modified: Wed, 12 Mar 2025 18:57:36 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5c5f94695e8712737f8083fcf8e13bdb8c6c02c11cfbd5eb52f55a3b785391`  
		Last Modified: Wed, 12 Mar 2025 18:57:36 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:651cec05973d7dcb5d1c8a77d78b72af881f6110ff626609eba3adc4ad1c4ff0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3040912786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a22597d8ad42488c8dea3bc36a559c96adddd1235b7eb6429d63a5f9303569`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:57:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Mar 2025 18:57:19 GMT
ENV MONGO_VERSION=8.0.5
# Wed, 12 Mar 2025 18:57:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Wed, 12 Mar 2025 18:57:21 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Wed, 12 Mar 2025 18:58:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:58:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 18:58:37 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 18:58:37 GMT
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
	-	`sha256:8ed6fec1b72c7a8b9a20653ed52d07f80d2cbec46367070f4dcaf8fe6be4b299`  
		Last Modified: Wed, 12 Mar 2025 18:58:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bcb4c153ff0f5490c331c6ff1830b2af1fb6594d7a87b00e86552c99e39df4`  
		Last Modified: Wed, 12 Mar 2025 18:58:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b90637bafa2ee45112e83d0c8b0ee6092db2304c5abda456ae43cb436c64c`  
		Last Modified: Wed, 12 Mar 2025 18:58:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5364e60d76403098f67e8935b682f87dcabb8b88e28aa9445df9796609486f`  
		Last Modified: Wed, 12 Mar 2025 18:58:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402034f52dd8075f4758aefcb5662043cc9c9b3beaea2f978a9ba326bbdfa1af`  
		Last Modified: Wed, 12 Mar 2025 18:59:43 GMT  
		Size: 771.0 MB (770962633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c895d11ad1e8f434e31ed666a80f0557ed2da28efea16e23412d088f986cf1`  
		Last Modified: Wed, 12 Mar 2025 18:58:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3ea8843243f89cdc7302b1e39aa67ef10f4565568fdefdef177c5ba3304aed`  
		Last Modified: Wed, 12 Mar 2025 18:58:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243636056b5ce394b33cdc686963ea624e388a5f7941c8f10b9813921123d03f`  
		Last Modified: Wed, 12 Mar 2025 18:58:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.7009; amd64

```console
$ docker pull mongo@sha256:3f57eb98b9303eb09911d44bcd155add658a44875df2166dfafff31938b8e594
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2922613619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a278ce02561551ba81c592301b052c494beb28b72f3fe95072a7c0de57df59`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 19:05:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Mar 2025 19:05:48 GMT
ENV MONGO_VERSION=8.0.5
# Wed, 12 Mar 2025 19:05:49 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Wed, 12 Mar 2025 19:05:50 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Wed, 12 Mar 2025 19:08:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 19:08:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 19:08:15 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 19:08:16 GMT
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
	-	`sha256:92885e0ad298d1c4e119bb89bc215c637da1b6c58f77c2bfc1b7fdc33c8f4096`  
		Last Modified: Wed, 12 Mar 2025 19:08:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98018c54fc665174a29dbc3d57a4fba95c4ed94b8eb0e6b1fb8c8ae2ac0078c6`  
		Last Modified: Wed, 12 Mar 2025 19:08:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4ec7c6a78a1fe08458e82b3fedf8b2be8166e132e30031f207fd904c07023f`  
		Last Modified: Wed, 12 Mar 2025 19:08:19 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba6ee6d015078dd86606505cce63cbdce98f4705cc2889253fa506a924d7262`  
		Last Modified: Wed, 12 Mar 2025 19:08:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cf7071f0cfae96dbdc2128b3ff4540fa59040cc3f38290e26a0d39269fdbab`  
		Last Modified: Wed, 12 Mar 2025 19:09:19 GMT  
		Size: 771.0 MB (770969872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d4ecd36d0ec9501393c570aa7de959eaef2c457ac787c91d07e542a6454d2d`  
		Last Modified: Wed, 12 Mar 2025 19:08:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c57d6763bdaf844d2cd337c8e927fb4b93bee55bc3e430ba6e80dbbe26a4e`  
		Last Modified: Wed, 12 Mar 2025 19:08:18 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c589283b818d125255da5a559a48f936e0bd7541ecdaf03b8eab97d848b2c143`  
		Last Modified: Wed, 12 Mar 2025 19:08:18 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
