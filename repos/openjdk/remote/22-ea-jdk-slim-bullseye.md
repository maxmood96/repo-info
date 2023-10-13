## `openjdk:22-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:36deaf2c9b804b5613d473dbba9ee575214c803413a5b87b4c6e7466fafcc993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:bea31dbaf8972798d84925b0975b80de8a893f78c9928340a43f07e6978ed9ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238558518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bae74ce500e599e5fe92bdc656333a2d4ae6ceb4443ccc465cee18a20639ce`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 02:49:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 12 Oct 2023 02:49:14 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 02:49:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 02:04:39 GMT
ENV JAVA_VERSION=22-ea+19
# Fri, 13 Oct 2023 02:05:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/19/GPL/openjdk-22-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='70bc0434cc0a8e1fa5351daa062cdd86b29caa784525f22e8a0cc0028e34a157'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/19/GPL/openjdk-22-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='973d8beb242379ed3bec118f7374dc61a99699411c38875ecdf158e506b0a3c0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Oct 2023 02:05:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690ed3663bf98b4029cf613714746f36fc250b67439c8f4bd42130227619fdcc`  
		Last Modified: Thu, 12 Oct 2023 02:50:55 GMT  
		Size: 1.6 MB (1584375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e9fef55425641907aba1404234a1e4ce10f6ee00a33e0a4faa98eaea86bd6`  
		Last Modified: Fri, 13 Oct 2023 02:09:25 GMT  
		Size: 205.6 MB (205556281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:067ac3a375539fa84ca35cf690352753009ec922090784f0a98789d63a27e08b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235400466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6196be03f04765586556d123fa67757fa4225942a0b2ae0bfdd940852ce5036e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:50:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 11 Oct 2023 22:50:55 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:50:55 GMT
ENV LANG=C.UTF-8
# Wed, 11 Oct 2023 22:50:55 GMT
ENV JAVA_VERSION=22-ea+18
# Wed, 11 Oct 2023 22:51:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='07830a4cc21745464a68057e8c441e98d4cd673cd02348e9791d9eafe9f3d0df'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='03432a54970a3005c521d34b44a2438ac28f8fe150bf686e28cea6ea9b2a002e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 11 Oct 2023 22:51:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f730b1d8252d43d9f960a724f9763804c245215a614762e839fb4b06c2c33bf`  
		Last Modified: Wed, 11 Oct 2023 22:53:31 GMT  
		Size: 1.6 MB (1567906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df8f9b917bb67a8dc67a36e4fa358ec7587447ace33c426ea8f89904d6e3d23`  
		Last Modified: Wed, 11 Oct 2023 22:53:43 GMT  
		Size: 203.8 MB (203768474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
