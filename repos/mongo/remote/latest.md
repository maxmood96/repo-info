## `mongo:latest`

```console
$ docker pull mongo@sha256:8565ecda5b221016d70f7745ac1ba0b97ccb05836157f8a343e987338fdc8350
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
$ docker pull mongo@sha256:4c51695374825d8b9ac756bb5113a120907071f0a9a8281d4edd5d5ac233c0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274359738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c09d23ad5d9004353bfb846e1fe884ffd5907a4e5d805e9605e73b1c2e2b09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 25 Oct 2024 04:15:38 GMT
ARG RELEASE
# Fri, 25 Oct 2024 04:15:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 25 Oct 2024 04:15:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 25 Oct 2024 04:15:38 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 25 Oct 2024 04:15:38 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Fri, 25 Oct 2024 04:15:38 GMT
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d73348b9ac0bf73865b9376ac0af4522db586a2a827598851035bfff4bc5ac9`  
		Last Modified: Tue, 03 Dec 2024 02:31:54 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1309d231648328adf35da09276e1c59a7f40217b0ed5011f218d6d032e5566`  
		Last Modified: Tue, 03 Dec 2024 02:31:54 GMT  
		Size: 1.5 MB (1507478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bde7d374c09583fac61f3d35d8725365492b64372b81e2a38b114944c6165c`  
		Last Modified: Tue, 03 Dec 2024 02:31:54 GMT  
		Size: 1.1 MB (1129927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0eb01246c7bacf40eef2ae80973baddce1131fd323c60f40b95838747fddbb`  
		Last Modified: Tue, 03 Dec 2024 02:31:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b3dabec753bd46e6e92e445fcbdd03f75adbce0101dd4caa2d5437f7d6012b`  
		Last Modified: Tue, 03 Dec 2024 02:31:54 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606fc5459f651e8ded47524d87aa1d57b9708df4fb160da2b7a8c49de0b6a48`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 242.0 MB (241963774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f50be4b980b0b98bcf4e66ef825a498ccb01c1bd9703751522391fda46de427`  
		Last Modified: Tue, 03 Dec 2024 02:31:55 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:20501bd156ebbe3ccd85b8c40e45e701d450baa7b3d9e92a18a4bc64a6365454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424875422d98c81d4a5fdba02d5c86ce99ce47c2a00cf41449679a5067cf5f8c`

```dockerfile
```

-	Layers:
	-	`sha256:6c3b81b7dfdc633e0fb4f90bdeb6a8502f317d06f59ad91bbc38b6e250734665`  
		Last Modified: Tue, 03 Dec 2024 02:31:54 GMT  
		Size: 2.5 MB (2497837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37304ea25e9644be30c1ffc4d2a3f30b586c90311c169b05f0446df307b845e1`  
		Last Modified: Tue, 03 Dec 2024 02:31:54 GMT  
		Size: 28.6 KB (28572 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:376948c713f4ab001c86f92d7ee560a799179f0dddc50ddcbe94c1b46910b87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263460874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e68e50ac985a9abf42882d28649f5210918029733d0794d59af492ae0189819`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 25 Oct 2024 04:15:38 GMT
ARG RELEASE
# Fri, 25 Oct 2024 04:15:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 25 Oct 2024 04:15:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 25 Oct 2024 04:15:38 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 25 Oct 2024 04:15:38 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Fri, 25 Oct 2024 04:15:38 GMT
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50af98a999ca9179bc6f9f96cff2b6b06de18db2640d1c22668f22607b3fb6aa`  
		Last Modified: Tue, 03 Dec 2024 06:14:00 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2b33d58e9a8050338a63963e7a4d3f199e76f3a82083b53b3eddf6bdcebf38`  
		Last Modified: Tue, 03 Dec 2024 06:14:00 GMT  
		Size: 1.5 MB (1491716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c5b23bf5cf2e4b85b5aa1d3cd7ea65fd9991be6d569a37036ccf5faca7b4b9`  
		Last Modified: Tue, 03 Dec 2024 06:15:17 GMT  
		Size: 1.1 MB (1060184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216f2761441aa3521e82846a06397d71b1d3412600a7ac411231adc34ee87524`  
		Last Modified: Tue, 03 Dec 2024 06:15:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075a696718bbbc686430ac5b0d2a17ebf9159f95a3d5a741df57d52658b338c8`  
		Last Modified: Tue, 03 Dec 2024 06:15:17 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c327374e39ba4afb6b851469a6bff0f1e7c9a82154797dea6c47e60325ae9558`  
		Last Modified: Tue, 03 Dec 2024 06:15:25 GMT  
		Size: 232.0 MB (232009709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189437efbe9d1f5141da892ab63ce2e8804a24d33f30b1f4a52f1aef90ea596`  
		Last Modified: Tue, 03 Dec 2024 06:15:18 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:latest` - unknown; unknown

```console
$ docker pull mongo@sha256:88c42e41c69081b37c55cc52e59a1c25ee9b881a58f9d500db1a1451febdfbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb7c99d399737d5fc2644e5176f68492adc7b79395c6632d8498b4e695ee067`

```dockerfile
```

-	Layers:
	-	`sha256:c1e089a6ffbfc51063dbaea0021367e8bef25c279802a65649cccb21947ad6d2`  
		Last Modified: Tue, 03 Dec 2024 06:15:18 GMT  
		Size: 2.5 MB (2498973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0d6483f92deed6aa6ec308ccacaf5985621509aed49bac6c31c8f63d6c5596`  
		Last Modified: Tue, 03 Dec 2024 06:15:17 GMT  
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
