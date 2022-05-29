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
-	[`orientdb:3.1.18`](#orientdb3118)
-	[`orientdb:3.1.18-tp3`](#orientdb3118-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.6`](#orientdb326)
-	[`orientdb:3.2.6-tp3`](#orientdb326-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.0`

```console
$ docker pull orientdb@sha256:18d6507d0c200d2ee08cefcf7761ed2b98786dbb02caceeab522ecfaf1987220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.0` - linux; amd64

```console
$ docker pull orientdb@sha256:0d2cfe7efe7539b22ea33f77a4a18fa488c396814109ae8db622b0de8b7a2050
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283570325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c37580cd40daec84e1d3ece202c10963b0a2efdd6aa329dd078c71335f1e59`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:12 GMT
ADD file:dd3d4b31d7f1d4062ad0eb2d85dba064cea067b1eb4a8b89a0b593ea90001cdf in / 
# Sat, 28 May 2022 01:20:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:40:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:41:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 19:37:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 19:39:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 19:39:13 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 19:39:13 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 19:39:13 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 19:39:13 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 19:39:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:30:02 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:30:02 GMT
ENV ORIENTDB_VERSION=2.0.18
# Sat, 28 May 2022 23:30:02 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Sat, 28 May 2022 23:30:02 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Sat, 28 May 2022 23:30:05 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:30:05 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:30:05 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:30:05 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:30:05 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:30:06 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:30:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e756f3fdd6a378aa16205b0f75d178b7532b110e86be7659004fc6a21183226c`  
		Last Modified: Sat, 28 May 2022 01:24:51 GMT  
		Size: 55.0 MB (55009253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf168a6748997eb97b48cc86234b7ff7d8bc907645b9be99013158b3f146b272`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 5.2 MB (5156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604223835ccf02d097187b5a58ca73e8598cadbb16a36202ca1943e97f56f1f`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 10.9 MB (10875008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5c91c4cd86dde23108ab3af91e9eae838d0059a380ee7dfd4f370b6d985523`  
		Last Modified: Sat, 28 May 2022 02:49:31 GMT  
		Size: 54.6 MB (54579133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e20d165240e4863f511ba9a1b730a75630545413cc7fee0c9eca825a3ad6b91`  
		Last Modified: Sat, 28 May 2022 19:47:13 GMT  
		Size: 5.4 MB (5420633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f67470f83789ace143e8a7d9b3f83b312f49eefa0400c8714ab556d364960d`  
		Last Modified: Sat, 28 May 2022 19:49:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddf137867aab9a44c3a9864b5267f6df8db5d791e4df4d3684c2f16e1a97a2f`  
		Last Modified: Sat, 28 May 2022 19:49:26 GMT  
		Size: 105.9 MB (105943492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4fdf4fc4f0fe39439678e20e0ce341f3c020e76be2f09f20ed2f29fc024b880`  
		Last Modified: Sat, 28 May 2022 23:32:39 GMT  
		Size: 46.6 MB (46586560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.0.18`

```console
$ docker pull orientdb@sha256:18d6507d0c200d2ee08cefcf7761ed2b98786dbb02caceeab522ecfaf1987220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.0.18` - linux; amd64

```console
$ docker pull orientdb@sha256:0d2cfe7efe7539b22ea33f77a4a18fa488c396814109ae8db622b0de8b7a2050
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283570325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c37580cd40daec84e1d3ece202c10963b0a2efdd6aa329dd078c71335f1e59`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:12 GMT
ADD file:dd3d4b31d7f1d4062ad0eb2d85dba064cea067b1eb4a8b89a0b593ea90001cdf in / 
# Sat, 28 May 2022 01:20:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:40:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:41:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 19:37:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 19:39:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 19:39:13 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 19:39:13 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 19:39:13 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 19:39:13 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 19:39:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:30:02 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:30:02 GMT
ENV ORIENTDB_VERSION=2.0.18
# Sat, 28 May 2022 23:30:02 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Sat, 28 May 2022 23:30:02 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Sat, 28 May 2022 23:30:05 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:30:05 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:30:05 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:30:05 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:30:05 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:30:06 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:30:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e756f3fdd6a378aa16205b0f75d178b7532b110e86be7659004fc6a21183226c`  
		Last Modified: Sat, 28 May 2022 01:24:51 GMT  
		Size: 55.0 MB (55009253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf168a6748997eb97b48cc86234b7ff7d8bc907645b9be99013158b3f146b272`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 5.2 MB (5156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604223835ccf02d097187b5a58ca73e8598cadbb16a36202ca1943e97f56f1f`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 10.9 MB (10875008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5c91c4cd86dde23108ab3af91e9eae838d0059a380ee7dfd4f370b6d985523`  
		Last Modified: Sat, 28 May 2022 02:49:31 GMT  
		Size: 54.6 MB (54579133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e20d165240e4863f511ba9a1b730a75630545413cc7fee0c9eca825a3ad6b91`  
		Last Modified: Sat, 28 May 2022 19:47:13 GMT  
		Size: 5.4 MB (5420633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f67470f83789ace143e8a7d9b3f83b312f49eefa0400c8714ab556d364960d`  
		Last Modified: Sat, 28 May 2022 19:49:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddf137867aab9a44c3a9864b5267f6df8db5d791e4df4d3684c2f16e1a97a2f`  
		Last Modified: Sat, 28 May 2022 19:49:26 GMT  
		Size: 105.9 MB (105943492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4fdf4fc4f0fe39439678e20e0ce341f3c020e76be2f09f20ed2f29fc024b880`  
		Last Modified: Sat, 28 May 2022 23:32:39 GMT  
		Size: 46.6 MB (46586560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.1`

```console
$ docker pull orientdb@sha256:4b4d2520b87b545d5ee7ce94e6d4d7c1d4afa7c41c9561535d68551a7b6a1445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.1` - linux; amd64

```console
$ docker pull orientdb@sha256:245c737d8f09319cef55933fe72bbd419b0c0c574bba5f47394c7ff5ba7588d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172370813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b5acb9ffbee2d3418fa6f42e0738d09e93f2a20abb56233311add43e3ec043`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:29:50 GMT
ENV ORIENTDB_VERSION=2.1.25
# Sat, 28 May 2022 23:29:50 GMT
ENV ORIENTDB_DOWNLOAD_MD5=054da3fb7c56e7822b2af116966576ce
# Sat, 28 May 2022 23:29:50 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=b7b08242b40117ac8eb9a201f8704bde839dfcb8
# Sat, 28 May 2022 23:29:55 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:58 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:58 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:58 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:58 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:58 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:58 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:58 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0dc3a669e92b6a5ec753382150c32aeee1bc7aedbec4ef8e34452b2e4b4ba5`  
		Last Modified: Sat, 28 May 2022 23:32:24 GMT  
		Size: 2.1 MB (2105646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28680e8750035b32a8de1b35c69e7e41ecfccc3b867bae4589d46b0c8b0ce6a7`  
		Last Modified: Sat, 28 May 2022 23:32:26 GMT  
		Size: 31.1 MB (31087992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.1.25`

```console
$ docker pull orientdb@sha256:4b4d2520b87b545d5ee7ce94e6d4d7c1d4afa7c41c9561535d68551a7b6a1445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.1.25` - linux; amd64

```console
$ docker pull orientdb@sha256:245c737d8f09319cef55933fe72bbd419b0c0c574bba5f47394c7ff5ba7588d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172370813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b5acb9ffbee2d3418fa6f42e0738d09e93f2a20abb56233311add43e3ec043`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:29:50 GMT
ENV ORIENTDB_VERSION=2.1.25
# Sat, 28 May 2022 23:29:50 GMT
ENV ORIENTDB_DOWNLOAD_MD5=054da3fb7c56e7822b2af116966576ce
# Sat, 28 May 2022 23:29:50 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=b7b08242b40117ac8eb9a201f8704bde839dfcb8
# Sat, 28 May 2022 23:29:55 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:58 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:58 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:58 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:58 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:58 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:58 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:58 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0dc3a669e92b6a5ec753382150c32aeee1bc7aedbec4ef8e34452b2e4b4ba5`  
		Last Modified: Sat, 28 May 2022 23:32:24 GMT  
		Size: 2.1 MB (2105646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28680e8750035b32a8de1b35c69e7e41ecfccc3b867bae4589d46b0c8b0ce6a7`  
		Last Modified: Sat, 28 May 2022 23:32:26 GMT  
		Size: 31.1 MB (31087992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2`

```console
$ docker pull orientdb@sha256:bcb1dd497fbf09eb8899d657cedb66c3b7a092d38eb064422a351dad71b838e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2` - linux; amd64

```console
$ docker pull orientdb@sha256:f2bc5e289d66338a70107058fad02aa8de477b92c0f65b44f2afc7fd830179f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187756713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b533a0363de8477ba91dd21cde4ab68806f2426032d5cc23533200a0e2e3d1e`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_VERSION=2.2.37
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Sat, 28 May 2022 23:29:40 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:43 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:43 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:43 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:43 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:43 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:43 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:44 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326b33dfb699290097085b101cab3264e373aa858e856824b4c49e8f2667ddb`  
		Last Modified: Sat, 28 May 2022 23:32:04 GMT  
		Size: 2.1 MB (2105661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42963cf89b5dbc05150c438b08af3fc87d59c04488e4d9338706b087c8484281`  
		Last Modified: Sat, 28 May 2022 23:32:07 GMT  
		Size: 46.5 MB (46473877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37`

```console
$ docker pull orientdb@sha256:bcb1dd497fbf09eb8899d657cedb66c3b7a092d38eb064422a351dad71b838e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37` - linux; amd64

```console
$ docker pull orientdb@sha256:f2bc5e289d66338a70107058fad02aa8de477b92c0f65b44f2afc7fd830179f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187756713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b533a0363de8477ba91dd21cde4ab68806f2426032d5cc23533200a0e2e3d1e`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_VERSION=2.2.37
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Sat, 28 May 2022 23:29:40 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:43 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:43 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:43 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:43 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:43 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:43 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:44 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326b33dfb699290097085b101cab3264e373aa858e856824b4c49e8f2667ddb`  
		Last Modified: Sat, 28 May 2022 23:32:04 GMT  
		Size: 2.1 MB (2105661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42963cf89b5dbc05150c438b08af3fc87d59c04488e4d9338706b087c8484281`  
		Last Modified: Sat, 28 May 2022 23:32:07 GMT  
		Size: 46.5 MB (46473877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37-spatial`

```console
$ docker pull orientdb@sha256:48c599847a7f07cf5bb08be68335d26efe437888c98ef9efab1f6b54b1c9c323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37-spatial` - linux; amd64

```console
$ docker pull orientdb@sha256:025cd703d25f2321b7c9404b4c4b857af91dd02663319b2d5770e91a2a201513
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188959306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f29762623c2fa1acb4b11a40ec5360d17a697116a2b6956da6d12893ccdb613`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_VERSION=2.2.37
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Sat, 28 May 2022 23:29:35 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Sat, 28 May 2022 23:29:40 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:43 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:43 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:43 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:43 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:43 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:43 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:44 GMT
CMD ["server.sh"]
# Sat, 28 May 2022 23:29:47 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_MD5=9f64ab5e959f5d9ad9ea5195d6d621d2
# Sat, 28 May 2022 23:29:47 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_SHA1=1748c9779ea7a8cb8fc068fcabf960e1778e8a19
# Sat, 28 May 2022 23:29:47 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-spatial/2.2.37/orientdb-spatial-2.2.37-dist.jar
# Sat, 28 May 2022 23:29:48 GMT
RUN wget $ORIENTDB_DOWNLOAD_SPATIAL_URL     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_MD5 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | md5sum -c -     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_SHA1 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | sha1sum -c -     && mv orientdb-spatial-*-dist.jar /orientdb/lib/
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326b33dfb699290097085b101cab3264e373aa858e856824b4c49e8f2667ddb`  
		Last Modified: Sat, 28 May 2022 23:32:04 GMT  
		Size: 2.1 MB (2105661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42963cf89b5dbc05150c438b08af3fc87d59c04488e4d9338706b087c8484281`  
		Last Modified: Sat, 28 May 2022 23:32:07 GMT  
		Size: 46.5 MB (46473877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8169d5125e3f2ac0266cf82b0b13b4c1f78b6584b2b5d760f0fd73da990f28`  
		Last Modified: Sat, 28 May 2022 23:32:16 GMT  
		Size: 1.2 MB (1202593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0`

```console
$ docker pull orientdb@sha256:0991463eb365a2e96891df035c390f51a3ffbe71d9ae5856838503c3fd3232f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0` - linux; amd64

```console
$ docker pull orientdb@sha256:e091a31e7ebeb26e4e65c793646547d263858996e790169ec897a33cfa9d2775
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178351377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6407d6ee05685b06c8b27e1c5b8505f79e3e2cbc4b3c66a861a7d26b730eef7`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_VERSION=3.0.42
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59ed522290668fb400e67503652bb813
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=fe6a510c72983b32a3ffd657be9ae62fab2b61f8
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.42/orientdb-community-3.0.42.tar.gz
# Sat, 28 May 2022 23:29:14 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:16 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:16 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:17 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:17 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:17 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:17 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a7b3fde7154e3b54ebb8216d485744d23cd70a6bb96faa8c07195894e62697`  
		Last Modified: Sat, 28 May 2022 23:31:38 GMT  
		Size: 2.1 MB (2105653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed238890ed91b5ed731c3b66e285f0b6c4374c7b53e4d4b91be2881a46ff4d1`  
		Last Modified: Sat, 28 May 2022 23:31:40 GMT  
		Size: 37.1 MB (37068549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0-tp3`

```console
$ docker pull orientdb@sha256:84e69ae0cf2e523bc64e8bae9a4aecdc7f2f51493c8abfbf161557c961f9d186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:1f7e2a41e1a2d1ccf3f441f3fb17183b92c6c79e8c412655e8c5b1b068d1bb2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205372144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cbaed553013f2b5a0c5dcd00c7f3c16920d2d490b49de964383b736e46ba1e`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_VERSION=3.0.42
# Sat, 28 May 2022 23:29:21 GMT
ENV ORIENTDB_DOWNLOAD_MD5=20104f313e82db3a2bd88b7501d596aa
# Sat, 28 May 2022 23:29:21 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1abc7a4979ca561d13edd01b1d18b3b869abace9
# Sat, 28 May 2022 23:29:21 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.42/orientdb-tp3-3.0.42.tar.gz
# Sat, 28 May 2022 23:29:25 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:30 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:31 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 28 May 2022 23:29:31 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:31 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:31 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:31 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:31 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:31 GMT
EXPOSE 8182
# Sat, 28 May 2022 23:29:31 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bd89fa4425de91b9113d3d4163c94bc79ebfbb6fbaaaf4f9453aa4ef9b3b21`  
		Last Modified: Sat, 28 May 2022 23:31:50 GMT  
		Size: 2.1 MB (2105660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0e5282383f68d43185e8ad187eef8f48b6019b4011ca946c74bedbda81708e`  
		Last Modified: Sat, 28 May 2022 23:31:54 GMT  
		Size: 64.1 MB (64087936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a6739e0898076775549e1e2b6aa6ce25ddd2f1833326265d8029ae55eb768b`  
		Last Modified: Sat, 28 May 2022 23:31:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.42`

```console
$ docker pull orientdb@sha256:0991463eb365a2e96891df035c390f51a3ffbe71d9ae5856838503c3fd3232f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.42` - linux; amd64

```console
$ docker pull orientdb@sha256:e091a31e7ebeb26e4e65c793646547d263858996e790169ec897a33cfa9d2775
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178351377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6407d6ee05685b06c8b27e1c5b8505f79e3e2cbc4b3c66a861a7d26b730eef7`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_VERSION=3.0.42
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59ed522290668fb400e67503652bb813
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=fe6a510c72983b32a3ffd657be9ae62fab2b61f8
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.42/orientdb-community-3.0.42.tar.gz
# Sat, 28 May 2022 23:29:14 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:16 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:16 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:16 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:17 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:17 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:17 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:17 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a7b3fde7154e3b54ebb8216d485744d23cd70a6bb96faa8c07195894e62697`  
		Last Modified: Sat, 28 May 2022 23:31:38 GMT  
		Size: 2.1 MB (2105653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed238890ed91b5ed731c3b66e285f0b6c4374c7b53e4d4b91be2881a46ff4d1`  
		Last Modified: Sat, 28 May 2022 23:31:40 GMT  
		Size: 37.1 MB (37068549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.42-tp3`

```console
$ docker pull orientdb@sha256:84e69ae0cf2e523bc64e8bae9a4aecdc7f2f51493c8abfbf161557c961f9d186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.42-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:1f7e2a41e1a2d1ccf3f441f3fb17183b92c6c79e8c412655e8c5b1b068d1bb2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205372144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cbaed553013f2b5a0c5dcd00c7f3c16920d2d490b49de964383b736e46ba1e`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:29:09 GMT
ENV ORIENTDB_VERSION=3.0.42
# Sat, 28 May 2022 23:29:21 GMT
ENV ORIENTDB_DOWNLOAD_MD5=20104f313e82db3a2bd88b7501d596aa
# Sat, 28 May 2022 23:29:21 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1abc7a4979ca561d13edd01b1d18b3b869abace9
# Sat, 28 May 2022 23:29:21 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.42/orientdb-tp3-3.0.42.tar.gz
# Sat, 28 May 2022 23:29:25 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:30 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:31 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 28 May 2022 23:29:31 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:31 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:31 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:31 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:31 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:31 GMT
EXPOSE 8182
# Sat, 28 May 2022 23:29:31 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9bd89fa4425de91b9113d3d4163c94bc79ebfbb6fbaaaf4f9453aa4ef9b3b21`  
		Last Modified: Sat, 28 May 2022 23:31:50 GMT  
		Size: 2.1 MB (2105660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0e5282383f68d43185e8ad187eef8f48b6019b4011ca946c74bedbda81708e`  
		Last Modified: Sat, 28 May 2022 23:31:54 GMT  
		Size: 64.1 MB (64087936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a6739e0898076775549e1e2b6aa6ce25ddd2f1833326265d8029ae55eb768b`  
		Last Modified: Sat, 28 May 2022 23:31:50 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:31217d39bfd5e56a971e6d49e0968659ee67b836e7fd21b3f69c8e1645e36e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:afb2f207c64b7634d919ccc2ee7891048438c559106575dc39a1a033d05d9f14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194321605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e1301fdc65f89fdff6c1e3e383c23b027cc8defe8e058570735ec66fb01bc4`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:45 GMT
ENV ORIENTDB_VERSION=3.1.18
# Sat, 28 May 2022 23:28:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b5039f79f08eeb5c60817699a650190a
# Sat, 28 May 2022 23:28:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f3201cec2eb59572fd813168489fe6de0682c698
# Sat, 28 May 2022 23:28:46 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.18/orientdb-community-3.1.18.tar.gz
# Sat, 28 May 2022 23:28:50 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:28:53 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:28:53 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:28:53 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:28:53 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:28:53 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:28:53 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:28:53 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de840c1b3926a2f91d8a5b6175425a897b313729c077fbe4c1761ad904054b9a`  
		Last Modified: Sat, 28 May 2022 23:31:11 GMT  
		Size: 2.1 MB (2105656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5114f222eecdc67efa2c96f8baddaf1260b0725bebf3f26cd7798ada23fa44`  
		Last Modified: Sat, 28 May 2022 23:31:14 GMT  
		Size: 53.0 MB (53038774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:667905dfc9ae163a0f0d3b763adff09bc2d66e647685f7d0f105538cf7ab7881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:a10527823f910e6826751b3282298c7b2c03c79bd1f6ddcc6bf7051eaaa50b04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217368307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215c2faa3aac8b883a3a5677f8e3bfbf256df716a78c150093c3ae50fd4a991e`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:45 GMT
ENV ORIENTDB_VERSION=3.1.18
# Sat, 28 May 2022 23:28:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=bebb872ef46dfce2a2430f27b4a7ffa9
# Sat, 28 May 2022 23:28:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f5641f1dc198435cb22efeb340b02e35df4ad55c
# Sat, 28 May 2022 23:28:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.18/orientdb-tp3-3.1.18.tar.gz
# Sat, 28 May 2022 23:29:02 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:05 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:05 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 28 May 2022 23:29:05 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:05 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:06 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:06 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:06 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:06 GMT
EXPOSE 8182
# Sat, 28 May 2022 23:29:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e3f8fc35528600c7ee5a574af1f330a7d0ed599cd4cf71994a5c8ee85567c2`  
		Last Modified: Sat, 28 May 2022 23:31:24 GMT  
		Size: 2.1 MB (2105616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296f1d0ed585412c49df36d5e15e0e1c6cfcbb54ca76b84767af14cd5a6a21d`  
		Last Modified: Sat, 28 May 2022 23:31:27 GMT  
		Size: 76.1 MB (76084141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15e2e7fee0ee9e7727cbe135a8e4e279f16343109dc5203697a67f575f3ec9a`  
		Last Modified: Sat, 28 May 2022 23:31:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.18`

```console
$ docker pull orientdb@sha256:31217d39bfd5e56a971e6d49e0968659ee67b836e7fd21b3f69c8e1645e36e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.18` - linux; amd64

```console
$ docker pull orientdb@sha256:afb2f207c64b7634d919ccc2ee7891048438c559106575dc39a1a033d05d9f14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194321605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e1301fdc65f89fdff6c1e3e383c23b027cc8defe8e058570735ec66fb01bc4`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:45 GMT
ENV ORIENTDB_VERSION=3.1.18
# Sat, 28 May 2022 23:28:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b5039f79f08eeb5c60817699a650190a
# Sat, 28 May 2022 23:28:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f3201cec2eb59572fd813168489fe6de0682c698
# Sat, 28 May 2022 23:28:46 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.18/orientdb-community-3.1.18.tar.gz
# Sat, 28 May 2022 23:28:50 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:28:53 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:28:53 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:28:53 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:28:53 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:28:53 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:28:53 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:28:53 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de840c1b3926a2f91d8a5b6175425a897b313729c077fbe4c1761ad904054b9a`  
		Last Modified: Sat, 28 May 2022 23:31:11 GMT  
		Size: 2.1 MB (2105656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5114f222eecdc67efa2c96f8baddaf1260b0725bebf3f26cd7798ada23fa44`  
		Last Modified: Sat, 28 May 2022 23:31:14 GMT  
		Size: 53.0 MB (53038774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.18-tp3`

```console
$ docker pull orientdb@sha256:667905dfc9ae163a0f0d3b763adff09bc2d66e647685f7d0f105538cf7ab7881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.18-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:a10527823f910e6826751b3282298c7b2c03c79bd1f6ddcc6bf7051eaaa50b04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217368307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215c2faa3aac8b883a3a5677f8e3bfbf256df716a78c150093c3ae50fd4a991e`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:45 GMT
ENV ORIENTDB_VERSION=3.1.18
# Sat, 28 May 2022 23:28:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=bebb872ef46dfce2a2430f27b4a7ffa9
# Sat, 28 May 2022 23:28:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f5641f1dc198435cb22efeb340b02e35df4ad55c
# Sat, 28 May 2022 23:28:57 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.18/orientdb-tp3-3.1.18.tar.gz
# Sat, 28 May 2022 23:29:02 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:29:05 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:29:05 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 28 May 2022 23:29:05 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:29:05 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:29:06 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:29:06 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:29:06 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:29:06 GMT
EXPOSE 8182
# Sat, 28 May 2022 23:29:06 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e3f8fc35528600c7ee5a574af1f330a7d0ed599cd4cf71994a5c8ee85567c2`  
		Last Modified: Sat, 28 May 2022 23:31:24 GMT  
		Size: 2.1 MB (2105616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296f1d0ed585412c49df36d5e15e0e1c6cfcbb54ca76b84767af14cd5a6a21d`  
		Last Modified: Sat, 28 May 2022 23:31:27 GMT  
		Size: 76.1 MB (76084141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15e2e7fee0ee9e7727cbe135a8e4e279f16343109dc5203697a67f575f3ec9a`  
		Last Modified: Sat, 28 May 2022 23:31:23 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:4c5ced5998cf2f972304eb94bb8809f3cb2a0a306ea14c146a1646ad796e48fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2` - linux; amd64

```console
$ docker pull orientdb@sha256:351dbd9fc4dbc9666ea791122fc4e74edc819b85448b7c1537febc8e6c52e915
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214036296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ce267ccf1c0ee0fe53cc5d4844adefb61caf61f551be9b179179f56849d34c`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_VERSION=3.2.6
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=08e39080df862d3c5570f834d9d6f92b
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ba07e961cd05dfe2d3bc623e865ae21e533ace68
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.6/orientdb-community-3.2.6.tar.gz
# Sat, 28 May 2022 23:28:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:28:27 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:28:27 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:28:27 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:28:28 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:28:28 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:28:28 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:28:28 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81e24edbfb36ef2f8fb16c818dfb34e807fa0a85811c72faafa7edd04532306`  
		Last Modified: Sat, 28 May 2022 23:30:33 GMT  
		Size: 2.1 MB (2105667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3277f8b93337b3b310a6c83af66aa211cc0842a759530541bcf77a24f39dabd8`  
		Last Modified: Sat, 28 May 2022 23:30:37 GMT  
		Size: 72.8 MB (72753454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:3d195101a3692c3d09def016053c7d0461e5ee86db37301ee6c848252b505e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:6ef6d43ec9bea409c89f596aecefbddac65579e37761c76c0599fd81f85c1114
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238310489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cbfb8250ba74c07781ffdff8b86d073b597a04a7047c2746fb262b985ae0a8`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_VERSION=3.2.6
# Sat, 28 May 2022 23:28:32 GMT
ENV ORIENTDB_DOWNLOAD_MD5=a5e17d6b99950130383fcb974e061cc6
# Sat, 28 May 2022 23:28:32 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c07371cd46382aa3683cbf5283ba5b332806df18
# Sat, 28 May 2022 23:28:32 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.6/orientdb-tp3-3.2.6.tar.gz
# Sat, 28 May 2022 23:28:36 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:28:42 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:28:42 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 28 May 2022 23:28:42 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:28:42 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:28:42 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:28:42 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:28:42 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:28:43 GMT
EXPOSE 8182
# Sat, 28 May 2022 23:28:43 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66f3997c54bc78b3deefe166c7f212ee287023318daf602e910f81498741e4c`  
		Last Modified: Sat, 28 May 2022 23:30:56 GMT  
		Size: 2.1 MB (2105681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360b240ed71e835205fbecc9734409351a8f804f35a2e47b627d28a4085f3e99`  
		Last Modified: Sat, 28 May 2022 23:31:01 GMT  
		Size: 97.0 MB (97026255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfde88978bbd0f02696d374870e665d163c0d0c1c0e0dcf5dae43ac827c4e5`  
		Last Modified: Sat, 28 May 2022 23:30:55 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.6`

```console
$ docker pull orientdb@sha256:4c5ced5998cf2f972304eb94bb8809f3cb2a0a306ea14c146a1646ad796e48fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2.6` - linux; amd64

```console
$ docker pull orientdb@sha256:351dbd9fc4dbc9666ea791122fc4e74edc819b85448b7c1537febc8e6c52e915
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214036296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ce267ccf1c0ee0fe53cc5d4844adefb61caf61f551be9b179179f56849d34c`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_VERSION=3.2.6
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=08e39080df862d3c5570f834d9d6f92b
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ba07e961cd05dfe2d3bc623e865ae21e533ace68
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.6/orientdb-community-3.2.6.tar.gz
# Sat, 28 May 2022 23:28:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:28:27 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:28:27 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:28:27 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:28:28 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:28:28 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:28:28 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:28:28 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81e24edbfb36ef2f8fb16c818dfb34e807fa0a85811c72faafa7edd04532306`  
		Last Modified: Sat, 28 May 2022 23:30:33 GMT  
		Size: 2.1 MB (2105667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3277f8b93337b3b310a6c83af66aa211cc0842a759530541bcf77a24f39dabd8`  
		Last Modified: Sat, 28 May 2022 23:30:37 GMT  
		Size: 72.8 MB (72753454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.6-tp3`

```console
$ docker pull orientdb@sha256:3d195101a3692c3d09def016053c7d0461e5ee86db37301ee6c848252b505e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2.6-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:6ef6d43ec9bea409c89f596aecefbddac65579e37761c76c0599fd81f85c1114
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238310489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cbfb8250ba74c07781ffdff8b86d073b597a04a7047c2746fb262b985ae0a8`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_VERSION=3.2.6
# Sat, 28 May 2022 23:28:32 GMT
ENV ORIENTDB_DOWNLOAD_MD5=a5e17d6b99950130383fcb974e061cc6
# Sat, 28 May 2022 23:28:32 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=c07371cd46382aa3683cbf5283ba5b332806df18
# Sat, 28 May 2022 23:28:32 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.6/orientdb-tp3-3.2.6.tar.gz
# Sat, 28 May 2022 23:28:36 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:28:42 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:28:42 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Sat, 28 May 2022 23:28:42 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:28:42 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:28:42 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:28:42 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:28:42 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:28:43 GMT
EXPOSE 8182
# Sat, 28 May 2022 23:28:43 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66f3997c54bc78b3deefe166c7f212ee287023318daf602e910f81498741e4c`  
		Last Modified: Sat, 28 May 2022 23:30:56 GMT  
		Size: 2.1 MB (2105681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360b240ed71e835205fbecc9734409351a8f804f35a2e47b627d28a4085f3e99`  
		Last Modified: Sat, 28 May 2022 23:31:01 GMT  
		Size: 97.0 MB (97026255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cfde88978bbd0f02696d374870e665d163c0d0c1c0e0dcf5dae43ac827c4e5`  
		Last Modified: Sat, 28 May 2022 23:30:55 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:4c5ced5998cf2f972304eb94bb8809f3cb2a0a306ea14c146a1646ad796e48fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:351dbd9fc4dbc9666ea791122fc4e74edc819b85448b7c1537febc8e6c52e915
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214036296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ce267ccf1c0ee0fe53cc5d4844adefb61caf61f551be9b179179f56849d34c`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_VERSION=3.2.6
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=08e39080df862d3c5570f834d9d6f92b
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ba07e961cd05dfe2d3bc623e865ae21e533ace68
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.6/orientdb-community-3.2.6.tar.gz
# Sat, 28 May 2022 23:28:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:28:27 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:28:27 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:28:27 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:28:28 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:28:28 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:28:28 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:28:28 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81e24edbfb36ef2f8fb16c818dfb34e807fa0a85811c72faafa7edd04532306`  
		Last Modified: Sat, 28 May 2022 23:30:33 GMT  
		Size: 2.1 MB (2105667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3277f8b93337b3b310a6c83af66aa211cc0842a759530541bcf77a24f39dabd8`  
		Last Modified: Sat, 28 May 2022 23:30:37 GMT  
		Size: 72.8 MB (72753454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
