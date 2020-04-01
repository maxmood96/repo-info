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
$ docker pull tomee@sha256:6c7ad500d4b580ce8238eae51e66694f7afdc8745decf2f26f9a6e3f753822dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:11-jre-8.0.1-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:0c2540cc4a1ab5445a82b81d5a52788e77021b6f694b715ceac26c9960bd21e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172139116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2375f608f9873b324cd7073c01b55b66c90d3b473ed5e276f060a14eec82b018`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:31 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 01 Apr 2020 08:38:34 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:34 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:34 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852489c11ff9d2713a3619bfa8dad17ea0185d46603ab8ad9eae6c31ace9cef6`  
		Last Modified: Wed, 01 Apr 2020 08:40:48 GMT  
		Size: 56.5 MB (56503601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:11-jre-8.0.1-plume`

```console
$ docker pull tomee@sha256:1a75213485e974ba313ba7bd453a56cd8e6f208892281e6c3e25aa5fee8c6565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:11-jre-8.0.1-plume` - linux; amd64

```console
$ docker pull tomee@sha256:20f8aa5aa626cf097157ba34c3de9a584dcd0db8ab8fa94ac9f4e749ce521d1f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184256773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fde49326fa050e8cce69d442d8b73bbe9b99e5898dbc225035e69e73509e04`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_BUILD=plume
# Wed, 01 Apr 2020 08:38:18 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:18 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:18 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f4a566ad17ab064c33d7ea7cd9213cd4e4217aa8dc75fbdf878ca51384570f`  
		Last Modified: Wed, 01 Apr 2020 08:40:30 GMT  
		Size: 68.6 MB (68621258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:11-jre-8.0.1-plus`

```console
$ docker pull tomee@sha256:6d2cafeaa0d8b19b62245c928b7ad86fd167bf8ef4f4f74f8c85d984883e7496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:11-jre-8.0.1-plus` - linux; amd64

```console
$ docker pull tomee@sha256:6b52fe900cab1caef9dc66df1befb1c701800ef47025430256bcd5eacacdd672
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177014767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6433f7cf93ab21165f42e0ebc0c4b5fbb77568b695f9a75d631904569fc359bc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:23 GMT
ENV TOMEE_BUILD=plus
# Wed, 01 Apr 2020 08:38:26 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:26 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:26 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a9c62fef86ccddd056cb06131c9c9f08349eeb845dbd303103d281b0b64d0c`  
		Last Modified: Wed, 01 Apr 2020 08:40:39 GMT  
		Size: 61.4 MB (61379252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:11-jre-8.0.1-webprofile`

```console
$ docker pull tomee@sha256:8e6da48870245025d52ba4b1ab7cefadb797daa2854b4e57d7dc90e921bc9c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:11-jre-8.0.1-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:201b604b99aeafabc16050259c08301d5bf896e4177249b949614c118b9205ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157806478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fc010d07c5b690a92511e6c16fc69d27fb7783f1aeea6ee669412475c4bedf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:38 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:38:40 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:40 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:41 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0e9e8a683439625a4b691eb0ba950243246e5a12113ca659daa89befabe4a7`  
		Last Modified: Wed, 01 Apr 2020 08:40:55 GMT  
		Size: 42.2 MB (42170963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7`

```console
$ docker pull tomee@sha256:077fc07f7c72e8d3726d7c5606c60899234decd39da8ea29d28b8fc570f1d73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7` - linux; amd64

```console
$ docker pull tomee@sha256:e93b469840c056271dda7dc59a4883e719befa52bb0d82d82162fafe23386789
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154388967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebc71b21d380ac92b747fc53ba21b85031295bdc8d573d02177fbc977cca259`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:31 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:37:34 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:34 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:35 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eff4524b1652183affc6106fc71a31feb47e5f372cfebcd5fa66afe9f060aff`  
		Last Modified: Wed, 01 Apr 2020 08:39:47 GMT  
		Size: 40.5 MB (40460202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.0`

```console
$ docker pull tomee@sha256:d81fbb7871e47de5813b5d0e53bac233031a991a944b61ffd6c3ceb2d41fb896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.0` - linux; amd64

```console
$ docker pull tomee@sha256:dab7eb9eebc163df3225f77ba102acdd96a3351d01ee7c094f63e93d7e389c4c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152265709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfaf772bd0a9cd767adee47577f1277bfec8ebbe2374948419206be426e5776`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:36:43 GMT
ENV TOMEE_VER=7.0.7
# Wed, 01 Apr 2020 08:37:00 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:37:03 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:03 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:03 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad745515fe8db0b980cde4daeda1e94629b450e273735759f2b37ce531538dd8`  
		Last Modified: Wed, 01 Apr 2020 08:39:14 GMT  
		Size: 38.3 MB (38336944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.0.7-plume`

```console
$ docker pull tomee@sha256:3b65daf1d6dafbc9e81c885d8542b0697885e9da51238ce2afc60f1201af4c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.0.7-plume` - linux; amd64

```console
$ docker pull tomee@sha256:3c164b9019c1760267f64bf750c045ac830a1abaef8c3ba719674d044d149d07
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176990451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b008829978ee43af045f868753e8cd7952e1e69e55139ba082316091d46a985`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:36:43 GMT
ENV TOMEE_VER=7.0.7
# Wed, 01 Apr 2020 08:36:43 GMT
ENV TOMEE_BUILD=plume
# Wed, 01 Apr 2020 08:36:47 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:36:48 GMT
USER tomee
# Wed, 01 Apr 2020 08:36:48 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:36:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaf3aefa6418da7fb9cbc9b1eaee75c08b7a8cb26f536fbc1e36abd9a7e211f`  
		Last Modified: Wed, 01 Apr 2020 08:38:58 GMT  
		Size: 63.1 MB (63061686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.0.7-plus`

```console
$ docker pull tomee@sha256:de5a0f6717a63b20f3fc1335b074f0ff45aed55a1eb24cb1bfae38dc05c80a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.0.7-plus` - linux; amd64

```console
$ docker pull tomee@sha256:d8c25a3edcb1a24fccba53941906823bfd5c48eb744a84101bdd06c3125b1728
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169918566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d922e586e5322de0b409be88564fbc3b87472f0b03e3f89bb20e7e291604966a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:36:43 GMT
ENV TOMEE_VER=7.0.7
# Wed, 01 Apr 2020 08:36:52 GMT
ENV TOMEE_BUILD=plus
# Wed, 01 Apr 2020 08:36:56 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:36:56 GMT
USER tomee
# Wed, 01 Apr 2020 08:36:56 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:36:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b6ac3ec32e0fbbb0171b8e8acadf55bdfcc788cb9573fd99369953d3981fe`  
		Last Modified: Wed, 01 Apr 2020 08:39:06 GMT  
		Size: 56.0 MB (55989801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1`

```console
$ docker pull tomee@sha256:077fc07f7c72e8d3726d7c5606c60899234decd39da8ea29d28b8fc570f1d73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1` - linux; amd64

```console
$ docker pull tomee@sha256:e93b469840c056271dda7dc59a4883e719befa52bb0d82d82162fafe23386789
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154388967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebc71b21d380ac92b747fc53ba21b85031295bdc8d573d02177fbc977cca259`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:31 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:37:34 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:34 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:35 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eff4524b1652183affc6106fc71a31feb47e5f372cfebcd5fa66afe9f060aff`  
		Last Modified: Wed, 01 Apr 2020 08:39:47 GMT  
		Size: 40.5 MB (40460202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.2-microprofile`

```console
$ docker pull tomee@sha256:d87f82cf56e0e92444cd00685dd80efed42ed3358ca1f4d0827d289cfc5a9842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1.2-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:46761ba7bc7386d30ba4d3d1b872db77fce740aadb57b9f8179e5ed2371dfaea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154899837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041e535f00e8894b966acc3ec7eda3ca8e0edab6d4b258927ef8781dd7d95c37`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:24 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 01 Apr 2020 08:37:27 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:28 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:28 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b470551b7caf51e64fed36e127a8a61b083cfcfe51c9b51e9029d52c2828602e`  
		Last Modified: Wed, 01 Apr 2020 08:39:39 GMT  
		Size: 41.0 MB (40971072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.2-plume`

```console
$ docker pull tomee@sha256:fb99b8074722ae63f341aabcd17d148828ccaa717dce119ab3600d5c2c843e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1.2-plume` - linux; amd64

```console
$ docker pull tomee@sha256:48777bf9371080b9df84a71f7e9e01f54981d3df7d2b7895e4c0579e8f979adc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179043069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c4ed93585bb22907bf4750b71cded7c4e3a6a8facdd62ee50985c7a7313281`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_BUILD=plume
# Wed, 01 Apr 2020 08:37:12 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:12 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:12 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe396bc86fa05b291d769f0ef4e79ca088a82c169c418e3b21530811e9d8dcb`  
		Last Modified: Wed, 01 Apr 2020 08:39:23 GMT  
		Size: 65.1 MB (65114304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.2-plus`

```console
$ docker pull tomee@sha256:6a59efe1cc5d3b9d245c99bfdb64eacfd483ce78977b71d9591ac15cbf82a307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1.2-plus` - linux; amd64

```console
$ docker pull tomee@sha256:052093c8ea7cafaba74d43b69e3cdea1fdfa1b0e586ef399bc2dcec2441f16ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (172008750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b4d8588503cb318df5c31dd3f5ddc897a0472fd5ba7ec84b869b17b6d41b43`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:16 GMT
ENV TOMEE_BUILD=plus
# Wed, 01 Apr 2020 08:37:19 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:20 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:20 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005fd93ea6957a1dd26aa9d84b792aeb30a14130b8cc11eafe7f560b272a03e2`  
		Last Modified: Wed, 01 Apr 2020 08:39:32 GMT  
		Size: 58.1 MB (58079985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:7.1.2-webprofile`

```console
$ docker pull tomee@sha256:077fc07f7c72e8d3726d7c5606c60899234decd39da8ea29d28b8fc570f1d73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:7.1.2-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:e93b469840c056271dda7dc59a4883e719befa52bb0d82d82162fafe23386789
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154388967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebc71b21d380ac92b747fc53ba21b85031295bdc8d573d02177fbc977cca259`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:31 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:37:34 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:34 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:35 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eff4524b1652183affc6106fc71a31feb47e5f372cfebcd5fa66afe9f060aff`  
		Last Modified: Wed, 01 Apr 2020 08:39:47 GMT  
		Size: 40.5 MB (40460202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8`

```console
$ docker pull tomee@sha256:8e6da48870245025d52ba4b1ab7cefadb797daa2854b4e57d7dc90e921bc9c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8` - linux; amd64

```console
$ docker pull tomee@sha256:201b604b99aeafabc16050259c08301d5bf896e4177249b949614c118b9205ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157806478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fc010d07c5b690a92511e6c16fc69d27fb7783f1aeea6ee669412475c4bedf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:38 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:38:40 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:40 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:41 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0e9e8a683439625a4b691eb0ba950243246e5a12113ca659daa89befabe4a7`  
		Last Modified: Wed, 01 Apr 2020 08:40:55 GMT  
		Size: 42.2 MB (42170963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.1-microprofile`

```console
$ docker pull tomee@sha256:6c7ad500d4b580ce8238eae51e66694f7afdc8745decf2f26f9a6e3f753822dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8.0.1-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:0c2540cc4a1ab5445a82b81d5a52788e77021b6f694b715ceac26c9960bd21e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172139116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2375f608f9873b324cd7073c01b55b66c90d3b473ed5e276f060a14eec82b018`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:31 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 01 Apr 2020 08:38:34 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:34 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:34 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852489c11ff9d2713a3619bfa8dad17ea0185d46603ab8ad9eae6c31ace9cef6`  
		Last Modified: Wed, 01 Apr 2020 08:40:48 GMT  
		Size: 56.5 MB (56503601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.1-plume`

```console
$ docker pull tomee@sha256:1a75213485e974ba313ba7bd453a56cd8e6f208892281e6c3e25aa5fee8c6565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8.0.1-plume` - linux; amd64

```console
$ docker pull tomee@sha256:20f8aa5aa626cf097157ba34c3de9a584dcd0db8ab8fa94ac9f4e749ce521d1f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184256773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fde49326fa050e8cce69d442d8b73bbe9b99e5898dbc225035e69e73509e04`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_BUILD=plume
# Wed, 01 Apr 2020 08:38:18 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:18 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:18 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f4a566ad17ab064c33d7ea7cd9213cd4e4217aa8dc75fbdf878ca51384570f`  
		Last Modified: Wed, 01 Apr 2020 08:40:30 GMT  
		Size: 68.6 MB (68621258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.1-plus`

```console
$ docker pull tomee@sha256:6d2cafeaa0d8b19b62245c928b7ad86fd167bf8ef4f4f74f8c85d984883e7496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8.0.1-plus` - linux; amd64

```console
$ docker pull tomee@sha256:6b52fe900cab1caef9dc66df1befb1c701800ef47025430256bcd5eacacdd672
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177014767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6433f7cf93ab21165f42e0ebc0c4b5fbb77568b695f9a75d631904569fc359bc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:23 GMT
ENV TOMEE_BUILD=plus
# Wed, 01 Apr 2020 08:38:26 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:26 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:26 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a9c62fef86ccddd056cb06131c9c9f08349eeb845dbd303103d281b0b64d0c`  
		Last Modified: Wed, 01 Apr 2020 08:40:39 GMT  
		Size: 61.4 MB (61379252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8.0.1-webprofile`

```console
$ docker pull tomee@sha256:8e6da48870245025d52ba4b1ab7cefadb797daa2854b4e57d7dc90e921bc9c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8.0.1-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:201b604b99aeafabc16050259c08301d5bf896e4177249b949614c118b9205ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157806478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fc010d07c5b690a92511e6c16fc69d27fb7783f1aeea6ee669412475c4bedf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:38 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:38:40 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:40 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:41 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0e9e8a683439625a4b691eb0ba950243246e5a12113ca659daa89befabe4a7`  
		Last Modified: Wed, 01 Apr 2020 08:40:55 GMT  
		Size: 42.2 MB (42170963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.7-plume`

```console
$ docker pull tomee@sha256:3b65daf1d6dafbc9e81c885d8542b0697885e9da51238ce2afc60f1201af4c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.0.7-plume` - linux; amd64

```console
$ docker pull tomee@sha256:3c164b9019c1760267f64bf750c045ac830a1abaef8c3ba719674d044d149d07
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176990451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b008829978ee43af045f868753e8cd7952e1e69e55139ba082316091d46a985`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:36:43 GMT
ENV TOMEE_VER=7.0.7
# Wed, 01 Apr 2020 08:36:43 GMT
ENV TOMEE_BUILD=plume
# Wed, 01 Apr 2020 08:36:47 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:36:48 GMT
USER tomee
# Wed, 01 Apr 2020 08:36:48 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:36:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceaf3aefa6418da7fb9cbc9b1eaee75c08b7a8cb26f536fbc1e36abd9a7e211f`  
		Last Modified: Wed, 01 Apr 2020 08:38:58 GMT  
		Size: 63.1 MB (63061686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.7-plus`

```console
$ docker pull tomee@sha256:de5a0f6717a63b20f3fc1335b074f0ff45aed55a1eb24cb1bfae38dc05c80a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.0.7-plus` - linux; amd64

```console
$ docker pull tomee@sha256:d8c25a3edcb1a24fccba53941906823bfd5c48eb744a84101bdd06c3125b1728
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169918566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d922e586e5322de0b409be88564fbc3b87472f0b03e3f89bb20e7e291604966a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:36:43 GMT
ENV TOMEE_VER=7.0.7
# Wed, 01 Apr 2020 08:36:52 GMT
ENV TOMEE_BUILD=plus
# Wed, 01 Apr 2020 08:36:56 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:36:56 GMT
USER tomee
# Wed, 01 Apr 2020 08:36:56 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:36:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466b6ac3ec32e0fbbb0171b8e8acadf55bdfcc788cb9573fd99369953d3981fe`  
		Last Modified: Wed, 01 Apr 2020 08:39:06 GMT  
		Size: 56.0 MB (55989801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.7-webprofile`

```console
$ docker pull tomee@sha256:d81fbb7871e47de5813b5d0e53bac233031a991a944b61ffd6c3ceb2d41fb896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.0.7-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:dab7eb9eebc163df3225f77ba102acdd96a3351d01ee7c094f63e93d7e389c4c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152265709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfaf772bd0a9cd767adee47577f1277bfec8ebbe2374948419206be426e5776`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:36:43 GMT
ENV TOMEE_VER=7.0.7
# Wed, 01 Apr 2020 08:37:00 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:37:03 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:03 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:03 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad745515fe8db0b980cde4daeda1e94629b450e273735759f2b37ce531538dd8`  
		Last Modified: Wed, 01 Apr 2020 08:39:14 GMT  
		Size: 38.3 MB (38336944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.2-microprofile`

```console
$ docker pull tomee@sha256:d87f82cf56e0e92444cd00685dd80efed42ed3358ca1f4d0827d289cfc5a9842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.1.2-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:46761ba7bc7386d30ba4d3d1b872db77fce740aadb57b9f8179e5ed2371dfaea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154899837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041e535f00e8894b966acc3ec7eda3ca8e0edab6d4b258927ef8781dd7d95c37`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:24 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 01 Apr 2020 08:37:27 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:28 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:28 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b470551b7caf51e64fed36e127a8a61b083cfcfe51c9b51e9029d52c2828602e`  
		Last Modified: Wed, 01 Apr 2020 08:39:39 GMT  
		Size: 41.0 MB (40971072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.2-plume`

```console
$ docker pull tomee@sha256:fb99b8074722ae63f341aabcd17d148828ccaa717dce119ab3600d5c2c843e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.1.2-plume` - linux; amd64

```console
$ docker pull tomee@sha256:48777bf9371080b9df84a71f7e9e01f54981d3df7d2b7895e4c0579e8f979adc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179043069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c4ed93585bb22907bf4750b71cded7c4e3a6a8facdd62ee50985c7a7313281`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_BUILD=plume
# Wed, 01 Apr 2020 08:37:12 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:12 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:12 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe396bc86fa05b291d769f0ef4e79ca088a82c169c418e3b21530811e9d8dcb`  
		Last Modified: Wed, 01 Apr 2020 08:39:23 GMT  
		Size: 65.1 MB (65114304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.2-plus`

```console
$ docker pull tomee@sha256:6a59efe1cc5d3b9d245c99bfdb64eacfd483ce78977b71d9591ac15cbf82a307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.1.2-plus` - linux; amd64

```console
$ docker pull tomee@sha256:052093c8ea7cafaba74d43b69e3cdea1fdfa1b0e586ef399bc2dcec2441f16ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (172008750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b4d8588503cb318df5c31dd3f5ddc897a0472fd5ba7ec84b869b17b6d41b43`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:16 GMT
ENV TOMEE_BUILD=plus
# Wed, 01 Apr 2020 08:37:19 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:20 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:20 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005fd93ea6957a1dd26aa9d84b792aeb30a14130b8cc11eafe7f560b272a03e2`  
		Last Modified: Wed, 01 Apr 2020 08:39:32 GMT  
		Size: 58.1 MB (58079985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.1.2-webprofile`

```console
$ docker pull tomee@sha256:077fc07f7c72e8d3726d7c5606c60899234decd39da8ea29d28b8fc570f1d73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-7.1.2-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:e93b469840c056271dda7dc59a4883e719befa52bb0d82d82162fafe23386789
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154388967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebc71b21d380ac92b747fc53ba21b85031295bdc8d573d02177fbc977cca259`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:07 GMT
ENV TOMEE_VER=7.1.2
# Wed, 01 Apr 2020 08:37:31 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:37:34 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:34 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:35 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eff4524b1652183affc6106fc71a31feb47e5f372cfebcd5fa66afe9f060aff`  
		Last Modified: Wed, 01 Apr 2020 08:39:47 GMT  
		Size: 40.5 MB (40460202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.1-microprofile`

```console
$ docker pull tomee@sha256:7ff9a906f421f306b2d12816fca06eaec9578c6f97a70dcd6dc70cee5dafcdac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-8.0.1-microprofile` - linux; amd64

```console
$ docker pull tomee@sha256:5d01b29b791bc2390b7a9f765cb24dc1e11768434888338e99dbde7c7fbfdd9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170432371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705a5a31895e1cd8c42354affeeb9b820d95f39639bea136c9b42abbbab2cd05`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:39 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:37:56 GMT
ENV TOMEE_BUILD=microprofile
# Wed, 01 Apr 2020 08:38:00 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:00 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:00 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1347459cddfb8630bdbda497a7eb87c85c1b4a85837c1200db82b44207b6fe`  
		Last Modified: Wed, 01 Apr 2020 08:40:14 GMT  
		Size: 56.5 MB (56503606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.1-plume`

```console
$ docker pull tomee@sha256:1bde633a8119776d5898a1dc5a2d59e6a7673fcd1df2c24330bd3bf9bf64cb8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-8.0.1-plume` - linux; amd64

```console
$ docker pull tomee@sha256:a7d024d003065ea24d4a5bd18ce9ccf3077fb82a0e3077ec610f35d74aa37fb8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182550009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1ad9b9ee8cdcf119caae314e5fa1619be967a3c859004021ace2a2f3b035c3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:39 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:37:39 GMT
ENV TOMEE_BUILD=plume
# Wed, 01 Apr 2020 08:37:43 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:44 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:44 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16a43774a947f94eda104a1332df215eb410d5e87b9dc0c4c881dfb82b73dda`  
		Last Modified: Wed, 01 Apr 2020 08:39:57 GMT  
		Size: 68.6 MB (68621244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.1-plus`

```console
$ docker pull tomee@sha256:32d818bba547886478402cae5f4dbe03fd5221b30152e35aca9446579f8f4430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-8.0.1-plus` - linux; amd64

```console
$ docker pull tomee@sha256:532e6b3fbe3ecb8ffae22a397e6ff7d39722881a38686bda458e39f5dcf28691
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175308028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319c5dc2c8576776a682436f791bc9b3603929f2f04cd7d6e538437932939e97`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:39 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:37:48 GMT
ENV TOMEE_BUILD=plus
# Wed, 01 Apr 2020 08:37:52 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:37:52 GMT
USER tomee
# Wed, 01 Apr 2020 08:37:52 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:37:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf8b8f405db666535d268a01a5cd8b21a9b1fb14c56a232ab8b2d126a7d4555`  
		Last Modified: Wed, 01 Apr 2020 08:40:06 GMT  
		Size: 61.4 MB (61379263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-8.0.1-webprofile`

```console
$ docker pull tomee@sha256:70429040a1bf43648fe2151b500856860c92036af5bb50b3e36d2b9f03869941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:8-jre-8.0.1-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:c4a24159b268aa76aaa4e8779d534a0394d6bd3fb09781a50c0befeeb57f0f52
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156099734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286d06409583ce34a8596ac96d3411f698f366f3cddefbaf71070a6daeb17504`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 31 Mar 2020 21:34:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_VERSION=8u242
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Tue, 31 Mar 2020 21:34:50 GMT
ENV JAVA_URL_VERSION=8u242b08
# Tue, 31 Mar 2020 21:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 01 Apr 2020 08:36:39 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:36:40 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:36:40 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:36:43 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:37:39 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:04 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:38:07 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:07 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:08 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefb948d0fef7542cd6e67eaba66b02006e818a75578513f43d64d72158fc214`  
		Last Modified: Tue, 31 Mar 2020 21:38:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637f123c2a5b7485d5f82b3557a5ddaf6905a9e6a944538848800c0110755e3`  
		Last Modified: Tue, 31 Mar 2020 21:38:10 GMT  
		Size: 40.2 MB (40187601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f4ca27f08f13f635ed95449affca6479eace2f8af0292af126bd73d3d1fa3`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60911b28afb2b14cb44f96e237d44fc39aeeb00e7a7763b549defdb00fe5ba65`  
		Last Modified: Wed, 01 Apr 2020 08:38:54 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a14fcbc234aae10ea1e752eb88de40164d12a98d85db7af2b286b61e32d4e4d`  
		Last Modified: Wed, 01 Apr 2020 08:40:21 GMT  
		Size: 42.2 MB (42170969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:latest`

```console
$ docker pull tomee@sha256:8e6da48870245025d52ba4b1ab7cefadb797daa2854b4e57d7dc90e921bc9c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `tomee:latest` - linux; amd64

```console
$ docker pull tomee@sha256:201b604b99aeafabc16050259c08301d5bf896e4177249b949614c118b9205ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157806478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fc010d07c5b690a92511e6c16fc69d27fb7783f1aeea6ee669412475c4bedf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 21:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:34:13 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:34:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 21:34:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:34:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_VERSION=11.0.6
# Tue, 31 Mar 2020 21:34:14 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Tue, 31 Mar 2020 21:34:15 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Tue, 31 Mar 2020 21:34:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 01 Apr 2020 08:38:12 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 08:38:12 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
WORKDIR /usr/local/tomee
# Wed, 01 Apr 2020 08:38:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Wed, 01 Apr 2020 08:38:14 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Wed, 01 Apr 2020 08:38:15 GMT
ENV TOMEE_VER=8.0.1
# Wed, 01 Apr 2020 08:38:38 GMT
ENV TOMEE_BUILD=webprofile
# Wed, 01 Apr 2020 08:38:40 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm tomee.tar.gz* 	&& useradd tomee 	&& chown -R tomee:tomee /usr/local/tomee
# Wed, 01 Apr 2020 08:38:40 GMT
USER tomee
# Wed, 01 Apr 2020 08:38:41 GMT
EXPOSE 8080
# Wed, 01 Apr 2020 08:38:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481ed7a416dccbc5f431c7e405e1b784e23792c43f9805a588528b48679efb40`  
		Last Modified: Tue, 31 Mar 2020 21:37:20 GMT  
		Size: 5.5 MB (5529367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ca091c8f09cd6ee948c1d391367ab7587a0cb65d1b1b27966855f8a9a9455f`  
		Last Modified: Tue, 31 Mar 2020 21:37:18 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6980d9a29b459228e32a9547ba80da252c3d60f8d8be99041c9522c998f22bb`  
		Last Modified: Tue, 31 Mar 2020 21:37:29 GMT  
		Size: 41.9 MB (41894350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae9092f45d18a1b0f93623a20e9842c8ffc0c57baef99df4a8ed5b483cf39b`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2a30bb70d0ce27af755f49be76537e5bc54f84ed88b7cf2529ca6809a06ccf`  
		Last Modified: Wed, 01 Apr 2020 08:40:25 GMT  
		Size: 20.9 KB (20939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0e9e8a683439625a4b691eb0ba950243246e5a12113ca659daa89befabe4a7`  
		Last Modified: Wed, 01 Apr 2020 08:40:55 GMT  
		Size: 42.2 MB (42170963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
