<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:2.0`](#orientdb20)
-	[`orientdb:2.0.18`](#orientdb2018)
-	[`orientdb:2.1`](#orientdb21)
-	[`orientdb:2.1.25`](#orientdb2125)
-	[`orientdb:2.2`](#orientdb22)
-	[`orientdb:2.2.37`](#orientdb2237)
-	[`orientdb:2.2.37-spatial`](#orientdb2237-spatial)
-	[`orientdb:3.0`](#orientdb30)
-	[`orientdb:3.0-tp3`](#orientdb30-tp3)
-	[`orientdb:3.0.42`](#orientdb3042)
-	[`orientdb:3.0.42-tp3`](#orientdb3042-tp3)
-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.15`](#orientdb3115)
-	[`orientdb:3.1.15-tp3`](#orientdb3115-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.4`](#orientdb324)
-	[`orientdb:3.2.4-tp3`](#orientdb324-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.0`

```console
$ docker pull orientdb@sha256:c422a7f708f8342977f0e0257c63e4b94d2f89ec7a9ae1caa88511541b3e2948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.0` - linux; amd64

```console
$ docker pull orientdb@sha256:3b00bf30ed1488fd840b4108063eaac1510f8b39418e68266afcabffac5f9bdd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283588217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a84fc9450d519795066958a851e52667b41e5bbf6afa6375e9f24b56fa83e2`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:46:19 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:46:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:54:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:54:16 GMT
ENV ORIENTDB_VERSION=2.0.18
# Thu, 03 Feb 2022 23:54:17 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Thu, 03 Feb 2022 23:54:17 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Thu, 03 Feb 2022 23:54:21 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:54:21 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:54:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:54:22 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:54:22 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:54:22 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:54:22 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed70148ebcf78cba8546f5af3e152a6d9422a3a9d814d7683242e4663e773c3`  
		Last Modified: Thu, 03 Feb 2022 21:02:59 GMT  
		Size: 106.1 MB (106072294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42bec70278c98aa00d947f7ec7bc85fb5d8eb93955fae303f1c2d40efc89146`  
		Last Modified: Thu, 03 Feb 2022 23:56:46 GMT  
		Size: 46.6 MB (46586574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.0.18`

```console
$ docker pull orientdb@sha256:c422a7f708f8342977f0e0257c63e4b94d2f89ec7a9ae1caa88511541b3e2948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.0.18` - linux; amd64

```console
$ docker pull orientdb@sha256:3b00bf30ed1488fd840b4108063eaac1510f8b39418e68266afcabffac5f9bdd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283588217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a84fc9450d519795066958a851e52667b41e5bbf6afa6375e9f24b56fa83e2`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:29:50 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:29:50 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:29:50 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:46:19 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:46:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:54:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:54:16 GMT
ENV ORIENTDB_VERSION=2.0.18
# Thu, 03 Feb 2022 23:54:17 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Thu, 03 Feb 2022 23:54:17 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Thu, 03 Feb 2022 23:54:21 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:54:21 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:54:21 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:54:22 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:54:22 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:54:22 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:54:22 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442ee9d8dd9896a5b3b67117060f2af4ae8e997af7297009e7d0ea4b6595163`  
		Last Modified: Wed, 26 Jan 2022 09:50:58 GMT  
		Size: 5.4 MB (5420014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5bcea956cbbcc7e16356354d5eb4b5b3834a43d708ca6c3fd048f33ddc579`  
		Last Modified: Wed, 26 Jan 2022 09:55:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed70148ebcf78cba8546f5af3e152a6d9422a3a9d814d7683242e4663e773c3`  
		Last Modified: Thu, 03 Feb 2022 21:02:59 GMT  
		Size: 106.1 MB (106072294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42bec70278c98aa00d947f7ec7bc85fb5d8eb93955fae303f1c2d40efc89146`  
		Last Modified: Thu, 03 Feb 2022 23:56:46 GMT  
		Size: 46.6 MB (46586574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.1`

```console
$ docker pull orientdb@sha256:e53b301790002d632150c0c08f56b080a6f47fdc300bcfc718ae640d2c61cdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.1` - linux; amd64

```console
$ docker pull orientdb@sha256:d37dd3c86e69ec234700f9d41612c4e6e99dcec2fae95dff8a1e2690deac771e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172486248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4abcb4afe8b4aa17f3e3fb622862f352cdf4514fe2cd6ce33e27b8b1e52d074`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:54:03 GMT
ENV ORIENTDB_VERSION=2.1.25
# Thu, 03 Feb 2022 23:54:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=054da3fb7c56e7822b2af116966576ce
# Thu, 03 Feb 2022 23:54:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=b7b08242b40117ac8eb9a201f8704bde839dfcb8
# Thu, 03 Feb 2022 23:54:08 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:54:11 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:54:12 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:54:12 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:54:12 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:54:12 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:54:13 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:54:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2ef651542702ea23afabcfcb53fdd53b08479b2c4507a8b93c5d9d8a116a05`  
		Last Modified: Thu, 03 Feb 2022 23:56:32 GMT  
		Size: 2.1 MB (2105541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f346221e491c0e5eead4b29d6ecc585d0b91610c26a9ff6b97424e6932e16`  
		Last Modified: Thu, 03 Feb 2022 23:56:34 GMT  
		Size: 31.1 MB (31087987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.1.25`

```console
$ docker pull orientdb@sha256:e53b301790002d632150c0c08f56b080a6f47fdc300bcfc718ae640d2c61cdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.1.25` - linux; amd64

```console
$ docker pull orientdb@sha256:d37dd3c86e69ec234700f9d41612c4e6e99dcec2fae95dff8a1e2690deac771e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172486248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4abcb4afe8b4aa17f3e3fb622862f352cdf4514fe2cd6ce33e27b8b1e52d074`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:54:03 GMT
ENV ORIENTDB_VERSION=2.1.25
# Thu, 03 Feb 2022 23:54:03 GMT
ENV ORIENTDB_DOWNLOAD_MD5=054da3fb7c56e7822b2af116966576ce
# Thu, 03 Feb 2022 23:54:03 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=b7b08242b40117ac8eb9a201f8704bde839dfcb8
# Thu, 03 Feb 2022 23:54:08 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:54:11 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:54:12 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:54:12 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:54:12 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:54:12 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:54:13 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:54:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2ef651542702ea23afabcfcb53fdd53b08479b2c4507a8b93c5d9d8a116a05`  
		Last Modified: Thu, 03 Feb 2022 23:56:32 GMT  
		Size: 2.1 MB (2105541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442f346221e491c0e5eead4b29d6ecc585d0b91610c26a9ff6b97424e6932e16`  
		Last Modified: Thu, 03 Feb 2022 23:56:34 GMT  
		Size: 31.1 MB (31087987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2`

```console
$ docker pull orientdb@sha256:c037d79b8479dd3d5320e0a30397379f53abd981013569876ff07490ae6862be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2` - linux; amd64

```console
$ docker pull orientdb@sha256:b69754efc7822f296af1e14f08ff5bb8581a40ff08f940a71b1efabc5f67841c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187872170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3592278af774788bf19cded645dd2d0d31f046f00ad18962a29eaf8b6e9d634c`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_VERSION=2.2.37
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Thu, 03 Feb 2022 23:53:50 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:53:53 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:53:53 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:53:54 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:53:54 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:53:54 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:53:54 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:53:55 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f55d2e93499bed5426ba2a74849c214bebe1ef3e6a9798e8281f01608e9255`  
		Last Modified: Thu, 03 Feb 2022 23:56:13 GMT  
		Size: 2.1 MB (2105551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0c83412ff7c22d9fead1dc3bd55d93b2b9c62fed7df1e49192b13c2a3fe006`  
		Last Modified: Thu, 03 Feb 2022 23:56:16 GMT  
		Size: 46.5 MB (46473899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37`

```console
$ docker pull orientdb@sha256:c037d79b8479dd3d5320e0a30397379f53abd981013569876ff07490ae6862be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37` - linux; amd64

```console
$ docker pull orientdb@sha256:b69754efc7822f296af1e14f08ff5bb8581a40ff08f940a71b1efabc5f67841c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187872170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3592278af774788bf19cded645dd2d0d31f046f00ad18962a29eaf8b6e9d634c`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_VERSION=2.2.37
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Thu, 03 Feb 2022 23:53:50 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:53:53 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:53:53 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:53:54 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:53:54 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:53:54 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:53:54 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:53:55 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f55d2e93499bed5426ba2a74849c214bebe1ef3e6a9798e8281f01608e9255`  
		Last Modified: Thu, 03 Feb 2022 23:56:13 GMT  
		Size: 2.1 MB (2105551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0c83412ff7c22d9fead1dc3bd55d93b2b9c62fed7df1e49192b13c2a3fe006`  
		Last Modified: Thu, 03 Feb 2022 23:56:16 GMT  
		Size: 46.5 MB (46473899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37-spatial`

```console
$ docker pull orientdb@sha256:d64d0fe74d02294161febae836b8d1a07d8470e792668f37930f072ea8d6f1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37-spatial` - linux; amd64

```console
$ docker pull orientdb@sha256:9ad3384dffd7e63d832cf93d49df1f6fd59c04f920a547bc55248d777061e89d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189074765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70beefb4d817b7aa7225166838d3664b8f506ac1c4cea7c6cf8e6f9070cdae60`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_VERSION=2.2.37
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Thu, 03 Feb 2022 23:53:45 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Thu, 03 Feb 2022 23:53:50 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:53:53 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:53:53 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:53:54 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:53:54 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:53:54 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:53:54 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:53:55 GMT
CMD ["server.sh"]
# Thu, 03 Feb 2022 23:53:58 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_MD5=9f64ab5e959f5d9ad9ea5195d6d621d2
# Thu, 03 Feb 2022 23:53:59 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_SHA1=1748c9779ea7a8cb8fc068fcabf960e1778e8a19
# Thu, 03 Feb 2022 23:53:59 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-spatial/2.2.37/orientdb-spatial-2.2.37-dist.jar
# Thu, 03 Feb 2022 23:54:00 GMT
RUN wget $ORIENTDB_DOWNLOAD_SPATIAL_URL     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_MD5 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | md5sum -c -     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_SHA1 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | sha1sum -c -     && mv orientdb-spatial-*-dist.jar /orientdb/lib/
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f55d2e93499bed5426ba2a74849c214bebe1ef3e6a9798e8281f01608e9255`  
		Last Modified: Thu, 03 Feb 2022 23:56:13 GMT  
		Size: 2.1 MB (2105551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0c83412ff7c22d9fead1dc3bd55d93b2b9c62fed7df1e49192b13c2a3fe006`  
		Last Modified: Thu, 03 Feb 2022 23:56:16 GMT  
		Size: 46.5 MB (46473899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8415e5bff4edfe7c7560adfc1afb631f9aff42c0b3e99e0472453eaf6e608e65`  
		Last Modified: Thu, 03 Feb 2022 23:56:25 GMT  
		Size: 1.2 MB (1202595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0`

```console
$ docker pull orientdb@sha256:90cfee1881ef0f8583bdd6d12ecf37183ea7e7c64a3b397831ac3113394983e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0` - linux; amd64

```console
$ docker pull orientdb@sha256:c067f72467e31b73ea64c64bca2aa7e09ba9e4460e690be68fdc727859259067
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178466866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8bbe18b287c850428e36403fa1fb7874e9912ba048ea13c7910e920d9fd98f`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:53:15 GMT
ENV ORIENTDB_VERSION=3.0.42
# Thu, 03 Feb 2022 23:53:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59ed522290668fb400e67503652bb813
# Thu, 03 Feb 2022 23:53:15 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=fe6a510c72983b32a3ffd657be9ae62fab2b61f8
# Thu, 03 Feb 2022 23:53:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.42/orientdb-community-3.0.42.tar.gz
# Thu, 03 Feb 2022 23:53:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:53:24 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:53:24 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:53:24 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:53:25 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:53:25 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:53:25 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:53:25 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2591104e6b210de60c05b2a586b249333d1c9982fe4c5077da9667556778dca`  
		Last Modified: Thu, 03 Feb 2022 23:55:48 GMT  
		Size: 2.1 MB (2105595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a95605ca387cb36a005301c089e4f186d1c9cfc5483eecd01c12ad26c30175`  
		Last Modified: Thu, 03 Feb 2022 23:55:50 GMT  
		Size: 37.1 MB (37068551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0-tp3`

```console
$ docker pull orientdb@sha256:d0bb977074c947913ae364a0f3496a673856e87d9ff4fa4b7b9138cc6c19cc33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:df5ddd29eaf9a8d0931ed81357e1ebdaa3652b939da62049b0ed89530f568ce4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205487600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ba49ec9b3fe1efcc7c620e83d711ceffb37789b49152d73b069a91da205b07`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:53:15 GMT
ENV ORIENTDB_VERSION=3.0.42
# Thu, 03 Feb 2022 23:53:28 GMT
ENV ORIENTDB_DOWNLOAD_MD5=20104f313e82db3a2bd88b7501d596aa
# Thu, 03 Feb 2022 23:53:29 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1abc7a4979ca561d13edd01b1d18b3b869abace9
# Thu, 03 Feb 2022 23:53:29 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.42/orientdb-tp3-3.0.42.tar.gz
# Thu, 03 Feb 2022 23:53:34 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:53:38 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:53:39 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 03 Feb 2022 23:53:39 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:53:39 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:53:39 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:53:40 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:53:40 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:53:40 GMT
EXPOSE 8182
# Thu, 03 Feb 2022 23:53:40 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60904072a2d483f2b95cd7664af8d144bcd54259dcfe206b971dc9464f7e0cee`  
		Last Modified: Thu, 03 Feb 2022 23:56:00 GMT  
		Size: 2.1 MB (2105556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cb84aa9aa1d353d00163e79f4ae6e8f71adfb01405afd4b1524b0173d8217b`  
		Last Modified: Thu, 03 Feb 2022 23:56:03 GMT  
		Size: 64.1 MB (64087947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d848a08c42793035ef4165414a2c69a18843cc58793dbe47405dbc68b087b8bd`  
		Last Modified: Thu, 03 Feb 2022 23:55:59 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.42`

```console
$ docker pull orientdb@sha256:90cfee1881ef0f8583bdd6d12ecf37183ea7e7c64a3b397831ac3113394983e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.42` - linux; amd64

```console
$ docker pull orientdb@sha256:c067f72467e31b73ea64c64bca2aa7e09ba9e4460e690be68fdc727859259067
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178466866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8bbe18b287c850428e36403fa1fb7874e9912ba048ea13c7910e920d9fd98f`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:53:15 GMT
ENV ORIENTDB_VERSION=3.0.42
# Thu, 03 Feb 2022 23:53:15 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59ed522290668fb400e67503652bb813
# Thu, 03 Feb 2022 23:53:15 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=fe6a510c72983b32a3ffd657be9ae62fab2b61f8
# Thu, 03 Feb 2022 23:53:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.42/orientdb-community-3.0.42.tar.gz
# Thu, 03 Feb 2022 23:53:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:53:24 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:53:24 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:53:24 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:53:25 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:53:25 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:53:25 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:53:25 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2591104e6b210de60c05b2a586b249333d1c9982fe4c5077da9667556778dca`  
		Last Modified: Thu, 03 Feb 2022 23:55:48 GMT  
		Size: 2.1 MB (2105595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a95605ca387cb36a005301c089e4f186d1c9cfc5483eecd01c12ad26c30175`  
		Last Modified: Thu, 03 Feb 2022 23:55:50 GMT  
		Size: 37.1 MB (37068551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.42-tp3`

```console
$ docker pull orientdb@sha256:d0bb977074c947913ae364a0f3496a673856e87d9ff4fa4b7b9138cc6c19cc33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.42-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:df5ddd29eaf9a8d0931ed81357e1ebdaa3652b939da62049b0ed89530f568ce4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205487600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ba49ec9b3fe1efcc7c620e83d711ceffb37789b49152d73b069a91da205b07`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:53:15 GMT
ENV ORIENTDB_VERSION=3.0.42
# Thu, 03 Feb 2022 23:53:28 GMT
ENV ORIENTDB_DOWNLOAD_MD5=20104f313e82db3a2bd88b7501d596aa
# Thu, 03 Feb 2022 23:53:29 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1abc7a4979ca561d13edd01b1d18b3b869abace9
# Thu, 03 Feb 2022 23:53:29 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.42/orientdb-tp3-3.0.42.tar.gz
# Thu, 03 Feb 2022 23:53:34 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:53:38 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:53:39 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 03 Feb 2022 23:53:39 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:53:39 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:53:39 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:53:40 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:53:40 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:53:40 GMT
EXPOSE 8182
# Thu, 03 Feb 2022 23:53:40 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60904072a2d483f2b95cd7664af8d144bcd54259dcfe206b971dc9464f7e0cee`  
		Last Modified: Thu, 03 Feb 2022 23:56:00 GMT  
		Size: 2.1 MB (2105556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cb84aa9aa1d353d00163e79f4ae6e8f71adfb01405afd4b1524b0173d8217b`  
		Last Modified: Thu, 03 Feb 2022 23:56:03 GMT  
		Size: 64.1 MB (64087947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d848a08c42793035ef4165414a2c69a18843cc58793dbe47405dbc68b087b8bd`  
		Last Modified: Thu, 03 Feb 2022 23:55:59 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:c1a32aad64645645a4d1b8e2cfd2a5193393067356ae43dfdc02fed5bc75c672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:630439071f019dcb6171c753a8cb7eb35a53c8f2ceee3ee1d16fdab41bb7b9c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193297871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf237bec51651b9839d9e7267d85741f134f417eed4e7d3064fba34d4ad63e6`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:52:45 GMT
ENV ORIENTDB_VERSION=3.1.15
# Thu, 03 Feb 2022 23:52:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=02073ca1909ec2d6ca9ef7566170cc18
# Thu, 03 Feb 2022 23:52:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=7f62eae6a19e4e5d719af78bd5b70f32b32492b2
# Thu, 03 Feb 2022 23:52:46 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.15/orientdb-community-3.1.15.tar.gz
# Thu, 03 Feb 2022 23:52:50 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:52:54 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:52:55 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:52:55 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:52:55 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:52:55 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:52:56 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:52:56 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7b2edb898d0adfaa50e85d725f91729bff1f32984b421351a1ccae5ad7bb7`  
		Last Modified: Thu, 03 Feb 2022 23:55:22 GMT  
		Size: 2.1 MB (2105596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ff773f7d5fc954f24d2a0100d6fdfa0f14344aae70847b4cf516dc9cf4f402`  
		Last Modified: Thu, 03 Feb 2022 23:55:25 GMT  
		Size: 51.9 MB (51899555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:e7e95b54235bce8dc9c15e4d8cf3eff2632b87f239e930e74b7005175fe84d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:19fae364a524959e029eaa8553ca16b5c1732c92dc47b2c0299e72a9391335bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216304387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87479708b1ddb31ce619922e20a6f89f5631f2543a339c75dd46b9000052eaa0`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:52:45 GMT
ENV ORIENTDB_VERSION=3.1.15
# Thu, 03 Feb 2022 23:52:59 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b04ae4e90985c0985b99bad34b6b6746
# Thu, 03 Feb 2022 23:52:59 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=3d36798106aee6a78f7807291b216dfe207f2f2c
# Thu, 03 Feb 2022 23:52:59 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.15/orientdb-tp3-3.1.15.tar.gz
# Thu, 03 Feb 2022 23:53:04 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:53:09 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:53:09 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 03 Feb 2022 23:53:10 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:53:10 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:53:10 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:53:10 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:53:11 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:53:11 GMT
EXPOSE 8182
# Thu, 03 Feb 2022 23:53:11 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319a59f793e02afedeb20838b74e0711d9df6bd215172d5801d26c1e165e6a52`  
		Last Modified: Thu, 03 Feb 2022 23:55:34 GMT  
		Size: 2.1 MB (2105551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff706790d56b5f00a4f49bf399513721940c9095c53cce81a0ffc6c53833f587`  
		Last Modified: Thu, 03 Feb 2022 23:55:38 GMT  
		Size: 74.9 MB (74904742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ff8563f644aea1e9891d25c53911d719fddaf75ea3f1e5a02f37574ab8c5c0`  
		Last Modified: Thu, 03 Feb 2022 23:55:34 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.15`

```console
$ docker pull orientdb@sha256:c1a32aad64645645a4d1b8e2cfd2a5193393067356ae43dfdc02fed5bc75c672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.15` - linux; amd64

```console
$ docker pull orientdb@sha256:630439071f019dcb6171c753a8cb7eb35a53c8f2ceee3ee1d16fdab41bb7b9c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193297871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf237bec51651b9839d9e7267d85741f134f417eed4e7d3064fba34d4ad63e6`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:52:45 GMT
ENV ORIENTDB_VERSION=3.1.15
# Thu, 03 Feb 2022 23:52:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=02073ca1909ec2d6ca9ef7566170cc18
# Thu, 03 Feb 2022 23:52:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=7f62eae6a19e4e5d719af78bd5b70f32b32492b2
# Thu, 03 Feb 2022 23:52:46 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.15/orientdb-community-3.1.15.tar.gz
# Thu, 03 Feb 2022 23:52:50 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:52:54 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:52:55 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:52:55 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:52:55 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:52:55 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:52:56 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:52:56 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e7b2edb898d0adfaa50e85d725f91729bff1f32984b421351a1ccae5ad7bb7`  
		Last Modified: Thu, 03 Feb 2022 23:55:22 GMT  
		Size: 2.1 MB (2105596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ff773f7d5fc954f24d2a0100d6fdfa0f14344aae70847b4cf516dc9cf4f402`  
		Last Modified: Thu, 03 Feb 2022 23:55:25 GMT  
		Size: 51.9 MB (51899555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.15-tp3`

```console
$ docker pull orientdb@sha256:e7e95b54235bce8dc9c15e4d8cf3eff2632b87f239e930e74b7005175fe84d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.15-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:19fae364a524959e029eaa8553ca16b5c1732c92dc47b2c0299e72a9391335bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216304387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87479708b1ddb31ce619922e20a6f89f5631f2543a339c75dd46b9000052eaa0`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:52:45 GMT
ENV ORIENTDB_VERSION=3.1.15
# Thu, 03 Feb 2022 23:52:59 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b04ae4e90985c0985b99bad34b6b6746
# Thu, 03 Feb 2022 23:52:59 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=3d36798106aee6a78f7807291b216dfe207f2f2c
# Thu, 03 Feb 2022 23:52:59 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.15/orientdb-tp3-3.1.15.tar.gz
# Thu, 03 Feb 2022 23:53:04 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:53:09 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:53:09 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 03 Feb 2022 23:53:10 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:53:10 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:53:10 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:53:10 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:53:11 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:53:11 GMT
EXPOSE 8182
# Thu, 03 Feb 2022 23:53:11 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319a59f793e02afedeb20838b74e0711d9df6bd215172d5801d26c1e165e6a52`  
		Last Modified: Thu, 03 Feb 2022 23:55:34 GMT  
		Size: 2.1 MB (2105551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff706790d56b5f00a4f49bf399513721940c9095c53cce81a0ffc6c53833f587`  
		Last Modified: Thu, 03 Feb 2022 23:55:38 GMT  
		Size: 74.9 MB (74904742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ff8563f644aea1e9891d25c53911d719fddaf75ea3f1e5a02f37574ab8c5c0`  
		Last Modified: Thu, 03 Feb 2022 23:55:34 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:4cc24343522f74b0e5127168cc6a6ed4e46682bc07f68b1024c58a592d4e9a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2` - linux; amd64

```console
$ docker pull orientdb@sha256:0b0aba33b88097d63dc09168fb8e7f2d185d57f4366ec429d80267787c864586
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212898901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60e7eed95c0cf6ffab8d01488f7c4df490000fc8a2dd8836a997a829171853`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_VERSION=3.2.4
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9ad71fd5e0bd783335ca4cbd94461ef5
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f910ed4ae9cf4c4038cd5b1f0cc7b19bf22ada03
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.4/orientdb-community-3.2.4.tar.gz
# Thu, 03 Feb 2022 23:52:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:52:24 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:52:25 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:52:25 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:52:25 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:52:25 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:52:26 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:52:26 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93ad3621686fa46910e083a61db9b76544a5c61001b55476c782e573ef37e7`  
		Last Modified: Thu, 03 Feb 2022 23:54:50 GMT  
		Size: 2.1 MB (2105546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525d18a8064f2a2d658ef728a75ed0df08615b0825c2e047d75d6aebb31adb3`  
		Last Modified: Thu, 03 Feb 2022 23:54:54 GMT  
		Size: 71.5 MB (71500635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:14c9ec9c548f02e4cc95321ebc5b10d217b83d0dc9f0f588c6fc4c050a459ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:ef8062386598e0796a694e352e7f81d30775435dc2c765c9a82d934fb520cb55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237176357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6141f4b1046a1345d55d1502d87b352b74a4c740bda15a1e23fc48a336a8ca7c`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_VERSION=3.2.4
# Thu, 03 Feb 2022 23:52:29 GMT
ENV ORIENTDB_DOWNLOAD_MD5=517a8962cb722a910248c76de4bf8fc6
# Thu, 03 Feb 2022 23:52:29 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a19b41a35932324e7c0f157fb53b2ad82c808e1b
# Thu, 03 Feb 2022 23:52:29 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.4/orientdb-tp3-3.2.4.tar.gz
# Thu, 03 Feb 2022 23:52:34 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:52:40 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:52:40 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 03 Feb 2022 23:52:41 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:52:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:52:41 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:52:41 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:52:41 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:52:42 GMT
EXPOSE 8182
# Thu, 03 Feb 2022 23:52:42 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7e5ed48b4de52f68b691c6703315753538ec3e65ed75766ef8fb06f2870d96`  
		Last Modified: Thu, 03 Feb 2022 23:55:06 GMT  
		Size: 2.1 MB (2105576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36825c9a9827ce62ce6b82067528f02eb8ec569392715186dc6d8e8e3ab8f0`  
		Last Modified: Thu, 03 Feb 2022 23:55:12 GMT  
		Size: 95.8 MB (95776684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64adc940bca004bcf8e0cd062f8b581f3834f18712e3e1394f01cfe581f4d2bd`  
		Last Modified: Thu, 03 Feb 2022 23:55:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.4`

```console
$ docker pull orientdb@sha256:4cc24343522f74b0e5127168cc6a6ed4e46682bc07f68b1024c58a592d4e9a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2.4` - linux; amd64

```console
$ docker pull orientdb@sha256:0b0aba33b88097d63dc09168fb8e7f2d185d57f4366ec429d80267787c864586
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212898901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60e7eed95c0cf6ffab8d01488f7c4df490000fc8a2dd8836a997a829171853`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_VERSION=3.2.4
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9ad71fd5e0bd783335ca4cbd94461ef5
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f910ed4ae9cf4c4038cd5b1f0cc7b19bf22ada03
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.4/orientdb-community-3.2.4.tar.gz
# Thu, 03 Feb 2022 23:52:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:52:24 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:52:25 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:52:25 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:52:25 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:52:25 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:52:26 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:52:26 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93ad3621686fa46910e083a61db9b76544a5c61001b55476c782e573ef37e7`  
		Last Modified: Thu, 03 Feb 2022 23:54:50 GMT  
		Size: 2.1 MB (2105546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525d18a8064f2a2d658ef728a75ed0df08615b0825c2e047d75d6aebb31adb3`  
		Last Modified: Thu, 03 Feb 2022 23:54:54 GMT  
		Size: 71.5 MB (71500635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.4-tp3`

```console
$ docker pull orientdb@sha256:14c9ec9c548f02e4cc95321ebc5b10d217b83d0dc9f0f588c6fc4c050a459ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2.4-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:ef8062386598e0796a694e352e7f81d30775435dc2c765c9a82d934fb520cb55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237176357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6141f4b1046a1345d55d1502d87b352b74a4c740bda15a1e23fc48a336a8ca7c`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_VERSION=3.2.4
# Thu, 03 Feb 2022 23:52:29 GMT
ENV ORIENTDB_DOWNLOAD_MD5=517a8962cb722a910248c76de4bf8fc6
# Thu, 03 Feb 2022 23:52:29 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=a19b41a35932324e7c0f157fb53b2ad82c808e1b
# Thu, 03 Feb 2022 23:52:29 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.4/orientdb-tp3-3.2.4.tar.gz
# Thu, 03 Feb 2022 23:52:34 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:52:40 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:52:40 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Thu, 03 Feb 2022 23:52:41 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:52:41 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:52:41 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:52:41 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:52:41 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:52:42 GMT
EXPOSE 8182
# Thu, 03 Feb 2022 23:52:42 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7e5ed48b4de52f68b691c6703315753538ec3e65ed75766ef8fb06f2870d96`  
		Last Modified: Thu, 03 Feb 2022 23:55:06 GMT  
		Size: 2.1 MB (2105576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36825c9a9827ce62ce6b82067528f02eb8ec569392715186dc6d8e8e3ab8f0`  
		Last Modified: Thu, 03 Feb 2022 23:55:12 GMT  
		Size: 95.8 MB (95776684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64adc940bca004bcf8e0cd062f8b581f3834f18712e3e1394f01cfe581f4d2bd`  
		Last Modified: Thu, 03 Feb 2022 23:55:06 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:4cc24343522f74b0e5127168cc6a6ed4e46682bc07f68b1024c58a592d4e9a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:0b0aba33b88097d63dc09168fb8e7f2d185d57f4366ec429d80267787c864586
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212898901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60e7eed95c0cf6ffab8d01488f7c4df490000fc8a2dd8836a997a829171853`
-	Default Command: `["server.sh"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:47:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 03 Feb 2022 23:52:12 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 03 Feb 2022 23:52:13 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_VERSION=3.2.4
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9ad71fd5e0bd783335ca4cbd94461ef5
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f910ed4ae9cf4c4038cd5b1f0cc7b19bf22ada03
# Thu, 03 Feb 2022 23:52:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.4/orientdb-community-3.2.4.tar.gz
# Thu, 03 Feb 2022 23:52:19 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Feb 2022 23:52:24 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 03 Feb 2022 23:52:25 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Feb 2022 23:52:25 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 03 Feb 2022 23:52:25 GMT
WORKDIR /orientdb
# Thu, 03 Feb 2022 23:52:25 GMT
EXPOSE 2424
# Thu, 03 Feb 2022 23:52:26 GMT
EXPOSE 2480
# Thu, 03 Feb 2022 23:52:26 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097a90b8f3b1ca509e2ab5e141e714364d09f2947b1c0f6dfc0509b2fcaadea0`  
		Last Modified: Thu, 03 Feb 2022 21:03:23 GMT  
		Size: 106.3 MB (106344203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b93ad3621686fa46910e083a61db9b76544a5c61001b55476c782e573ef37e7`  
		Last Modified: Thu, 03 Feb 2022 23:54:50 GMT  
		Size: 2.1 MB (2105546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525d18a8064f2a2d658ef728a75ed0df08615b0825c2e047d75d6aebb31adb3`  
		Last Modified: Thu, 03 Feb 2022 23:54:54 GMT  
		Size: 71.5 MB (71500635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
