<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `tomee`

-	[`tomee:11-jre-8.0.1-microprofile`](#tomee11-jre-801-microprofile)
-	[`tomee:11-jre-8.0.1-plume`](#tomee11-jre-801-plume)
-	[`tomee:11-jre-8.0.1-plus`](#tomee11-jre-801-plus)
-	[`tomee:11-jre-8.0.1-webprofile`](#tomee11-jre-801-webprofile)
-	[`tomee:7`](#tomee7)
-	[`tomee:7.0`](#tomee70)
-	[`tomee:7.0.7-plume`](#tomee707-plume)
-	[`tomee:7.0.7-plus`](#tomee707-plus)
-	[`tomee:7.1`](#tomee71)
-	[`tomee:7.1.2-microprofile`](#tomee712-microprofile)
-	[`tomee:7.1.2-plume`](#tomee712-plume)
-	[`tomee:7.1.2-plus`](#tomee712-plus)
-	[`tomee:7.1.2-webprofile`](#tomee712-webprofile)
-	[`tomee:8`](#tomee8)
-	[`tomee:8.0.1-microprofile`](#tomee801-microprofile)
-	[`tomee:8.0.1-plume`](#tomee801-plume)
-	[`tomee:8.0.1-plus`](#tomee801-plus)
-	[`tomee:8.0.1-webprofile`](#tomee801-webprofile)
-	[`tomee:8-jre-7.0.7-plume`](#tomee8-jre-707-plume)
-	[`tomee:8-jre-7.0.7-plus`](#tomee8-jre-707-plus)
-	[`tomee:8-jre-7.0.7-webprofile`](#tomee8-jre-707-webprofile)
-	[`tomee:8-jre-7.1.2-microprofile`](#tomee8-jre-712-microprofile)
-	[`tomee:8-jre-7.1.2-plume`](#tomee8-jre-712-plume)
-	[`tomee:8-jre-7.1.2-plus`](#tomee8-jre-712-plus)
-	[`tomee:8-jre-7.1.2-webprofile`](#tomee8-jre-712-webprofile)
-	[`tomee:8-jre-8.0.1-microprofile`](#tomee8-jre-801-microprofile)
-	[`tomee:8-jre-8.0.1-plume`](#tomee8-jre-801-plume)
-	[`tomee:8-jre-8.0.1-plus`](#tomee8-jre-801-plus)
-	[`tomee:8-jre-8.0.1-webprofile`](#tomee8-jre-801-webprofile)
-	[`tomee:latest`](#tomeelatest)

## `tomee:11-jre-8.0.1-microprofile`

```console
$ docker pull tomee@sha256:0ee38fe078d6f8aa43ff6aeeb45f703e0ecc84601a90e1dd2171c8e13b068d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:11-jre-8.0.1-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:3ab05467ca02f5aa3cfe0a342c215ae33b90ffbca66a22bb69d3c2e2a659d193
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172138849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c821aab66976ee48292bf2e684862e494b8b69f325015c32e660e3e86c27f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:46 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 27 Feb 2020 08:04:49 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:49 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:49 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91aa0bb3023839d0d2d04bc80f9bc46ce14a247a408b4777a34e926d54bb007`  
		Last Modified: Thu, 27 Feb 2020 08:07:17 GMT  
		Size: 56.5 MB (56503574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:11-jre-8.0.1-plume`

```console
$ docker pull tomee@sha256:e387e2d48300c3b2dfec84d952eadd9d9bc1dceee34285a4206fac96d62a4cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:11-jre-8.0.1-plume` - linux; amd64

```console
$ docker pull tomee@sha256:f30ffee72c2b6c6851a922bd772e5236d1184dc6e483acb049d4b6dddf1974c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184256537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808cd51e3d8b03a14299c42f90a70595e82db5e58398dace01e6bb5a5ec7c444`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_BUILD=plume
# Thu, 27 Feb 2020 08:04:33 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:34 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:34 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeb5d84f4d81803b183dc5376e3cd34f66c6c7b30c145283201711964ca77a2`  
		Last Modified: Thu, 27 Feb 2020 08:06:57 GMT  
		Size: 68.6 MB (68621262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:11-jre-8.0.1-plus`

```console
$ docker pull tomee@sha256:2307cf49b02b78d171fe7d2b63d199f3d4dec8acef4373d11bd94eb4f93545f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:11-jre-8.0.1-plus` - linux; amd64

```console
$ docker pull tomee@sha256:b8e5289c17d2ed33aab6cb22e59873eb351133d1311dc66fead47a43e5cd9753
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177014505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8732c4ff437250772f8fa01d2a9dd4c3d117481f81a8884aaf3ac71c8d144285`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:38 GMT
ENV TOMEE_BUILD=plus
# Thu, 27 Feb 2020 08:04:41 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:42 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:42 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fea86757d0cf29c2ceb1f8c4079fff294663bcb5b390bb0d16e689fd1e52483`  
		Last Modified: Thu, 27 Feb 2020 08:07:06 GMT  
		Size: 61.4 MB (61379230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:11-jre-8.0.1-webprofile`

```console
$ docker pull tomee@sha256:0ba1c4a769e71061e2fa9cb9db5b9e65c1ae9052e91ed22536348ccc2b68864d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:11-jre-8.0.1-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:5f3d477808ead86cdaa74fa95b8f76fe3042f80db591b00eb1da6e02a48c4f38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157806239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b9bd0a5c8b50f66c6c52dbec3929ea2acfdfcc62d4fbb512367b37c57337de`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:53 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:04:55 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:56 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:56 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453dd84bbe3e765c8e44611703b4bb8bba037185ac6cbf1f916a72fa0185767`  
		Last Modified: Thu, 27 Feb 2020 08:07:24 GMT  
		Size: 42.2 MB (42170964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7`

```console
$ docker pull tomee@sha256:8c4c2a43ffe3fd8bcecc68c0ea48f4aa29750ff26a1a14ee2f4ee58fdd0be1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7` - linux; amd64

```console
$ docker pull tomee@sha256:10912c487b992f481d0ac59ac4e2703f1aa35c4801aa469a962cf75f478c0b1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154388796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eebd3389099c6745005e70f1d9430a0416bfbcbb1aaeafffed2cdbeec07732f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:45 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:03:48 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:48 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:48 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f06f64c2bd96e8e56ae5298c8396cb7b94fc3e2177887829248a1788f807ca`  
		Last Modified: Thu, 27 Feb 2020 08:06:14 GMT  
		Size: 40.5 MB (40460196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.0`

```console
$ docker pull tomee@sha256:3926ae6cad3a19818e0c694576562109f63942c901a39d1fe18618a41f70413f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.0` - linux; amd64

```console
$ docker pull tomee@sha256:2479eb13d7e5a5c93d19578b6c7e9ceb6b041daa761b3d606469a41ed50eb48b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152265546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f125d70dcd73ba47d29701d2678a6514c89e4e9f67671ff255d86415031b00`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:02:53 GMT
ENV TOMEE_VER=7.0.7
# Thu, 27 Feb 2020 08:03:11 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:03:15 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:15 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:15 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de16090c8639840f36416c1a346d4dedeaa2bebb148c9b413f8dc1ec1507c3d9`  
		Last Modified: Thu, 27 Feb 2020 08:05:42 GMT  
		Size: 38.3 MB (38336946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.0.7-plume`

```console
$ docker pull tomee@sha256:b946470eda0683da273cb4e56bef568ded242bd2e5d3d89e44200dab7f6fe8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.0.7-plume` - linux; amd64

```console
$ docker pull tomee@sha256:a46460e19598bdeef6d95632ce2d56175f379cbb6ae7e0e901a5fd0947217d96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176990285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9362dc94b79862d86ff82e29888330d2908d1f79bf74825098c88b831c91f6f7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:02:53 GMT
ENV TOMEE_VER=7.0.7
# Thu, 27 Feb 2020 08:02:53 GMT
ENV TOMEE_BUILD=plume
# Thu, 27 Feb 2020 08:02:57 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:02:57 GMT
USER tomee
# Thu, 27 Feb 2020 08:02:57 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:02:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31e21925d76492e9b062c4f306934eb60c4444480ad9b4d1f4c79a533de32d`  
		Last Modified: Thu, 27 Feb 2020 08:05:17 GMT  
		Size: 63.1 MB (63061685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.0.7-plus`

```console
$ docker pull tomee@sha256:7954b960cf77ca55428d98151e36902974e41dd5b5111d7d46d6820338a85f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.0.7-plus` - linux; amd64

```console
$ docker pull tomee@sha256:d366ed876cc454878e353f9f333619b4aaff178650c87f5c7ddd41e91f8ef5fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169918391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d9f633fa03dcdb26f96cdb02442d3da3d1530897aa568871daf2f451ae70d4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:02:53 GMT
ENV TOMEE_VER=7.0.7
# Thu, 27 Feb 2020 08:03:03 GMT
ENV TOMEE_BUILD=plus
# Thu, 27 Feb 2020 08:03:07 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:07 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:07 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caf114d8b245ccdbc55c9c531c518f219546f5f753f991f04b53c916711c04e`  
		Last Modified: Thu, 27 Feb 2020 08:05:25 GMT  
		Size: 56.0 MB (55989791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1`

```console
$ docker pull tomee@sha256:8c4c2a43ffe3fd8bcecc68c0ea48f4aa29750ff26a1a14ee2f4ee58fdd0be1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1` - linux; amd64

```console
$ docker pull tomee@sha256:10912c487b992f481d0ac59ac4e2703f1aa35c4801aa469a962cf75f478c0b1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154388796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eebd3389099c6745005e70f1d9430a0416bfbcbb1aaeafffed2cdbeec07732f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:45 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:03:48 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:48 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:48 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f06f64c2bd96e8e56ae5298c8396cb7b94fc3e2177887829248a1788f807ca`  
		Last Modified: Thu, 27 Feb 2020 08:06:14 GMT  
		Size: 40.5 MB (40460196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.2-microprofile`

```console
$ docker pull tomee@sha256:779b98a4a9e1612e140f1796a4f9bd96a7bd9f49e63b13c122021467b0eb566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1.2-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:4faa96eb2ff4953016814225a10a33faf2edf1a8b6d1efa3f6103b659a97c382
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154899652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e941ec1399f3564255de7d8a37b8f0a539e025e7d7be2f3c2164872029a3bcc1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:37 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 27 Feb 2020 08:03:40 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:40 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:40 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7c25571d6f1800147cb5e689da9d472311a2ac44f566bd0bedaa1de050d265`  
		Last Modified: Thu, 27 Feb 2020 08:06:07 GMT  
		Size: 41.0 MB (40971052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.2-plume`

```console
$ docker pull tomee@sha256:3cbd3cb29c5105623490073adc780bb54f5a247c7c97fd8967b13df71a879656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1.2-plume` - linux; amd64

```console
$ docker pull tomee@sha256:d16d6eb553f28a5fa1a7bb958e5bf59a27d391f022551834d7d34614ff7fcfb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179042788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee1fad3939f94c448934e3fbedca57bdd66ff9f33608f8182ec85b52cd3ff82`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_BUILD=plume
# Thu, 27 Feb 2020 08:03:24 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:24 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:24 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb9d7e5aafcac712c7456c27142fc53c2d4b741f5e2831571f28c430f1ba3b`  
		Last Modified: Thu, 27 Feb 2020 08:05:51 GMT  
		Size: 65.1 MB (65114188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.2-plus`

```console
$ docker pull tomee@sha256:e88cb0c77802e4bc3fc514626610358788b097e6f60663630a3702520ba22ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1.2-plus` - linux; amd64

```console
$ docker pull tomee@sha256:bef86a595331df7a8d3b303c078bfa61310d1e92f51126b211046478f512e588
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (172008564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545e1c26bc4a1f3b181bd96cf642daf51879355e92f8688b1f3181035c6ec624`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:28 GMT
ENV TOMEE_BUILD=plus
# Thu, 27 Feb 2020 08:03:32 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:32 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:33 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deaa78a5721612c10ed0817f8aa3b9c7d334626a2168694274fb9243e48d4e4`  
		Last Modified: Thu, 27 Feb 2020 08:06:00 GMT  
		Size: 58.1 MB (58079964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.2-webprofile`

```console
$ docker pull tomee@sha256:8c4c2a43ffe3fd8bcecc68c0ea48f4aa29750ff26a1a14ee2f4ee58fdd0be1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1.2-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:10912c487b992f481d0ac59ac4e2703f1aa35c4801aa469a962cf75f478c0b1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154388796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eebd3389099c6745005e70f1d9430a0416bfbcbb1aaeafffed2cdbeec07732f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:45 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:03:48 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:48 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:48 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f06f64c2bd96e8e56ae5298c8396cb7b94fc3e2177887829248a1788f807ca`  
		Last Modified: Thu, 27 Feb 2020 08:06:14 GMT  
		Size: 40.5 MB (40460196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8`

```console
$ docker pull tomee@sha256:0ba1c4a769e71061e2fa9cb9db5b9e65c1ae9052e91ed22536348ccc2b68864d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8` - linux; amd64

```console
$ docker pull tomee@sha256:5f3d477808ead86cdaa74fa95b8f76fe3042f80db591b00eb1da6e02a48c4f38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157806239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b9bd0a5c8b50f66c6c52dbec3929ea2acfdfcc62d4fbb512367b37c57337de`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:53 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:04:55 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:56 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:56 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453dd84bbe3e765c8e44611703b4bb8bba037185ac6cbf1f916a72fa0185767`  
		Last Modified: Thu, 27 Feb 2020 08:07:24 GMT  
		Size: 42.2 MB (42170964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.1-microprofile`

```console
$ docker pull tomee@sha256:0ee38fe078d6f8aa43ff6aeeb45f703e0ecc84601a90e1dd2171c8e13b068d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8.0.1-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:3ab05467ca02f5aa3cfe0a342c215ae33b90ffbca66a22bb69d3c2e2a659d193
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172138849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c821aab66976ee48292bf2e684862e494b8b69f325015c32e660e3e86c27f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:46 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 27 Feb 2020 08:04:49 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:49 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:49 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91aa0bb3023839d0d2d04bc80f9bc46ce14a247a408b4777a34e926d54bb007`  
		Last Modified: Thu, 27 Feb 2020 08:07:17 GMT  
		Size: 56.5 MB (56503574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.1-plume`

```console
$ docker pull tomee@sha256:e387e2d48300c3b2dfec84d952eadd9d9bc1dceee34285a4206fac96d62a4cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8.0.1-plume` - linux; amd64

```console
$ docker pull tomee@sha256:f30ffee72c2b6c6851a922bd772e5236d1184dc6e483acb049d4b6dddf1974c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184256537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808cd51e3d8b03a14299c42f90a70595e82db5e58398dace01e6bb5a5ec7c444`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_BUILD=plume
# Thu, 27 Feb 2020 08:04:33 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:34 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:34 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeb5d84f4d81803b183dc5376e3cd34f66c6c7b30c145283201711964ca77a2`  
		Last Modified: Thu, 27 Feb 2020 08:06:57 GMT  
		Size: 68.6 MB (68621262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.1-plus`

```console
$ docker pull tomee@sha256:2307cf49b02b78d171fe7d2b63d199f3d4dec8acef4373d11bd94eb4f93545f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8.0.1-plus` - linux; amd64

```console
$ docker pull tomee@sha256:b8e5289c17d2ed33aab6cb22e59873eb351133d1311dc66fead47a43e5cd9753
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177014505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8732c4ff437250772f8fa01d2a9dd4c3d117481f81a8884aaf3ac71c8d144285`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:38 GMT
ENV TOMEE_BUILD=plus
# Thu, 27 Feb 2020 08:04:41 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:42 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:42 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fea86757d0cf29c2ceb1f8c4079fff294663bcb5b390bb0d16e689fd1e52483`  
		Last Modified: Thu, 27 Feb 2020 08:07:06 GMT  
		Size: 61.4 MB (61379230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.1-webprofile`

```console
$ docker pull tomee@sha256:0ba1c4a769e71061e2fa9cb9db5b9e65c1ae9052e91ed22536348ccc2b68864d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8.0.1-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:5f3d477808ead86cdaa74fa95b8f76fe3042f80db591b00eb1da6e02a48c4f38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157806239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b9bd0a5c8b50f66c6c52dbec3929ea2acfdfcc62d4fbb512367b37c57337de`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:53 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:04:55 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:56 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:56 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453dd84bbe3e765c8e44611703b4bb8bba037185ac6cbf1f916a72fa0185767`  
		Last Modified: Thu, 27 Feb 2020 08:07:24 GMT  
		Size: 42.2 MB (42170964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.7-plume`

```console
$ docker pull tomee@sha256:b946470eda0683da273cb4e56bef568ded242bd2e5d3d89e44200dab7f6fe8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.0.7-plume` - linux; amd64

```console
$ docker pull tomee@sha256:a46460e19598bdeef6d95632ce2d56175f379cbb6ae7e0e901a5fd0947217d96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176990285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9362dc94b79862d86ff82e29888330d2908d1f79bf74825098c88b831c91f6f7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:02:53 GMT
ENV TOMEE_VER=7.0.7
# Thu, 27 Feb 2020 08:02:53 GMT
ENV TOMEE_BUILD=plume
# Thu, 27 Feb 2020 08:02:57 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:02:57 GMT
USER tomee
# Thu, 27 Feb 2020 08:02:57 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:02:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31e21925d76492e9b062c4f306934eb60c4444480ad9b4d1f4c79a533de32d`  
		Last Modified: Thu, 27 Feb 2020 08:05:17 GMT  
		Size: 63.1 MB (63061685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.7-plus`

```console
$ docker pull tomee@sha256:7954b960cf77ca55428d98151e36902974e41dd5b5111d7d46d6820338a85f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.0.7-plus` - linux; amd64

```console
$ docker pull tomee@sha256:d366ed876cc454878e353f9f333619b4aaff178650c87f5c7ddd41e91f8ef5fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169918391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d9f633fa03dcdb26f96cdb02442d3da3d1530897aa568871daf2f451ae70d4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:02:53 GMT
ENV TOMEE_VER=7.0.7
# Thu, 27 Feb 2020 08:03:03 GMT
ENV TOMEE_BUILD=plus
# Thu, 27 Feb 2020 08:03:07 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:07 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:07 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caf114d8b245ccdbc55c9c531c518f219546f5f753f991f04b53c916711c04e`  
		Last Modified: Thu, 27 Feb 2020 08:05:25 GMT  
		Size: 56.0 MB (55989791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.7-webprofile`

```console
$ docker pull tomee@sha256:3926ae6cad3a19818e0c694576562109f63942c901a39d1fe18618a41f70413f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.0.7-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:2479eb13d7e5a5c93d19578b6c7e9ceb6b041daa761b3d606469a41ed50eb48b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152265546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f125d70dcd73ba47d29701d2678a6514c89e4e9f67671ff255d86415031b00`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:02:53 GMT
ENV TOMEE_VER=7.0.7
# Thu, 27 Feb 2020 08:03:11 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:03:15 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:15 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:15 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de16090c8639840f36416c1a346d4dedeaa2bebb148c9b413f8dc1ec1507c3d9`  
		Last Modified: Thu, 27 Feb 2020 08:05:42 GMT  
		Size: 38.3 MB (38336946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.2-microprofile`

```console
$ docker pull tomee@sha256:779b98a4a9e1612e140f1796a4f9bd96a7bd9f49e63b13c122021467b0eb566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.1.2-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:4faa96eb2ff4953016814225a10a33faf2edf1a8b6d1efa3f6103b659a97c382
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154899652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e941ec1399f3564255de7d8a37b8f0a539e025e7d7be2f3c2164872029a3bcc1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:37 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 27 Feb 2020 08:03:40 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:40 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:40 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7c25571d6f1800147cb5e689da9d472311a2ac44f566bd0bedaa1de050d265`  
		Last Modified: Thu, 27 Feb 2020 08:06:07 GMT  
		Size: 41.0 MB (40971052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.2-plume`

```console
$ docker pull tomee@sha256:3cbd3cb29c5105623490073adc780bb54f5a247c7c97fd8967b13df71a879656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.1.2-plume` - linux; amd64

```console
$ docker pull tomee@sha256:d16d6eb553f28a5fa1a7bb958e5bf59a27d391f022551834d7d34614ff7fcfb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179042788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee1fad3939f94c448934e3fbedca57bdd66ff9f33608f8182ec85b52cd3ff82`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_BUILD=plume
# Thu, 27 Feb 2020 08:03:24 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:24 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:24 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb9d7e5aafcac712c7456c27142fc53c2d4b741f5e2831571f28c430f1ba3b`  
		Last Modified: Thu, 27 Feb 2020 08:05:51 GMT  
		Size: 65.1 MB (65114188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.2-plus`

```console
$ docker pull tomee@sha256:e88cb0c77802e4bc3fc514626610358788b097e6f60663630a3702520ba22ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.1.2-plus` - linux; amd64

```console
$ docker pull tomee@sha256:bef86a595331df7a8d3b303c078bfa61310d1e92f51126b211046478f512e588
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (172008564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545e1c26bc4a1f3b181bd96cf642daf51879355e92f8688b1f3181035c6ec624`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:28 GMT
ENV TOMEE_BUILD=plus
# Thu, 27 Feb 2020 08:03:32 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:32 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:33 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deaa78a5721612c10ed0817f8aa3b9c7d334626a2168694274fb9243e48d4e4`  
		Last Modified: Thu, 27 Feb 2020 08:06:00 GMT  
		Size: 58.1 MB (58079964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.2-webprofile`

```console
$ docker pull tomee@sha256:8c4c2a43ffe3fd8bcecc68c0ea48f4aa29750ff26a1a14ee2f4ee58fdd0be1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.1.2-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:10912c487b992f481d0ac59ac4e2703f1aa35c4801aa469a962cf75f478c0b1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154388796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eebd3389099c6745005e70f1d9430a0416bfbcbb1aaeafffed2cdbeec07732f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:19 GMT
ENV TOMEE_VER=7.1.2
# Thu, 27 Feb 2020 08:03:45 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:03:48 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:48 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:48 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f06f64c2bd96e8e56ae5298c8396cb7b94fc3e2177887829248a1788f807ca`  
		Last Modified: Thu, 27 Feb 2020 08:06:14 GMT  
		Size: 40.5 MB (40460196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.1-microprofile`

```console
$ docker pull tomee@sha256:9bcf3ae00f0cd9f8ff03d7521831326276219d911807273fdf3ad0b78e073efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-8.0.1-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:6988ae34ab823353e2c6f24d1e0039734dad444217278c3a95710c741b3284b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170432184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1ae5caf1ae583a539657a778266b4ce2a5251bf414534e7e28d6d767f3b38a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:52 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:10 GMT
ENV TOMEE_BUILD=microprofile
# Thu, 27 Feb 2020 08:04:14 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:14 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:14 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975f346320d5959c4f888d3496cbb37ac6f73ea16560168ababe5bbe2400f970`  
		Last Modified: Thu, 27 Feb 2020 08:06:41 GMT  
		Size: 56.5 MB (56503584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.1-plume`

```console
$ docker pull tomee@sha256:5eb8a624ed2f18a7401b97dd7fc49cc1e581068a57710bc5e855b5269e7592d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-8.0.1-plume` - linux; amd64

```console
$ docker pull tomee@sha256:615ec9dcb00569638747d0c3ffd838551fca9f6e5d9d71c30a51e331a03669d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182549854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63616a88ab1be0ac9eb74f95d662906acc86bcf96d953143b74175440727b3b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:52 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:03:53 GMT
ENV TOMEE_BUILD=plume
# Thu, 27 Feb 2020 08:03:57 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:03:57 GMT
USER tomee
# Thu, 27 Feb 2020 08:03:58 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:03:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31fd3d67d457a9454aef3c3d3d9d512ba4d01e7aedd8138105d06e6b8743b11`  
		Last Modified: Thu, 27 Feb 2020 08:06:25 GMT  
		Size: 68.6 MB (68621254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.1-plus`

```console
$ docker pull tomee@sha256:07d977ebc359a55a9817144a7bc4e2e6c531d2ba78d386ec520aa6e3e0384eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-8.0.1-plus` - linux; amd64

```console
$ docker pull tomee@sha256:48863c7ae5a70681a63449b83356cba897d7172d40bf21583b7cd3ecbe21c0bc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175307813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79b896b8e432927d7879e40159f01da4b01cbbd53acae82ad21b4a4dd3fd6ee`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:52 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:01 GMT
ENV TOMEE_BUILD=plus
# Thu, 27 Feb 2020 08:04:06 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:06 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:06 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78063e1e9d73323f7bf5ecb2d902d7a27e285a4ea574a203cbb78e3fe7fee5`  
		Last Modified: Thu, 27 Feb 2020 08:06:33 GMT  
		Size: 61.4 MB (61379213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.1-webprofile`

```console
$ docker pull tomee@sha256:fa75a5ca8cfabf796ae0e3baf15fa5734f86a23f574661e26e455b1638c23a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-8.0.1-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:dbb145911052ba53b74ecd8a84742f016d91f632a0764389fa461ad533008da4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156099552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083a8d6cd1747f7a7119b72799d841d85c5fe917b8c9837a825b7a13e9045a31`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Feb 2020 20:22:06 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:22:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_VERSION=8u242
# Wed, 26 Feb 2020 20:22:07 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 26 Feb 2020 20:22:08 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 26 Feb 2020 20:22:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 27 Feb 2020 08:02:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:02:50 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:02:50 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:02:52 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:03:52 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:19 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:04:23 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:23 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:23 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf499b4631c576793071adf6f14d1ca3de58a32c5cd70a199f6ba9ce172866f3`  
		Last Modified: Wed, 26 Feb 2020 20:28:26 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f3946cbcde7588c6228950e3be3fee1247b1c02c84213dcafda524abd2b87c`  
		Last Modified: Wed, 26 Feb 2020 20:28:32 GMT  
		Size: 40.2 MB (40187615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a6e76c177db29f6efd3f073b8a18336d57b68bc7244317d455efaed347d91`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675413172691a4ff00aaadf7c0f1727aa113c186e8dc7d364dc66941cf196c5e`  
		Last Modified: Thu, 27 Feb 2020 08:05:13 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6ac6178f7dd7d09274acd4798287b1fdda71317ee5385c103c589156c81f5d`  
		Last Modified: Thu, 27 Feb 2020 08:06:49 GMT  
		Size: 42.2 MB (42170952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:latest`

```console
$ docker pull tomee@sha256:0ba1c4a769e71061e2fa9cb9db5b9e65c1ae9052e91ed22536348ccc2b68864d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:latest` - linux; amd64

```console
$ docker pull tomee@sha256:5f3d477808ead86cdaa74fa95b8f76fe3042f80db591b00eb1da6e02a48c4f38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157806239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b9bd0a5c8b50f66c6c52dbec3929ea2acfdfcc62d4fbb512367b37c57337de`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 20:20:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:59 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:21:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:21:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:21:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:01 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 27 Feb 2020 08:04:27 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 08:04:28 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
WORKDIR /usr/local/tomee
# Thu, 27 Feb 2020 08:04:28 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 27 Feb 2020 08:04:30 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 27 Feb 2020 08:04:30 GMT
ENV TOMEE_VER=8.0.1
# Thu, 27 Feb 2020 08:04:53 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 27 Feb 2020 08:04:55 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Thu, 27 Feb 2020 08:04:56 GMT
USER tomee
# Thu, 27 Feb 2020 08:04:56 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 08:04:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8c5daaf911497d9044b4a185f63d0673e1637fb8f425d7c8e04dd699324d3a`  
		Last Modified: Wed, 26 Feb 2020 20:27:22 GMT  
		Size: 5.5 MB (5529310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9447ec3543c49941e84e796019684ce89c5c32d3ba652a0a41b9807f8b81fa61`  
		Last Modified: Wed, 26 Feb 2020 20:27:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b440bc601eb6f3892913c71ff3c78a8a16bd61c9b09e5d4f436e6819fafac`  
		Last Modified: Wed, 26 Feb 2020 20:27:29 GMT  
		Size: 41.9 MB (41894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20aee4f4cef2224f886fc970ed1f1c88abc758f68c282569f042a9181267feca`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a77086fcfe6195bc9a7d1cdfe7446fbda839c859b5b56ffa5aedb4fd7b6798`  
		Last Modified: Thu, 27 Feb 2020 08:06:52 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453dd84bbe3e765c8e44611703b4bb8bba037185ac6cbf1f916a72fa0185767`  
		Last Modified: Thu, 27 Feb 2020 08:07:24 GMT  
		Size: 42.2 MB (42170964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
