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
-	[`orientdb:3.0.36`](#orientdb3036)
-	[`orientdb:3.0.36-tp3`](#orientdb3036-tp3)
-	[`orientdb:3.0-tp3`](#orientdb30-tp3)
-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1.7`](#orientdb317)
-	[`orientdb:3.1.7-tp3`](#orientdb317-tp3)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.0`

```console
$ docker pull orientdb@sha256:ef891059b67551d212004803f93dabfa4d056bd156118d0f6421d3b5ff3c6c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.0` - linux; amd64

```console
$ docker pull orientdb@sha256:78d144d6d457a53cd949d49b843f15b471d696d214197241ebe0b863a68aea5e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278125331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9a831aeda29d7cd4184dcc6ffa2db62e57ba31cd15907d9975849a6e113c4d`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:36 GMT
ADD file:53e587afdbeaee60cc14bd95907f14c8303c04b98c72f98e2c54d4343f15dd38 in / 
# Tue, 12 Jan 2021 00:32:37 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:57:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 03:57:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:42 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:42 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:42 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:42 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:56:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:18:45 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:18:45 GMT
ENV ORIENTDB_VERSION=2.0.18
# Mon, 01 Feb 2021 22:18:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Mon, 01 Feb 2021 22:18:46 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Mon, 01 Feb 2021 22:18:51 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:18:51 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:18:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:18:51 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:18:51 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:18:52 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:18:52 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b9a857cbf04d2c0d2f0f6b73e894b20a977a6d3b6edd9e27d080e03142954950`  
		Last Modified: Tue, 12 Jan 2021 00:38:49 GMT  
		Size: 50.4 MB (50399171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d557ee20540b597f518df05bc6888778cfc92bf46040c701d4a622389feb6807`  
		Last Modified: Tue, 12 Jan 2021 04:05:56 GMT  
		Size: 7.8 MB (7812018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ca4f00c2e4896c65625d678544b764d7483dca9dcab92b62093db72f21d3e`  
		Last Modified: Tue, 12 Jan 2021 04:05:55 GMT  
		Size: 10.0 MB (9996375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667fd949ed9338da3c1e09f9b75408c214368c637c448e0fd839467f6f7717b5`  
		Last Modified: Tue, 12 Jan 2021 04:06:20 GMT  
		Size: 51.8 MB (51830144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a945768a17999f090b8cc2ca5b0f89742cd646480cec3e3b146ba8d2c33333`  
		Last Modified: Mon, 01 Feb 2021 20:09:02 GMT  
		Size: 5.6 MB (5587010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7094777fa8f81d0dda6397635f5e98d4aadfc223af1384ba75525c1b2d1f1f`  
		Last Modified: Mon, 01 Feb 2021 20:11:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01ae7a16c097d7a24db8917a7e58332cbef73819d163aa3858683ca929cd11b`  
		Last Modified: Mon, 01 Feb 2021 20:11:18 GMT  
		Size: 105.9 MB (105913845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3427a4c38412b4666868f987a9967b34ddc658bcbebcb4b6193cb7e128013f48`  
		Last Modified: Mon, 01 Feb 2021 22:20:18 GMT  
		Size: 46.6 MB (46586555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.0.18`

```console
$ docker pull orientdb@sha256:ef891059b67551d212004803f93dabfa4d056bd156118d0f6421d3b5ff3c6c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.0.18` - linux; amd64

```console
$ docker pull orientdb@sha256:78d144d6d457a53cd949d49b843f15b471d696d214197241ebe0b863a68aea5e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278125331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9a831aeda29d7cd4184dcc6ffa2db62e57ba31cd15907d9975849a6e113c4d`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:36 GMT
ADD file:53e587afdbeaee60cc14bd95907f14c8303c04b98c72f98e2c54d4343f15dd38 in / 
# Tue, 12 Jan 2021 00:32:37 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:57:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 03:57:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:42 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:42 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:42 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:42 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:56:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:18:45 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:18:45 GMT
ENV ORIENTDB_VERSION=2.0.18
# Mon, 01 Feb 2021 22:18:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Mon, 01 Feb 2021 22:18:46 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Mon, 01 Feb 2021 22:18:51 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:18:51 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:18:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:18:51 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:18:51 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:18:52 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:18:52 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b9a857cbf04d2c0d2f0f6b73e894b20a977a6d3b6edd9e27d080e03142954950`  
		Last Modified: Tue, 12 Jan 2021 00:38:49 GMT  
		Size: 50.4 MB (50399171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d557ee20540b597f518df05bc6888778cfc92bf46040c701d4a622389feb6807`  
		Last Modified: Tue, 12 Jan 2021 04:05:56 GMT  
		Size: 7.8 MB (7812018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ca4f00c2e4896c65625d678544b764d7483dca9dcab92b62093db72f21d3e`  
		Last Modified: Tue, 12 Jan 2021 04:05:55 GMT  
		Size: 10.0 MB (9996375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667fd949ed9338da3c1e09f9b75408c214368c637c448e0fd839467f6f7717b5`  
		Last Modified: Tue, 12 Jan 2021 04:06:20 GMT  
		Size: 51.8 MB (51830144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a945768a17999f090b8cc2ca5b0f89742cd646480cec3e3b146ba8d2c33333`  
		Last Modified: Mon, 01 Feb 2021 20:09:02 GMT  
		Size: 5.6 MB (5587010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7094777fa8f81d0dda6397635f5e98d4aadfc223af1384ba75525c1b2d1f1f`  
		Last Modified: Mon, 01 Feb 2021 20:11:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01ae7a16c097d7a24db8917a7e58332cbef73819d163aa3858683ca929cd11b`  
		Last Modified: Mon, 01 Feb 2021 20:11:18 GMT  
		Size: 105.9 MB (105913845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3427a4c38412b4666868f987a9967b34ddc658bcbebcb4b6193cb7e128013f48`  
		Last Modified: Mon, 01 Feb 2021 22:20:18 GMT  
		Size: 46.6 MB (46586555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.1`

```console
$ docker pull orientdb@sha256:e844583054bd176a5660b760593b27bc2a8f8ccbe01657831851c7cf31a9b112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.1` - linux; amd64

```console
$ docker pull orientdb@sha256:4a68343356c0844143244dae6c2289d2f47be03daeac932131eba2b73378554d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170243476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b0ea839d6f32800000ce76f74c390cecd88a9aded93caa0f45cd506b947c16`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:18:24 GMT
ENV ORIENTDB_VERSION=2.1.25
# Mon, 01 Feb 2021 22:18:24 GMT
ENV ORIENTDB_DOWNLOAD_MD5=054da3fb7c56e7822b2af116966576ce
# Mon, 01 Feb 2021 22:18:24 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=b7b08242b40117ac8eb9a201f8704bde839dfcb8
# Mon, 01 Feb 2021 22:18:32 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:18:37 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:18:37 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:18:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:18:38 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:18:38 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:18:38 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:18:39 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1f1db632405582c3963540eb888bfa2a5c32e942495773dd02212415392f53`  
		Last Modified: Mon, 01 Feb 2021 22:20:08 GMT  
		Size: 2.6 MB (2614892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5678517c3687c453d114569135c0ea3cd5f97cd5c3f59698216450a020fb6ded`  
		Last Modified: Mon, 01 Feb 2021 22:20:10 GMT  
		Size: 31.1 MB (31087967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.1.25`

```console
$ docker pull orientdb@sha256:e844583054bd176a5660b760593b27bc2a8f8ccbe01657831851c7cf31a9b112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.1.25` - linux; amd64

```console
$ docker pull orientdb@sha256:4a68343356c0844143244dae6c2289d2f47be03daeac932131eba2b73378554d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170243476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b0ea839d6f32800000ce76f74c390cecd88a9aded93caa0f45cd506b947c16`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:18:24 GMT
ENV ORIENTDB_VERSION=2.1.25
# Mon, 01 Feb 2021 22:18:24 GMT
ENV ORIENTDB_DOWNLOAD_MD5=054da3fb7c56e7822b2af116966576ce
# Mon, 01 Feb 2021 22:18:24 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=b7b08242b40117ac8eb9a201f8704bde839dfcb8
# Mon, 01 Feb 2021 22:18:32 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:18:37 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:18:37 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:18:38 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:18:38 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:18:38 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:18:38 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:18:39 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1f1db632405582c3963540eb888bfa2a5c32e942495773dd02212415392f53`  
		Last Modified: Mon, 01 Feb 2021 22:20:08 GMT  
		Size: 2.6 MB (2614892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5678517c3687c453d114569135c0ea3cd5f97cd5c3f59698216450a020fb6ded`  
		Last Modified: Mon, 01 Feb 2021 22:20:10 GMT  
		Size: 31.1 MB (31087967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2`

```console
$ docker pull orientdb@sha256:37c26b53f6686216056bd6871145ee01a0653fdb23417172da987808e9c48519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.2` - linux; amd64

```console
$ docker pull orientdb@sha256:b52e461ff1bef201dfbb859ff5d4f4e1a9e7f1530eea0444d7073546c9679856
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185629292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f459a9f51f77a92e79148b320502dbb02a08eaaa20150e69c11534485e653`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:18:00 GMT
ENV ORIENTDB_VERSION=2.2.37
# Mon, 01 Feb 2021 22:18:00 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Mon, 01 Feb 2021 22:18:00 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Mon, 01 Feb 2021 22:18:01 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Mon, 01 Feb 2021 22:18:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:18:10 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:18:11 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:18:11 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:18:11 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:18:11 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:18:11 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:18:12 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07678044786987533d83188e102b541b5c678ba2bb3845952bade04b30284be4`  
		Last Modified: Mon, 01 Feb 2021 22:19:57 GMT  
		Size: 2.6 MB (2614785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5d9d22f0b94608f1a911a8d6d2c48353b9aa088c62087613cba46062b23a7a`  
		Last Modified: Mon, 01 Feb 2021 22:20:00 GMT  
		Size: 46.5 MB (46473890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37`

```console
$ docker pull orientdb@sha256:37c26b53f6686216056bd6871145ee01a0653fdb23417172da987808e9c48519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.2.37` - linux; amd64

```console
$ docker pull orientdb@sha256:b52e461ff1bef201dfbb859ff5d4f4e1a9e7f1530eea0444d7073546c9679856
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185629292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f459a9f51f77a92e79148b320502dbb02a08eaaa20150e69c11534485e653`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:18:00 GMT
ENV ORIENTDB_VERSION=2.2.37
# Mon, 01 Feb 2021 22:18:00 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Mon, 01 Feb 2021 22:18:00 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Mon, 01 Feb 2021 22:18:01 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Mon, 01 Feb 2021 22:18:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:18:10 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:18:11 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:18:11 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:18:11 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:18:11 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:18:11 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:18:12 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07678044786987533d83188e102b541b5c678ba2bb3845952bade04b30284be4`  
		Last Modified: Mon, 01 Feb 2021 22:19:57 GMT  
		Size: 2.6 MB (2614785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5d9d22f0b94608f1a911a8d6d2c48353b9aa088c62087613cba46062b23a7a`  
		Last Modified: Mon, 01 Feb 2021 22:20:00 GMT  
		Size: 46.5 MB (46473890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37-spatial`

```console
$ docker pull orientdb@sha256:a84fb6c86c02021d00b2f29a732d3f68a826328bee5f3d1b90de06c22b19e60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:2.2.37-spatial` - linux; amd64

```console
$ docker pull orientdb@sha256:a27e34bf06e60a207ff8023a564e9760216449f8b9b2e33ac87aa3cd7f1e426c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186831870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06846b54ff52a5ea574a518e2deb603a8ae0e994245f1db261e0f69e8ed693`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:18:00 GMT
ENV ORIENTDB_VERSION=2.2.37
# Mon, 01 Feb 2021 22:18:00 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Mon, 01 Feb 2021 22:18:00 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Mon, 01 Feb 2021 22:18:01 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Mon, 01 Feb 2021 22:18:07 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:18:10 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:18:11 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:18:11 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:18:11 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:18:11 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:18:11 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:18:12 GMT
CMD ["server.sh"]
# Mon, 01 Feb 2021 22:18:17 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_MD5=9f64ab5e959f5d9ad9ea5195d6d621d2
# Mon, 01 Feb 2021 22:18:17 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_SHA1=1748c9779ea7a8cb8fc068fcabf960e1778e8a19
# Mon, 01 Feb 2021 22:18:17 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-spatial/2.2.37/orientdb-spatial-2.2.37-dist.jar
# Mon, 01 Feb 2021 22:18:18 GMT
RUN wget $ORIENTDB_DOWNLOAD_SPATIAL_URL     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_MD5 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | md5sum -c -     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_SHA1 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | sha1sum -c -     && mv orientdb-spatial-*-dist.jar /orientdb/lib/
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07678044786987533d83188e102b541b5c678ba2bb3845952bade04b30284be4`  
		Last Modified: Mon, 01 Feb 2021 22:19:57 GMT  
		Size: 2.6 MB (2614785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5d9d22f0b94608f1a911a8d6d2c48353b9aa088c62087613cba46062b23a7a`  
		Last Modified: Mon, 01 Feb 2021 22:20:00 GMT  
		Size: 46.5 MB (46473890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9fe7b37ad2729a26d5c42882787a7b0ae9274cf76a03de44589117eb43bc0d`  
		Last Modified: Mon, 01 Feb 2021 22:20:04 GMT  
		Size: 1.2 MB (1202578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0`

```console
$ docker pull orientdb@sha256:3765b381cf119ab194d4ef941f7a9a5633331241ae69802a2a8ea697a69e4b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.0` - linux; amd64

```console
$ docker pull orientdb@sha256:a79b2ce4c68aa478b1fb3b2a2897067f32a03a4a10d941def6d455399e73d653
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176179204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7305b49dfb9d3afbb25f06e5d301156249a049ce2d5aec381c45c74495151e27`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_VERSION=3.0.36
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=bb67dbe7d283ad9087bb86e79a747ab8
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=3025eb137071ce86808e1932f858f48915023c9b
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.36/orientdb-community-3.0.36.tar.gz
# Mon, 01 Feb 2021 22:17:26 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:17:31 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:17:31 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:17:31 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:17:31 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:17:32 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:17:32 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:17:32 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef645fe95ea6a5c9ef4c298dbe72c287caec4fa3bfc718524be435f66cc25cef`  
		Last Modified: Mon, 01 Feb 2021 22:19:39 GMT  
		Size: 2.6 MB (2614814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3097ff8ec5c954a2ba405608fa1339f483dbfd4dea105dd02ae3cb793858ccb2`  
		Last Modified: Mon, 01 Feb 2021 22:19:42 GMT  
		Size: 37.0 MB (37023773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.36`

```console
$ docker pull orientdb@sha256:3765b381cf119ab194d4ef941f7a9a5633331241ae69802a2a8ea697a69e4b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.0.36` - linux; amd64

```console
$ docker pull orientdb@sha256:a79b2ce4c68aa478b1fb3b2a2897067f32a03a4a10d941def6d455399e73d653
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176179204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7305b49dfb9d3afbb25f06e5d301156249a049ce2d5aec381c45c74495151e27`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_VERSION=3.0.36
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_DOWNLOAD_MD5=bb67dbe7d283ad9087bb86e79a747ab8
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=3025eb137071ce86808e1932f858f48915023c9b
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.36/orientdb-community-3.0.36.tar.gz
# Mon, 01 Feb 2021 22:17:26 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:17:31 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:17:31 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:17:31 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:17:31 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:17:32 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:17:32 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:17:32 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef645fe95ea6a5c9ef4c298dbe72c287caec4fa3bfc718524be435f66cc25cef`  
		Last Modified: Mon, 01 Feb 2021 22:19:39 GMT  
		Size: 2.6 MB (2614814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3097ff8ec5c954a2ba405608fa1339f483dbfd4dea105dd02ae3cb793858ccb2`  
		Last Modified: Mon, 01 Feb 2021 22:19:42 GMT  
		Size: 37.0 MB (37023773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.36-tp3`

```console
$ docker pull orientdb@sha256:9b18324e78b527fd05e8e568f5ec5af624bbf3cc46bb3f841d74340df2043487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.0.36-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:8b2697a6d68a9029ee5fa3e7be623579a4bcd96343333fa91d0a228b7fb03cb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203199395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb03a6c5340a5c3e39274464591dd1e728ef8633e033364fed98f9d6a635160`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_VERSION=3.0.36
# Mon, 01 Feb 2021 22:17:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=60e18af604ac757f3e41fe67b5961f01
# Mon, 01 Feb 2021 22:17:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8c9ffe0ee9ae69f5f5faee33a3ba5a88e3e09483
# Mon, 01 Feb 2021 22:17:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.36/orientdb-tp3-3.0.36.tar.gz
# Mon, 01 Feb 2021 22:17:45 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:17:51 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:17:52 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Mon, 01 Feb 2021 22:17:52 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:17:52 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:17:52 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:17:53 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:17:53 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:17:53 GMT
EXPOSE 8182
# Mon, 01 Feb 2021 22:17:53 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ce704ee1313e2e6b9d735233cad2a8dafc7c90eca12be81545263593122570`  
		Last Modified: Mon, 01 Feb 2021 22:19:47 GMT  
		Size: 2.6 MB (2614843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f950e39dddacfe72e6619c70832ddc9424c3f33431c1ca18e319449c14a29`  
		Last Modified: Mon, 01 Feb 2021 22:19:51 GMT  
		Size: 64.0 MB (64042560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad80ec600459fbb8bd4da36bfb43ffbb7634fc95a9658dceba5c16bb7becec92`  
		Last Modified: Mon, 01 Feb 2021 22:19:46 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0-tp3`

```console
$ docker pull orientdb@sha256:9b18324e78b527fd05e8e568f5ec5af624bbf3cc46bb3f841d74340df2043487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.0-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:8b2697a6d68a9029ee5fa3e7be623579a4bcd96343333fa91d0a228b7fb03cb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203199395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb03a6c5340a5c3e39274464591dd1e728ef8633e033364fed98f9d6a635160`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:17:19 GMT
ENV ORIENTDB_VERSION=3.0.36
# Mon, 01 Feb 2021 22:17:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=60e18af604ac757f3e41fe67b5961f01
# Mon, 01 Feb 2021 22:17:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=8c9ffe0ee9ae69f5f5faee33a3ba5a88e3e09483
# Mon, 01 Feb 2021 22:17:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.36/orientdb-tp3-3.0.36.tar.gz
# Mon, 01 Feb 2021 22:17:45 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:17:51 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:17:52 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Mon, 01 Feb 2021 22:17:52 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:17:52 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:17:52 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:17:53 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:17:53 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:17:53 GMT
EXPOSE 8182
# Mon, 01 Feb 2021 22:17:53 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ce704ee1313e2e6b9d735233cad2a8dafc7c90eca12be81545263593122570`  
		Last Modified: Mon, 01 Feb 2021 22:19:47 GMT  
		Size: 2.6 MB (2614843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880f950e39dddacfe72e6619c70832ddc9424c3f33431c1ca18e319449c14a29`  
		Last Modified: Mon, 01 Feb 2021 22:19:51 GMT  
		Size: 64.0 MB (64042560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad80ec600459fbb8bd4da36bfb43ffbb7634fc95a9658dceba5c16bb7becec92`  
		Last Modified: Mon, 01 Feb 2021 22:19:46 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:52cf9571335deb09ae1997663addda05b5d6c0377db7dc3bb7385665c22298c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:a0945d81c742898940f9cef6909734c191133a5e03a8a1e43a605fe8944a8c00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191587437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e895fad423e4075c4a219aa1c55332cc7caed2fe12dc53e56a61886952139713`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:16:38 GMT
ENV ORIENTDB_VERSION=3.1.7
# Mon, 01 Feb 2021 22:16:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0fc8324fc463488ff5cc43ad7fad76c7
# Mon, 01 Feb 2021 22:16:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=aeaec1cfba7c3a9eb7d8959aa23a568305c3be14
# Mon, 01 Feb 2021 22:16:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.7/orientdb-community-3.1.7.tar.gz
# Mon, 01 Feb 2021 22:16:46 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:16:51 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:16:51 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:16:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:16:51 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:16:52 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:16:52 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:16:52 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34276863638fca6d83cf0fb9af35ab02e018ab2d6662226c98bd92e9ece79b9c`  
		Last Modified: Mon, 01 Feb 2021 22:19:15 GMT  
		Size: 2.6 MB (2614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f2a2dfbae2d6eb3c7ee1be7fc8384d5276a05469f241307e5410982b17940a`  
		Last Modified: Mon, 01 Feb 2021 22:19:19 GMT  
		Size: 52.4 MB (52432012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.7`

```console
$ docker pull orientdb@sha256:52cf9571335deb09ae1997663addda05b5d6c0377db7dc3bb7385665c22298c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.1.7` - linux; amd64

```console
$ docker pull orientdb@sha256:a0945d81c742898940f9cef6909734c191133a5e03a8a1e43a605fe8944a8c00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191587437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e895fad423e4075c4a219aa1c55332cc7caed2fe12dc53e56a61886952139713`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:16:38 GMT
ENV ORIENTDB_VERSION=3.1.7
# Mon, 01 Feb 2021 22:16:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0fc8324fc463488ff5cc43ad7fad76c7
# Mon, 01 Feb 2021 22:16:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=aeaec1cfba7c3a9eb7d8959aa23a568305c3be14
# Mon, 01 Feb 2021 22:16:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.7/orientdb-community-3.1.7.tar.gz
# Mon, 01 Feb 2021 22:16:46 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:16:51 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:16:51 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:16:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:16:51 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:16:52 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:16:52 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:16:52 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34276863638fca6d83cf0fb9af35ab02e018ab2d6662226c98bd92e9ece79b9c`  
		Last Modified: Mon, 01 Feb 2021 22:19:15 GMT  
		Size: 2.6 MB (2614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f2a2dfbae2d6eb3c7ee1be7fc8384d5276a05469f241307e5410982b17940a`  
		Last Modified: Mon, 01 Feb 2021 22:19:19 GMT  
		Size: 52.4 MB (52432012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.7-tp3`

```console
$ docker pull orientdb@sha256:4adf2bda6652ee2c8da5e21f1bb296ac419a3c817511bc38fe65d2931050b111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.1.7-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:21a322906c835885066e6cb7c60131914453eabaabb5437ce5c759b621c80d81
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215587120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c6cdc27ecfb4e4d699ff593e0815f0d8a9ebecf2b8e5fc32d72b73d6cb6835`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:16:38 GMT
ENV ORIENTDB_VERSION=3.1.7
# Mon, 01 Feb 2021 22:16:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=bb6400da14765fa94e973c24a38ee925
# Mon, 01 Feb 2021 22:16:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1c89c4ef68f1d9d428ae812f25fa153c9562bc9
# Mon, 01 Feb 2021 22:16:58 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.7/orientdb-tp3-3.1.7.tar.gz
# Mon, 01 Feb 2021 22:17:04 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:17:11 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:17:12 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Mon, 01 Feb 2021 22:17:12 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:17:12 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:17:12 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:17:13 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:17:13 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:17:13 GMT
EXPOSE 8182
# Mon, 01 Feb 2021 22:17:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa675cd70aaecf6008f865fd9b20aabf3e4712c0a282e4830ac501b914de9b16`  
		Last Modified: Mon, 01 Feb 2021 22:19:25 GMT  
		Size: 2.6 MB (2614810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb4246847a5ab0d50d6c692f29a589bcd514b1c99620cd57f416a2d08dc2464`  
		Last Modified: Mon, 01 Feb 2021 22:19:29 GMT  
		Size: 76.4 MB (76430317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceb2480d830a17322b29475d5249555e019efcd9857f2faf86d9e4c1cd3dd7d`  
		Last Modified: Mon, 01 Feb 2021 22:19:24 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:4adf2bda6652ee2c8da5e21f1bb296ac419a3c817511bc38fe65d2931050b111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:21a322906c835885066e6cb7c60131914453eabaabb5437ce5c759b621c80d81
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215587120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c6cdc27ecfb4e4d699ff593e0815f0d8a9ebecf2b8e5fc32d72b73d6cb6835`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:16:38 GMT
ENV ORIENTDB_VERSION=3.1.7
# Mon, 01 Feb 2021 22:16:57 GMT
ENV ORIENTDB_DOWNLOAD_MD5=bb6400da14765fa94e973c24a38ee925
# Mon, 01 Feb 2021 22:16:57 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f1c89c4ef68f1d9d428ae812f25fa153c9562bc9
# Mon, 01 Feb 2021 22:16:58 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.7/orientdb-tp3-3.1.7.tar.gz
# Mon, 01 Feb 2021 22:17:04 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:17:11 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:17:12 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Mon, 01 Feb 2021 22:17:12 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:17:12 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:17:12 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:17:13 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:17:13 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:17:13 GMT
EXPOSE 8182
# Mon, 01 Feb 2021 22:17:13 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa675cd70aaecf6008f865fd9b20aabf3e4712c0a282e4830ac501b914de9b16`  
		Last Modified: Mon, 01 Feb 2021 22:19:25 GMT  
		Size: 2.6 MB (2614810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb4246847a5ab0d50d6c692f29a589bcd514b1c99620cd57f416a2d08dc2464`  
		Last Modified: Mon, 01 Feb 2021 22:19:29 GMT  
		Size: 76.4 MB (76430317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceb2480d830a17322b29475d5249555e019efcd9857f2faf86d9e4c1cd3dd7d`  
		Last Modified: Mon, 01 Feb 2021 22:19:24 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:52cf9571335deb09ae1997663addda05b5d6c0377db7dc3bb7385665c22298c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:a0945d81c742898940f9cef6909734c191133a5e03a8a1e43a605fe8944a8c00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191587437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e895fad423e4075c4a219aa1c55332cc7caed2fe12dc53e56a61886952139713`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:56:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Mon, 01 Feb 2021 19:56:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:56:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:56:58 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:56:58 GMT
ENV JAVA_VERSION=8u282
# Mon, 01 Feb 2021 19:57:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Mon, 01 Feb 2021 22:16:38 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Mon, 01 Feb 2021 22:16:38 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:16:38 GMT
ENV ORIENTDB_VERSION=3.1.7
# Mon, 01 Feb 2021 22:16:39 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0fc8324fc463488ff5cc43ad7fad76c7
# Mon, 01 Feb 2021 22:16:39 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=aeaec1cfba7c3a9eb7d8959aa23a568305c3be14
# Mon, 01 Feb 2021 22:16:39 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.7/orientdb-community-3.1.7.tar.gz
# Mon, 01 Feb 2021 22:16:46 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 22:16:51 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Mon, 01 Feb 2021 22:16:51 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:16:51 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Mon, 01 Feb 2021 22:16:51 GMT
WORKDIR /orientdb
# Mon, 01 Feb 2021 22:16:52 GMT
EXPOSE 2424
# Mon, 01 Feb 2021 22:16:52 GMT
EXPOSE 2480
# Mon, 01 Feb 2021 22:16:52 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf659c946760b22203efd07517094398c96b09cf88600f4fa5246e91aeafe21`  
		Last Modified: Mon, 01 Feb 2021 20:11:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c32a0229c3c9f787abf70622867e8264133206c048a5b9a337e93d1b4ad3d6`  
		Last Modified: Mon, 01 Feb 2021 20:11:45 GMT  
		Size: 106.2 MB (106183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34276863638fca6d83cf0fb9af35ab02e018ab2d6662226c98bd92e9ece79b9c`  
		Last Modified: Mon, 01 Feb 2021 22:19:15 GMT  
		Size: 2.6 MB (2614808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f2a2dfbae2d6eb3c7ee1be7fc8384d5276a05469f241307e5410982b17940a`  
		Last Modified: Mon, 01 Feb 2021 22:19:19 GMT  
		Size: 52.4 MB (52432012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
