<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `jetty`

-	[`jetty:9`](#jetty9)
-	[`jetty:9.2.29-jre8`](#jetty9229-jre8)
-	[`jetty:9.2-jre8`](#jetty92-jre8)
-	[`jetty:9.3.28-jre8`](#jetty9328-jre8)
-	[`jetty:9.3-jre8`](#jetty93-jre8)
-	[`jetty:9.4`](#jetty94)
-	[`jetty:9.4.26`](#jetty9426)
-	[`jetty:9.4.26-jdk13`](#jetty9426-jdk13)
-	[`jetty:9.4.26-jdk13-slim`](#jetty9426-jdk13-slim)
-	[`jetty:9.4.26-jre11`](#jetty9426-jre11)
-	[`jetty:9.4.26-jre11-slim`](#jetty9426-jre11-slim)
-	[`jetty:9.4.26-jre8`](#jetty9426-jre8)
-	[`jetty:9.4-jdk13`](#jetty94-jdk13)
-	[`jetty:9.4-jdk13-slim`](#jetty94-jdk13-slim)
-	[`jetty:9.4-jre11`](#jetty94-jre11)
-	[`jetty:9.4-jre11-slim`](#jetty94-jre11-slim)
-	[`jetty:9.4-jre8`](#jetty94-jre8)
-	[`jetty:9-jdk13`](#jetty9-jdk13)
-	[`jetty:9-jdk13-slim`](#jetty9-jdk13-slim)
-	[`jetty:9-jre11`](#jetty9-jre11)
-	[`jetty:9-jre11-slim`](#jetty9-jre11-slim)
-	[`jetty:9-jre8`](#jetty9-jre8)
-	[`jetty:jdk13`](#jettyjdk13)
-	[`jetty:latest`](#jettylatest)

## `jetty:9`

```console
$ docker pull jetty@sha256:d8f374b030b7e0af3d422887dafefa75ef9fe1b4de36f3e4e1a806de59fbbeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `jetty:9` - linux; amd64

```console
$ docker pull jetty@sha256:c2f362b5654ae4e16cd96f410c479e3b0cac574607a32c13501dd922e0a20ad5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115270945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7cfb40b7f4b3aaab1f50c4ca270acd53caf6cf9c2c04e332eedd72bc3006c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 08:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:55:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 Dec 2019 08:56:57 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_VERSION=8u232
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_URL_VERSION=8u232b09
# Sat, 28 Dec 2019 08:57:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sun, 29 Dec 2019 08:31:21 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Sun, 29 Dec 2019 08:31:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sun, 29 Dec 2019 08:31:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2019 08:31:22 GMT
RUN mkdir -p "$JETTY_HOME"
# Sun, 29 Dec 2019 08:31:23 GMT
WORKDIR /usr/local/jetty
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Sun, 29 Dec 2019 08:31:27 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sun, 29 Dec 2019 08:31:28 GMT
RUN mkdir -p "$JETTY_BASE"
# Sun, 29 Dec 2019 08:31:28 GMT
WORKDIR /var/lib/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:30 GMT
ENV TMPDIR=/tmp/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Sun, 29 Dec 2019 08:31:31 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Sun, 29 Dec 2019 08:31:31 GMT
USER jetty
# Sun, 29 Dec 2019 08:31:31 GMT
EXPOSE 8080
# Sun, 29 Dec 2019 08:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 Dec 2019 08:31:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8d3cd13de4f1c574d86de1c90b7e0f96d2394349c7e882117daaa86ad08ad`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 5.1 MB (5126129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06bdc5e0db3a85fca16aae57afb18ced9fad56ed4571f9bd0d748f38930b22`  
		Last Modified: Sat, 28 Dec 2019 09:03:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b1f94cfe4ae6c7ca9e45cc45491b7f732d099001d933ac72211dbd09d19e0d`  
		Last Modified: Sat, 28 Dec 2019 09:03:45 GMT  
		Size: 40.2 MB (40196546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe20b880320d8f58a256fe49d1c7c23c61b64baa639ad7279118a09e05b99b2b`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b913b52ac10d2aec4b74f5b78af565b0c0b25888a4c4826a1301239a847aab`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95861d4f30fde9cf21c8c2cb828a68434818251a138bdbdd7d275ca2e78987a`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 9.4 MB (9424429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecc3b45eaba005a5e755b9d4186273b7300646c4a3392159aab8b7ddd4f8d6`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46a5d5760312fac8ac9744158c27194bc30d047cb09045715eb95886f0376e9`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95bd8335f7360f38bfa50b47f5a83975722151ddc1cc65f78dbd7775f1e568`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5526a96dfe33daca789ac452c1286664ab7610d5447d2089cdd69f93c0bd3bd1`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9` - linux; arm variant v5

```console
$ docker pull jetty@sha256:6b79ec2ccfa3ee643017cecbdeee7565e32a4b74912ab39d95bbb17a1d1f7700
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180287052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965e56aa7b329cf860c5d90d360d6f490b43bfdb9ec51dfb7235b27e1cabbcbb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:53:17 GMT
ADD file:5dfe3b771bd67a2856913544993e219cb8c7933c33523cc56fe13a3a0e76ce9b in / 
# Wed, 08 May 2019 08:53:18 GMT
CMD ["bash"]
# Wed, 08 May 2019 10:01:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 10:01:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 11:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:35:27 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 11:35:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 11:35:31 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 11:36:37 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 16:15:13 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 16:15:13 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 16:15:14 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 16:15:16 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 16:15:16 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 16:15:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 16:15:24 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 16:15:27 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 16:15:27 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 16:15:32 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:32 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 16:15:35 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 16:15:36 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 16:15:37 GMT
USER jetty
# Wed, 08 May 2019 16:15:37 GMT
EXPOSE 8080
# Wed, 08 May 2019 16:15:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 16:15:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ca892ced475bf1c51c1f13b76a64549cfc5d1a0b55d33d8b9418efbb47887bf8`  
		Last Modified: Wed, 08 May 2019 08:59:09 GMT  
		Size: 44.0 MB (44045778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b30b379469b50f6ada866964876f5c4ba164c22896bf3a08aabab61869e51`  
		Last Modified: Wed, 08 May 2019 10:09:26 GMT  
		Size: 9.9 MB (9854225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e257762b4747840fc09dce269e7f68146ac9864b8bf218e57475b4af367a74`  
		Last Modified: Wed, 08 May 2019 10:09:24 GMT  
		Size: 4.2 MB (4159009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0d161136f55f6e5c26bbd9fde30327cf06dec15e40d7ac330b8db368e4b9ee`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 846.1 KB (846058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a59da16addae7a15d26d4edba174883fd994d29bb943085361990730c6787`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d14b7a612bfb82f68156f623a22e64ab4524cbf82c592f9365a904bac033a5`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e798df308d1bafc2c22d22386cb75aa71c9b8fc3c7b9ff5e736c1464c83bea`  
		Last Modified: Wed, 08 May 2019 11:53:24 GMT  
		Size: 112.0 MB (111951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5962f9d6fd65875c9975a6db12ff0c916944d89184389e3ae3272c6d5690381`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085503a369edcce69a9e4e547a07f501228a3e71b00141b07bf7e4bf3beb4cf2`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5110522604cdddba047cc0be366f16edb6238a77df6c0b690e81f538401402c6`  
		Last Modified: Wed, 08 May 2019 16:17:30 GMT  
		Size: 9.4 MB (9424456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dc9134cb78fa8c8012494e966655a51906b8fbb9a287ff677f112cb6df5b7b`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1cc6aa008e3c92d0e543846f48ffc0278671ad3336e433360f2bbab577e4b7`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 2.1 KB (2066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62368ad6255191b9e3dafc29336216dd0f25b1acacf11eacdfa4a0a9d95b2f5c`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c246600f5484d9d71da31a270a9f1543cf79da2bf94a224314c659b9a66a875e`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9` - linux; arm variant v7

```console
$ docker pull jetty@sha256:9f4c641dc0a44707812e694e8eade3015b6c059b468a4e688634a3c20ed24d0c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176059054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea2dba1b53efa6f56de5449b6625a4945aaa26e65463ca0f2ae298f2ad8ab22`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 12:03:26 GMT
ADD file:7e8dcc40e246d53b86266855a2de8080d26e6b4ed9f594c1acc565784405735b in / 
# Wed, 08 May 2019 12:03:27 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:04:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:14:59 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:15:01 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:16:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 17:55:00 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 17:55:03 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 17:55:03 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 17:55:03 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 17:55:10 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 17:55:12 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 17:55:12 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 17:55:14 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 17:55:16 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 17:55:17 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 17:55:18 GMT
USER jetty
# Wed, 08 May 2019 17:55:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 17:55:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 17:55:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f2a2fd7c1ab35cd1b5ea6fcc2b801f3877852797e2698ecdb9556e0dee3accb5`  
		Last Modified: Wed, 08 May 2019 12:09:40 GMT  
		Size: 42.1 MB (42082604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047df9a92c9f7376283a8d6af526f5126d95995ba48dd7de49979ef57da3e15b`  
		Last Modified: Wed, 08 May 2019 13:12:20 GMT  
		Size: 9.5 MB (9485167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeed4ac8d1e2c751afd6fd3517f1d154365467039353c377c8206fd5eb81d4b`  
		Last Modified: Wed, 08 May 2019 13:12:18 GMT  
		Size: 3.9 MB (3918605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646a29b8c83d854b86dccdbf390a7b296f5144aef4e38276c8a7b649e0804`  
		Last Modified: Wed, 08 May 2019 14:31:13 GMT  
		Size: 830.4 KB (830410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb3a067c54308aa02398bf021c38a952c18f27646b736d71732cbbc9b1010b0`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2c033d6c592b7d46aafecc714f1393be324b57f01f5e6c76e832e8ea04576a`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0d9e8d93d276090a71cd6c8346c468c9e051903bf52760756359c4451d33b`  
		Last Modified: Wed, 08 May 2019 14:34:14 GMT  
		Size: 110.3 MB (110311680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f07a446b7fe57fd236711da5953265e8d532d43c9cb8f25a533320e93a636`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6395f8d7de3564b4ae1e386bf6ed4e0f7723e94d4940a70b485a86504a75926`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc147ed50354f0d2a7587b28055ead9eec49df4f8eb5341d91e746671a6890d9`  
		Last Modified: Wed, 08 May 2019 17:57:20 GMT  
		Size: 9.4 MB (9424492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c93706301b9ef0c48c932aa219a1caa545887de6b3900e134bce06740648f8b`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d03e292fef5d40aada56fd958955f649c1637f1247f0ce20ccbe82940b6ccfd`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 2.1 KB (2069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f2350cc0ff9abae232377501904cbd64860bdbd5db9ef7c24bce5508cf073c`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d04c42b72f7e6024f6fdb7413c30b11da394d870eaa464bda596aa3e99142fc`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2fbb5ca36da5cad300aa58956606b38a8e3f3cecbb41851cdfd0c8696482575e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180322238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2bb61e7225a1b482f1f4664ddfbefa8060a5b43bc65fcd64f9680a51dc4749`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:48:25 GMT
ADD file:153045f4fe6532d8c2ff273bb249a7a3a4cba913c26a4103ba5ddce1af02c1e5 in / 
# Wed, 08 May 2019 08:48:26 GMT
CMD ["bash"]
# Wed, 08 May 2019 11:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:51:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 17 May 2019 22:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 May 2019 22:50:40 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2019 22:50:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 17 May 2019 22:50:42 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_VERSION=8u212
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Fri, 17 May 2019 22:51:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 17 Jul 2019 23:35:39 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2019 23:35:41 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 17 Jul 2019 23:35:41 GMT
WORKDIR /usr/local/jetty
# Wed, 17 Jul 2019 23:35:41 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 17 Jul 2019 23:35:47 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 17 Jul 2019 23:35:49 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 17 Jul 2019 23:35:49 GMT
WORKDIR /var/lib/jetty
# Wed, 17 Jul 2019 23:35:51 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:52 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 17 Jul 2019 23:35:53 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 17 Jul 2019 23:35:53 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 17 Jul 2019 23:35:54 GMT
USER jetty
# Wed, 17 Jul 2019 23:35:54 GMT
EXPOSE 8080
# Wed, 17 Jul 2019 23:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jul 2019 23:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5894e28291972e44f5c3eba2779a85979bae6f95ed4f3e43ea5c98a132f06c48`  
		Last Modified: Wed, 08 May 2019 08:54:43 GMT  
		Size: 43.1 MB (43141955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e6888cee6fef7c223eeaf2ca4c51bc0c21b4631971f416eb6a529a05e96cb`  
		Last Modified: Wed, 08 May 2019 12:07:05 GMT  
		Size: 9.7 MB (9733078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf90e854779f4c5edab378626d847fd0ab7aa9441b63a7db31a7db55d2b255b`  
		Last Modified: Wed, 08 May 2019 12:07:03 GMT  
		Size: 4.1 MB (4094187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc920c054370e9fe777d4546e8898e94588c01909d487696f8378c34d00b67e`  
		Last Modified: Fri, 17 May 2019 22:56:09 GMT  
		Size: 839.6 KB (839611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf483f25e9254d4337fac759851db8d04b5a2eea6056b1375ff19c2df554464`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a594c16f5b8360bf6256529e6a21eddf648595ac48000e0d91808fd21a9798`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9e1dac91c466b57c47d5738767104f91af563b89a969f98a2eff0d0692cd6`  
		Last Modified: Fri, 17 May 2019 23:00:18 GMT  
		Size: 113.1 MB (113082862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7e6b7fd0cb47998762442e0d2b1852c2692786149020092d36d17cbaddad32`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511814053ebc4a22abd8857c39836a2c1b6b9ee89da025924601e08bfb12412c`  
		Last Modified: Wed, 17 Jul 2019 23:37:42 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0bf7b138eb0319a3d75d1ab842fb65cd204e1c83dd7e92e2a0fb122cb2403d`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 9.4 MB (9424451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588601cf5b3de57b436e290ae8115f8bd4cd5553d0a88a42e233f763d21441b0`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2670e29c10dc3bc2f5c75c700e415015925039c9b4751a8920fdaebbb4f1c2e`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a627374a49fddcb68bd3f2ce734e8fbd58f7c745c55ac425411ca144d003de8`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b7659478cc7567aa9d6d6a3700403d10e80bf5542bc7846c6fc05f366f870`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9` - linux; 386

```console
$ docker pull jetty@sha256:f532a68e9bbf79732ee7dbfaa205e1b742f0c2fefb7e19ba5c0d6d1491cbba08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194362543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd22310a1a4ac81a7cd7b96c967f835781080ad5f817dd7161256eb8ae0207e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 10:49:19 GMT
ADD file:fde8cf5700c66c38b88d4b3254ec1544d09194e06568c23fe3989f7eaa1f5785 in / 
# Wed, 08 May 2019 10:49:20 GMT
CMD ["bash"]
# Wed, 08 May 2019 19:08:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 19:08:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 22:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 22:16:13 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 22:16:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 22:16:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 04:57:10 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 04:57:11 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 04:57:11 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 04:57:16 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 04:57:17 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 04:57:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 04:57:19 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:19 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 04:57:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 04:57:20 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 04:57:20 GMT
USER jetty
# Thu, 09 May 2019 04:57:20 GMT
EXPOSE 8080
# Thu, 09 May 2019 04:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 04:57:21 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b5d586ad7adeab23f6ff0b7ec90785dc757eaccd445976fda3f6d7db64d20585`  
		Last Modified: Wed, 08 May 2019 10:57:26 GMT  
		Size: 46.1 MB (46063371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b18ff57de8d55737be40848138cbd66efcc99443ae507217ae5dd45e3cf41a`  
		Last Modified: Wed, 08 May 2019 19:14:07 GMT  
		Size: 10.8 MB (10802110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc701b379559241c696cd079ff9b83f0bba19faec8747d75654fe5bc7e8adb03`  
		Last Modified: Wed, 08 May 2019 19:14:05 GMT  
		Size: 4.6 MB (4561353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad72e88a4544f4570c0df9df66b43ca05325a8df5fe4bdac5e0240836f47d28`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 862.0 KB (862001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215fde6b1eafb43012d68d65388471bca2066ad401d508df13b046aa8b830e1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf128bb9e196d3a692d14dc4ed9c91920ab3ecb3fcb3d7e4c968fb1f18b9ce1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47742760e75d51e74c18576e2a0b2d447e91b2c3a023dc9e3b1e4a83aa7bdc1a`  
		Last Modified: Wed, 08 May 2019 22:52:46 GMT  
		Size: 122.6 MB (122643377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13df399b06606cedbc7ffce659af330dab9041dfebd5d98933853a74a0be48d3`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d50318d694cf0cf2727460d2057498228249819a1d83c2f92296c96dbfb1e`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad229b08fbaea588098dc7e42976c29d5b7a16be0e2a84b3ba0d811c5d724494`  
		Last Modified: Thu, 09 May 2019 04:58:53 GMT  
		Size: 9.4 MB (9424415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7161f78a4fe1f1d0ee6787a7f6f28b0a0241c7390a5c919ee688aac0caf3fef`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4163317071202eac58e9e3c5ec95d8b071ae013148d4f1376fdc09a340c7ed6b`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4d72a3ad59ec8fada471aa84164b581dd500aea022f038334b0eda00c0ec19`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7621b6c4a7959d913a05ce51aa49a199c616badaaa439ea6873fe8c5a9b89ee`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9` - linux; ppc64le

```console
$ docker pull jetty@sha256:1c8d35096fdcfc3c448b203db5c12734655105f9f779d3734522511764e58233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184781497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eacbfac25da6c191d70cca800f7ed9b015a19adef7c4ab701c0b31540a6159e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:57:43 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:57:49 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:57:56 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:57:59 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 12:58:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 12:58:05 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 13:05:08 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 21:43:25 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 21:43:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 21:43:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 21:43:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 21:43:51 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 21:43:57 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 21:44:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 21:44:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 21:44:22 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:44:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 21:44:33 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 21:44:40 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 21:44:57 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:45:03 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 21:45:10 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 21:45:11 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 21:45:13 GMT
USER jetty
# Wed, 08 May 2019 21:45:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 21:45:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 21:45:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e4e060b9a0f1aadc5647d44be482b1363697a3fd8a4aeb6a4b9c53e17ecc4`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 848.6 KB (848616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e24f3bccdd6d1d666b5c75ba2971c3c1d1b974352776ac0c8d91b0244f35cb`  
		Last Modified: Wed, 08 May 2019 13:20:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f7a6e570eaf9c696f99b09d6fb9eaf034d87e7a1e9bf092cd38e9f71777a8b`  
		Last Modified: Wed, 08 May 2019 13:20:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a3232b209a6e8e5f133bb2d4b9c377dab2d71b8b57de44e32eefb5584bfd2`  
		Last Modified: Wed, 08 May 2019 13:21:49 GMT  
		Size: 114.6 MB (114611463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321ac118136d891526d4b7d585903133a760850fd8ba7b73f5608b51d289a8a`  
		Last Modified: Wed, 08 May 2019 21:50:41 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86141b28655e4b923da175ff032f463f8ef7bf16d23578dd00d25badfdce9b79`  
		Last Modified: Wed, 08 May 2019 21:50:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0e68a17da043f652f2d812d9c650558c382a9c2be40bb8fd901e19d89cb162`  
		Last Modified: Wed, 08 May 2019 21:50:38 GMT  
		Size: 9.4 MB (9424473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec696722258c05e106b7c921898aac4da7e2ab6ae65076942a12749f1049140b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cae7017c7325beea0f896b47ae71aa44260cac66b36379a32dbb0ed9309eaf`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 2.1 KB (2062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8302b92229dab552b306d2b48fba615a169e28af57e2c7fae6324ef3b4b028`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd387f05feedbcf33516453c4c46c64a80261af3ff1e6ebf007ccac52a95b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9` - linux; s390x

```console
$ docker pull jetty@sha256:eb8f97a23898ccdc5be026ea051ef231615b9455a4d78a72cbeb093439440cf5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184363097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55031fcaf6fba1a2c7256bad7bbcc09b11b036dbceb1807ceeacc9202792f231`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:42:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:52:21 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:52:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:52:32 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:52:35 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:54:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 05:12:37 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 05:12:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 05:12:42 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 05:12:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 05:12:59 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 05:13:05 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 05:13:06 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 05:13:16 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:16 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 05:13:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 05:13:21 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 05:13:22 GMT
USER jetty
# Thu, 09 May 2019 05:13:23 GMT
EXPOSE 8080
# Thu, 09 May 2019 05:13:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 05:13:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf61465b03d8ec5e8064ba91220d0e97c4dd5b75a7d2fe644aab7cc4a0a514c`  
		Last Modified: Wed, 08 May 2019 15:01:34 GMT  
		Size: 863.9 KB (863943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35375a807e76af07efe2bf1c77fce29498511166f4b41f158e181805528ce229`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53975ff11a25b69ce30d4b02d88f1b27cff3e5b1a2e08d05f6721e388f4a5d`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d381e46be773491220b0199e519c4f97308fee82af49481321e3d769db7b7b0a`  
		Last Modified: Wed, 08 May 2019 15:05:36 GMT  
		Size: 114.2 MB (114184348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e456897b935f1efded84a648055389e6c4fffbee3a50167ab95bf7cf047142`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace4f725dd5f318c30a864c4400d34b9d1dfeb8dba95f242af7e8668945d2a20`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6df7195f7b6c83e938c25f1940930649b862e2b5369ec6e041631c4cb1ebef`  
		Last Modified: Thu, 09 May 2019 05:17:27 GMT  
		Size: 9.4 MB (9424383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef61c6677aef99352724f560861db552edff24e57f288598be141e49f0802c8`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16572dc3fb4702653a0252ed5b29eb536479f0085f7ec2596c9d1c2e8214fd2f`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0aa75b063a662a0cd7f4af7b720863dfa8c7643b98bfc4b8ee5124a1bb069e`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ce48b6bff7dbea769d046b7311e98e7ea33aec40dca23a246a4b2c1fe530c5`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.2.29-jre8`

**does not exist** (yet?)

## `jetty:9.2-jre8`

```console
$ docker pull jetty@sha256:647ea8e3454e36dd501cd4a608eb9746f46affa7340ca1ba64a72b8b661bd090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `jetty:9.2-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:0f58026e54e34b177140dc6062ba104cc866b80d4960262638109b6070ac7269
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115881642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e41574dde1222a4a095abe35df7d94c055873ba7a3575befb08363fd9f8d77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 08:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:55:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 Dec 2019 08:56:57 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_VERSION=8u232
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_URL_VERSION=8u232b09
# Sat, 28 Dec 2019 08:57:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sun, 29 Dec 2019 08:31:21 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Sun, 29 Dec 2019 08:31:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sun, 29 Dec 2019 08:31:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2019 08:31:22 GMT
RUN mkdir -p "$JETTY_HOME"
# Sun, 29 Dec 2019 08:31:23 GMT
WORKDIR /usr/local/jetty
# Sun, 29 Dec 2019 08:31:57 GMT
ENV JETTY_VERSION=9.2.28.v20190418
# Sun, 29 Dec 2019 08:31:57 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.28.v20190418/jetty-distribution-9.2.28.v20190418.tar.gz
# Sun, 29 Dec 2019 08:31:57 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Sun, 29 Dec 2019 08:32:02 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:32:02 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sun, 29 Dec 2019 08:32:03 GMT
RUN mkdir -p "$JETTY_BASE"
# Sun, 29 Dec 2019 08:32:03 GMT
WORKDIR /var/lib/jetty
# Sun, 29 Dec 2019 08:32:04 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:32:04 GMT
ENV TMPDIR=/tmp/jetty
# Sun, 29 Dec 2019 08:32:05 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Sun, 29 Dec 2019 08:32:05 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Sun, 29 Dec 2019 08:32:06 GMT
USER jetty
# Sun, 29 Dec 2019 08:32:06 GMT
EXPOSE 8080
# Sun, 29 Dec 2019 08:32:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 Dec 2019 08:32:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8d3cd13de4f1c574d86de1c90b7e0f96d2394349c7e882117daaa86ad08ad`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 5.1 MB (5126129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06bdc5e0db3a85fca16aae57afb18ced9fad56ed4571f9bd0d748f38930b22`  
		Last Modified: Sat, 28 Dec 2019 09:03:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b1f94cfe4ae6c7ca9e45cc45491b7f732d099001d933ac72211dbd09d19e0d`  
		Last Modified: Sat, 28 Dec 2019 09:03:45 GMT  
		Size: 40.2 MB (40196546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe20b880320d8f58a256fe49d1c7c23c61b64baa639ad7279118a09e05b99b2b`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b913b52ac10d2aec4b74f5b78af565b0c0b25888a4c4826a1301239a847aab`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee26f495823e96ca864fb8d1e65f31d1cfec9d4375161bc13540ee592b7d9ec`  
		Last Modified: Sun, 29 Dec 2019 08:32:45 GMT  
		Size: 10.0 MB (10035655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f2fa2f5dff4e85e6550218739e967717d3f511f4984ba1758d1608920d186`  
		Last Modified: Sun, 29 Dec 2019 08:32:44 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddee3cdbaef69e82e12891a14b2a0bfe9150622fe1f00158c3d4cfe1e2e11e46`  
		Last Modified: Sun, 29 Dec 2019 08:32:44 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60ff7f23a4f2c7818fe1201defdff411ba46eeb10154809378a3d9a28c59e7a`  
		Last Modified: Sun, 29 Dec 2019 08:32:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fc1a72cf7868feeb84e4a6ccb7095b8ece52b8bb2c54951c5d77b802d7dc27`  
		Last Modified: Sun, 29 Dec 2019 08:32:44 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.2-jre8` - linux; arm variant v5

```console
$ docker pull jetty@sha256:04d8f63470130f972c0cee6f016b0baa5bcd7f84eb534451940ba56994f7875a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180897860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8349f1c1658fddcbd4fdd7c9108255a012fc21fe99bd0d6c08acc53c21a08335`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:53:17 GMT
ADD file:5dfe3b771bd67a2856913544993e219cb8c7933c33523cc56fe13a3a0e76ce9b in / 
# Wed, 08 May 2019 08:53:18 GMT
CMD ["bash"]
# Wed, 08 May 2019 10:01:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 10:01:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 11:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:35:27 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 11:35:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 11:35:31 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 11:36:37 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 16:15:13 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 16:15:13 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 16:15:14 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 16:15:16 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 16:15:16 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 16:16:12 GMT
ENV JETTY_VERSION=9.2.28.v20190418
# Wed, 08 May 2019 16:16:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.28.v20190418/jetty-distribution-9.2.28.v20190418.tar.gz
# Wed, 08 May 2019 16:16:13 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 16:16:19 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:16:19 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 16:16:21 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 16:16:21 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 16:16:25 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:16:25 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 16:16:27 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 16:16:28 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 16:16:28 GMT
USER jetty
# Wed, 08 May 2019 16:16:28 GMT
EXPOSE 8080
# Wed, 08 May 2019 16:16:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 16:16:29 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ca892ced475bf1c51c1f13b76a64549cfc5d1a0b55d33d8b9418efbb47887bf8`  
		Last Modified: Wed, 08 May 2019 08:59:09 GMT  
		Size: 44.0 MB (44045778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b30b379469b50f6ada866964876f5c4ba164c22896bf3a08aabab61869e51`  
		Last Modified: Wed, 08 May 2019 10:09:26 GMT  
		Size: 9.9 MB (9854225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e257762b4747840fc09dce269e7f68146ac9864b8bf218e57475b4af367a74`  
		Last Modified: Wed, 08 May 2019 10:09:24 GMT  
		Size: 4.2 MB (4159009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0d161136f55f6e5c26bbd9fde30327cf06dec15e40d7ac330b8db368e4b9ee`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 846.1 KB (846058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a59da16addae7a15d26d4edba174883fd994d29bb943085361990730c6787`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d14b7a612bfb82f68156f623a22e64ab4524cbf82c592f9365a904bac033a5`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e798df308d1bafc2c22d22386cb75aa71c9b8fc3c7b9ff5e736c1464c83bea`  
		Last Modified: Wed, 08 May 2019 11:53:24 GMT  
		Size: 112.0 MB (111951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5962f9d6fd65875c9975a6db12ff0c916944d89184389e3ae3272c6d5690381`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085503a369edcce69a9e4e547a07f501228a3e71b00141b07bf7e4bf3beb4cf2`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4394d3a44132d93fde6811a4ad046fdffbd055716381183253bb16ce72fabd09`  
		Last Modified: Wed, 08 May 2019 16:18:01 GMT  
		Size: 10.0 MB (10035789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4701b6fbd811bf80abf890555a098d3840d011cc92e00c7877c74b1fc89e4eff`  
		Last Modified: Wed, 08 May 2019 16:17:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd5f0ce7f1be935f5054ca2c09fb3051c8c17c509f25a6926f08f9340553fe5`  
		Last Modified: Wed, 08 May 2019 16:17:59 GMT  
		Size: 1.5 KB (1540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1c11b7d2f4497a0fa82e5885e4f0ddb7193461c09ab0cf97e058310511f337`  
		Last Modified: Wed, 08 May 2019 16:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76801c1c23aecbd124e83da380de8c9620dd49fcf337479380a04b635af6a7`  
		Last Modified: Wed, 08 May 2019 16:18:00 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.2-jre8` - linux; arm variant v7

```console
$ docker pull jetty@sha256:26b7882088c12fab8ac457d0ae92f2d833153eaff9817bd874dcce541e3912f4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176669804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4b052f2691d3058dd13b45463adafd25f5756fc084541c072c21568c307105`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 12:03:26 GMT
ADD file:7e8dcc40e246d53b86266855a2de8080d26e6b4ed9f594c1acc565784405735b in / 
# Wed, 08 May 2019 12:03:27 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:04:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:14:59 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:15:01 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:16:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 17:55:00 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 17:55:03 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 17:55:03 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 17:56:00 GMT
ENV JETTY_VERSION=9.2.28.v20190418
# Wed, 08 May 2019 17:56:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.28.v20190418/jetty-distribution-9.2.28.v20190418.tar.gz
# Wed, 08 May 2019 17:56:02 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 17:56:09 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:56:09 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 17:56:11 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 17:56:11 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 17:56:14 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:56:14 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 17:56:16 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 17:56:16 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 17:56:17 GMT
USER jetty
# Wed, 08 May 2019 17:56:17 GMT
EXPOSE 8080
# Wed, 08 May 2019 17:56:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 17:56:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f2a2fd7c1ab35cd1b5ea6fcc2b801f3877852797e2698ecdb9556e0dee3accb5`  
		Last Modified: Wed, 08 May 2019 12:09:40 GMT  
		Size: 42.1 MB (42082604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047df9a92c9f7376283a8d6af526f5126d95995ba48dd7de49979ef57da3e15b`  
		Last Modified: Wed, 08 May 2019 13:12:20 GMT  
		Size: 9.5 MB (9485167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeed4ac8d1e2c751afd6fd3517f1d154365467039353c377c8206fd5eb81d4b`  
		Last Modified: Wed, 08 May 2019 13:12:18 GMT  
		Size: 3.9 MB (3918605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646a29b8c83d854b86dccdbf390a7b296f5144aef4e38276c8a7b649e0804`  
		Last Modified: Wed, 08 May 2019 14:31:13 GMT  
		Size: 830.4 KB (830410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb3a067c54308aa02398bf021c38a952c18f27646b736d71732cbbc9b1010b0`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2c033d6c592b7d46aafecc714f1393be324b57f01f5e6c76e832e8ea04576a`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0d9e8d93d276090a71cd6c8346c468c9e051903bf52760756359c4451d33b`  
		Last Modified: Wed, 08 May 2019 14:34:14 GMT  
		Size: 110.3 MB (110311680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f07a446b7fe57fd236711da5953265e8d532d43c9cb8f25a533320e93a636`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6395f8d7de3564b4ae1e386bf6ed4e0f7723e94d4940a70b485a86504a75926`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c8e67e281bfebf30f03c7ad2a55f479e03af517206c0a24788f69bff9c0672`  
		Last Modified: Wed, 08 May 2019 17:57:55 GMT  
		Size: 10.0 MB (10035777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a964ed2ec6aa3c089e730074b69cfb590984bb0dcee3b6d6328884b85a6e1704`  
		Last Modified: Wed, 08 May 2019 17:57:53 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e09f0811fe2b633039c694b686e82137c1cd51933072d7326b2b2f35a49c3d4`  
		Last Modified: Wed, 08 May 2019 17:57:53 GMT  
		Size: 1.5 KB (1533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b3ea602d270c8a9010918480ffffffdad9183699e112458ef198d21c6b6e07`  
		Last Modified: Wed, 08 May 2019 17:57:53 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303fec51625f64aff15e746da0b837cbd52aa569f11af11c3e09bb126973a5e0`  
		Last Modified: Wed, 08 May 2019 17:57:53 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.2-jre8` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:8ed921ed17db5e9bc65d9746ee348dd2fec5cc75831653a325cd6a759b167397
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180933029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d3d88c828034a62b47ba9fbf8cefb095514ae3e4a82df3c524b84e334bb162`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:48:25 GMT
ADD file:153045f4fe6532d8c2ff273bb249a7a3a4cba913c26a4103ba5ddce1af02c1e5 in / 
# Wed, 08 May 2019 08:48:26 GMT
CMD ["bash"]
# Wed, 08 May 2019 11:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:51:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 17 May 2019 22:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 May 2019 22:50:40 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2019 22:50:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 17 May 2019 22:50:42 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_VERSION=8u212
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Fri, 17 May 2019 22:51:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 17 Jul 2019 23:35:39 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2019 23:35:41 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 17 Jul 2019 23:35:41 GMT
WORKDIR /usr/local/jetty
# Wed, 17 Jul 2019 23:36:55 GMT
ENV JETTY_VERSION=9.2.28.v20190418
# Wed, 17 Jul 2019 23:36:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.28.v20190418/jetty-distribution-9.2.28.v20190418.tar.gz
# Wed, 17 Jul 2019 23:36:55 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 17 Jul 2019 23:37:01 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:37:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 17 Jul 2019 23:37:02 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 17 Jul 2019 23:37:03 GMT
WORKDIR /var/lib/jetty
# Wed, 17 Jul 2019 23:37:04 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:37:05 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 17 Jul 2019 23:37:06 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 17 Jul 2019 23:37:07 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 17 Jul 2019 23:37:07 GMT
USER jetty
# Wed, 17 Jul 2019 23:37:07 GMT
EXPOSE 8080
# Wed, 17 Jul 2019 23:37:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jul 2019 23:37:08 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5894e28291972e44f5c3eba2779a85979bae6f95ed4f3e43ea5c98a132f06c48`  
		Last Modified: Wed, 08 May 2019 08:54:43 GMT  
		Size: 43.1 MB (43141955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e6888cee6fef7c223eeaf2ca4c51bc0c21b4631971f416eb6a529a05e96cb`  
		Last Modified: Wed, 08 May 2019 12:07:05 GMT  
		Size: 9.7 MB (9733078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf90e854779f4c5edab378626d847fd0ab7aa9441b63a7db31a7db55d2b255b`  
		Last Modified: Wed, 08 May 2019 12:07:03 GMT  
		Size: 4.1 MB (4094187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc920c054370e9fe777d4546e8898e94588c01909d487696f8378c34d00b67e`  
		Last Modified: Fri, 17 May 2019 22:56:09 GMT  
		Size: 839.6 KB (839611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf483f25e9254d4337fac759851db8d04b5a2eea6056b1375ff19c2df554464`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a594c16f5b8360bf6256529e6a21eddf648595ac48000e0d91808fd21a9798`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9e1dac91c466b57c47d5738767104f91af563b89a969f98a2eff0d0692cd6`  
		Last Modified: Fri, 17 May 2019 23:00:18 GMT  
		Size: 113.1 MB (113082862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7e6b7fd0cb47998762442e0d2b1852c2692786149020092d36d17cbaddad32`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511814053ebc4a22abd8857c39836a2c1b6b9ee89da025924601e08bfb12412c`  
		Last Modified: Wed, 17 Jul 2019 23:37:42 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b994ec9d2073a6b432d855cd85d09cfac1aaafe7bc32bf39656c4e6cc9eb079a`  
		Last Modified: Wed, 17 Jul 2019 23:38:38 GMT  
		Size: 10.0 MB (10035770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947a1fafbaae2a6dc8bab210c922a669bfe4d98e83926672957f6e7ad4f101a9`  
		Last Modified: Wed, 17 Jul 2019 23:38:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173cc86dea934ea621dedb85f39ec97f346684c541e7925b17dc2609278a076e`  
		Last Modified: Wed, 17 Jul 2019 23:38:36 GMT  
		Size: 1.5 KB (1533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4854ecaa51fb036678e712b2e97740cad605f9d9fed9b633ae21ea922a3fd327`  
		Last Modified: Wed, 17 Jul 2019 23:38:36 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a690d7c9918c7c12f6c6008eb3166675a41703ff9b36b0f4155bd25eaf9d2e26`  
		Last Modified: Wed, 17 Jul 2019 23:38:36 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.2-jre8` - linux; 386

```console
$ docker pull jetty@sha256:240eb848c98a39fb8f5111abef371d1abc157384d68391e5dd4c3cd11b1015b6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194973289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4dfaebb65b4dd721f6dce7bf07ce97c4f9794ea36d8c29543e43d17a71a236`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 10:49:19 GMT
ADD file:fde8cf5700c66c38b88d4b3254ec1544d09194e06568c23fe3989f7eaa1f5785 in / 
# Wed, 08 May 2019 10:49:20 GMT
CMD ["bash"]
# Wed, 08 May 2019 19:08:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 19:08:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 22:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 22:16:13 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 22:16:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 22:16:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 04:57:10 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 04:57:11 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 04:57:11 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 04:57:42 GMT
ENV JETTY_VERSION=9.2.28.v20190418
# Thu, 09 May 2019 04:57:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.28.v20190418/jetty-distribution-9.2.28.v20190418.tar.gz
# Thu, 09 May 2019 04:57:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 04:57:46 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:46 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 04:57:47 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 04:57:47 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 04:57:49 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:49 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 04:57:50 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 04:57:50 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 04:57:50 GMT
USER jetty
# Thu, 09 May 2019 04:57:50 GMT
EXPOSE 8080
# Thu, 09 May 2019 04:57:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 04:57:51 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b5d586ad7adeab23f6ff0b7ec90785dc757eaccd445976fda3f6d7db64d20585`  
		Last Modified: Wed, 08 May 2019 10:57:26 GMT  
		Size: 46.1 MB (46063371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b18ff57de8d55737be40848138cbd66efcc99443ae507217ae5dd45e3cf41a`  
		Last Modified: Wed, 08 May 2019 19:14:07 GMT  
		Size: 10.8 MB (10802110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc701b379559241c696cd079ff9b83f0bba19faec8747d75654fe5bc7e8adb03`  
		Last Modified: Wed, 08 May 2019 19:14:05 GMT  
		Size: 4.6 MB (4561353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad72e88a4544f4570c0df9df66b43ca05325a8df5fe4bdac5e0240836f47d28`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 862.0 KB (862001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215fde6b1eafb43012d68d65388471bca2066ad401d508df13b046aa8b830e1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf128bb9e196d3a692d14dc4ed9c91920ab3ecb3fcb3d7e4c968fb1f18b9ce1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47742760e75d51e74c18576e2a0b2d447e91b2c3a023dc9e3b1e4a83aa7bdc1a`  
		Last Modified: Wed, 08 May 2019 22:52:46 GMT  
		Size: 122.6 MB (122643377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13df399b06606cedbc7ffce659af330dab9041dfebd5d98933853a74a0be48d3`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d50318d694cf0cf2727460d2057498228249819a1d83c2f92296c96dbfb1e`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4362b7bb0069be5dcff8e4175e33aa799469f44202503a028ee8d80f76694c0`  
		Last Modified: Thu, 09 May 2019 04:59:10 GMT  
		Size: 10.0 MB (10035691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e05220547325e601521869a2e7821138bd81d71bc19d683b4fe7881da22fd`  
		Last Modified: Thu, 09 May 2019 04:59:09 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b78f6dc7c369b47071d27683746217050158591b0d5baa06360576c851c86a1`  
		Last Modified: Thu, 09 May 2019 04:59:09 GMT  
		Size: 1.5 KB (1467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae71d6df37d64b1efab22bd6be93d506508a614ea8cd6bc7fac9d7eb0a41d250`  
		Last Modified: Thu, 09 May 2019 04:59:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0933db5a2583461e382c74a9c9c032c607ceecbeaae6c32f40f21c0737c581`  
		Last Modified: Thu, 09 May 2019 04:59:09 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.2-jre8` - linux; ppc64le

```console
$ docker pull jetty@sha256:95d72b250edf1075705bb173517d3f2cbfc26c0141376295831fbd7ef1fb1511
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185392272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851f8fcf725361f7602448a4259de9f291cb70286f31b3653933c3137f370d27`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:57:43 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:57:49 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:57:56 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:57:59 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 12:58:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 12:58:05 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 13:05:08 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 21:43:25 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 21:43:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 21:43:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 21:43:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 21:43:51 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 21:47:29 GMT
ENV JETTY_VERSION=9.2.28.v20190418
# Wed, 08 May 2019 21:47:34 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.28.v20190418/jetty-distribution-9.2.28.v20190418.tar.gz
# Wed, 08 May 2019 21:47:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 21:48:01 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:48:07 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 21:48:19 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 21:48:24 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 21:48:32 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:48:36 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 21:48:48 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 21:48:50 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 21:48:55 GMT
USER jetty
# Wed, 08 May 2019 21:49:01 GMT
EXPOSE 8080
# Wed, 08 May 2019 21:49:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 21:49:10 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e4e060b9a0f1aadc5647d44be482b1363697a3fd8a4aeb6a4b9c53e17ecc4`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 848.6 KB (848616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e24f3bccdd6d1d666b5c75ba2971c3c1d1b974352776ac0c8d91b0244f35cb`  
		Last Modified: Wed, 08 May 2019 13:20:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f7a6e570eaf9c696f99b09d6fb9eaf034d87e7a1e9bf092cd38e9f71777a8b`  
		Last Modified: Wed, 08 May 2019 13:20:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a3232b209a6e8e5f133bb2d4b9c377dab2d71b8b57de44e32eefb5584bfd2`  
		Last Modified: Wed, 08 May 2019 13:21:49 GMT  
		Size: 114.6 MB (114611463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321ac118136d891526d4b7d585903133a760850fd8ba7b73f5608b51d289a8a`  
		Last Modified: Wed, 08 May 2019 21:50:41 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86141b28655e4b923da175ff032f463f8ef7bf16d23578dd00d25badfdce9b79`  
		Last Modified: Wed, 08 May 2019 21:50:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90a6f854f5d66dc9d7ebdb45f2437c46c6fe629b67d676f323d44a0ea3a78db`  
		Last Modified: Wed, 08 May 2019 21:51:46 GMT  
		Size: 10.0 MB (10035772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2501adb43cfe8f31b9d5dea6808cea8f931fbbca1d4b310a77613dadac09d1`  
		Last Modified: Wed, 08 May 2019 21:51:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f266ff04ecfdaeb3b35d7acf47b8c5d959844e7d98f192c3ed8bda8641df568`  
		Last Modified: Wed, 08 May 2019 21:51:39 GMT  
		Size: 1.5 KB (1534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dccb15c0535a080eb93171585f16fc232705e175830cf2ec4ad359bb3c17fd`  
		Last Modified: Wed, 08 May 2019 21:51:39 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472cbf5e822fcebafdb1df247378fa42cc984efd7d23ba27127754aa0cdba2c5`  
		Last Modified: Wed, 08 May 2019 21:51:39 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.2-jre8` - linux; s390x

```console
$ docker pull jetty@sha256:422b7b0da1638af7a02380abd11dbb3959b2d9483a0009cbe4ab73ad15e328e9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184973868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75613612d16bede30db5d7c07a18d37fcc52be99255f5a1da518d54b64ec6db5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:42:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:52:21 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:52:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:52:32 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:52:35 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:54:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 05:12:37 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 05:12:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 05:12:42 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 05:14:58 GMT
ENV JETTY_VERSION=9.2.28.v20190418
# Thu, 09 May 2019 05:15:00 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.28.v20190418/jetty-distribution-9.2.28.v20190418.tar.gz
# Thu, 09 May 2019 05:15:00 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 05:15:14 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:15:15 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 05:15:20 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 05:15:21 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 05:15:30 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:15:31 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 05:15:38 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 05:15:40 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 05:15:41 GMT
USER jetty
# Thu, 09 May 2019 05:15:42 GMT
EXPOSE 8080
# Thu, 09 May 2019 05:15:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 05:15:44 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf61465b03d8ec5e8064ba91220d0e97c4dd5b75a7d2fe644aab7cc4a0a514c`  
		Last Modified: Wed, 08 May 2019 15:01:34 GMT  
		Size: 863.9 KB (863943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35375a807e76af07efe2bf1c77fce29498511166f4b41f158e181805528ce229`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53975ff11a25b69ce30d4b02d88f1b27cff3e5b1a2e08d05f6721e388f4a5d`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d381e46be773491220b0199e519c4f97308fee82af49481321e3d769db7b7b0a`  
		Last Modified: Wed, 08 May 2019 15:05:36 GMT  
		Size: 114.2 MB (114184348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e456897b935f1efded84a648055389e6c4fffbee3a50167ab95bf7cf047142`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace4f725dd5f318c30a864c4400d34b9d1dfeb8dba95f242af7e8668945d2a20`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f133e710a2013852ce9e63358900aa65303aaa87f2c2d29fcd31a32fce55dd38`  
		Last Modified: Thu, 09 May 2019 05:18:29 GMT  
		Size: 10.0 MB (10035674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755dd9e2914bb6d8b8bfa1b22c6de9836c44eeb4e3a854e03a8807825cf48961`  
		Last Modified: Thu, 09 May 2019 05:18:26 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e570acfe6497460e017fee350a5d063d080f3e8a9d0bc8c7e3fddbd5187310`  
		Last Modified: Thu, 09 May 2019 05:18:26 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3ab93ffb9396b0dc938b136f25aea904427993e887df005179cb3c20c04786`  
		Last Modified: Thu, 09 May 2019 05:18:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e45d01b816d46383495b78f5c3ac2525b7cafd2e5099b10ccd58a5c163882e`  
		Last Modified: Thu, 09 May 2019 05:18:26 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.3.28-jre8`

**does not exist** (yet?)

## `jetty:9.3-jre8`

```console
$ docker pull jetty@sha256:faaab03682b7c610639c4971d52e2d4c8956a1c1309856d46487ff749393ff84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `jetty:9.3-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:4123b030cb02e7e77ec022cb10c35c461b24300dc47bc75f4ed0ed1566898393
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113958720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed4d6b05aa21e1f4405294b7f151ea15510af5ad4ce050b40d47f076b9f2ab6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 08:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:55:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 Dec 2019 08:56:57 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_VERSION=8u232
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_URL_VERSION=8u232b09
# Sat, 28 Dec 2019 08:57:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sun, 29 Dec 2019 08:31:21 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Sun, 29 Dec 2019 08:31:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sun, 29 Dec 2019 08:31:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2019 08:31:22 GMT
RUN mkdir -p "$JETTY_HOME"
# Sun, 29 Dec 2019 08:31:23 GMT
WORKDIR /usr/local/jetty
# Sun, 29 Dec 2019 08:31:40 GMT
ENV JETTY_VERSION=9.3.27.v20190418
# Sun, 29 Dec 2019 08:31:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.27.v20190418/jetty-distribution-9.3.27.v20190418.tar.gz
# Sun, 29 Dec 2019 08:31:40 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Sun, 29 Dec 2019 08:31:45 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:45 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sun, 29 Dec 2019 08:31:46 GMT
RUN mkdir -p "$JETTY_BASE"
# Sun, 29 Dec 2019 08:31:46 GMT
WORKDIR /var/lib/jetty
# Sun, 29 Dec 2019 08:31:47 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:48 GMT
ENV TMPDIR=/tmp/jetty
# Sun, 29 Dec 2019 08:31:48 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Sun, 29 Dec 2019 08:31:48 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Sun, 29 Dec 2019 08:31:49 GMT
USER jetty
# Sun, 29 Dec 2019 08:31:49 GMT
EXPOSE 8080
# Sun, 29 Dec 2019 08:31:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 Dec 2019 08:31:49 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8d3cd13de4f1c574d86de1c90b7e0f96d2394349c7e882117daaa86ad08ad`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 5.1 MB (5126129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06bdc5e0db3a85fca16aae57afb18ced9fad56ed4571f9bd0d748f38930b22`  
		Last Modified: Sat, 28 Dec 2019 09:03:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b1f94cfe4ae6c7ca9e45cc45491b7f732d099001d933ac72211dbd09d19e0d`  
		Last Modified: Sat, 28 Dec 2019 09:03:45 GMT  
		Size: 40.2 MB (40196546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe20b880320d8f58a256fe49d1c7c23c61b64baa639ad7279118a09e05b99b2b`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b913b52ac10d2aec4b74f5b78af565b0c0b25888a4c4826a1301239a847aab`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b46272054ce3d5927bc6b926d76002ecba7fad0c3a03b0c55c5fd716aef836`  
		Last Modified: Sun, 29 Dec 2019 08:32:39 GMT  
		Size: 8.1 MB (8112443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7dd267fa512e4b076b5cbd006da8222f98edabd0a54b948d4ebeee24679a8fd`  
		Last Modified: Sun, 29 Dec 2019 08:32:39 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d8fe1136a772025228bb66d2f05f776775b4117655e2cdff8241a051e576da`  
		Last Modified: Sun, 29 Dec 2019 08:32:38 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd8a35721d30ac712a1da11eaad54e8fa95c264d6e5119ac7d70614686f43b`  
		Last Modified: Sun, 29 Dec 2019 08:32:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71d7e3ee50e57617e8677d53ebe7c94db7d0d1dd2308462e6ebcf0ffe841cbb`  
		Last Modified: Sun, 29 Dec 2019 08:32:38 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.3-jre8` - linux; arm variant v5

```console
$ docker pull jetty@sha256:9a2c0fd004b59134ef9a6d9a1aebed4dda3e92493a427dee77ef2eee934ed733
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178974966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f2c8bb94dce94cc2954b47ab757fc3b889fa6e01781267320f3946be4f5055`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:53:17 GMT
ADD file:5dfe3b771bd67a2856913544993e219cb8c7933c33523cc56fe13a3a0e76ce9b in / 
# Wed, 08 May 2019 08:53:18 GMT
CMD ["bash"]
# Wed, 08 May 2019 10:01:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 10:01:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 11:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:35:27 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 11:35:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 11:35:31 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 11:36:37 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 16:15:13 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 16:15:13 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 16:15:14 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 16:15:16 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 16:15:16 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 16:15:46 GMT
ENV JETTY_VERSION=9.3.27.v20190418
# Wed, 08 May 2019 16:15:46 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.27.v20190418/jetty-distribution-9.3.27.v20190418.tar.gz
# Wed, 08 May 2019 16:15:47 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 16:15:53 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:54 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 16:15:56 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 16:15:57 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 16:16:00 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:16:01 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 16:16:02 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 16:16:03 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 16:16:03 GMT
USER jetty
# Wed, 08 May 2019 16:16:04 GMT
EXPOSE 8080
# Wed, 08 May 2019 16:16:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 16:16:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ca892ced475bf1c51c1f13b76a64549cfc5d1a0b55d33d8b9418efbb47887bf8`  
		Last Modified: Wed, 08 May 2019 08:59:09 GMT  
		Size: 44.0 MB (44045778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b30b379469b50f6ada866964876f5c4ba164c22896bf3a08aabab61869e51`  
		Last Modified: Wed, 08 May 2019 10:09:26 GMT  
		Size: 9.9 MB (9854225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e257762b4747840fc09dce269e7f68146ac9864b8bf218e57475b4af367a74`  
		Last Modified: Wed, 08 May 2019 10:09:24 GMT  
		Size: 4.2 MB (4159009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0d161136f55f6e5c26bbd9fde30327cf06dec15e40d7ac330b8db368e4b9ee`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 846.1 KB (846058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a59da16addae7a15d26d4edba174883fd994d29bb943085361990730c6787`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d14b7a612bfb82f68156f623a22e64ab4524cbf82c592f9365a904bac033a5`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e798df308d1bafc2c22d22386cb75aa71c9b8fc3c7b9ff5e736c1464c83bea`  
		Last Modified: Wed, 08 May 2019 11:53:24 GMT  
		Size: 112.0 MB (111951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5962f9d6fd65875c9975a6db12ff0c916944d89184389e3ae3272c6d5690381`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085503a369edcce69a9e4e547a07f501228a3e71b00141b07bf7e4bf3beb4cf2`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa64654895e21a0d839b20c75bb94bc89b086f28115dfa4f76fc9bf43620956`  
		Last Modified: Wed, 08 May 2019 16:17:50 GMT  
		Size: 8.1 MB (8112616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01053321181aadbed28369c013c2a7a5692c107fe2230a95ca09198c482543a`  
		Last Modified: Wed, 08 May 2019 16:17:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a63c2c0edce6a42756999b23836125327ce8083ddda862106fa3da9006c9bb`  
		Last Modified: Wed, 08 May 2019 16:17:48 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ef8ad30ad282980494fe3779952b74d90f576aa55ba75137d8888016c42fc0`  
		Last Modified: Wed, 08 May 2019 16:17:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53f8f6183bb855f7fe940d9b71304e5a8d471b0b49143b41df155197adafed`  
		Last Modified: Wed, 08 May 2019 16:17:47 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.3-jre8` - linux; arm variant v7

```console
$ docker pull jetty@sha256:3c9e4ab980befd7642ff13d758e1184b9a1c31339da0f44a75ff16d8dd7be879
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174746924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb95bd01cd40d9dbf9c7cfeae2180d5910665e923ff37f0bbb74367f86ca388`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 12:03:26 GMT
ADD file:7e8dcc40e246d53b86266855a2de8080d26e6b4ed9f594c1acc565784405735b in / 
# Wed, 08 May 2019 12:03:27 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:04:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:14:59 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:15:01 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:16:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 17:55:00 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 17:55:03 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 17:55:03 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 17:55:24 GMT
ENV JETTY_VERSION=9.3.27.v20190418
# Wed, 08 May 2019 17:55:24 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.27.v20190418/jetty-distribution-9.3.27.v20190418.tar.gz
# Wed, 08 May 2019 17:55:25 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 17:55:38 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:39 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 17:55:41 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 17:55:42 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 17:55:45 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:46 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 17:55:49 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 17:55:50 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 17:55:51 GMT
USER jetty
# Wed, 08 May 2019 17:55:52 GMT
EXPOSE 8080
# Wed, 08 May 2019 17:55:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 17:55:53 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f2a2fd7c1ab35cd1b5ea6fcc2b801f3877852797e2698ecdb9556e0dee3accb5`  
		Last Modified: Wed, 08 May 2019 12:09:40 GMT  
		Size: 42.1 MB (42082604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047df9a92c9f7376283a8d6af526f5126d95995ba48dd7de49979ef57da3e15b`  
		Last Modified: Wed, 08 May 2019 13:12:20 GMT  
		Size: 9.5 MB (9485167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeed4ac8d1e2c751afd6fd3517f1d154365467039353c377c8206fd5eb81d4b`  
		Last Modified: Wed, 08 May 2019 13:12:18 GMT  
		Size: 3.9 MB (3918605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646a29b8c83d854b86dccdbf390a7b296f5144aef4e38276c8a7b649e0804`  
		Last Modified: Wed, 08 May 2019 14:31:13 GMT  
		Size: 830.4 KB (830410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb3a067c54308aa02398bf021c38a952c18f27646b736d71732cbbc9b1010b0`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2c033d6c592b7d46aafecc714f1393be324b57f01f5e6c76e832e8ea04576a`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0d9e8d93d276090a71cd6c8346c468c9e051903bf52760756359c4451d33b`  
		Last Modified: Wed, 08 May 2019 14:34:14 GMT  
		Size: 110.3 MB (110311680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f07a446b7fe57fd236711da5953265e8d532d43c9cb8f25a533320e93a636`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6395f8d7de3564b4ae1e386bf6ed4e0f7723e94d4940a70b485a86504a75926`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed79c7214e3927cc16347baf991c71506de6ed3b99df2ac1986ec0a71d468fc5`  
		Last Modified: Wed, 08 May 2019 17:57:42 GMT  
		Size: 8.1 MB (8112610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676d0589d51fa477055e033badb156b7b45a1207966368714b8d995baaa8e14`  
		Last Modified: Wed, 08 May 2019 17:57:42 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4564a1b599d6c52bc62ee7c35bc6c82e29f61592e078410e70824fe631f7043b`  
		Last Modified: Wed, 08 May 2019 17:57:42 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39b975c7afc95a4d2ef7ba9e978abe2caa7ccabb87775366feb0b697aeea087`  
		Last Modified: Wed, 08 May 2019 17:57:42 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6415eef82c638fd9db9ada27384593728b0ec7bbdc3a734681c8f5c687d948cb`  
		Last Modified: Wed, 08 May 2019 17:57:42 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.3-jre8` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:cd9c937d3fbd046816733cbac4c92528fd2701850261ebf585165901620e7080
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179010153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e90bd6337b2eacccb3d215e646727e21944e26545d94699227d7dd454375497`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:48:25 GMT
ADD file:153045f4fe6532d8c2ff273bb249a7a3a4cba913c26a4103ba5ddce1af02c1e5 in / 
# Wed, 08 May 2019 08:48:26 GMT
CMD ["bash"]
# Wed, 08 May 2019 11:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:51:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 17 May 2019 22:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 May 2019 22:50:40 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2019 22:50:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 17 May 2019 22:50:42 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_VERSION=8u212
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Fri, 17 May 2019 22:51:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 17 Jul 2019 23:35:39 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2019 23:35:41 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 17 Jul 2019 23:35:41 GMT
WORKDIR /usr/local/jetty
# Wed, 17 Jul 2019 23:36:20 GMT
ENV JETTY_VERSION=9.3.27.v20190418
# Wed, 17 Jul 2019 23:36:20 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.27.v20190418/jetty-distribution-9.3.27.v20190418.tar.gz
# Wed, 17 Jul 2019 23:36:20 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 17 Jul 2019 23:36:26 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:36:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 17 Jul 2019 23:36:27 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 17 Jul 2019 23:36:28 GMT
WORKDIR /var/lib/jetty
# Wed, 17 Jul 2019 23:36:29 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:36:30 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 17 Jul 2019 23:36:31 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 17 Jul 2019 23:36:32 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 17 Jul 2019 23:36:32 GMT
USER jetty
# Wed, 17 Jul 2019 23:36:32 GMT
EXPOSE 8080
# Wed, 17 Jul 2019 23:36:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jul 2019 23:36:33 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5894e28291972e44f5c3eba2779a85979bae6f95ed4f3e43ea5c98a132f06c48`  
		Last Modified: Wed, 08 May 2019 08:54:43 GMT  
		Size: 43.1 MB (43141955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e6888cee6fef7c223eeaf2ca4c51bc0c21b4631971f416eb6a529a05e96cb`  
		Last Modified: Wed, 08 May 2019 12:07:05 GMT  
		Size: 9.7 MB (9733078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf90e854779f4c5edab378626d847fd0ab7aa9441b63a7db31a7db55d2b255b`  
		Last Modified: Wed, 08 May 2019 12:07:03 GMT  
		Size: 4.1 MB (4094187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc920c054370e9fe777d4546e8898e94588c01909d487696f8378c34d00b67e`  
		Last Modified: Fri, 17 May 2019 22:56:09 GMT  
		Size: 839.6 KB (839611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf483f25e9254d4337fac759851db8d04b5a2eea6056b1375ff19c2df554464`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a594c16f5b8360bf6256529e6a21eddf648595ac48000e0d91808fd21a9798`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9e1dac91c466b57c47d5738767104f91af563b89a969f98a2eff0d0692cd6`  
		Last Modified: Fri, 17 May 2019 23:00:18 GMT  
		Size: 113.1 MB (113082862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7e6b7fd0cb47998762442e0d2b1852c2692786149020092d36d17cbaddad32`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511814053ebc4a22abd8857c39836a2c1b6b9ee89da025924601e08bfb12412c`  
		Last Modified: Wed, 17 Jul 2019 23:37:42 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1669c4a01794382b9f7b7c242b62668c06b88f5338e51237da45e7856da93b7a`  
		Last Modified: Wed, 17 Jul 2019 23:38:18 GMT  
		Size: 8.1 MB (8112605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e7314d2a2ed743c7ce24d820ca62085ed68ef4885e64ffff7249608288bd60`  
		Last Modified: Wed, 17 Jul 2019 23:38:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240f421ae2e1e166a7ca0639bf50b032f6ee2f890740cca92111c4805c96ad8c`  
		Last Modified: Wed, 17 Jul 2019 23:38:17 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70542f4001675d8eeb4d82ec86473739370681b33868645dc23cdf0269622ce`  
		Last Modified: Wed, 17 Jul 2019 23:38:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851e96f32b072a250cad7419a64e937e133dcf27007a203579ef234619d5112f`  
		Last Modified: Wed, 17 Jul 2019 23:38:17 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.3-jre8` - linux; 386

```console
$ docker pull jetty@sha256:a6f607a7a7f8d2546012d4e3422a6c3d6f6e43df9543593e20d8871fd7e66c99
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193050317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23aded063c9088f34ed66467d405d399487943f0d49cd8e8c012b5febabadfb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 10:49:19 GMT
ADD file:fde8cf5700c66c38b88d4b3254ec1544d09194e06568c23fe3989f7eaa1f5785 in / 
# Wed, 08 May 2019 10:49:20 GMT
CMD ["bash"]
# Wed, 08 May 2019 19:08:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 19:08:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 22:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 22:16:13 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 22:16:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 22:16:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 04:57:10 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 04:57:11 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 04:57:11 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 04:57:27 GMT
ENV JETTY_VERSION=9.3.27.v20190418
# Thu, 09 May 2019 04:57:27 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.27.v20190418/jetty-distribution-9.3.27.v20190418.tar.gz
# Thu, 09 May 2019 04:57:27 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 04:57:31 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:32 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 04:57:32 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 04:57:33 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 04:57:34 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:34 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 04:57:34 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 04:57:35 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 04:57:35 GMT
USER jetty
# Thu, 09 May 2019 04:57:35 GMT
EXPOSE 8080
# Thu, 09 May 2019 04:57:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 04:57:36 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b5d586ad7adeab23f6ff0b7ec90785dc757eaccd445976fda3f6d7db64d20585`  
		Last Modified: Wed, 08 May 2019 10:57:26 GMT  
		Size: 46.1 MB (46063371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b18ff57de8d55737be40848138cbd66efcc99443ae507217ae5dd45e3cf41a`  
		Last Modified: Wed, 08 May 2019 19:14:07 GMT  
		Size: 10.8 MB (10802110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc701b379559241c696cd079ff9b83f0bba19faec8747d75654fe5bc7e8adb03`  
		Last Modified: Wed, 08 May 2019 19:14:05 GMT  
		Size: 4.6 MB (4561353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad72e88a4544f4570c0df9df66b43ca05325a8df5fe4bdac5e0240836f47d28`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 862.0 KB (862001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215fde6b1eafb43012d68d65388471bca2066ad401d508df13b046aa8b830e1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf128bb9e196d3a692d14dc4ed9c91920ab3ecb3fcb3d7e4c968fb1f18b9ce1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47742760e75d51e74c18576e2a0b2d447e91b2c3a023dc9e3b1e4a83aa7bdc1a`  
		Last Modified: Wed, 08 May 2019 22:52:46 GMT  
		Size: 122.6 MB (122643377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13df399b06606cedbc7ffce659af330dab9041dfebd5d98933853a74a0be48d3`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d50318d694cf0cf2727460d2057498228249819a1d83c2f92296c96dbfb1e`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864e6c3ae8aca67441df2c8007d02446393a53171068fede74ff1b80c11462a3`  
		Last Modified: Thu, 09 May 2019 04:59:03 GMT  
		Size: 8.1 MB (8112431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f4a7e3ba70aa71189103dde69213bf3966b2c388ced64a7e2cbffd461e94a`  
		Last Modified: Thu, 09 May 2019 04:59:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff8fd6cce9079c0ee3d522d90accca4f6e5f9695abcd6f70e959ef042fa652c`  
		Last Modified: Thu, 09 May 2019 04:59:02 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b1ca7e0ef2e17a06ce88f7eb09fa4b858307fd98864c4c6c6b08bdd381db43`  
		Last Modified: Thu, 09 May 2019 04:59:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d64581023d5c5d98784d1d1454ae03dc5e33121d56e4969261976e6eb0cef05`  
		Last Modified: Thu, 09 May 2019 04:59:02 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.3-jre8` - linux; ppc64le

```console
$ docker pull jetty@sha256:bc1adc209abab1d407ce2f59ab2ff58dc0454eb65831c1f629b30b2bd6693bcd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183469405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f90b80884367852c84df6387b4c3ac53df8ed462f4d0106bd44aca55fc25dfd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:57:43 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:57:49 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:57:56 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:57:59 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 12:58:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 12:58:05 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 13:05:08 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 21:43:25 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 21:43:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 21:43:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 21:43:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 21:43:51 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 21:45:40 GMT
ENV JETTY_VERSION=9.3.27.v20190418
# Wed, 08 May 2019 21:45:43 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.27.v20190418/jetty-distribution-9.3.27.v20190418.tar.gz
# Wed, 08 May 2019 21:45:48 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 21:46:05 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:46:11 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 21:46:19 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 21:46:22 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 21:46:30 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:46:35 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 21:46:47 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 21:46:50 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 21:46:57 GMT
USER jetty
# Wed, 08 May 2019 21:47:02 GMT
EXPOSE 8080
# Wed, 08 May 2019 21:47:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 21:47:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e4e060b9a0f1aadc5647d44be482b1363697a3fd8a4aeb6a4b9c53e17ecc4`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 848.6 KB (848616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e24f3bccdd6d1d666b5c75ba2971c3c1d1b974352776ac0c8d91b0244f35cb`  
		Last Modified: Wed, 08 May 2019 13:20:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f7a6e570eaf9c696f99b09d6fb9eaf034d87e7a1e9bf092cd38e9f71777a8b`  
		Last Modified: Wed, 08 May 2019 13:20:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a3232b209a6e8e5f133bb2d4b9c377dab2d71b8b57de44e32eefb5584bfd2`  
		Last Modified: Wed, 08 May 2019 13:21:49 GMT  
		Size: 114.6 MB (114611463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321ac118136d891526d4b7d585903133a760850fd8ba7b73f5608b51d289a8a`  
		Last Modified: Wed, 08 May 2019 21:50:41 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86141b28655e4b923da175ff032f463f8ef7bf16d23578dd00d25badfdce9b79`  
		Last Modified: Wed, 08 May 2019 21:50:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd00917fa24bffdaf5886f30aeb072ab7af22aaf642ec62043f4a93e4e8eca9`  
		Last Modified: Wed, 08 May 2019 21:51:19 GMT  
		Size: 8.1 MB (8112617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b8427bf4fee39ae57ce16b61d54e41d6bd5c13ea3db72f3267db03348ceaa8`  
		Last Modified: Wed, 08 May 2019 21:51:18 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79268d11728e430ebb6758a62d414be86d45892897480775c0d146edcaa99026`  
		Last Modified: Wed, 08 May 2019 21:51:18 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46a45c9a6f559fcba9cd0663c5a82be202a55ff15037d2e5b69bbf62382064c`  
		Last Modified: Wed, 08 May 2019 21:51:17 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274c2355856144a2a690be6fee9e56a49502b3cfe7473019f267e7ab046f37a`  
		Last Modified: Wed, 08 May 2019 21:51:18 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.3-jre8` - linux; s390x

```console
$ docker pull jetty@sha256:67df356247c4c7668b43e5574857d2086fc2243bdb79e1d141f22f7016c964be
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183050901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed1aad4765436ed23d7452e10af3c685df9f191b0148b4913b5d210107a95f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:42:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:52:21 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:52:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:52:32 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:52:35 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:54:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 05:12:37 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 05:12:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 05:12:42 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 05:13:54 GMT
ENV JETTY_VERSION=9.3.27.v20190418
# Thu, 09 May 2019 05:13:55 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.27.v20190418/jetty-distribution-9.3.27.v20190418.tar.gz
# Thu, 09 May 2019 05:13:56 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 05:14:11 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:14:12 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 05:14:16 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 05:14:18 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 05:14:24 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:14:25 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 05:14:28 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 05:14:30 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 05:14:31 GMT
USER jetty
# Thu, 09 May 2019 05:14:32 GMT
EXPOSE 8080
# Thu, 09 May 2019 05:14:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 05:14:34 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf61465b03d8ec5e8064ba91220d0e97c4dd5b75a7d2fe644aab7cc4a0a514c`  
		Last Modified: Wed, 08 May 2019 15:01:34 GMT  
		Size: 863.9 KB (863943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35375a807e76af07efe2bf1c77fce29498511166f4b41f158e181805528ce229`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53975ff11a25b69ce30d4b02d88f1b27cff3e5b1a2e08d05f6721e388f4a5d`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d381e46be773491220b0199e519c4f97308fee82af49481321e3d769db7b7b0a`  
		Last Modified: Wed, 08 May 2019 15:05:36 GMT  
		Size: 114.2 MB (114184348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e456897b935f1efded84a648055389e6c4fffbee3a50167ab95bf7cf047142`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace4f725dd5f318c30a864c4400d34b9d1dfeb8dba95f242af7e8668945d2a20`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d578038cec9b51670404917d38dfef27e7bc5457413cf8e0e551189742d88ee6`  
		Last Modified: Thu, 09 May 2019 05:18:07 GMT  
		Size: 8.1 MB (8112430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe835ac0b580ef796f79cde185f34dd5b711dd55c329e97d5455e81a847270a`  
		Last Modified: Thu, 09 May 2019 05:18:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fd694f6b9708ff1ed5f830a47496807d613782e3544b3d91962676362f1f7d`  
		Last Modified: Thu, 09 May 2019 05:18:03 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c03a134f68318e2f3fc9ac093a92e3148599c5bd3fb0fc53441558fdf8710d7`  
		Last Modified: Thu, 09 May 2019 05:18:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152922021b29a3596f137e59310bcee32cb3341cfc24737e1383e33e9cd1f`  
		Last Modified: Thu, 09 May 2019 05:18:03 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4`

```console
$ docker pull jetty@sha256:d8f374b030b7e0af3d422887dafefa75ef9fe1b4de36f3e4e1a806de59fbbeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `jetty:9.4` - linux; amd64

```console
$ docker pull jetty@sha256:c2f362b5654ae4e16cd96f410c479e3b0cac574607a32c13501dd922e0a20ad5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115270945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7cfb40b7f4b3aaab1f50c4ca270acd53caf6cf9c2c04e332eedd72bc3006c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 08:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:55:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 Dec 2019 08:56:57 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_VERSION=8u232
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_URL_VERSION=8u232b09
# Sat, 28 Dec 2019 08:57:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sun, 29 Dec 2019 08:31:21 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Sun, 29 Dec 2019 08:31:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sun, 29 Dec 2019 08:31:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2019 08:31:22 GMT
RUN mkdir -p "$JETTY_HOME"
# Sun, 29 Dec 2019 08:31:23 GMT
WORKDIR /usr/local/jetty
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Sun, 29 Dec 2019 08:31:27 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sun, 29 Dec 2019 08:31:28 GMT
RUN mkdir -p "$JETTY_BASE"
# Sun, 29 Dec 2019 08:31:28 GMT
WORKDIR /var/lib/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:30 GMT
ENV TMPDIR=/tmp/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Sun, 29 Dec 2019 08:31:31 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Sun, 29 Dec 2019 08:31:31 GMT
USER jetty
# Sun, 29 Dec 2019 08:31:31 GMT
EXPOSE 8080
# Sun, 29 Dec 2019 08:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 Dec 2019 08:31:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8d3cd13de4f1c574d86de1c90b7e0f96d2394349c7e882117daaa86ad08ad`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 5.1 MB (5126129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06bdc5e0db3a85fca16aae57afb18ced9fad56ed4571f9bd0d748f38930b22`  
		Last Modified: Sat, 28 Dec 2019 09:03:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b1f94cfe4ae6c7ca9e45cc45491b7f732d099001d933ac72211dbd09d19e0d`  
		Last Modified: Sat, 28 Dec 2019 09:03:45 GMT  
		Size: 40.2 MB (40196546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe20b880320d8f58a256fe49d1c7c23c61b64baa639ad7279118a09e05b99b2b`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b913b52ac10d2aec4b74f5b78af565b0c0b25888a4c4826a1301239a847aab`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95861d4f30fde9cf21c8c2cb828a68434818251a138bdbdd7d275ca2e78987a`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 9.4 MB (9424429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecc3b45eaba005a5e755b9d4186273b7300646c4a3392159aab8b7ddd4f8d6`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46a5d5760312fac8ac9744158c27194bc30d047cb09045715eb95886f0376e9`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95bd8335f7360f38bfa50b47f5a83975722151ddc1cc65f78dbd7775f1e568`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5526a96dfe33daca789ac452c1286664ab7610d5447d2089cdd69f93c0bd3bd1`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4` - linux; arm variant v5

```console
$ docker pull jetty@sha256:6b79ec2ccfa3ee643017cecbdeee7565e32a4b74912ab39d95bbb17a1d1f7700
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180287052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965e56aa7b329cf860c5d90d360d6f490b43bfdb9ec51dfb7235b27e1cabbcbb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:53:17 GMT
ADD file:5dfe3b771bd67a2856913544993e219cb8c7933c33523cc56fe13a3a0e76ce9b in / 
# Wed, 08 May 2019 08:53:18 GMT
CMD ["bash"]
# Wed, 08 May 2019 10:01:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 10:01:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 11:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:35:27 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 11:35:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 11:35:31 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 11:36:37 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 16:15:13 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 16:15:13 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 16:15:14 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 16:15:16 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 16:15:16 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 16:15:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 16:15:24 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 16:15:27 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 16:15:27 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 16:15:32 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:32 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 16:15:35 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 16:15:36 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 16:15:37 GMT
USER jetty
# Wed, 08 May 2019 16:15:37 GMT
EXPOSE 8080
# Wed, 08 May 2019 16:15:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 16:15:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ca892ced475bf1c51c1f13b76a64549cfc5d1a0b55d33d8b9418efbb47887bf8`  
		Last Modified: Wed, 08 May 2019 08:59:09 GMT  
		Size: 44.0 MB (44045778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b30b379469b50f6ada866964876f5c4ba164c22896bf3a08aabab61869e51`  
		Last Modified: Wed, 08 May 2019 10:09:26 GMT  
		Size: 9.9 MB (9854225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e257762b4747840fc09dce269e7f68146ac9864b8bf218e57475b4af367a74`  
		Last Modified: Wed, 08 May 2019 10:09:24 GMT  
		Size: 4.2 MB (4159009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0d161136f55f6e5c26bbd9fde30327cf06dec15e40d7ac330b8db368e4b9ee`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 846.1 KB (846058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a59da16addae7a15d26d4edba174883fd994d29bb943085361990730c6787`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d14b7a612bfb82f68156f623a22e64ab4524cbf82c592f9365a904bac033a5`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e798df308d1bafc2c22d22386cb75aa71c9b8fc3c7b9ff5e736c1464c83bea`  
		Last Modified: Wed, 08 May 2019 11:53:24 GMT  
		Size: 112.0 MB (111951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5962f9d6fd65875c9975a6db12ff0c916944d89184389e3ae3272c6d5690381`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085503a369edcce69a9e4e547a07f501228a3e71b00141b07bf7e4bf3beb4cf2`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5110522604cdddba047cc0be366f16edb6238a77df6c0b690e81f538401402c6`  
		Last Modified: Wed, 08 May 2019 16:17:30 GMT  
		Size: 9.4 MB (9424456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dc9134cb78fa8c8012494e966655a51906b8fbb9a287ff677f112cb6df5b7b`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1cc6aa008e3c92d0e543846f48ffc0278671ad3336e433360f2bbab577e4b7`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 2.1 KB (2066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62368ad6255191b9e3dafc29336216dd0f25b1acacf11eacdfa4a0a9d95b2f5c`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c246600f5484d9d71da31a270a9f1543cf79da2bf94a224314c659b9a66a875e`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4` - linux; arm variant v7

```console
$ docker pull jetty@sha256:9f4c641dc0a44707812e694e8eade3015b6c059b468a4e688634a3c20ed24d0c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176059054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea2dba1b53efa6f56de5449b6625a4945aaa26e65463ca0f2ae298f2ad8ab22`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 12:03:26 GMT
ADD file:7e8dcc40e246d53b86266855a2de8080d26e6b4ed9f594c1acc565784405735b in / 
# Wed, 08 May 2019 12:03:27 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:04:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:14:59 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:15:01 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:16:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 17:55:00 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 17:55:03 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 17:55:03 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 17:55:03 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 17:55:10 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 17:55:12 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 17:55:12 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 17:55:14 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 17:55:16 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 17:55:17 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 17:55:18 GMT
USER jetty
# Wed, 08 May 2019 17:55:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 17:55:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 17:55:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f2a2fd7c1ab35cd1b5ea6fcc2b801f3877852797e2698ecdb9556e0dee3accb5`  
		Last Modified: Wed, 08 May 2019 12:09:40 GMT  
		Size: 42.1 MB (42082604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047df9a92c9f7376283a8d6af526f5126d95995ba48dd7de49979ef57da3e15b`  
		Last Modified: Wed, 08 May 2019 13:12:20 GMT  
		Size: 9.5 MB (9485167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeed4ac8d1e2c751afd6fd3517f1d154365467039353c377c8206fd5eb81d4b`  
		Last Modified: Wed, 08 May 2019 13:12:18 GMT  
		Size: 3.9 MB (3918605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646a29b8c83d854b86dccdbf390a7b296f5144aef4e38276c8a7b649e0804`  
		Last Modified: Wed, 08 May 2019 14:31:13 GMT  
		Size: 830.4 KB (830410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb3a067c54308aa02398bf021c38a952c18f27646b736d71732cbbc9b1010b0`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2c033d6c592b7d46aafecc714f1393be324b57f01f5e6c76e832e8ea04576a`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0d9e8d93d276090a71cd6c8346c468c9e051903bf52760756359c4451d33b`  
		Last Modified: Wed, 08 May 2019 14:34:14 GMT  
		Size: 110.3 MB (110311680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f07a446b7fe57fd236711da5953265e8d532d43c9cb8f25a533320e93a636`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6395f8d7de3564b4ae1e386bf6ed4e0f7723e94d4940a70b485a86504a75926`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc147ed50354f0d2a7587b28055ead9eec49df4f8eb5341d91e746671a6890d9`  
		Last Modified: Wed, 08 May 2019 17:57:20 GMT  
		Size: 9.4 MB (9424492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c93706301b9ef0c48c932aa219a1caa545887de6b3900e134bce06740648f8b`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d03e292fef5d40aada56fd958955f649c1637f1247f0ce20ccbe82940b6ccfd`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 2.1 KB (2069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f2350cc0ff9abae232377501904cbd64860bdbd5db9ef7c24bce5508cf073c`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d04c42b72f7e6024f6fdb7413c30b11da394d870eaa464bda596aa3e99142fc`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2fbb5ca36da5cad300aa58956606b38a8e3f3cecbb41851cdfd0c8696482575e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180322238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2bb61e7225a1b482f1f4664ddfbefa8060a5b43bc65fcd64f9680a51dc4749`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:48:25 GMT
ADD file:153045f4fe6532d8c2ff273bb249a7a3a4cba913c26a4103ba5ddce1af02c1e5 in / 
# Wed, 08 May 2019 08:48:26 GMT
CMD ["bash"]
# Wed, 08 May 2019 11:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:51:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 17 May 2019 22:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 May 2019 22:50:40 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2019 22:50:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 17 May 2019 22:50:42 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_VERSION=8u212
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Fri, 17 May 2019 22:51:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 17 Jul 2019 23:35:39 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2019 23:35:41 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 17 Jul 2019 23:35:41 GMT
WORKDIR /usr/local/jetty
# Wed, 17 Jul 2019 23:35:41 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 17 Jul 2019 23:35:47 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 17 Jul 2019 23:35:49 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 17 Jul 2019 23:35:49 GMT
WORKDIR /var/lib/jetty
# Wed, 17 Jul 2019 23:35:51 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:52 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 17 Jul 2019 23:35:53 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 17 Jul 2019 23:35:53 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 17 Jul 2019 23:35:54 GMT
USER jetty
# Wed, 17 Jul 2019 23:35:54 GMT
EXPOSE 8080
# Wed, 17 Jul 2019 23:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jul 2019 23:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5894e28291972e44f5c3eba2779a85979bae6f95ed4f3e43ea5c98a132f06c48`  
		Last Modified: Wed, 08 May 2019 08:54:43 GMT  
		Size: 43.1 MB (43141955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e6888cee6fef7c223eeaf2ca4c51bc0c21b4631971f416eb6a529a05e96cb`  
		Last Modified: Wed, 08 May 2019 12:07:05 GMT  
		Size: 9.7 MB (9733078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf90e854779f4c5edab378626d847fd0ab7aa9441b63a7db31a7db55d2b255b`  
		Last Modified: Wed, 08 May 2019 12:07:03 GMT  
		Size: 4.1 MB (4094187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc920c054370e9fe777d4546e8898e94588c01909d487696f8378c34d00b67e`  
		Last Modified: Fri, 17 May 2019 22:56:09 GMT  
		Size: 839.6 KB (839611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf483f25e9254d4337fac759851db8d04b5a2eea6056b1375ff19c2df554464`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a594c16f5b8360bf6256529e6a21eddf648595ac48000e0d91808fd21a9798`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9e1dac91c466b57c47d5738767104f91af563b89a969f98a2eff0d0692cd6`  
		Last Modified: Fri, 17 May 2019 23:00:18 GMT  
		Size: 113.1 MB (113082862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7e6b7fd0cb47998762442e0d2b1852c2692786149020092d36d17cbaddad32`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511814053ebc4a22abd8857c39836a2c1b6b9ee89da025924601e08bfb12412c`  
		Last Modified: Wed, 17 Jul 2019 23:37:42 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0bf7b138eb0319a3d75d1ab842fb65cd204e1c83dd7e92e2a0fb122cb2403d`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 9.4 MB (9424451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588601cf5b3de57b436e290ae8115f8bd4cd5553d0a88a42e233f763d21441b0`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2670e29c10dc3bc2f5c75c700e415015925039c9b4751a8920fdaebbb4f1c2e`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a627374a49fddcb68bd3f2ce734e8fbd58f7c745c55ac425411ca144d003de8`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b7659478cc7567aa9d6d6a3700403d10e80bf5542bc7846c6fc05f366f870`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4` - linux; 386

```console
$ docker pull jetty@sha256:f532a68e9bbf79732ee7dbfaa205e1b742f0c2fefb7e19ba5c0d6d1491cbba08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194362543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd22310a1a4ac81a7cd7b96c967f835781080ad5f817dd7161256eb8ae0207e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 10:49:19 GMT
ADD file:fde8cf5700c66c38b88d4b3254ec1544d09194e06568c23fe3989f7eaa1f5785 in / 
# Wed, 08 May 2019 10:49:20 GMT
CMD ["bash"]
# Wed, 08 May 2019 19:08:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 19:08:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 22:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 22:16:13 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 22:16:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 22:16:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 04:57:10 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 04:57:11 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 04:57:11 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 04:57:16 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 04:57:17 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 04:57:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 04:57:19 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:19 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 04:57:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 04:57:20 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 04:57:20 GMT
USER jetty
# Thu, 09 May 2019 04:57:20 GMT
EXPOSE 8080
# Thu, 09 May 2019 04:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 04:57:21 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b5d586ad7adeab23f6ff0b7ec90785dc757eaccd445976fda3f6d7db64d20585`  
		Last Modified: Wed, 08 May 2019 10:57:26 GMT  
		Size: 46.1 MB (46063371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b18ff57de8d55737be40848138cbd66efcc99443ae507217ae5dd45e3cf41a`  
		Last Modified: Wed, 08 May 2019 19:14:07 GMT  
		Size: 10.8 MB (10802110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc701b379559241c696cd079ff9b83f0bba19faec8747d75654fe5bc7e8adb03`  
		Last Modified: Wed, 08 May 2019 19:14:05 GMT  
		Size: 4.6 MB (4561353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad72e88a4544f4570c0df9df66b43ca05325a8df5fe4bdac5e0240836f47d28`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 862.0 KB (862001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215fde6b1eafb43012d68d65388471bca2066ad401d508df13b046aa8b830e1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf128bb9e196d3a692d14dc4ed9c91920ab3ecb3fcb3d7e4c968fb1f18b9ce1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47742760e75d51e74c18576e2a0b2d447e91b2c3a023dc9e3b1e4a83aa7bdc1a`  
		Last Modified: Wed, 08 May 2019 22:52:46 GMT  
		Size: 122.6 MB (122643377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13df399b06606cedbc7ffce659af330dab9041dfebd5d98933853a74a0be48d3`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d50318d694cf0cf2727460d2057498228249819a1d83c2f92296c96dbfb1e`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad229b08fbaea588098dc7e42976c29d5b7a16be0e2a84b3ba0d811c5d724494`  
		Last Modified: Thu, 09 May 2019 04:58:53 GMT  
		Size: 9.4 MB (9424415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7161f78a4fe1f1d0ee6787a7f6f28b0a0241c7390a5c919ee688aac0caf3fef`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4163317071202eac58e9e3c5ec95d8b071ae013148d4f1376fdc09a340c7ed6b`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4d72a3ad59ec8fada471aa84164b581dd500aea022f038334b0eda00c0ec19`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7621b6c4a7959d913a05ce51aa49a199c616badaaa439ea6873fe8c5a9b89ee`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4` - linux; ppc64le

```console
$ docker pull jetty@sha256:1c8d35096fdcfc3c448b203db5c12734655105f9f779d3734522511764e58233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184781497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eacbfac25da6c191d70cca800f7ed9b015a19adef7c4ab701c0b31540a6159e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:57:43 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:57:49 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:57:56 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:57:59 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 12:58:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 12:58:05 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 13:05:08 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 21:43:25 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 21:43:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 21:43:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 21:43:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 21:43:51 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 21:43:57 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 21:44:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 21:44:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 21:44:22 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:44:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 21:44:33 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 21:44:40 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 21:44:57 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:45:03 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 21:45:10 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 21:45:11 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 21:45:13 GMT
USER jetty
# Wed, 08 May 2019 21:45:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 21:45:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 21:45:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e4e060b9a0f1aadc5647d44be482b1363697a3fd8a4aeb6a4b9c53e17ecc4`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 848.6 KB (848616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e24f3bccdd6d1d666b5c75ba2971c3c1d1b974352776ac0c8d91b0244f35cb`  
		Last Modified: Wed, 08 May 2019 13:20:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f7a6e570eaf9c696f99b09d6fb9eaf034d87e7a1e9bf092cd38e9f71777a8b`  
		Last Modified: Wed, 08 May 2019 13:20:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a3232b209a6e8e5f133bb2d4b9c377dab2d71b8b57de44e32eefb5584bfd2`  
		Last Modified: Wed, 08 May 2019 13:21:49 GMT  
		Size: 114.6 MB (114611463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321ac118136d891526d4b7d585903133a760850fd8ba7b73f5608b51d289a8a`  
		Last Modified: Wed, 08 May 2019 21:50:41 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86141b28655e4b923da175ff032f463f8ef7bf16d23578dd00d25badfdce9b79`  
		Last Modified: Wed, 08 May 2019 21:50:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0e68a17da043f652f2d812d9c650558c382a9c2be40bb8fd901e19d89cb162`  
		Last Modified: Wed, 08 May 2019 21:50:38 GMT  
		Size: 9.4 MB (9424473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec696722258c05e106b7c921898aac4da7e2ab6ae65076942a12749f1049140b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cae7017c7325beea0f896b47ae71aa44260cac66b36379a32dbb0ed9309eaf`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 2.1 KB (2062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8302b92229dab552b306d2b48fba615a169e28af57e2c7fae6324ef3b4b028`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd387f05feedbcf33516453c4c46c64a80261af3ff1e6ebf007ccac52a95b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4` - linux; s390x

```console
$ docker pull jetty@sha256:eb8f97a23898ccdc5be026ea051ef231615b9455a4d78a72cbeb093439440cf5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184363097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55031fcaf6fba1a2c7256bad7bbcc09b11b036dbceb1807ceeacc9202792f231`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:42:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:52:21 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:52:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:52:32 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:52:35 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:54:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 05:12:37 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 05:12:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 05:12:42 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 05:12:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 05:12:59 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 05:13:05 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 05:13:06 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 05:13:16 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:16 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 05:13:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 05:13:21 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 05:13:22 GMT
USER jetty
# Thu, 09 May 2019 05:13:23 GMT
EXPOSE 8080
# Thu, 09 May 2019 05:13:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 05:13:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf61465b03d8ec5e8064ba91220d0e97c4dd5b75a7d2fe644aab7cc4a0a514c`  
		Last Modified: Wed, 08 May 2019 15:01:34 GMT  
		Size: 863.9 KB (863943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35375a807e76af07efe2bf1c77fce29498511166f4b41f158e181805528ce229`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53975ff11a25b69ce30d4b02d88f1b27cff3e5b1a2e08d05f6721e388f4a5d`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d381e46be773491220b0199e519c4f97308fee82af49481321e3d769db7b7b0a`  
		Last Modified: Wed, 08 May 2019 15:05:36 GMT  
		Size: 114.2 MB (114184348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e456897b935f1efded84a648055389e6c4fffbee3a50167ab95bf7cf047142`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace4f725dd5f318c30a864c4400d34b9d1dfeb8dba95f242af7e8668945d2a20`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6df7195f7b6c83e938c25f1940930649b862e2b5369ec6e041631c4cb1ebef`  
		Last Modified: Thu, 09 May 2019 05:17:27 GMT  
		Size: 9.4 MB (9424383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef61c6677aef99352724f560861db552edff24e57f288598be141e49f0802c8`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16572dc3fb4702653a0252ed5b29eb536479f0085f7ec2596c9d1c2e8214fd2f`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0aa75b063a662a0cd7f4af7b720863dfa8c7643b98bfc4b8ee5124a1bb069e`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ce48b6bff7dbea769d046b7311e98e7ea33aec40dca23a246a4b2c1fe530c5`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4.26`

**does not exist** (yet?)

## `jetty:9.4.26-jdk13`

**does not exist** (yet?)

## `jetty:9.4.26-jdk13-slim`

**does not exist** (yet?)

## `jetty:9.4.26-jre11`

**does not exist** (yet?)

## `jetty:9.4.26-jre11-slim`

**does not exist** (yet?)

## `jetty:9.4.26-jre8`

**does not exist** (yet?)

## `jetty:9.4-jdk13`

**does not exist** (yet?)

## `jetty:9.4-jdk13-slim`

**does not exist** (yet?)

## `jetty:9.4-jre11`

```console
$ docker pull jetty@sha256:743448bd33459baa801590f0459b27209284160d7efd6ef6808a388d5e5739e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `jetty:9.4-jre11` - linux; amd64

```console
$ docker pull jetty@sha256:df02049c665533624aba2da58feae02bc3505c860d2fc2e852924ef458f4b48c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116986183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9a100055b8fae61a4ed9daa37cd9156c453ba6914cf9088f47d795bbeaa26d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 08:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:55:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:55:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 Dec 2019 08:55:42 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:55:43 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 15 Jan 2020 21:29:23 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 15 Jan 2020 21:29:23 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 15 Jan 2020 21:29:24 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 15 Jan 2020 21:29:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 15 Jan 2020 22:06:18 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 15 Jan 2020 22:06:19 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Jan 2020 22:06:19 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2020 22:06:19 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 15 Jan 2020 22:06:20 GMT
WORKDIR /usr/local/jetty
# Wed, 15 Jan 2020 22:06:20 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 15 Jan 2020 22:06:20 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 15 Jan 2020 22:06:20 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 15 Jan 2020 22:06:24 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 15 Jan 2020 22:06:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Jan 2020 22:06:25 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 15 Jan 2020 22:06:25 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Jan 2020 22:06:27 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 15 Jan 2020 22:06:27 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Jan 2020 22:06:28 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 15 Jan 2020 22:06:28 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 15 Jan 2020 22:06:28 GMT
USER jetty
# Wed, 15 Jan 2020 22:06:28 GMT
EXPOSE 8080
# Wed, 15 Jan 2020 22:06:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Jan 2020 22:06:29 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8d3cd13de4f1c574d86de1c90b7e0f96d2394349c7e882117daaa86ad08ad`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 5.1 MB (5126129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99458a0c1a9454bc8cf23d0875b1272a6515fb2c6c4f0211cbc1a5f5fb0877d9`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770f7d01f29ecbf7dfad49bbbdfd6a2da7d92622a36cb6f59871cc1e0beafa3d`  
		Last Modified: Wed, 15 Jan 2020 21:35:02 GMT  
		Size: 41.9 MB (41911767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53a9636d83ae98e7185f901922690bde44fa39ed25d7ec7b8d600cfe730e30c`  
		Last Modified: Wed, 15 Jan 2020 22:07:04 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3536d604435e83016765fa72572c7f7fabcfa910f7bc825191362a9512b0c121`  
		Last Modified: Wed, 15 Jan 2020 22:07:04 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9df820f4c12827c92db1c93471467a9a85ac1486cbfff5321da1c87541c7147`  
		Last Modified: Wed, 15 Jan 2020 22:07:04 GMT  
		Size: 9.4 MB (9424442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c41edf12d4602f8e7e6f333d35f000ab2f672fd89bd5c7aaa74268282136f7`  
		Last Modified: Wed, 15 Jan 2020 22:07:03 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2ea1f3c555c6b911bf1987ccdbf0130e82c12655aaab12913e84eaa82936d`  
		Last Modified: Wed, 15 Jan 2020 22:07:03 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3351b55c9a541e5e2dbd145927c012feb5539a67a40fa8130eb405ce078bde`  
		Last Modified: Wed, 15 Jan 2020 22:07:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38606e8425bbc3662df6557c62bf28a49767e4525e1d17b89b7c2264ace3960`  
		Last Modified: Wed, 15 Jan 2020 22:07:03 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre11` - linux; arm variant v5

```console
$ docker pull jetty@sha256:e61dc4a9deb0e535e885492b717e194a793d87f0ef42cc2865cf291bd42ef87b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182727261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee22a3053daa67fd23097448e122bfc16fa0ab00f6a44db79016433570c1d25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:53:17 GMT
ADD file:5dfe3b771bd67a2856913544993e219cb8c7933c33523cc56fe13a3a0e76ce9b in / 
# Wed, 08 May 2019 08:53:18 GMT
CMD ["bash"]
# Wed, 08 May 2019 10:01:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 10:01:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 11:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:29:22 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 11:29:23 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 11:29:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 11:29:25 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 11:29:26 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 11:29:26 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 11:29:26 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 11:30:39 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 16:14:36 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 16:14:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 16:14:37 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 16:14:39 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 16:14:40 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 16:14:40 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 16:14:41 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 16:14:41 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 16:14:48 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:14:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 16:14:52 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 16:14:52 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 16:15:00 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:01 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 16:15:03 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 16:15:04 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 16:15:04 GMT
USER jetty
# Wed, 08 May 2019 16:15:05 GMT
EXPOSE 8080
# Wed, 08 May 2019 16:15:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 16:15:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ca892ced475bf1c51c1f13b76a64549cfc5d1a0b55d33d8b9418efbb47887bf8`  
		Last Modified: Wed, 08 May 2019 08:59:09 GMT  
		Size: 44.0 MB (44045778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b30b379469b50f6ada866964876f5c4ba164c22896bf3a08aabab61869e51`  
		Last Modified: Wed, 08 May 2019 10:09:26 GMT  
		Size: 9.9 MB (9854225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e257762b4747840fc09dce269e7f68146ac9864b8bf218e57475b4af367a74`  
		Last Modified: Wed, 08 May 2019 10:09:24 GMT  
		Size: 4.2 MB (4159009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0d161136f55f6e5c26bbd9fde30327cf06dec15e40d7ac330b8db368e4b9ee`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 846.1 KB (846058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5e8a953b512e86412d1d172548252ed8bbacdaa35b2f782a77deea2bc921d5`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cb1f59d6130f400627aa8a690ef028bb74ac9c0d19014a63d4a6e92f287919`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f6ed55942b2f3bdcbd69d0da3ad8c000707d9ccaa6cae8b61904819e9d4ad`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7894bb11a0e1b10913a4fca8f468f0cb96be5b70c48747027a3f8ba2ca4ee7b`  
		Last Modified: Wed, 08 May 2019 11:50:55 GMT  
		Size: 114.4 MB (114391453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b588bb59f0c45f2f6771f9e9c79e0226a7c731bc9aaee590e21a8ec705dc8402`  
		Last Modified: Wed, 08 May 2019 16:17:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186a0d3b3192bf16deb3eeba8f1df80d7fac471ee8792d0bc247919b970a8a4b`  
		Last Modified: Wed, 08 May 2019 16:17:19 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b6bbad04440d1a7ea395b78998ed2567802c265cfc26033a1299980b243ddc`  
		Last Modified: Wed, 08 May 2019 16:17:21 GMT  
		Size: 9.4 MB (9424423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5f28a51a21092851a210fcecda8e7d925f61f18d3e583114d9331c531a370e`  
		Last Modified: Wed, 08 May 2019 16:17:17 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b62f92ae9c631465a7092544ae2510c9bd0609012964470006257c25989f629`  
		Last Modified: Wed, 08 May 2019 16:17:18 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fda1533df868c03d8f2e763427fd72c5172c1bece17e16288dccfa7212d05b6`  
		Last Modified: Wed, 08 May 2019 16:17:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce5eb7099d7b0bcf1f2cbc10d7d5f22581ff5a72783fcac33bb6c033c9e7f00`  
		Last Modified: Wed, 08 May 2019 16:17:18 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre11` - linux; arm variant v7

```console
$ docker pull jetty@sha256:1ecfc60021b617f0b65e00a61f598388efda31bfa8498ae38bc31256e2d9fcf2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181917632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3931c46ad067ec7a675152dc901c10d01afbb07d47227ab30b45d8b83fa47dba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 12:03:26 GMT
ADD file:7e8dcc40e246d53b86266855a2de8080d26e6b4ed9f594c1acc565784405735b in / 
# Wed, 08 May 2019 12:03:27 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:04:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:10:10 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 14:10:11 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:10:15 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:10:19 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:10:20 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 14:10:20 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 14:10:21 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 14:11:25 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 17:54:33 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 17:54:33 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 17:54:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 17:54:35 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 17:54:36 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 17:54:36 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 17:54:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 17:54:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 17:54:43 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:54:44 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 17:54:45 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 17:54:46 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 17:54:48 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:54:48 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 17:54:50 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 17:54:51 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 17:54:51 GMT
USER jetty
# Wed, 08 May 2019 17:54:52 GMT
EXPOSE 8080
# Wed, 08 May 2019 17:54:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 17:54:53 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f2a2fd7c1ab35cd1b5ea6fcc2b801f3877852797e2698ecdb9556e0dee3accb5`  
		Last Modified: Wed, 08 May 2019 12:09:40 GMT  
		Size: 42.1 MB (42082604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047df9a92c9f7376283a8d6af526f5126d95995ba48dd7de49979ef57da3e15b`  
		Last Modified: Wed, 08 May 2019 13:12:20 GMT  
		Size: 9.5 MB (9485167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeed4ac8d1e2c751afd6fd3517f1d154365467039353c377c8206fd5eb81d4b`  
		Last Modified: Wed, 08 May 2019 13:12:18 GMT  
		Size: 3.9 MB (3918605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646a29b8c83d854b86dccdbf390a7b296f5144aef4e38276c8a7b649e0804`  
		Last Modified: Wed, 08 May 2019 14:31:13 GMT  
		Size: 830.4 KB (830410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6f0d217548ad4fca27f3fca1ad13e1d42b51dfdc66efe11ca75bec1768f91e`  
		Last Modified: Wed, 08 May 2019 14:31:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b3a1a9cf41d4f4ba6bd276263e9aa9d9510a7f587316f5128b4b8848a3fb8`  
		Last Modified: Wed, 08 May 2019 14:31:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5554c002ae1621fa85e450b809bb153315535856beedc3a4de016e7f8088ee3`  
		Last Modified: Wed, 08 May 2019 14:31:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74989df1042192176323ee1dd7ec5a173ef7c944e14eb3192d1cd38ca6750c97`  
		Last Modified: Wed, 08 May 2019 14:31:44 GMT  
		Size: 116.2 MB (116170095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b905662366849813f2538eae8fdfddf73101be031e315b3e1cfe5d2ecb091c2`  
		Last Modified: Wed, 08 May 2019 17:57:09 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a15e595b79d8819812a7c811c08d462e194fe42cf9848813bb0d506d0525c8`  
		Last Modified: Wed, 08 May 2019 17:57:09 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468d0998b6f9bfa90d04cef61fb3fe9a05229b655f4ef6919ebfc98eb38f1a30`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 9.4 MB (9424444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5c4061898f1685d8b125a0c028f4ebce0e067ad354f2450df4890ba8b9c6f4`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b048e8985511af8971bb264592da262faf16656240c48d00c00d1bb477f0f7`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c6b6b0b67d545dff18961b21a6789ac2efa79e0e229e7e9ea2f2137ca2155f`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07ed6686762d8dbe77cefd25092cc139992ed1f5bcb16e585207b54fe2375d`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre11` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:0bcbb36e80c2c1fe1dcb34fea01c7406b8c835e5baac6f8a2b1a403394f828f3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112480520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34960a7c18f0fd99929cb1c5e10bc53bbcb535cbc0823f3db8799358492905a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:15:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 18:28:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:28:53 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 18:28:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 Dec 2019 18:28:55 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 18:28:58 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 15 Jan 2020 21:52:37 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 15 Jan 2020 21:52:38 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 15 Jan 2020 21:52:39 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 15 Jan 2020 21:52:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 15 Jan 2020 22:48:40 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 15 Jan 2020 22:48:41 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Jan 2020 22:48:41 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2020 22:48:43 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 15 Jan 2020 22:48:44 GMT
WORKDIR /usr/local/jetty
# Wed, 15 Jan 2020 22:48:44 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 15 Jan 2020 22:48:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 15 Jan 2020 22:48:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 15 Jan 2020 22:48:50 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 15 Jan 2020 22:48:51 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Jan 2020 22:48:52 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 15 Jan 2020 22:48:53 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Jan 2020 22:48:55 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 15 Jan 2020 22:48:56 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Jan 2020 22:48:58 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 15 Jan 2020 22:48:58 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 15 Jan 2020 22:48:59 GMT
USER jetty
# Wed, 15 Jan 2020 22:49:00 GMT
EXPOSE 8080
# Wed, 15 Jan 2020 22:49:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Jan 2020 22:49:01 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f31062581dadb1f69c43e9441040dd46788bf13ae51f20c66929fac82b506b`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 9.7 MB (9748258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62337a296a607f48a5dc3a7c07639360d98e0e78982ca8e459c832719012f12`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 4.1 MB (4094448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa93134dbc80dab62077651c441c2b4f5f8eab4626587ec74711ad51d46ec4ca`  
		Last Modified: Sat, 28 Dec 2019 18:31:59 GMT  
		Size: 5.0 MB (5027084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40624577614540513606003282ed1300f9d6f1a8b046d54c9296b4ff823bed3e`  
		Last Modified: Sat, 28 Dec 2019 18:31:58 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26943aa2587f2cbaa709fd95b2c1252891e411037eaa8b92d20b524c72dc0093`  
		Last Modified: Wed, 15 Jan 2020 21:55:28 GMT  
		Size: 41.0 MB (41013873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b7163c3b6e2c910c8cceaac0e190dcfcebe006dfc8823ef925b286959c0a97`  
		Last Modified: Wed, 15 Jan 2020 22:49:50 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9644e47a63c665b9df0b5d57af2c17e96a867c8492e37984a7b24351d8cc39`  
		Last Modified: Wed, 15 Jan 2020 22:49:50 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e66d081444beea67a939cd03b75f7c67533b366fb267e5d794c0dc38339cdb`  
		Last Modified: Wed, 15 Jan 2020 22:49:50 GMT  
		Size: 9.4 MB (9424444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f9f8a44fc93244382edeaa036b725464a8fb4832e441264a4eece16e7ded`  
		Last Modified: Wed, 15 Jan 2020 22:49:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e50754055223f2f91d44b59640d119eb54d8c0fb0d827a5ff9c4a6adb53e9f6`  
		Last Modified: Wed, 15 Jan 2020 22:49:49 GMT  
		Size: 2.1 KB (2067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59af7c77b5971d9e25e091c2906290d72cca0a5d1179c451a867f4f0f72847b`  
		Last Modified: Wed, 15 Jan 2020 22:49:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916d2bc24cb918d077da9d794ed577547723529c96e9f51771476db6219b02f8`  
		Last Modified: Wed, 15 Jan 2020 22:49:49 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre11` - linux; 386

```console
$ docker pull jetty@sha256:df37be9c17a3ded9d55712e500da0834a54dae8701bf8cec4068ea80fec9a51d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208102749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f8257a74c907091d1c93581da69d1816286a503d26abd587ef5649811eac9e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 10:49:19 GMT
ADD file:fde8cf5700c66c38b88d4b3254ec1544d09194e06568c23fe3989f7eaa1f5785 in / 
# Wed, 08 May 2019 10:49:20 GMT
CMD ["bash"]
# Wed, 08 May 2019 19:08:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 19:08:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 22:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 22:13:16 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 22:13:16 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 22:13:17 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 22:13:18 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 22:13:18 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 22:13:18 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 22:13:18 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 22:14:01 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 04:56:56 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 04:56:56 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 04:56:56 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 04:56:57 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 04:56:57 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 04:56:57 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 04:56:57 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 04:56:57 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 04:57:02 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:02 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 04:57:02 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 04:57:03 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 04:57:04 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:04 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 04:57:05 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 04:57:05 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 04:57:05 GMT
USER jetty
# Thu, 09 May 2019 04:57:05 GMT
EXPOSE 8080
# Thu, 09 May 2019 04:57:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 04:57:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b5d586ad7adeab23f6ff0b7ec90785dc757eaccd445976fda3f6d7db64d20585`  
		Last Modified: Wed, 08 May 2019 10:57:26 GMT  
		Size: 46.1 MB (46063371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b18ff57de8d55737be40848138cbd66efcc99443ae507217ae5dd45e3cf41a`  
		Last Modified: Wed, 08 May 2019 19:14:07 GMT  
		Size: 10.8 MB (10802110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc701b379559241c696cd079ff9b83f0bba19faec8747d75654fe5bc7e8adb03`  
		Last Modified: Wed, 08 May 2019 19:14:05 GMT  
		Size: 4.6 MB (4561353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad72e88a4544f4570c0df9df66b43ca05325a8df5fe4bdac5e0240836f47d28`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 862.0 KB (862001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d563d964c8c48c0bf9ce2911e516238b632ac5f81600f42779901aad7954efb1`  
		Last Modified: Wed, 08 May 2019 22:48:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448b9d083751b7e5b0e8c9c68a54cb84e7d8e85e56fb1576c41defa410151dc4`  
		Last Modified: Wed, 08 May 2019 22:48:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dde35a9cb946023f1ef745968d557ccc74c2a8718a6eb1893bf03b29780681`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f132fb339ff847f4e8d45fa1121a1dd7c3518bcbca5455379e20a438d90051`  
		Last Modified: Wed, 08 May 2019 22:49:21 GMT  
		Size: 136.4 MB (136383359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9f73035593a6432298a218ec76ea04a3bbe74b2ddf734954be5cdf0f19a884`  
		Last Modified: Thu, 09 May 2019 04:58:20 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34450b099ff0d4b45f09b6e00ed3d2f026f6d2181b0855a8e604d6c50f438ce8`  
		Last Modified: Thu, 09 May 2019 04:58:20 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f6bfd4f4e9bbe80a06aac3454c6a6000bc4f9420f0a11eff9fc8c13c991ea`  
		Last Modified: Thu, 09 May 2019 04:58:43 GMT  
		Size: 9.4 MB (9424412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fd4fadc048c535a97814ead296a6de898dca7a8fd68ae4f85c077be1c890b9`  
		Last Modified: Thu, 09 May 2019 04:58:19 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3281f27ff370a5a26ddf56f7cd5534d772cd235c28ae20c14344af171db6b6cb`  
		Last Modified: Thu, 09 May 2019 04:58:19 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d06705f17aaeed0c4c486c318c9933ae35cbe904e486948cc4d8acafb8c747c`  
		Last Modified: Thu, 09 May 2019 04:58:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e70071461854031178286e82a09dd470e12b18954be16f72b4dfc28faa7d7c`  
		Last Modified: Thu, 09 May 2019 04:58:19 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre11` - linux; ppc64le

```console
$ docker pull jetty@sha256:07be9dfcfd9808776f141b115e6ee606dd9d7771e6f78b947d0fc91483eebd0b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189621947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7a17938314024b414f098753ede070efa2a9509e0b47e7d89f2ed89d20d812`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:39:34 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 12:39:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:39:45 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:39:54 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:39:57 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 12:40:00 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 12:40:04 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 12:45:53 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 21:41:05 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 21:41:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 21:41:21 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 21:41:33 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 21:41:40 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 21:41:45 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 21:41:53 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 21:41:57 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 21:42:14 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:42:19 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 21:42:25 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 21:42:30 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 21:42:40 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:42:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 21:42:49 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 21:42:50 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 21:42:55 GMT
USER jetty
# Wed, 08 May 2019 21:42:59 GMT
EXPOSE 8080
# Wed, 08 May 2019 21:43:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 21:43:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e4e060b9a0f1aadc5647d44be482b1363697a3fd8a4aeb6a4b9c53e17ecc4`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 848.6 KB (848616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afcad30d91e6ef6a6235e8ee8ea34984a8a03714f83006880a27d23e1ec6b07`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17792a5a83e70e4555affd27a076727218038ebe3722cbcecde52eb8d81e41e8`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743f9ba8d5fbd6557dc6ece9e230fd856733b23a5d6477a9a669a4f68c61da85`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4c5964ec2a98758cf78dd517a7d26b5badaa386bdfb0386d00ef2df17dd4bd`  
		Last Modified: Wed, 08 May 2019 13:16:33 GMT  
		Size: 119.5 MB (119451690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df08f032fbe3dbde5f9f0ad89f0a4e6b889f432b721ab9dbfb85353ee0e9fef`  
		Last Modified: Wed, 08 May 2019 21:50:17 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bf0a36101b3a646c73c79d0434d3900443d359a61db049c61f105c19ecafe0`  
		Last Modified: Wed, 08 May 2019 21:50:17 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f294abacdbae073a70caa4320195b3b9747092e2d4b540e9c9296789a3e8d0`  
		Last Modified: Wed, 08 May 2019 21:50:13 GMT  
		Size: 9.4 MB (9424455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c32361000d26c34e33dff0be63e8711ddd60602752733496f49039c4bc6a525`  
		Last Modified: Wed, 08 May 2019 21:50:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431afe509baab77de49754d848729f64e98b4d841263f3a7215c3ae1dd72dea`  
		Last Modified: Wed, 08 May 2019 21:50:12 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943c1c5aa0915ad87574f6e5c8654d3c82a05a3e14010d8de39a1cfc1cc0e79e`  
		Last Modified: Wed, 08 May 2019 21:50:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc862d40e0df89a75d83b1f1aea167aef04d762834923ff91b44d616879b71d5`  
		Last Modified: Wed, 08 May 2019 21:50:12 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre11` - linux; s390x

```console
$ docker pull jetty@sha256:2b3945632b33b3f0de7929625c216ee1ffda84af072056c4680ab3b4d68c4c10
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189340518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd80fb0108049e37a092dc1371a502210f2d1d9167218cb3db90b1d0f34c13bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:42:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:42:15 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 14:42:16 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:42:20 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:42:23 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:42:24 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 14:42:25 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 14:42:25 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 14:45:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 05:11:08 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 05:11:09 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 05:11:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 05:11:14 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 05:11:15 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 05:11:17 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 05:11:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 05:11:19 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 05:11:35 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:11:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 05:11:42 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 05:11:43 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 05:11:54 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:11:55 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 05:11:58 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 05:11:59 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 05:12:00 GMT
USER jetty
# Thu, 09 May 2019 05:12:01 GMT
EXPOSE 8080
# Thu, 09 May 2019 05:12:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 05:12:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf61465b03d8ec5e8064ba91220d0e97c4dd5b75a7d2fe644aab7cc4a0a514c`  
		Last Modified: Wed, 08 May 2019 15:01:34 GMT  
		Size: 863.9 KB (863943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7875682bb43ee4dfedb0db2f5ffa045803895445c3434edfed0723d3f4dd700`  
		Last Modified: Wed, 08 May 2019 15:01:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7406aa79a5f911227056620e3ae81aaf33a7c207f34292a287bda26a00db256a`  
		Last Modified: Wed, 08 May 2019 15:01:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82c65756cebc86ea719c2cabfae397ed4030a5a942dc03f44dd0f91272fb555`  
		Last Modified: Wed, 08 May 2019 15:01:33 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b85b1ac77736c32a8c794742d393f3ab32897f6833cba700dd680ab8fd406f2`  
		Last Modified: Wed, 08 May 2019 15:02:08 GMT  
		Size: 119.2 MB (119161534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd44949cd09d1d0e5969fcb7156d120b69832e2497ea2b33b30297ae070ddc48`  
		Last Modified: Thu, 09 May 2019 05:17:11 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f268f0bd558aeccb48a867e42b5a5ce837a651f8cc8cdc767237dafac042df76`  
		Last Modified: Thu, 09 May 2019 05:17:11 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3568694999bdf31b1c2961e9ca7a5b69b7b2530a2d09a136023f8ee2eddcc718`  
		Last Modified: Thu, 09 May 2019 05:17:11 GMT  
		Size: 9.4 MB (9424386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab0e2f0ac2e6648b212cb353f9b0bc31b5c587e992d1ac351bd2766f926055d`  
		Last Modified: Thu, 09 May 2019 05:17:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7851714d11fef24e37dd11b911a3fa3462d109d5e6fdd3e9aca6ad5036cec029`  
		Last Modified: Thu, 09 May 2019 05:17:09 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f887c9590eb836ca23b01454d6e4e0521c7764202e43f7c655694e11aa5cf5e5`  
		Last Modified: Thu, 09 May 2019 05:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd93f6136177d3f01602a7548a1a92272b16419c77a0aa835043c8533a403cdb`  
		Last Modified: Thu, 09 May 2019 05:17:09 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9.4-jre11-slim`

**does not exist** (yet?)

## `jetty:9.4-jre8`

```console
$ docker pull jetty@sha256:d8f374b030b7e0af3d422887dafefa75ef9fe1b4de36f3e4e1a806de59fbbeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `jetty:9.4-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:c2f362b5654ae4e16cd96f410c479e3b0cac574607a32c13501dd922e0a20ad5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115270945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7cfb40b7f4b3aaab1f50c4ca270acd53caf6cf9c2c04e332eedd72bc3006c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 08:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:55:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 Dec 2019 08:56:57 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_VERSION=8u232
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_URL_VERSION=8u232b09
# Sat, 28 Dec 2019 08:57:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sun, 29 Dec 2019 08:31:21 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Sun, 29 Dec 2019 08:31:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sun, 29 Dec 2019 08:31:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2019 08:31:22 GMT
RUN mkdir -p "$JETTY_HOME"
# Sun, 29 Dec 2019 08:31:23 GMT
WORKDIR /usr/local/jetty
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Sun, 29 Dec 2019 08:31:27 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sun, 29 Dec 2019 08:31:28 GMT
RUN mkdir -p "$JETTY_BASE"
# Sun, 29 Dec 2019 08:31:28 GMT
WORKDIR /var/lib/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:30 GMT
ENV TMPDIR=/tmp/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Sun, 29 Dec 2019 08:31:31 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Sun, 29 Dec 2019 08:31:31 GMT
USER jetty
# Sun, 29 Dec 2019 08:31:31 GMT
EXPOSE 8080
# Sun, 29 Dec 2019 08:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 Dec 2019 08:31:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8d3cd13de4f1c574d86de1c90b7e0f96d2394349c7e882117daaa86ad08ad`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 5.1 MB (5126129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06bdc5e0db3a85fca16aae57afb18ced9fad56ed4571f9bd0d748f38930b22`  
		Last Modified: Sat, 28 Dec 2019 09:03:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b1f94cfe4ae6c7ca9e45cc45491b7f732d099001d933ac72211dbd09d19e0d`  
		Last Modified: Sat, 28 Dec 2019 09:03:45 GMT  
		Size: 40.2 MB (40196546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe20b880320d8f58a256fe49d1c7c23c61b64baa639ad7279118a09e05b99b2b`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b913b52ac10d2aec4b74f5b78af565b0c0b25888a4c4826a1301239a847aab`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95861d4f30fde9cf21c8c2cb828a68434818251a138bdbdd7d275ca2e78987a`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 9.4 MB (9424429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecc3b45eaba005a5e755b9d4186273b7300646c4a3392159aab8b7ddd4f8d6`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46a5d5760312fac8ac9744158c27194bc30d047cb09045715eb95886f0376e9`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95bd8335f7360f38bfa50b47f5a83975722151ddc1cc65f78dbd7775f1e568`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5526a96dfe33daca789ac452c1286664ab7610d5447d2089cdd69f93c0bd3bd1`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre8` - linux; arm variant v5

```console
$ docker pull jetty@sha256:6b79ec2ccfa3ee643017cecbdeee7565e32a4b74912ab39d95bbb17a1d1f7700
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180287052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965e56aa7b329cf860c5d90d360d6f490b43bfdb9ec51dfb7235b27e1cabbcbb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:53:17 GMT
ADD file:5dfe3b771bd67a2856913544993e219cb8c7933c33523cc56fe13a3a0e76ce9b in / 
# Wed, 08 May 2019 08:53:18 GMT
CMD ["bash"]
# Wed, 08 May 2019 10:01:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 10:01:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 11:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:35:27 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 11:35:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 11:35:31 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 11:36:37 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 16:15:13 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 16:15:13 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 16:15:14 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 16:15:16 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 16:15:16 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 16:15:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 16:15:24 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 16:15:27 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 16:15:27 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 16:15:32 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:32 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 16:15:35 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 16:15:36 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 16:15:37 GMT
USER jetty
# Wed, 08 May 2019 16:15:37 GMT
EXPOSE 8080
# Wed, 08 May 2019 16:15:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 16:15:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ca892ced475bf1c51c1f13b76a64549cfc5d1a0b55d33d8b9418efbb47887bf8`  
		Last Modified: Wed, 08 May 2019 08:59:09 GMT  
		Size: 44.0 MB (44045778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b30b379469b50f6ada866964876f5c4ba164c22896bf3a08aabab61869e51`  
		Last Modified: Wed, 08 May 2019 10:09:26 GMT  
		Size: 9.9 MB (9854225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e257762b4747840fc09dce269e7f68146ac9864b8bf218e57475b4af367a74`  
		Last Modified: Wed, 08 May 2019 10:09:24 GMT  
		Size: 4.2 MB (4159009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0d161136f55f6e5c26bbd9fde30327cf06dec15e40d7ac330b8db368e4b9ee`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 846.1 KB (846058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a59da16addae7a15d26d4edba174883fd994d29bb943085361990730c6787`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d14b7a612bfb82f68156f623a22e64ab4524cbf82c592f9365a904bac033a5`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e798df308d1bafc2c22d22386cb75aa71c9b8fc3c7b9ff5e736c1464c83bea`  
		Last Modified: Wed, 08 May 2019 11:53:24 GMT  
		Size: 112.0 MB (111951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5962f9d6fd65875c9975a6db12ff0c916944d89184389e3ae3272c6d5690381`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085503a369edcce69a9e4e547a07f501228a3e71b00141b07bf7e4bf3beb4cf2`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5110522604cdddba047cc0be366f16edb6238a77df6c0b690e81f538401402c6`  
		Last Modified: Wed, 08 May 2019 16:17:30 GMT  
		Size: 9.4 MB (9424456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dc9134cb78fa8c8012494e966655a51906b8fbb9a287ff677f112cb6df5b7b`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1cc6aa008e3c92d0e543846f48ffc0278671ad3336e433360f2bbab577e4b7`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 2.1 KB (2066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62368ad6255191b9e3dafc29336216dd0f25b1acacf11eacdfa4a0a9d95b2f5c`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c246600f5484d9d71da31a270a9f1543cf79da2bf94a224314c659b9a66a875e`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre8` - linux; arm variant v7

```console
$ docker pull jetty@sha256:9f4c641dc0a44707812e694e8eade3015b6c059b468a4e688634a3c20ed24d0c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176059054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea2dba1b53efa6f56de5449b6625a4945aaa26e65463ca0f2ae298f2ad8ab22`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 12:03:26 GMT
ADD file:7e8dcc40e246d53b86266855a2de8080d26e6b4ed9f594c1acc565784405735b in / 
# Wed, 08 May 2019 12:03:27 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:04:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:14:59 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:15:01 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:16:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 17:55:00 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 17:55:03 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 17:55:03 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 17:55:03 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 17:55:10 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 17:55:12 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 17:55:12 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 17:55:14 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 17:55:16 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 17:55:17 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 17:55:18 GMT
USER jetty
# Wed, 08 May 2019 17:55:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 17:55:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 17:55:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f2a2fd7c1ab35cd1b5ea6fcc2b801f3877852797e2698ecdb9556e0dee3accb5`  
		Last Modified: Wed, 08 May 2019 12:09:40 GMT  
		Size: 42.1 MB (42082604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047df9a92c9f7376283a8d6af526f5126d95995ba48dd7de49979ef57da3e15b`  
		Last Modified: Wed, 08 May 2019 13:12:20 GMT  
		Size: 9.5 MB (9485167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeed4ac8d1e2c751afd6fd3517f1d154365467039353c377c8206fd5eb81d4b`  
		Last Modified: Wed, 08 May 2019 13:12:18 GMT  
		Size: 3.9 MB (3918605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646a29b8c83d854b86dccdbf390a7b296f5144aef4e38276c8a7b649e0804`  
		Last Modified: Wed, 08 May 2019 14:31:13 GMT  
		Size: 830.4 KB (830410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb3a067c54308aa02398bf021c38a952c18f27646b736d71732cbbc9b1010b0`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2c033d6c592b7d46aafecc714f1393be324b57f01f5e6c76e832e8ea04576a`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0d9e8d93d276090a71cd6c8346c468c9e051903bf52760756359c4451d33b`  
		Last Modified: Wed, 08 May 2019 14:34:14 GMT  
		Size: 110.3 MB (110311680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f07a446b7fe57fd236711da5953265e8d532d43c9cb8f25a533320e93a636`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6395f8d7de3564b4ae1e386bf6ed4e0f7723e94d4940a70b485a86504a75926`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc147ed50354f0d2a7587b28055ead9eec49df4f8eb5341d91e746671a6890d9`  
		Last Modified: Wed, 08 May 2019 17:57:20 GMT  
		Size: 9.4 MB (9424492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c93706301b9ef0c48c932aa219a1caa545887de6b3900e134bce06740648f8b`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d03e292fef5d40aada56fd958955f649c1637f1247f0ce20ccbe82940b6ccfd`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 2.1 KB (2069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f2350cc0ff9abae232377501904cbd64860bdbd5db9ef7c24bce5508cf073c`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d04c42b72f7e6024f6fdb7413c30b11da394d870eaa464bda596aa3e99142fc`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre8` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2fbb5ca36da5cad300aa58956606b38a8e3f3cecbb41851cdfd0c8696482575e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180322238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2bb61e7225a1b482f1f4664ddfbefa8060a5b43bc65fcd64f9680a51dc4749`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:48:25 GMT
ADD file:153045f4fe6532d8c2ff273bb249a7a3a4cba913c26a4103ba5ddce1af02c1e5 in / 
# Wed, 08 May 2019 08:48:26 GMT
CMD ["bash"]
# Wed, 08 May 2019 11:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:51:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 17 May 2019 22:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 May 2019 22:50:40 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2019 22:50:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 17 May 2019 22:50:42 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_VERSION=8u212
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Fri, 17 May 2019 22:51:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 17 Jul 2019 23:35:39 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2019 23:35:41 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 17 Jul 2019 23:35:41 GMT
WORKDIR /usr/local/jetty
# Wed, 17 Jul 2019 23:35:41 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 17 Jul 2019 23:35:47 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 17 Jul 2019 23:35:49 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 17 Jul 2019 23:35:49 GMT
WORKDIR /var/lib/jetty
# Wed, 17 Jul 2019 23:35:51 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:52 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 17 Jul 2019 23:35:53 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 17 Jul 2019 23:35:53 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 17 Jul 2019 23:35:54 GMT
USER jetty
# Wed, 17 Jul 2019 23:35:54 GMT
EXPOSE 8080
# Wed, 17 Jul 2019 23:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jul 2019 23:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5894e28291972e44f5c3eba2779a85979bae6f95ed4f3e43ea5c98a132f06c48`  
		Last Modified: Wed, 08 May 2019 08:54:43 GMT  
		Size: 43.1 MB (43141955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e6888cee6fef7c223eeaf2ca4c51bc0c21b4631971f416eb6a529a05e96cb`  
		Last Modified: Wed, 08 May 2019 12:07:05 GMT  
		Size: 9.7 MB (9733078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf90e854779f4c5edab378626d847fd0ab7aa9441b63a7db31a7db55d2b255b`  
		Last Modified: Wed, 08 May 2019 12:07:03 GMT  
		Size: 4.1 MB (4094187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc920c054370e9fe777d4546e8898e94588c01909d487696f8378c34d00b67e`  
		Last Modified: Fri, 17 May 2019 22:56:09 GMT  
		Size: 839.6 KB (839611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf483f25e9254d4337fac759851db8d04b5a2eea6056b1375ff19c2df554464`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a594c16f5b8360bf6256529e6a21eddf648595ac48000e0d91808fd21a9798`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9e1dac91c466b57c47d5738767104f91af563b89a969f98a2eff0d0692cd6`  
		Last Modified: Fri, 17 May 2019 23:00:18 GMT  
		Size: 113.1 MB (113082862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7e6b7fd0cb47998762442e0d2b1852c2692786149020092d36d17cbaddad32`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511814053ebc4a22abd8857c39836a2c1b6b9ee89da025924601e08bfb12412c`  
		Last Modified: Wed, 17 Jul 2019 23:37:42 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0bf7b138eb0319a3d75d1ab842fb65cd204e1c83dd7e92e2a0fb122cb2403d`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 9.4 MB (9424451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588601cf5b3de57b436e290ae8115f8bd4cd5553d0a88a42e233f763d21441b0`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2670e29c10dc3bc2f5c75c700e415015925039c9b4751a8920fdaebbb4f1c2e`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a627374a49fddcb68bd3f2ce734e8fbd58f7c745c55ac425411ca144d003de8`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b7659478cc7567aa9d6d6a3700403d10e80bf5542bc7846c6fc05f366f870`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre8` - linux; 386

```console
$ docker pull jetty@sha256:f532a68e9bbf79732ee7dbfaa205e1b742f0c2fefb7e19ba5c0d6d1491cbba08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194362543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd22310a1a4ac81a7cd7b96c967f835781080ad5f817dd7161256eb8ae0207e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 10:49:19 GMT
ADD file:fde8cf5700c66c38b88d4b3254ec1544d09194e06568c23fe3989f7eaa1f5785 in / 
# Wed, 08 May 2019 10:49:20 GMT
CMD ["bash"]
# Wed, 08 May 2019 19:08:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 19:08:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 22:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 22:16:13 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 22:16:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 22:16:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 04:57:10 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 04:57:11 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 04:57:11 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 04:57:16 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 04:57:17 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 04:57:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 04:57:19 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:19 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 04:57:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 04:57:20 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 04:57:20 GMT
USER jetty
# Thu, 09 May 2019 04:57:20 GMT
EXPOSE 8080
# Thu, 09 May 2019 04:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 04:57:21 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b5d586ad7adeab23f6ff0b7ec90785dc757eaccd445976fda3f6d7db64d20585`  
		Last Modified: Wed, 08 May 2019 10:57:26 GMT  
		Size: 46.1 MB (46063371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b18ff57de8d55737be40848138cbd66efcc99443ae507217ae5dd45e3cf41a`  
		Last Modified: Wed, 08 May 2019 19:14:07 GMT  
		Size: 10.8 MB (10802110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc701b379559241c696cd079ff9b83f0bba19faec8747d75654fe5bc7e8adb03`  
		Last Modified: Wed, 08 May 2019 19:14:05 GMT  
		Size: 4.6 MB (4561353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad72e88a4544f4570c0df9df66b43ca05325a8df5fe4bdac5e0240836f47d28`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 862.0 KB (862001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215fde6b1eafb43012d68d65388471bca2066ad401d508df13b046aa8b830e1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf128bb9e196d3a692d14dc4ed9c91920ab3ecb3fcb3d7e4c968fb1f18b9ce1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47742760e75d51e74c18576e2a0b2d447e91b2c3a023dc9e3b1e4a83aa7bdc1a`  
		Last Modified: Wed, 08 May 2019 22:52:46 GMT  
		Size: 122.6 MB (122643377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13df399b06606cedbc7ffce659af330dab9041dfebd5d98933853a74a0be48d3`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d50318d694cf0cf2727460d2057498228249819a1d83c2f92296c96dbfb1e`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad229b08fbaea588098dc7e42976c29d5b7a16be0e2a84b3ba0d811c5d724494`  
		Last Modified: Thu, 09 May 2019 04:58:53 GMT  
		Size: 9.4 MB (9424415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7161f78a4fe1f1d0ee6787a7f6f28b0a0241c7390a5c919ee688aac0caf3fef`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4163317071202eac58e9e3c5ec95d8b071ae013148d4f1376fdc09a340c7ed6b`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4d72a3ad59ec8fada471aa84164b581dd500aea022f038334b0eda00c0ec19`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7621b6c4a7959d913a05ce51aa49a199c616badaaa439ea6873fe8c5a9b89ee`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre8` - linux; ppc64le

```console
$ docker pull jetty@sha256:1c8d35096fdcfc3c448b203db5c12734655105f9f779d3734522511764e58233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184781497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eacbfac25da6c191d70cca800f7ed9b015a19adef7c4ab701c0b31540a6159e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:57:43 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:57:49 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:57:56 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:57:59 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 12:58:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 12:58:05 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 13:05:08 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 21:43:25 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 21:43:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 21:43:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 21:43:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 21:43:51 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 21:43:57 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 21:44:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 21:44:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 21:44:22 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:44:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 21:44:33 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 21:44:40 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 21:44:57 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:45:03 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 21:45:10 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 21:45:11 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 21:45:13 GMT
USER jetty
# Wed, 08 May 2019 21:45:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 21:45:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 21:45:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e4e060b9a0f1aadc5647d44be482b1363697a3fd8a4aeb6a4b9c53e17ecc4`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 848.6 KB (848616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e24f3bccdd6d1d666b5c75ba2971c3c1d1b974352776ac0c8d91b0244f35cb`  
		Last Modified: Wed, 08 May 2019 13:20:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f7a6e570eaf9c696f99b09d6fb9eaf034d87e7a1e9bf092cd38e9f71777a8b`  
		Last Modified: Wed, 08 May 2019 13:20:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a3232b209a6e8e5f133bb2d4b9c377dab2d71b8b57de44e32eefb5584bfd2`  
		Last Modified: Wed, 08 May 2019 13:21:49 GMT  
		Size: 114.6 MB (114611463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321ac118136d891526d4b7d585903133a760850fd8ba7b73f5608b51d289a8a`  
		Last Modified: Wed, 08 May 2019 21:50:41 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86141b28655e4b923da175ff032f463f8ef7bf16d23578dd00d25badfdce9b79`  
		Last Modified: Wed, 08 May 2019 21:50:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0e68a17da043f652f2d812d9c650558c382a9c2be40bb8fd901e19d89cb162`  
		Last Modified: Wed, 08 May 2019 21:50:38 GMT  
		Size: 9.4 MB (9424473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec696722258c05e106b7c921898aac4da7e2ab6ae65076942a12749f1049140b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cae7017c7325beea0f896b47ae71aa44260cac66b36379a32dbb0ed9309eaf`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 2.1 KB (2062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8302b92229dab552b306d2b48fba615a169e28af57e2c7fae6324ef3b4b028`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd387f05feedbcf33516453c4c46c64a80261af3ff1e6ebf007ccac52a95b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9.4-jre8` - linux; s390x

```console
$ docker pull jetty@sha256:eb8f97a23898ccdc5be026ea051ef231615b9455a4d78a72cbeb093439440cf5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184363097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55031fcaf6fba1a2c7256bad7bbcc09b11b036dbceb1807ceeacc9202792f231`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:42:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:52:21 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:52:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:52:32 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:52:35 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:54:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 05:12:37 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 05:12:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 05:12:42 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 05:12:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 05:12:59 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 05:13:05 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 05:13:06 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 05:13:16 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:16 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 05:13:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 05:13:21 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 05:13:22 GMT
USER jetty
# Thu, 09 May 2019 05:13:23 GMT
EXPOSE 8080
# Thu, 09 May 2019 05:13:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 05:13:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf61465b03d8ec5e8064ba91220d0e97c4dd5b75a7d2fe644aab7cc4a0a514c`  
		Last Modified: Wed, 08 May 2019 15:01:34 GMT  
		Size: 863.9 KB (863943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35375a807e76af07efe2bf1c77fce29498511166f4b41f158e181805528ce229`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53975ff11a25b69ce30d4b02d88f1b27cff3e5b1a2e08d05f6721e388f4a5d`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d381e46be773491220b0199e519c4f97308fee82af49481321e3d769db7b7b0a`  
		Last Modified: Wed, 08 May 2019 15:05:36 GMT  
		Size: 114.2 MB (114184348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e456897b935f1efded84a648055389e6c4fffbee3a50167ab95bf7cf047142`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace4f725dd5f318c30a864c4400d34b9d1dfeb8dba95f242af7e8668945d2a20`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6df7195f7b6c83e938c25f1940930649b862e2b5369ec6e041631c4cb1ebef`  
		Last Modified: Thu, 09 May 2019 05:17:27 GMT  
		Size: 9.4 MB (9424383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef61c6677aef99352724f560861db552edff24e57f288598be141e49f0802c8`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16572dc3fb4702653a0252ed5b29eb536479f0085f7ec2596c9d1c2e8214fd2f`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0aa75b063a662a0cd7f4af7b720863dfa8c7643b98bfc4b8ee5124a1bb069e`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ce48b6bff7dbea769d046b7311e98e7ea33aec40dca23a246a4b2c1fe530c5`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9-jdk13`

**does not exist** (yet?)

## `jetty:9-jdk13-slim`

**does not exist** (yet?)

## `jetty:9-jre11`

```console
$ docker pull jetty@sha256:743448bd33459baa801590f0459b27209284160d7efd6ef6808a388d5e5739e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `jetty:9-jre11` - linux; amd64

```console
$ docker pull jetty@sha256:df02049c665533624aba2da58feae02bc3505c860d2fc2e852924ef458f4b48c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116986183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9a100055b8fae61a4ed9daa37cd9156c453ba6914cf9088f47d795bbeaa26d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 08:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:55:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:55:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 Dec 2019 08:55:42 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:55:43 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 15 Jan 2020 21:29:23 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 15 Jan 2020 21:29:23 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 15 Jan 2020 21:29:24 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 15 Jan 2020 21:29:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 15 Jan 2020 22:06:18 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 15 Jan 2020 22:06:19 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Jan 2020 22:06:19 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2020 22:06:19 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 15 Jan 2020 22:06:20 GMT
WORKDIR /usr/local/jetty
# Wed, 15 Jan 2020 22:06:20 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 15 Jan 2020 22:06:20 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 15 Jan 2020 22:06:20 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 15 Jan 2020 22:06:24 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 15 Jan 2020 22:06:24 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Jan 2020 22:06:25 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 15 Jan 2020 22:06:25 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Jan 2020 22:06:27 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 15 Jan 2020 22:06:27 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Jan 2020 22:06:28 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 15 Jan 2020 22:06:28 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 15 Jan 2020 22:06:28 GMT
USER jetty
# Wed, 15 Jan 2020 22:06:28 GMT
EXPOSE 8080
# Wed, 15 Jan 2020 22:06:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Jan 2020 22:06:29 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8d3cd13de4f1c574d86de1c90b7e0f96d2394349c7e882117daaa86ad08ad`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 5.1 MB (5126129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99458a0c1a9454bc8cf23d0875b1272a6515fb2c6c4f0211cbc1a5f5fb0877d9`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770f7d01f29ecbf7dfad49bbbdfd6a2da7d92622a36cb6f59871cc1e0beafa3d`  
		Last Modified: Wed, 15 Jan 2020 21:35:02 GMT  
		Size: 41.9 MB (41911767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53a9636d83ae98e7185f901922690bde44fa39ed25d7ec7b8d600cfe730e30c`  
		Last Modified: Wed, 15 Jan 2020 22:07:04 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3536d604435e83016765fa72572c7f7fabcfa910f7bc825191362a9512b0c121`  
		Last Modified: Wed, 15 Jan 2020 22:07:04 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9df820f4c12827c92db1c93471467a9a85ac1486cbfff5321da1c87541c7147`  
		Last Modified: Wed, 15 Jan 2020 22:07:04 GMT  
		Size: 9.4 MB (9424442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c41edf12d4602f8e7e6f333d35f000ab2f672fd89bd5c7aaa74268282136f7`  
		Last Modified: Wed, 15 Jan 2020 22:07:03 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2ea1f3c555c6b911bf1987ccdbf0130e82c12655aaab12913e84eaa82936d`  
		Last Modified: Wed, 15 Jan 2020 22:07:03 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3351b55c9a541e5e2dbd145927c012feb5539a67a40fa8130eb405ce078bde`  
		Last Modified: Wed, 15 Jan 2020 22:07:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38606e8425bbc3662df6557c62bf28a49767e4525e1d17b89b7c2264ace3960`  
		Last Modified: Wed, 15 Jan 2020 22:07:03 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre11` - linux; arm variant v5

```console
$ docker pull jetty@sha256:e61dc4a9deb0e535e885492b717e194a793d87f0ef42cc2865cf291bd42ef87b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182727261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee22a3053daa67fd23097448e122bfc16fa0ab00f6a44db79016433570c1d25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:53:17 GMT
ADD file:5dfe3b771bd67a2856913544993e219cb8c7933c33523cc56fe13a3a0e76ce9b in / 
# Wed, 08 May 2019 08:53:18 GMT
CMD ["bash"]
# Wed, 08 May 2019 10:01:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 10:01:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 11:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:29:22 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 11:29:23 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 11:29:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 11:29:25 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 11:29:26 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 11:29:26 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 11:29:26 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 11:30:39 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 16:14:36 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 16:14:37 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 16:14:37 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 16:14:39 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 16:14:40 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 16:14:40 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 16:14:41 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 16:14:41 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 16:14:48 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:14:49 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 16:14:52 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 16:14:52 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 16:15:00 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:01 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 16:15:03 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 16:15:04 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 16:15:04 GMT
USER jetty
# Wed, 08 May 2019 16:15:05 GMT
EXPOSE 8080
# Wed, 08 May 2019 16:15:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 16:15:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ca892ced475bf1c51c1f13b76a64549cfc5d1a0b55d33d8b9418efbb47887bf8`  
		Last Modified: Wed, 08 May 2019 08:59:09 GMT  
		Size: 44.0 MB (44045778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b30b379469b50f6ada866964876f5c4ba164c22896bf3a08aabab61869e51`  
		Last Modified: Wed, 08 May 2019 10:09:26 GMT  
		Size: 9.9 MB (9854225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e257762b4747840fc09dce269e7f68146ac9864b8bf218e57475b4af367a74`  
		Last Modified: Wed, 08 May 2019 10:09:24 GMT  
		Size: 4.2 MB (4159009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0d161136f55f6e5c26bbd9fde30327cf06dec15e40d7ac330b8db368e4b9ee`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 846.1 KB (846058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5e8a953b512e86412d1d172548252ed8bbacdaa35b2f782a77deea2bc921d5`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cb1f59d6130f400627aa8a690ef028bb74ac9c0d19014a63d4a6e92f287919`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f6ed55942b2f3bdcbd69d0da3ad8c000707d9ccaa6cae8b61904819e9d4ad`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7894bb11a0e1b10913a4fca8f468f0cb96be5b70c48747027a3f8ba2ca4ee7b`  
		Last Modified: Wed, 08 May 2019 11:50:55 GMT  
		Size: 114.4 MB (114391453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b588bb59f0c45f2f6771f9e9c79e0226a7c731bc9aaee590e21a8ec705dc8402`  
		Last Modified: Wed, 08 May 2019 16:17:19 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186a0d3b3192bf16deb3eeba8f1df80d7fac471ee8792d0bc247919b970a8a4b`  
		Last Modified: Wed, 08 May 2019 16:17:19 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b6bbad04440d1a7ea395b78998ed2567802c265cfc26033a1299980b243ddc`  
		Last Modified: Wed, 08 May 2019 16:17:21 GMT  
		Size: 9.4 MB (9424423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5f28a51a21092851a210fcecda8e7d925f61f18d3e583114d9331c531a370e`  
		Last Modified: Wed, 08 May 2019 16:17:17 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b62f92ae9c631465a7092544ae2510c9bd0609012964470006257c25989f629`  
		Last Modified: Wed, 08 May 2019 16:17:18 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fda1533df868c03d8f2e763427fd72c5172c1bece17e16288dccfa7212d05b6`  
		Last Modified: Wed, 08 May 2019 16:17:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce5eb7099d7b0bcf1f2cbc10d7d5f22581ff5a72783fcac33bb6c033c9e7f00`  
		Last Modified: Wed, 08 May 2019 16:17:18 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre11` - linux; arm variant v7

```console
$ docker pull jetty@sha256:1ecfc60021b617f0b65e00a61f598388efda31bfa8498ae38bc31256e2d9fcf2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181917632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3931c46ad067ec7a675152dc901c10d01afbb07d47227ab30b45d8b83fa47dba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 12:03:26 GMT
ADD file:7e8dcc40e246d53b86266855a2de8080d26e6b4ed9f594c1acc565784405735b in / 
# Wed, 08 May 2019 12:03:27 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:04:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:10:10 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 14:10:11 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:10:15 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:10:19 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:10:20 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 14:10:20 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 14:10:21 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 14:11:25 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 17:54:33 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 17:54:33 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 17:54:34 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 17:54:35 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 17:54:36 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 17:54:36 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 17:54:37 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 17:54:37 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 17:54:43 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:54:44 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 17:54:45 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 17:54:46 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 17:54:48 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:54:48 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 17:54:50 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 17:54:51 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 17:54:51 GMT
USER jetty
# Wed, 08 May 2019 17:54:52 GMT
EXPOSE 8080
# Wed, 08 May 2019 17:54:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 17:54:53 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f2a2fd7c1ab35cd1b5ea6fcc2b801f3877852797e2698ecdb9556e0dee3accb5`  
		Last Modified: Wed, 08 May 2019 12:09:40 GMT  
		Size: 42.1 MB (42082604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047df9a92c9f7376283a8d6af526f5126d95995ba48dd7de49979ef57da3e15b`  
		Last Modified: Wed, 08 May 2019 13:12:20 GMT  
		Size: 9.5 MB (9485167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeed4ac8d1e2c751afd6fd3517f1d154365467039353c377c8206fd5eb81d4b`  
		Last Modified: Wed, 08 May 2019 13:12:18 GMT  
		Size: 3.9 MB (3918605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646a29b8c83d854b86dccdbf390a7b296f5144aef4e38276c8a7b649e0804`  
		Last Modified: Wed, 08 May 2019 14:31:13 GMT  
		Size: 830.4 KB (830410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6f0d217548ad4fca27f3fca1ad13e1d42b51dfdc66efe11ca75bec1768f91e`  
		Last Modified: Wed, 08 May 2019 14:31:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b3a1a9cf41d4f4ba6bd276263e9aa9d9510a7f587316f5128b4b8848a3fb8`  
		Last Modified: Wed, 08 May 2019 14:31:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5554c002ae1621fa85e450b809bb153315535856beedc3a4de016e7f8088ee3`  
		Last Modified: Wed, 08 May 2019 14:31:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74989df1042192176323ee1dd7ec5a173ef7c944e14eb3192d1cd38ca6750c97`  
		Last Modified: Wed, 08 May 2019 14:31:44 GMT  
		Size: 116.2 MB (116170095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b905662366849813f2538eae8fdfddf73101be031e315b3e1cfe5d2ecb091c2`  
		Last Modified: Wed, 08 May 2019 17:57:09 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a15e595b79d8819812a7c811c08d462e194fe42cf9848813bb0d506d0525c8`  
		Last Modified: Wed, 08 May 2019 17:57:09 GMT  
		Size: 181.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468d0998b6f9bfa90d04cef61fb3fe9a05229b655f4ef6919ebfc98eb38f1a30`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 9.4 MB (9424444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5c4061898f1685d8b125a0c028f4ebce0e067ad354f2450df4890ba8b9c6f4`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b048e8985511af8971bb264592da262faf16656240c48d00c00d1bb477f0f7`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c6b6b0b67d545dff18961b21a6789ac2efa79e0e229e7e9ea2f2137ca2155f`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f07ed6686762d8dbe77cefd25092cc139992ed1f5bcb16e585207b54fe2375d`  
		Last Modified: Wed, 08 May 2019 17:57:07 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre11` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:0bcbb36e80c2c1fe1dcb34fea01c7406b8c835e5baac6f8a2b1a403394f828f3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112480520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34960a7c18f0fd99929cb1c5e10bc53bbcb535cbc0823f3db8799358492905a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:15:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 18:28:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:28:53 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 18:28:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 Dec 2019 18:28:55 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 18:28:58 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 15 Jan 2020 21:52:37 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 15 Jan 2020 21:52:38 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 15 Jan 2020 21:52:39 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 15 Jan 2020 21:52:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Wed, 15 Jan 2020 22:48:40 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 15 Jan 2020 22:48:41 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 15 Jan 2020 22:48:41 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2020 22:48:43 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 15 Jan 2020 22:48:44 GMT
WORKDIR /usr/local/jetty
# Wed, 15 Jan 2020 22:48:44 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 15 Jan 2020 22:48:45 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 15 Jan 2020 22:48:45 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 15 Jan 2020 22:48:50 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 15 Jan 2020 22:48:51 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 15 Jan 2020 22:48:52 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 15 Jan 2020 22:48:53 GMT
WORKDIR /var/lib/jetty
# Wed, 15 Jan 2020 22:48:55 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 15 Jan 2020 22:48:56 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 15 Jan 2020 22:48:58 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 15 Jan 2020 22:48:58 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 15 Jan 2020 22:48:59 GMT
USER jetty
# Wed, 15 Jan 2020 22:49:00 GMT
EXPOSE 8080
# Wed, 15 Jan 2020 22:49:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Jan 2020 22:49:01 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f31062581dadb1f69c43e9441040dd46788bf13ae51f20c66929fac82b506b`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 9.7 MB (9748258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62337a296a607f48a5dc3a7c07639360d98e0e78982ca8e459c832719012f12`  
		Last Modified: Sat, 28 Dec 2019 06:24:15 GMT  
		Size: 4.1 MB (4094448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa93134dbc80dab62077651c441c2b4f5f8eab4626587ec74711ad51d46ec4ca`  
		Last Modified: Sat, 28 Dec 2019 18:31:59 GMT  
		Size: 5.0 MB (5027084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40624577614540513606003282ed1300f9d6f1a8b046d54c9296b4ff823bed3e`  
		Last Modified: Sat, 28 Dec 2019 18:31:58 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26943aa2587f2cbaa709fd95b2c1252891e411037eaa8b92d20b524c72dc0093`  
		Last Modified: Wed, 15 Jan 2020 21:55:28 GMT  
		Size: 41.0 MB (41013873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b7163c3b6e2c910c8cceaac0e190dcfcebe006dfc8823ef925b286959c0a97`  
		Last Modified: Wed, 15 Jan 2020 22:49:50 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9644e47a63c665b9df0b5d57af2c17e96a867c8492e37984a7b24351d8cc39`  
		Last Modified: Wed, 15 Jan 2020 22:49:50 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e66d081444beea67a939cd03b75f7c67533b366fb267e5d794c0dc38339cdb`  
		Last Modified: Wed, 15 Jan 2020 22:49:50 GMT  
		Size: 9.4 MB (9424444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f9f8a44fc93244382edeaa036b725464a8fb4832e441264a4eece16e7ded`  
		Last Modified: Wed, 15 Jan 2020 22:49:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e50754055223f2f91d44b59640d119eb54d8c0fb0d827a5ff9c4a6adb53e9f6`  
		Last Modified: Wed, 15 Jan 2020 22:49:49 GMT  
		Size: 2.1 KB (2067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59af7c77b5971d9e25e091c2906290d72cca0a5d1179c451a867f4f0f72847b`  
		Last Modified: Wed, 15 Jan 2020 22:49:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916d2bc24cb918d077da9d794ed577547723529c96e9f51771476db6219b02f8`  
		Last Modified: Wed, 15 Jan 2020 22:49:49 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre11` - linux; 386

```console
$ docker pull jetty@sha256:df37be9c17a3ded9d55712e500da0834a54dae8701bf8cec4068ea80fec9a51d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208102749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f8257a74c907091d1c93581da69d1816286a503d26abd587ef5649811eac9e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 10:49:19 GMT
ADD file:fde8cf5700c66c38b88d4b3254ec1544d09194e06568c23fe3989f7eaa1f5785 in / 
# Wed, 08 May 2019 10:49:20 GMT
CMD ["bash"]
# Wed, 08 May 2019 19:08:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 19:08:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 22:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 22:13:16 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 22:13:16 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 22:13:17 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 22:13:18 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 22:13:18 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 22:13:18 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 22:13:18 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 22:14:01 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 04:56:56 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 04:56:56 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 04:56:56 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 04:56:57 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 04:56:57 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 04:56:57 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 04:56:57 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 04:56:57 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 04:57:02 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:02 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 04:57:02 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 04:57:03 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 04:57:04 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:04 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 04:57:05 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 04:57:05 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 04:57:05 GMT
USER jetty
# Thu, 09 May 2019 04:57:05 GMT
EXPOSE 8080
# Thu, 09 May 2019 04:57:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 04:57:06 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b5d586ad7adeab23f6ff0b7ec90785dc757eaccd445976fda3f6d7db64d20585`  
		Last Modified: Wed, 08 May 2019 10:57:26 GMT  
		Size: 46.1 MB (46063371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b18ff57de8d55737be40848138cbd66efcc99443ae507217ae5dd45e3cf41a`  
		Last Modified: Wed, 08 May 2019 19:14:07 GMT  
		Size: 10.8 MB (10802110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc701b379559241c696cd079ff9b83f0bba19faec8747d75654fe5bc7e8adb03`  
		Last Modified: Wed, 08 May 2019 19:14:05 GMT  
		Size: 4.6 MB (4561353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad72e88a4544f4570c0df9df66b43ca05325a8df5fe4bdac5e0240836f47d28`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 862.0 KB (862001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d563d964c8c48c0bf9ce2911e516238b632ac5f81600f42779901aad7954efb1`  
		Last Modified: Wed, 08 May 2019 22:48:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448b9d083751b7e5b0e8c9c68a54cb84e7d8e85e56fb1576c41defa410151dc4`  
		Last Modified: Wed, 08 May 2019 22:48:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dde35a9cb946023f1ef745968d557ccc74c2a8718a6eb1893bf03b29780681`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f132fb339ff847f4e8d45fa1121a1dd7c3518bcbca5455379e20a438d90051`  
		Last Modified: Wed, 08 May 2019 22:49:21 GMT  
		Size: 136.4 MB (136383359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9f73035593a6432298a218ec76ea04a3bbe74b2ddf734954be5cdf0f19a884`  
		Last Modified: Thu, 09 May 2019 04:58:20 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34450b099ff0d4b45f09b6e00ed3d2f026f6d2181b0855a8e604d6c50f438ce8`  
		Last Modified: Thu, 09 May 2019 04:58:20 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f6bfd4f4e9bbe80a06aac3454c6a6000bc4f9420f0a11eff9fc8c13c991ea`  
		Last Modified: Thu, 09 May 2019 04:58:43 GMT  
		Size: 9.4 MB (9424412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fd4fadc048c535a97814ead296a6de898dca7a8fd68ae4f85c077be1c890b9`  
		Last Modified: Thu, 09 May 2019 04:58:19 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3281f27ff370a5a26ddf56f7cd5534d772cd235c28ae20c14344af171db6b6cb`  
		Last Modified: Thu, 09 May 2019 04:58:19 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d06705f17aaeed0c4c486c318c9933ae35cbe904e486948cc4d8acafb8c747c`  
		Last Modified: Thu, 09 May 2019 04:58:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e70071461854031178286e82a09dd470e12b18954be16f72b4dfc28faa7d7c`  
		Last Modified: Thu, 09 May 2019 04:58:19 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre11` - linux; ppc64le

```console
$ docker pull jetty@sha256:07be9dfcfd9808776f141b115e6ee606dd9d7771e6f78b947d0fc91483eebd0b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189621947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7a17938314024b414f098753ede070efa2a9509e0b47e7d89f2ed89d20d812`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:39:34 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 12:39:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:39:45 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:39:54 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:39:57 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 12:40:00 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 12:40:04 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 12:45:53 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 21:41:05 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 21:41:11 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 21:41:21 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 21:41:33 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 21:41:40 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 21:41:45 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 21:41:53 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 21:41:57 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 21:42:14 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:42:19 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 21:42:25 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 21:42:30 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 21:42:40 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:42:43 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 21:42:49 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 21:42:50 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 21:42:55 GMT
USER jetty
# Wed, 08 May 2019 21:42:59 GMT
EXPOSE 8080
# Wed, 08 May 2019 21:43:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 21:43:05 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e4e060b9a0f1aadc5647d44be482b1363697a3fd8a4aeb6a4b9c53e17ecc4`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 848.6 KB (848616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afcad30d91e6ef6a6235e8ee8ea34984a8a03714f83006880a27d23e1ec6b07`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17792a5a83e70e4555affd27a076727218038ebe3722cbcecde52eb8d81e41e8`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743f9ba8d5fbd6557dc6ece9e230fd856733b23a5d6477a9a669a4f68c61da85`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4c5964ec2a98758cf78dd517a7d26b5badaa386bdfb0386d00ef2df17dd4bd`  
		Last Modified: Wed, 08 May 2019 13:16:33 GMT  
		Size: 119.5 MB (119451690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df08f032fbe3dbde5f9f0ad89f0a4e6b889f432b721ab9dbfb85353ee0e9fef`  
		Last Modified: Wed, 08 May 2019 21:50:17 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bf0a36101b3a646c73c79d0434d3900443d359a61db049c61f105c19ecafe0`  
		Last Modified: Wed, 08 May 2019 21:50:17 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f294abacdbae073a70caa4320195b3b9747092e2d4b540e9c9296789a3e8d0`  
		Last Modified: Wed, 08 May 2019 21:50:13 GMT  
		Size: 9.4 MB (9424455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c32361000d26c34e33dff0be63e8711ddd60602752733496f49039c4bc6a525`  
		Last Modified: Wed, 08 May 2019 21:50:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431afe509baab77de49754d848729f64e98b4d841263f3a7215c3ae1dd72dea`  
		Last Modified: Wed, 08 May 2019 21:50:12 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943c1c5aa0915ad87574f6e5c8654d3c82a05a3e14010d8de39a1cfc1cc0e79e`  
		Last Modified: Wed, 08 May 2019 21:50:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc862d40e0df89a75d83b1f1aea167aef04d762834923ff91b44d616879b71d5`  
		Last Modified: Wed, 08 May 2019 21:50:12 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre11` - linux; s390x

```console
$ docker pull jetty@sha256:2b3945632b33b3f0de7929625c216ee1ffda84af072056c4680ab3b4d68c4c10
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189340518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd80fb0108049e37a092dc1371a502210f2d1d9167218cb3db90b1d0f34c13bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:42:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:42:15 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/stretch-backports.list
# Wed, 08 May 2019 14:42:16 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:42:20 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:42:23 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:42:24 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 08 May 2019 14:42:25 GMT
ENV JAVA_VERSION=11.0.3
# Wed, 08 May 2019 14:42:25 GMT
ENV JAVA_DEBIAN_VERSION=11.0.3+1-1~bpo9+1
# Wed, 08 May 2019 14:45:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-11-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		keytool -importkeystore -srckeystore /etc/ssl/certs/java/cacerts -destkeystore /etc/ssl/certs/java/cacerts.jks -deststoretype JKS -srcstorepass changeit -deststorepass changeit -noprompt; 	mv /etc/ssl/certs/java/cacerts.jks /etc/ssl/certs/java/cacerts; 	/var/lib/dpkg/info/ca-certificates-java.postinst configure; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 05:11:08 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 05:11:09 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 05:11:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 05:11:14 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 05:11:15 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 05:11:17 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 05:11:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 05:11:19 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 05:11:35 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:11:35 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 05:11:42 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 05:11:43 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 05:11:54 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:11:55 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 05:11:58 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 05:11:59 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 05:12:00 GMT
USER jetty
# Thu, 09 May 2019 05:12:01 GMT
EXPOSE 8080
# Thu, 09 May 2019 05:12:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 05:12:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf61465b03d8ec5e8064ba91220d0e97c4dd5b75a7d2fe644aab7cc4a0a514c`  
		Last Modified: Wed, 08 May 2019 15:01:34 GMT  
		Size: 863.9 KB (863943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7875682bb43ee4dfedb0db2f5ffa045803895445c3434edfed0723d3f4dd700`  
		Last Modified: Wed, 08 May 2019 15:01:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7406aa79a5f911227056620e3ae81aaf33a7c207f34292a287bda26a00db256a`  
		Last Modified: Wed, 08 May 2019 15:01:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82c65756cebc86ea719c2cabfae397ed4030a5a942dc03f44dd0f91272fb555`  
		Last Modified: Wed, 08 May 2019 15:01:33 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b85b1ac77736c32a8c794742d393f3ab32897f6833cba700dd680ab8fd406f2`  
		Last Modified: Wed, 08 May 2019 15:02:08 GMT  
		Size: 119.2 MB (119161534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd44949cd09d1d0e5969fcb7156d120b69832e2497ea2b33b30297ae070ddc48`  
		Last Modified: Thu, 09 May 2019 05:17:11 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f268f0bd558aeccb48a867e42b5a5ce837a651f8cc8cdc767237dafac042df76`  
		Last Modified: Thu, 09 May 2019 05:17:11 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3568694999bdf31b1c2961e9ca7a5b69b7b2530a2d09a136023f8ee2eddcc718`  
		Last Modified: Thu, 09 May 2019 05:17:11 GMT  
		Size: 9.4 MB (9424386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab0e2f0ac2e6648b212cb353f9b0bc31b5c587e992d1ac351bd2766f926055d`  
		Last Modified: Thu, 09 May 2019 05:17:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7851714d11fef24e37dd11b911a3fa3462d109d5e6fdd3e9aca6ad5036cec029`  
		Last Modified: Thu, 09 May 2019 05:17:09 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f887c9590eb836ca23b01454d6e4e0521c7764202e43f7c655694e11aa5cf5e5`  
		Last Modified: Thu, 09 May 2019 05:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd93f6136177d3f01602a7548a1a92272b16419c77a0aa835043c8533a403cdb`  
		Last Modified: Thu, 09 May 2019 05:17:09 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:9-jre11-slim`

**does not exist** (yet?)

## `jetty:9-jre8`

```console
$ docker pull jetty@sha256:d8f374b030b7e0af3d422887dafefa75ef9fe1b4de36f3e4e1a806de59fbbeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `jetty:9-jre8` - linux; amd64

```console
$ docker pull jetty@sha256:c2f362b5654ae4e16cd96f410c479e3b0cac574607a32c13501dd922e0a20ad5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115270945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7cfb40b7f4b3aaab1f50c4ca270acd53caf6cf9c2c04e332eedd72bc3006c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 08:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:55:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 Dec 2019 08:56:57 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_VERSION=8u232
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_URL_VERSION=8u232b09
# Sat, 28 Dec 2019 08:57:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sun, 29 Dec 2019 08:31:21 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Sun, 29 Dec 2019 08:31:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sun, 29 Dec 2019 08:31:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2019 08:31:22 GMT
RUN mkdir -p "$JETTY_HOME"
# Sun, 29 Dec 2019 08:31:23 GMT
WORKDIR /usr/local/jetty
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Sun, 29 Dec 2019 08:31:27 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sun, 29 Dec 2019 08:31:28 GMT
RUN mkdir -p "$JETTY_BASE"
# Sun, 29 Dec 2019 08:31:28 GMT
WORKDIR /var/lib/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:30 GMT
ENV TMPDIR=/tmp/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Sun, 29 Dec 2019 08:31:31 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Sun, 29 Dec 2019 08:31:31 GMT
USER jetty
# Sun, 29 Dec 2019 08:31:31 GMT
EXPOSE 8080
# Sun, 29 Dec 2019 08:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 Dec 2019 08:31:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8d3cd13de4f1c574d86de1c90b7e0f96d2394349c7e882117daaa86ad08ad`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 5.1 MB (5126129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06bdc5e0db3a85fca16aae57afb18ced9fad56ed4571f9bd0d748f38930b22`  
		Last Modified: Sat, 28 Dec 2019 09:03:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b1f94cfe4ae6c7ca9e45cc45491b7f732d099001d933ac72211dbd09d19e0d`  
		Last Modified: Sat, 28 Dec 2019 09:03:45 GMT  
		Size: 40.2 MB (40196546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe20b880320d8f58a256fe49d1c7c23c61b64baa639ad7279118a09e05b99b2b`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b913b52ac10d2aec4b74f5b78af565b0c0b25888a4c4826a1301239a847aab`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95861d4f30fde9cf21c8c2cb828a68434818251a138bdbdd7d275ca2e78987a`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 9.4 MB (9424429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecc3b45eaba005a5e755b9d4186273b7300646c4a3392159aab8b7ddd4f8d6`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46a5d5760312fac8ac9744158c27194bc30d047cb09045715eb95886f0376e9`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95bd8335f7360f38bfa50b47f5a83975722151ddc1cc65f78dbd7775f1e568`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5526a96dfe33daca789ac452c1286664ab7610d5447d2089cdd69f93c0bd3bd1`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre8` - linux; arm variant v5

```console
$ docker pull jetty@sha256:6b79ec2ccfa3ee643017cecbdeee7565e32a4b74912ab39d95bbb17a1d1f7700
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180287052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965e56aa7b329cf860c5d90d360d6f490b43bfdb9ec51dfb7235b27e1cabbcbb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:53:17 GMT
ADD file:5dfe3b771bd67a2856913544993e219cb8c7933c33523cc56fe13a3a0e76ce9b in / 
# Wed, 08 May 2019 08:53:18 GMT
CMD ["bash"]
# Wed, 08 May 2019 10:01:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 10:01:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 11:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:35:27 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 11:35:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 11:35:31 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 11:36:37 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 16:15:13 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 16:15:13 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 16:15:14 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 16:15:16 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 16:15:16 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 16:15:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 16:15:24 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 16:15:27 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 16:15:27 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 16:15:32 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:32 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 16:15:35 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 16:15:36 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 16:15:37 GMT
USER jetty
# Wed, 08 May 2019 16:15:37 GMT
EXPOSE 8080
# Wed, 08 May 2019 16:15:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 16:15:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ca892ced475bf1c51c1f13b76a64549cfc5d1a0b55d33d8b9418efbb47887bf8`  
		Last Modified: Wed, 08 May 2019 08:59:09 GMT  
		Size: 44.0 MB (44045778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b30b379469b50f6ada866964876f5c4ba164c22896bf3a08aabab61869e51`  
		Last Modified: Wed, 08 May 2019 10:09:26 GMT  
		Size: 9.9 MB (9854225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e257762b4747840fc09dce269e7f68146ac9864b8bf218e57475b4af367a74`  
		Last Modified: Wed, 08 May 2019 10:09:24 GMT  
		Size: 4.2 MB (4159009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0d161136f55f6e5c26bbd9fde30327cf06dec15e40d7ac330b8db368e4b9ee`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 846.1 KB (846058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a59da16addae7a15d26d4edba174883fd994d29bb943085361990730c6787`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d14b7a612bfb82f68156f623a22e64ab4524cbf82c592f9365a904bac033a5`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e798df308d1bafc2c22d22386cb75aa71c9b8fc3c7b9ff5e736c1464c83bea`  
		Last Modified: Wed, 08 May 2019 11:53:24 GMT  
		Size: 112.0 MB (111951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5962f9d6fd65875c9975a6db12ff0c916944d89184389e3ae3272c6d5690381`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085503a369edcce69a9e4e547a07f501228a3e71b00141b07bf7e4bf3beb4cf2`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5110522604cdddba047cc0be366f16edb6238a77df6c0b690e81f538401402c6`  
		Last Modified: Wed, 08 May 2019 16:17:30 GMT  
		Size: 9.4 MB (9424456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dc9134cb78fa8c8012494e966655a51906b8fbb9a287ff677f112cb6df5b7b`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1cc6aa008e3c92d0e543846f48ffc0278671ad3336e433360f2bbab577e4b7`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 2.1 KB (2066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62368ad6255191b9e3dafc29336216dd0f25b1acacf11eacdfa4a0a9d95b2f5c`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c246600f5484d9d71da31a270a9f1543cf79da2bf94a224314c659b9a66a875e`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre8` - linux; arm variant v7

```console
$ docker pull jetty@sha256:9f4c641dc0a44707812e694e8eade3015b6c059b468a4e688634a3c20ed24d0c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176059054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea2dba1b53efa6f56de5449b6625a4945aaa26e65463ca0f2ae298f2ad8ab22`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 12:03:26 GMT
ADD file:7e8dcc40e246d53b86266855a2de8080d26e6b4ed9f594c1acc565784405735b in / 
# Wed, 08 May 2019 12:03:27 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:04:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:14:59 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:15:01 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:16:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 17:55:00 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 17:55:03 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 17:55:03 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 17:55:03 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 17:55:10 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 17:55:12 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 17:55:12 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 17:55:14 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 17:55:16 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 17:55:17 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 17:55:18 GMT
USER jetty
# Wed, 08 May 2019 17:55:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 17:55:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 17:55:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f2a2fd7c1ab35cd1b5ea6fcc2b801f3877852797e2698ecdb9556e0dee3accb5`  
		Last Modified: Wed, 08 May 2019 12:09:40 GMT  
		Size: 42.1 MB (42082604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047df9a92c9f7376283a8d6af526f5126d95995ba48dd7de49979ef57da3e15b`  
		Last Modified: Wed, 08 May 2019 13:12:20 GMT  
		Size: 9.5 MB (9485167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeed4ac8d1e2c751afd6fd3517f1d154365467039353c377c8206fd5eb81d4b`  
		Last Modified: Wed, 08 May 2019 13:12:18 GMT  
		Size: 3.9 MB (3918605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646a29b8c83d854b86dccdbf390a7b296f5144aef4e38276c8a7b649e0804`  
		Last Modified: Wed, 08 May 2019 14:31:13 GMT  
		Size: 830.4 KB (830410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb3a067c54308aa02398bf021c38a952c18f27646b736d71732cbbc9b1010b0`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2c033d6c592b7d46aafecc714f1393be324b57f01f5e6c76e832e8ea04576a`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0d9e8d93d276090a71cd6c8346c468c9e051903bf52760756359c4451d33b`  
		Last Modified: Wed, 08 May 2019 14:34:14 GMT  
		Size: 110.3 MB (110311680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f07a446b7fe57fd236711da5953265e8d532d43c9cb8f25a533320e93a636`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6395f8d7de3564b4ae1e386bf6ed4e0f7723e94d4940a70b485a86504a75926`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc147ed50354f0d2a7587b28055ead9eec49df4f8eb5341d91e746671a6890d9`  
		Last Modified: Wed, 08 May 2019 17:57:20 GMT  
		Size: 9.4 MB (9424492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c93706301b9ef0c48c932aa219a1caa545887de6b3900e134bce06740648f8b`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d03e292fef5d40aada56fd958955f649c1637f1247f0ce20ccbe82940b6ccfd`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 2.1 KB (2069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f2350cc0ff9abae232377501904cbd64860bdbd5db9ef7c24bce5508cf073c`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d04c42b72f7e6024f6fdb7413c30b11da394d870eaa464bda596aa3e99142fc`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre8` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2fbb5ca36da5cad300aa58956606b38a8e3f3cecbb41851cdfd0c8696482575e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180322238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2bb61e7225a1b482f1f4664ddfbefa8060a5b43bc65fcd64f9680a51dc4749`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:48:25 GMT
ADD file:153045f4fe6532d8c2ff273bb249a7a3a4cba913c26a4103ba5ddce1af02c1e5 in / 
# Wed, 08 May 2019 08:48:26 GMT
CMD ["bash"]
# Wed, 08 May 2019 11:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:51:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 17 May 2019 22:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 May 2019 22:50:40 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2019 22:50:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 17 May 2019 22:50:42 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_VERSION=8u212
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Fri, 17 May 2019 22:51:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 17 Jul 2019 23:35:39 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2019 23:35:41 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 17 Jul 2019 23:35:41 GMT
WORKDIR /usr/local/jetty
# Wed, 17 Jul 2019 23:35:41 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 17 Jul 2019 23:35:47 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 17 Jul 2019 23:35:49 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 17 Jul 2019 23:35:49 GMT
WORKDIR /var/lib/jetty
# Wed, 17 Jul 2019 23:35:51 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:52 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 17 Jul 2019 23:35:53 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 17 Jul 2019 23:35:53 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 17 Jul 2019 23:35:54 GMT
USER jetty
# Wed, 17 Jul 2019 23:35:54 GMT
EXPOSE 8080
# Wed, 17 Jul 2019 23:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jul 2019 23:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5894e28291972e44f5c3eba2779a85979bae6f95ed4f3e43ea5c98a132f06c48`  
		Last Modified: Wed, 08 May 2019 08:54:43 GMT  
		Size: 43.1 MB (43141955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e6888cee6fef7c223eeaf2ca4c51bc0c21b4631971f416eb6a529a05e96cb`  
		Last Modified: Wed, 08 May 2019 12:07:05 GMT  
		Size: 9.7 MB (9733078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf90e854779f4c5edab378626d847fd0ab7aa9441b63a7db31a7db55d2b255b`  
		Last Modified: Wed, 08 May 2019 12:07:03 GMT  
		Size: 4.1 MB (4094187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc920c054370e9fe777d4546e8898e94588c01909d487696f8378c34d00b67e`  
		Last Modified: Fri, 17 May 2019 22:56:09 GMT  
		Size: 839.6 KB (839611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf483f25e9254d4337fac759851db8d04b5a2eea6056b1375ff19c2df554464`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a594c16f5b8360bf6256529e6a21eddf648595ac48000e0d91808fd21a9798`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9e1dac91c466b57c47d5738767104f91af563b89a969f98a2eff0d0692cd6`  
		Last Modified: Fri, 17 May 2019 23:00:18 GMT  
		Size: 113.1 MB (113082862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7e6b7fd0cb47998762442e0d2b1852c2692786149020092d36d17cbaddad32`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511814053ebc4a22abd8857c39836a2c1b6b9ee89da025924601e08bfb12412c`  
		Last Modified: Wed, 17 Jul 2019 23:37:42 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0bf7b138eb0319a3d75d1ab842fb65cd204e1c83dd7e92e2a0fb122cb2403d`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 9.4 MB (9424451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588601cf5b3de57b436e290ae8115f8bd4cd5553d0a88a42e233f763d21441b0`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2670e29c10dc3bc2f5c75c700e415015925039c9b4751a8920fdaebbb4f1c2e`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a627374a49fddcb68bd3f2ce734e8fbd58f7c745c55ac425411ca144d003de8`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b7659478cc7567aa9d6d6a3700403d10e80bf5542bc7846c6fc05f366f870`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre8` - linux; 386

```console
$ docker pull jetty@sha256:f532a68e9bbf79732ee7dbfaa205e1b742f0c2fefb7e19ba5c0d6d1491cbba08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194362543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd22310a1a4ac81a7cd7b96c967f835781080ad5f817dd7161256eb8ae0207e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 10:49:19 GMT
ADD file:fde8cf5700c66c38b88d4b3254ec1544d09194e06568c23fe3989f7eaa1f5785 in / 
# Wed, 08 May 2019 10:49:20 GMT
CMD ["bash"]
# Wed, 08 May 2019 19:08:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 19:08:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 22:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 22:16:13 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 22:16:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 22:16:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 04:57:10 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 04:57:11 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 04:57:11 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 04:57:16 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 04:57:17 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 04:57:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 04:57:19 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:19 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 04:57:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 04:57:20 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 04:57:20 GMT
USER jetty
# Thu, 09 May 2019 04:57:20 GMT
EXPOSE 8080
# Thu, 09 May 2019 04:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 04:57:21 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b5d586ad7adeab23f6ff0b7ec90785dc757eaccd445976fda3f6d7db64d20585`  
		Last Modified: Wed, 08 May 2019 10:57:26 GMT  
		Size: 46.1 MB (46063371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b18ff57de8d55737be40848138cbd66efcc99443ae507217ae5dd45e3cf41a`  
		Last Modified: Wed, 08 May 2019 19:14:07 GMT  
		Size: 10.8 MB (10802110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc701b379559241c696cd079ff9b83f0bba19faec8747d75654fe5bc7e8adb03`  
		Last Modified: Wed, 08 May 2019 19:14:05 GMT  
		Size: 4.6 MB (4561353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad72e88a4544f4570c0df9df66b43ca05325a8df5fe4bdac5e0240836f47d28`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 862.0 KB (862001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215fde6b1eafb43012d68d65388471bca2066ad401d508df13b046aa8b830e1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf128bb9e196d3a692d14dc4ed9c91920ab3ecb3fcb3d7e4c968fb1f18b9ce1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47742760e75d51e74c18576e2a0b2d447e91b2c3a023dc9e3b1e4a83aa7bdc1a`  
		Last Modified: Wed, 08 May 2019 22:52:46 GMT  
		Size: 122.6 MB (122643377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13df399b06606cedbc7ffce659af330dab9041dfebd5d98933853a74a0be48d3`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d50318d694cf0cf2727460d2057498228249819a1d83c2f92296c96dbfb1e`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad229b08fbaea588098dc7e42976c29d5b7a16be0e2a84b3ba0d811c5d724494`  
		Last Modified: Thu, 09 May 2019 04:58:53 GMT  
		Size: 9.4 MB (9424415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7161f78a4fe1f1d0ee6787a7f6f28b0a0241c7390a5c919ee688aac0caf3fef`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4163317071202eac58e9e3c5ec95d8b071ae013148d4f1376fdc09a340c7ed6b`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4d72a3ad59ec8fada471aa84164b581dd500aea022f038334b0eda00c0ec19`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7621b6c4a7959d913a05ce51aa49a199c616badaaa439ea6873fe8c5a9b89ee`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre8` - linux; ppc64le

```console
$ docker pull jetty@sha256:1c8d35096fdcfc3c448b203db5c12734655105f9f779d3734522511764e58233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184781497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eacbfac25da6c191d70cca800f7ed9b015a19adef7c4ab701c0b31540a6159e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:57:43 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:57:49 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:57:56 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:57:59 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 12:58:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 12:58:05 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 13:05:08 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 21:43:25 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 21:43:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 21:43:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 21:43:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 21:43:51 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 21:43:57 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 21:44:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 21:44:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 21:44:22 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:44:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 21:44:33 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 21:44:40 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 21:44:57 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:45:03 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 21:45:10 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 21:45:11 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 21:45:13 GMT
USER jetty
# Wed, 08 May 2019 21:45:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 21:45:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 21:45:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e4e060b9a0f1aadc5647d44be482b1363697a3fd8a4aeb6a4b9c53e17ecc4`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 848.6 KB (848616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e24f3bccdd6d1d666b5c75ba2971c3c1d1b974352776ac0c8d91b0244f35cb`  
		Last Modified: Wed, 08 May 2019 13:20:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f7a6e570eaf9c696f99b09d6fb9eaf034d87e7a1e9bf092cd38e9f71777a8b`  
		Last Modified: Wed, 08 May 2019 13:20:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a3232b209a6e8e5f133bb2d4b9c377dab2d71b8b57de44e32eefb5584bfd2`  
		Last Modified: Wed, 08 May 2019 13:21:49 GMT  
		Size: 114.6 MB (114611463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321ac118136d891526d4b7d585903133a760850fd8ba7b73f5608b51d289a8a`  
		Last Modified: Wed, 08 May 2019 21:50:41 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86141b28655e4b923da175ff032f463f8ef7bf16d23578dd00d25badfdce9b79`  
		Last Modified: Wed, 08 May 2019 21:50:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0e68a17da043f652f2d812d9c650558c382a9c2be40bb8fd901e19d89cb162`  
		Last Modified: Wed, 08 May 2019 21:50:38 GMT  
		Size: 9.4 MB (9424473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec696722258c05e106b7c921898aac4da7e2ab6ae65076942a12749f1049140b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cae7017c7325beea0f896b47ae71aa44260cac66b36379a32dbb0ed9309eaf`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 2.1 KB (2062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8302b92229dab552b306d2b48fba615a169e28af57e2c7fae6324ef3b4b028`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd387f05feedbcf33516453c4c46c64a80261af3ff1e6ebf007ccac52a95b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:9-jre8` - linux; s390x

```console
$ docker pull jetty@sha256:eb8f97a23898ccdc5be026ea051ef231615b9455a4d78a72cbeb093439440cf5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184363097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55031fcaf6fba1a2c7256bad7bbcc09b11b036dbceb1807ceeacc9202792f231`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:42:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:52:21 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:52:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:52:32 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:52:35 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:54:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 05:12:37 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 05:12:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 05:12:42 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 05:12:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 05:12:59 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 05:13:05 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 05:13:06 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 05:13:16 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:16 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 05:13:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 05:13:21 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 05:13:22 GMT
USER jetty
# Thu, 09 May 2019 05:13:23 GMT
EXPOSE 8080
# Thu, 09 May 2019 05:13:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 05:13:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf61465b03d8ec5e8064ba91220d0e97c4dd5b75a7d2fe644aab7cc4a0a514c`  
		Last Modified: Wed, 08 May 2019 15:01:34 GMT  
		Size: 863.9 KB (863943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35375a807e76af07efe2bf1c77fce29498511166f4b41f158e181805528ce229`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53975ff11a25b69ce30d4b02d88f1b27cff3e5b1a2e08d05f6721e388f4a5d`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d381e46be773491220b0199e519c4f97308fee82af49481321e3d769db7b7b0a`  
		Last Modified: Wed, 08 May 2019 15:05:36 GMT  
		Size: 114.2 MB (114184348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e456897b935f1efded84a648055389e6c4fffbee3a50167ab95bf7cf047142`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace4f725dd5f318c30a864c4400d34b9d1dfeb8dba95f242af7e8668945d2a20`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6df7195f7b6c83e938c25f1940930649b862e2b5369ec6e041631c4cb1ebef`  
		Last Modified: Thu, 09 May 2019 05:17:27 GMT  
		Size: 9.4 MB (9424383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef61c6677aef99352724f560861db552edff24e57f288598be141e49f0802c8`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16572dc3fb4702653a0252ed5b29eb536479f0085f7ec2596c9d1c2e8214fd2f`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0aa75b063a662a0cd7f4af7b720863dfa8c7643b98bfc4b8ee5124a1bb069e`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ce48b6bff7dbea769d046b7311e98e7ea33aec40dca23a246a4b2c1fe530c5`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `jetty:jdk13`

**does not exist** (yet?)

## `jetty:latest`

```console
$ docker pull jetty@sha256:d8f374b030b7e0af3d422887dafefa75ef9fe1b4de36f3e4e1a806de59fbbeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `jetty:latest` - linux; amd64

```console
$ docker pull jetty@sha256:c2f362b5654ae4e16cd96f410c479e3b0cac574607a32c13501dd922e0a20ad5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115270945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7cfb40b7f4b3aaab1f50c4ca270acd53caf6cf9c2c04e332eedd72bc3006c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 08:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:55:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 Dec 2019 08:56:57 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_VERSION=8u232
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u232-b09/OpenJDK8U-jre_
# Sat, 28 Dec 2019 08:56:58 GMT
ENV JAVA_URL_VERSION=8u232b09
# Sat, 28 Dec 2019 08:57:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sun, 29 Dec 2019 08:31:21 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Sun, 29 Dec 2019 08:31:21 GMT
ENV JETTY_HOME=/usr/local/jetty
# Sun, 29 Dec 2019 08:31:22 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2019 08:31:22 GMT
RUN mkdir -p "$JETTY_HOME"
# Sun, 29 Dec 2019 08:31:23 GMT
WORKDIR /usr/local/jetty
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Sun, 29 Dec 2019 08:31:23 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Sun, 29 Dec 2019 08:31:27 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:27 GMT
ENV JETTY_BASE=/var/lib/jetty
# Sun, 29 Dec 2019 08:31:28 GMT
RUN mkdir -p "$JETTY_BASE"
# Sun, 29 Dec 2019 08:31:28 GMT
WORKDIR /var/lib/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Sun, 29 Dec 2019 08:31:30 GMT
ENV TMPDIR=/tmp/jetty
# Sun, 29 Dec 2019 08:31:30 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Sun, 29 Dec 2019 08:31:31 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Sun, 29 Dec 2019 08:31:31 GMT
USER jetty
# Sun, 29 Dec 2019 08:31:31 GMT
EXPOSE 8080
# Sun, 29 Dec 2019 08:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 Dec 2019 08:31:31 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8d3cd13de4f1c574d86de1c90b7e0f96d2394349c7e882117daaa86ad08ad`  
		Last Modified: Sat, 28 Dec 2019 09:02:34 GMT  
		Size: 5.1 MB (5126129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06bdc5e0db3a85fca16aae57afb18ced9fad56ed4571f9bd0d748f38930b22`  
		Last Modified: Sat, 28 Dec 2019 09:03:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b1f94cfe4ae6c7ca9e45cc45491b7f732d099001d933ac72211dbd09d19e0d`  
		Last Modified: Sat, 28 Dec 2019 09:03:45 GMT  
		Size: 40.2 MB (40196546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe20b880320d8f58a256fe49d1c7c23c61b64baa639ad7279118a09e05b99b2b`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b913b52ac10d2aec4b74f5b78af565b0c0b25888a4c4826a1301239a847aab`  
		Last Modified: Sun, 29 Dec 2019 08:32:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95861d4f30fde9cf21c8c2cb828a68434818251a138bdbdd7d275ca2e78987a`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 9.4 MB (9424429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecc3b45eaba005a5e755b9d4186273b7300646c4a3392159aab8b7ddd4f8d6`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46a5d5760312fac8ac9744158c27194bc30d047cb09045715eb95886f0376e9`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b95bd8335f7360f38bfa50b47f5a83975722151ddc1cc65f78dbd7775f1e568`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5526a96dfe33daca789ac452c1286664ab7610d5447d2089cdd69f93c0bd3bd1`  
		Last Modified: Sun, 29 Dec 2019 08:32:30 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:latest` - linux; arm variant v5

```console
$ docker pull jetty@sha256:6b79ec2ccfa3ee643017cecbdeee7565e32a4b74912ab39d95bbb17a1d1f7700
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180287052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965e56aa7b329cf860c5d90d360d6f490b43bfdb9ec51dfb7235b27e1cabbcbb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:53:17 GMT
ADD file:5dfe3b771bd67a2856913544993e219cb8c7933c33523cc56fe13a3a0e76ce9b in / 
# Wed, 08 May 2019 08:53:18 GMT
CMD ["bash"]
# Wed, 08 May 2019 10:01:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 10:01:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 11:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:35:27 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 11:35:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 11:35:30 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 11:35:31 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 11:36:37 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 16:15:13 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 16:15:13 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 16:15:14 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 16:15:16 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 16:15:16 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 16:15:17 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 16:15:18 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 16:15:24 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:25 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 16:15:27 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 16:15:27 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 16:15:32 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 16:15:32 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 16:15:35 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 16:15:36 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 16:15:37 GMT
USER jetty
# Wed, 08 May 2019 16:15:37 GMT
EXPOSE 8080
# Wed, 08 May 2019 16:15:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 16:15:38 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:ca892ced475bf1c51c1f13b76a64549cfc5d1a0b55d33d8b9418efbb47887bf8`  
		Last Modified: Wed, 08 May 2019 08:59:09 GMT  
		Size: 44.0 MB (44045778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7b30b379469b50f6ada866964876f5c4ba164c22896bf3a08aabab61869e51`  
		Last Modified: Wed, 08 May 2019 10:09:26 GMT  
		Size: 9.9 MB (9854225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e257762b4747840fc09dce269e7f68146ac9864b8bf218e57475b4af367a74`  
		Last Modified: Wed, 08 May 2019 10:09:24 GMT  
		Size: 4.2 MB (4159009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0d161136f55f6e5c26bbd9fde30327cf06dec15e40d7ac330b8db368e4b9ee`  
		Last Modified: Wed, 08 May 2019 11:50:21 GMT  
		Size: 846.1 KB (846058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a59da16addae7a15d26d4edba174883fd994d29bb943085361990730c6787`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d14b7a612bfb82f68156f623a22e64ab4524cbf82c592f9365a904bac033a5`  
		Last Modified: Wed, 08 May 2019 11:52:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e798df308d1bafc2c22d22386cb75aa71c9b8fc3c7b9ff5e736c1464c83bea`  
		Last Modified: Wed, 08 May 2019 11:53:24 GMT  
		Size: 112.0 MB (111951438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5962f9d6fd65875c9975a6db12ff0c916944d89184389e3ae3272c6d5690381`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085503a369edcce69a9e4e547a07f501228a3e71b00141b07bf7e4bf3beb4cf2`  
		Last Modified: Wed, 08 May 2019 16:17:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5110522604cdddba047cc0be366f16edb6238a77df6c0b690e81f538401402c6`  
		Last Modified: Wed, 08 May 2019 16:17:30 GMT  
		Size: 9.4 MB (9424456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dc9134cb78fa8c8012494e966655a51906b8fbb9a287ff677f112cb6df5b7b`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1cc6aa008e3c92d0e543846f48ffc0278671ad3336e433360f2bbab577e4b7`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 2.1 KB (2066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62368ad6255191b9e3dafc29336216dd0f25b1acacf11eacdfa4a0a9d95b2f5c`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c246600f5484d9d71da31a270a9f1543cf79da2bf94a224314c659b9a66a875e`  
		Last Modified: Wed, 08 May 2019 16:17:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:latest` - linux; arm variant v7

```console
$ docker pull jetty@sha256:9f4c641dc0a44707812e694e8eade3015b6c059b468a4e688634a3c20ed24d0c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176059054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea2dba1b53efa6f56de5449b6625a4945aaa26e65463ca0f2ae298f2ad8ab22`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 12:03:26 GMT
ADD file:7e8dcc40e246d53b86266855a2de8080d26e6b4ed9f594c1acc565784405735b in / 
# Wed, 08 May 2019 12:03:27 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:04:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:14:59 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:15:01 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:15:02 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:15:03 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:16:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 17:55:00 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 17:55:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 17:55:03 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 17:55:03 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 17:55:03 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 17:55:04 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 17:55:10 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:10 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 17:55:12 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 17:55:12 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 17:55:14 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 17:55:15 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 17:55:16 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 17:55:17 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 17:55:18 GMT
USER jetty
# Wed, 08 May 2019 17:55:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 17:55:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 17:55:19 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f2a2fd7c1ab35cd1b5ea6fcc2b801f3877852797e2698ecdb9556e0dee3accb5`  
		Last Modified: Wed, 08 May 2019 12:09:40 GMT  
		Size: 42.1 MB (42082604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047df9a92c9f7376283a8d6af526f5126d95995ba48dd7de49979ef57da3e15b`  
		Last Modified: Wed, 08 May 2019 13:12:20 GMT  
		Size: 9.5 MB (9485167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeed4ac8d1e2c751afd6fd3517f1d154365467039353c377c8206fd5eb81d4b`  
		Last Modified: Wed, 08 May 2019 13:12:18 GMT  
		Size: 3.9 MB (3918605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646a29b8c83d854b86dccdbf390a7b296f5144aef4e38276c8a7b649e0804`  
		Last Modified: Wed, 08 May 2019 14:31:13 GMT  
		Size: 830.4 KB (830410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb3a067c54308aa02398bf021c38a952c18f27646b736d71732cbbc9b1010b0`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2c033d6c592b7d46aafecc714f1393be324b57f01f5e6c76e832e8ea04576a`  
		Last Modified: Wed, 08 May 2019 14:33:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0d9e8d93d276090a71cd6c8346c468c9e051903bf52760756359c4451d33b`  
		Last Modified: Wed, 08 May 2019 14:34:14 GMT  
		Size: 110.3 MB (110311680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2f07a446b7fe57fd236711da5953265e8d532d43c9cb8f25a533320e93a636`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6395f8d7de3564b4ae1e386bf6ed4e0f7723e94d4940a70b485a86504a75926`  
		Last Modified: Wed, 08 May 2019 17:57:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc147ed50354f0d2a7587b28055ead9eec49df4f8eb5341d91e746671a6890d9`  
		Last Modified: Wed, 08 May 2019 17:57:20 GMT  
		Size: 9.4 MB (9424492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c93706301b9ef0c48c932aa219a1caa545887de6b3900e134bce06740648f8b`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d03e292fef5d40aada56fd958955f649c1637f1247f0ce20ccbe82940b6ccfd`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 2.1 KB (2069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f2350cc0ff9abae232377501904cbd64860bdbd5db9ef7c24bce5508cf073c`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d04c42b72f7e6024f6fdb7413c30b11da394d870eaa464bda596aa3e99142fc`  
		Last Modified: Wed, 08 May 2019 17:57:16 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:latest` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:2fbb5ca36da5cad300aa58956606b38a8e3f3cecbb41851cdfd0c8696482575e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180322238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2bb61e7225a1b482f1f4664ddfbefa8060a5b43bc65fcd64f9680a51dc4749`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 08:48:25 GMT
ADD file:153045f4fe6532d8c2ff273bb249a7a3a4cba913c26a4103ba5ddce1af02c1e5 in / 
# Wed, 08 May 2019 08:48:26 GMT
CMD ["bash"]
# Wed, 08 May 2019 11:51:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 11:51:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 17 May 2019 22:46:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 17 May 2019 22:50:40 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2019 22:50:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 17 May 2019 22:50:42 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_VERSION=8u212
# Fri, 17 May 2019 22:50:43 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Fri, 17 May 2019 22:51:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 17 Jul 2019 23:35:39 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 17 Jul 2019 23:35:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2019 23:35:41 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 17 Jul 2019 23:35:41 GMT
WORKDIR /usr/local/jetty
# Wed, 17 Jul 2019 23:35:41 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 17 Jul 2019 23:35:42 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 17 Jul 2019 23:35:47 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:47 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 17 Jul 2019 23:35:49 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 17 Jul 2019 23:35:49 GMT
WORKDIR /var/lib/jetty
# Wed, 17 Jul 2019 23:35:51 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 17 Jul 2019 23:35:52 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 17 Jul 2019 23:35:53 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 17 Jul 2019 23:35:53 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 17 Jul 2019 23:35:54 GMT
USER jetty
# Wed, 17 Jul 2019 23:35:54 GMT
EXPOSE 8080
# Wed, 17 Jul 2019 23:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jul 2019 23:35:55 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:5894e28291972e44f5c3eba2779a85979bae6f95ed4f3e43ea5c98a132f06c48`  
		Last Modified: Wed, 08 May 2019 08:54:43 GMT  
		Size: 43.1 MB (43141955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e6888cee6fef7c223eeaf2ca4c51bc0c21b4631971f416eb6a529a05e96cb`  
		Last Modified: Wed, 08 May 2019 12:07:05 GMT  
		Size: 9.7 MB (9733078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf90e854779f4c5edab378626d847fd0ab7aa9441b63a7db31a7db55d2b255b`  
		Last Modified: Wed, 08 May 2019 12:07:03 GMT  
		Size: 4.1 MB (4094187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc920c054370e9fe777d4546e8898e94588c01909d487696f8378c34d00b67e`  
		Last Modified: Fri, 17 May 2019 22:56:09 GMT  
		Size: 839.6 KB (839611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf483f25e9254d4337fac759851db8d04b5a2eea6056b1375ff19c2df554464`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a594c16f5b8360bf6256529e6a21eddf648595ac48000e0d91808fd21a9798`  
		Last Modified: Fri, 17 May 2019 22:59:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9e1dac91c466b57c47d5738767104f91af563b89a969f98a2eff0d0692cd6`  
		Last Modified: Fri, 17 May 2019 23:00:18 GMT  
		Size: 113.1 MB (113082862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7e6b7fd0cb47998762442e0d2b1852c2692786149020092d36d17cbaddad32`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511814053ebc4a22abd8857c39836a2c1b6b9ee89da025924601e08bfb12412c`  
		Last Modified: Wed, 17 Jul 2019 23:37:42 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0bf7b138eb0319a3d75d1ab842fb65cd204e1c83dd7e92e2a0fb122cb2403d`  
		Last Modified: Wed, 17 Jul 2019 23:37:43 GMT  
		Size: 9.4 MB (9424451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588601cf5b3de57b436e290ae8115f8bd4cd5553d0a88a42e233f763d21441b0`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2670e29c10dc3bc2f5c75c700e415015925039c9b4751a8920fdaebbb4f1c2e`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a627374a49fddcb68bd3f2ce734e8fbd58f7c745c55ac425411ca144d003de8`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b7659478cc7567aa9d6d6a3700403d10e80bf5542bc7846c6fc05f366f870`  
		Last Modified: Wed, 17 Jul 2019 23:37:41 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:latest` - linux; 386

```console
$ docker pull jetty@sha256:f532a68e9bbf79732ee7dbfaa205e1b742f0c2fefb7e19ba5c0d6d1491cbba08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194362543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd22310a1a4ac81a7cd7b96c967f835781080ad5f817dd7161256eb8ae0207e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 10:49:19 GMT
ADD file:fde8cf5700c66c38b88d4b3254ec1544d09194e06568c23fe3989f7eaa1f5785 in / 
# Wed, 08 May 2019 10:49:20 GMT
CMD ["bash"]
# Wed, 08 May 2019 19:08:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 19:08:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 22:13:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 22:16:13 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 22:16:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 22:16:15 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 22:16:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 04:57:10 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 04:57:10 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 04:57:11 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 04:57:11 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 04:57:12 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 04:57:16 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:16 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 04:57:17 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 04:57:17 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 04:57:19 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 04:57:19 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 04:57:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 04:57:20 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 04:57:20 GMT
USER jetty
# Thu, 09 May 2019 04:57:20 GMT
EXPOSE 8080
# Thu, 09 May 2019 04:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 04:57:21 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:b5d586ad7adeab23f6ff0b7ec90785dc757eaccd445976fda3f6d7db64d20585`  
		Last Modified: Wed, 08 May 2019 10:57:26 GMT  
		Size: 46.1 MB (46063371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b18ff57de8d55737be40848138cbd66efcc99443ae507217ae5dd45e3cf41a`  
		Last Modified: Wed, 08 May 2019 19:14:07 GMT  
		Size: 10.8 MB (10802110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc701b379559241c696cd079ff9b83f0bba19faec8747d75654fe5bc7e8adb03`  
		Last Modified: Wed, 08 May 2019 19:14:05 GMT  
		Size: 4.6 MB (4561353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad72e88a4544f4570c0df9df66b43ca05325a8df5fe4bdac5e0240836f47d28`  
		Last Modified: Wed, 08 May 2019 22:48:29 GMT  
		Size: 862.0 KB (862001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215fde6b1eafb43012d68d65388471bca2066ad401d508df13b046aa8b830e1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf128bb9e196d3a692d14dc4ed9c91920ab3ecb3fcb3d7e4c968fb1f18b9ce1`  
		Last Modified: Wed, 08 May 2019 22:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47742760e75d51e74c18576e2a0b2d447e91b2c3a023dc9e3b1e4a83aa7bdc1a`  
		Last Modified: Wed, 08 May 2019 22:52:46 GMT  
		Size: 122.6 MB (122643377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13df399b06606cedbc7ffce659af330dab9041dfebd5d98933853a74a0be48d3`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d50318d694cf0cf2727460d2057498228249819a1d83c2f92296c96dbfb1e`  
		Last Modified: Thu, 09 May 2019 04:58:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad229b08fbaea588098dc7e42976c29d5b7a16be0e2a84b3ba0d811c5d724494`  
		Last Modified: Thu, 09 May 2019 04:58:53 GMT  
		Size: 9.4 MB (9424415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7161f78a4fe1f1d0ee6787a7f6f28b0a0241c7390a5c919ee688aac0caf3fef`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4163317071202eac58e9e3c5ec95d8b071ae013148d4f1376fdc09a340c7ed6b`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4d72a3ad59ec8fada471aa84164b581dd500aea022f038334b0eda00c0ec19`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7621b6c4a7959d913a05ce51aa49a199c616badaaa439ea6873fe8c5a9b89ee`  
		Last Modified: Thu, 09 May 2019 04:58:47 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:latest` - linux; ppc64le

```console
$ docker pull jetty@sha256:1c8d35096fdcfc3c448b203db5c12734655105f9f779d3734522511764e58233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184781497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eacbfac25da6c191d70cca800f7ed9b015a19adef7c4ab701c0b31540a6159e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 09:03:26 GMT
ADD file:844cea0aa071f0f6b2640d4c452590a8777485fa27a0aad789553110eaeb7081 in / 
# Wed, 08 May 2019 09:03:33 GMT
CMD ["bash"]
# Wed, 08 May 2019 12:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:07:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 12:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 12:57:43 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 12:57:49 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 12:57:56 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 12:57:59 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 12:58:03 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 12:58:05 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 13:05:08 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 08 May 2019 21:43:25 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 08 May 2019 21:43:27 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 08 May 2019 21:43:30 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 May 2019 21:43:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 08 May 2019 21:43:51 GMT
WORKDIR /usr/local/jetty
# Wed, 08 May 2019 21:43:57 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Wed, 08 May 2019 21:44:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Wed, 08 May 2019 21:44:06 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Wed, 08 May 2019 21:44:22 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:44:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 08 May 2019 21:44:33 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 08 May 2019 21:44:40 GMT
WORKDIR /var/lib/jetty
# Wed, 08 May 2019 21:44:57 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 08 May 2019 21:45:03 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 08 May 2019 21:45:10 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 08 May 2019 21:45:11 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Wed, 08 May 2019 21:45:13 GMT
USER jetty
# Wed, 08 May 2019 21:45:18 GMT
EXPOSE 8080
# Wed, 08 May 2019 21:45:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 May 2019 21:45:22 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c6c4df30bc4ffa8fb97a3dda6f8758fb0ddeb8929d159369cf5974dd3f2ac117`  
		Last Modified: Wed, 08 May 2019 09:21:32 GMT  
		Size: 45.6 MB (45603184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b6d64c78121ab5074c55b90272e1a13e72e3b7854d6a6c7e638eff77307ba`  
		Last Modified: Wed, 08 May 2019 12:24:57 GMT  
		Size: 10.0 MB (9991084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663d68dc2e1243453bf4b04afcb5394452ca5371b05a1c96f41a0df4189631e8`  
		Last Modified: Wed, 08 May 2019 12:24:54 GMT  
		Size: 4.3 MB (4296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e4e060b9a0f1aadc5647d44be482b1363697a3fd8a4aeb6a4b9c53e17ecc4`  
		Last Modified: Wed, 08 May 2019 13:14:21 GMT  
		Size: 848.6 KB (848616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e24f3bccdd6d1d666b5c75ba2971c3c1d1b974352776ac0c8d91b0244f35cb`  
		Last Modified: Wed, 08 May 2019 13:20:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f7a6e570eaf9c696f99b09d6fb9eaf034d87e7a1e9bf092cd38e9f71777a8b`  
		Last Modified: Wed, 08 May 2019 13:20:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5a3232b209a6e8e5f133bb2d4b9c377dab2d71b8b57de44e32eefb5584bfd2`  
		Last Modified: Wed, 08 May 2019 13:21:49 GMT  
		Size: 114.6 MB (114611463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321ac118136d891526d4b7d585903133a760850fd8ba7b73f5608b51d289a8a`  
		Last Modified: Wed, 08 May 2019 21:50:41 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86141b28655e4b923da175ff032f463f8ef7bf16d23578dd00d25badfdce9b79`  
		Last Modified: Wed, 08 May 2019 21:50:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0e68a17da043f652f2d812d9c650558c382a9c2be40bb8fd901e19d89cb162`  
		Last Modified: Wed, 08 May 2019 21:50:38 GMT  
		Size: 9.4 MB (9424473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec696722258c05e106b7c921898aac4da7e2ab6ae65076942a12749f1049140b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cae7017c7325beea0f896b47ae71aa44260cac66b36379a32dbb0ed9309eaf`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 2.1 KB (2062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8302b92229dab552b306d2b48fba615a169e28af57e2c7fae6324ef3b4b028`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffadd387f05feedbcf33516453c4c46c64a80261af3ff1e6ebf007ccac52a95b`  
		Last Modified: Wed, 08 May 2019 21:50:37 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:latest` - linux; s390x

```console
$ docker pull jetty@sha256:eb8f97a23898ccdc5be026ea051ef231615b9455a4d78a72cbeb093439440cf5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184363097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55031fcaf6fba1a2c7256bad7bbcc09b11b036dbceb1807ceeacc9202792f231`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 08 May 2019 11:46:30 GMT
ADD file:35b243252442c1fc6a9e4f7bea498f5b7302c530eb804ed6a79c5b84a68a96fd in / 
# Wed, 08 May 2019 11:46:31 GMT
CMD ["bash"]
# Wed, 08 May 2019 13:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 13:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 08 May 2019 14:42:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 08 May 2019 14:52:21 GMT
ENV LANG=C.UTF-8
# Wed, 08 May 2019 14:52:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 08 May 2019 14:52:32 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 08 May 2019 14:52:35 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_VERSION=8u212
# Wed, 08 May 2019 14:52:36 GMT
ENV JAVA_DEBIAN_VERSION=8u212-b01-1~deb9u1
# Wed, 08 May 2019 14:54:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y --no-install-recommends 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 09 May 2019 05:12:37 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 09 May 2019 05:12:38 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2019 05:12:42 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 09 May 2019 05:12:42 GMT
WORKDIR /usr/local/jetty
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_VERSION=9.4.18.v20190429
# Thu, 09 May 2019 05:12:44 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.18.v20190429/jetty-home-9.4.18.v20190429.tar.gz
# Thu, 09 May 2019 05:12:46 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 09 May 2019 05:12:59 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:00 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 09 May 2019 05:13:05 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 09 May 2019 05:13:06 GMT
WORKDIR /var/lib/jetty
# Thu, 09 May 2019 05:13:16 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 09 May 2019 05:13:16 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 09 May 2019 05:13:20 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 09 May 2019 05:13:21 GMT
COPY multi:87587db67954487ef9f6dc57fa1fcab90f0134d7aa6d2af7a98d1b98a6047a64 in / 
# Thu, 09 May 2019 05:13:22 GMT
USER jetty
# Thu, 09 May 2019 05:13:23 GMT
EXPOSE 8080
# Thu, 09 May 2019 05:13:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 09 May 2019 05:13:24 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:3602dd773e45048fcb10569c368bf7ddac54267760f371efbe1bb65ba8d67361`  
		Last Modified: Wed, 08 May 2019 11:52:15 GMT  
		Size: 45.2 MB (45197648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412a17b553a57c91ed490be0279a1aafa108b9a60b10f8c482ed85ca94de3a3c`  
		Last Modified: Wed, 08 May 2019 14:00:34 GMT  
		Size: 10.3 MB (10314565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007dca2cc2afa05648742b75324a09e45eae504d384750ed7c6de3e5e5d65d2`  
		Last Modified: Wed, 08 May 2019 14:00:30 GMT  
		Size: 4.4 MB (4372280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf61465b03d8ec5e8064ba91220d0e97c4dd5b75a7d2fe644aab7cc4a0a514c`  
		Last Modified: Wed, 08 May 2019 15:01:34 GMT  
		Size: 863.9 KB (863943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35375a807e76af07efe2bf1c77fce29498511166f4b41f158e181805528ce229`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53975ff11a25b69ce30d4b02d88f1b27cff3e5b1a2e08d05f6721e388f4a5d`  
		Last Modified: Wed, 08 May 2019 15:04:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d381e46be773491220b0199e519c4f97308fee82af49481321e3d769db7b7b0a`  
		Last Modified: Wed, 08 May 2019 15:05:36 GMT  
		Size: 114.2 MB (114184348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e456897b935f1efded84a648055389e6c4fffbee3a50167ab95bf7cf047142`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace4f725dd5f318c30a864c4400d34b9d1dfeb8dba95f242af7e8668945d2a20`  
		Last Modified: Thu, 09 May 2019 05:17:26 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6df7195f7b6c83e938c25f1940930649b862e2b5369ec6e041631c4cb1ebef`  
		Last Modified: Thu, 09 May 2019 05:17:27 GMT  
		Size: 9.4 MB (9424383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef61c6677aef99352724f560861db552edff24e57f288598be141e49f0802c8`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16572dc3fb4702653a0252ed5b29eb536479f0085f7ec2596c9d1c2e8214fd2f`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0aa75b063a662a0cd7f4af7b720863dfa8c7643b98bfc4b8ee5124a1bb069e`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ce48b6bff7dbea769d046b7311e98e7ea33aec40dca23a246a4b2c1fe530c5`  
		Last Modified: Thu, 09 May 2019 05:17:24 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
