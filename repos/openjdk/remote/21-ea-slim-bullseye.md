## `openjdk:21-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:14bcbfd46fbd58d4f5de7a6750e4bdc1e2424e15812adf60e903e0ebe4eda29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:fb9239a590fe8a0f82da51003f771d02fd7390b4c394e95189d511232810bd12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232473793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62e89b9a3bbf889a1eb7ee5b3fe63731701925ecbf1e3b5cf6f81bfd0cfa516`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 07:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 07:04:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 11 Jan 2023 07:04:10 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 07:04:10 GMT
ENV LANG=C.UTF-8
# Fri, 13 Jan 2023 00:29:21 GMT
ENV JAVA_VERSION=21-ea+5
# Fri, 13 Jan 2023 00:29:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/5/GPL/openjdk-21-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2dba614859e77c261a7a30b3019b05dc1e7b5651d065de741426ea540a4ba264'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/5/GPL/openjdk-21-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='621f8196ad96481076d3730496db77ff154976c81798fc7ff3064cd1deeacdb8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Jan 2023 00:29:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec49d0093a3b27f87b047abc2b89aef94d6db65ce71e6660520e4b01f9ceae25`  
		Last Modified: Wed, 11 Jan 2023 07:11:03 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24041c0afdf7b7a9a7a4675bcecff1c44dce36c146f749566bacce79fe7f5692`  
		Last Modified: Fri, 13 Jan 2023 00:36:59 GMT  
		Size: 199.5 MB (199494531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:88ba4f620a55c99cd49e9e2fbf979974fc475e75a3d37dcbf2073aaff0c25bb1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229563059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6518e2a64abd593bef887b084fc4843515eb2622262023c753cd156c79a1c6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:32:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 11 Jan 2023 13:32:36 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 13:32:36 GMT
ENV LANG=C.UTF-8
# Fri, 13 Jan 2023 00:48:58 GMT
ENV JAVA_VERSION=21-ea+5
# Fri, 13 Jan 2023 00:49:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/5/GPL/openjdk-21-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2dba614859e77c261a7a30b3019b05dc1e7b5651d065de741426ea540a4ba264'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/5/GPL/openjdk-21-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='621f8196ad96481076d3730496db77ff154976c81798fc7ff3064cd1deeacdb8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Jan 2023 00:49:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952b21a8c620d2674eb6bd797758f3f454dc67048f31040dae03e31ad11d9bab`  
		Last Modified: Wed, 11 Jan 2023 13:39:26 GMT  
		Size: 1.6 MB (1566309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3805d8ea648f993cb73c06b767e27b5ede2e1b82dcb876397f2454be9b98d8e5`  
		Last Modified: Fri, 13 Jan 2023 00:56:40 GMT  
		Size: 198.0 MB (197951936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
