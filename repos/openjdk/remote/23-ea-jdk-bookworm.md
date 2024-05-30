## `openjdk:23-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:40055c150fc6b370442be2e6c7ea25a570568f886757064d43a8f532951c21d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:1741d700d609e0b567dfc67ffea55a1eaff7ee8e2f6ae74e64d65b3885b39b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365309696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b06a5418e91d5d2b80dd48da89c7b7373f567d568ece015136ee34e126179e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 24 May 2024 06:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 May 2024 06:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_VERSION=23-ea+24
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 May 2024 06:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf8ca8dd393257f0cdb4193875b2de67197c376c7c8bd9b8a6273590428a91e`  
		Last Modified: Wed, 29 May 2024 23:01:16 GMT  
		Size: 16.9 MB (16949351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65145882773ed3db07b440a6c36f9385d254ca81a676e158b094764d8f69ecf`  
		Last Modified: Wed, 29 May 2024 23:01:20 GMT  
		Size: 210.6 MB (210591484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1ee59a4e439b795eac14645e97fcae42158e318de7ccc1cb20360d24c2372216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8240242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70623a1389492dc859b447dd745222a78880403f5dcdd3bdfe721a963deca174`

```dockerfile
```

-	Layers:
	-	`sha256:1939ee9882b9ee524e0e0d071d0c8f261afa8e10ff4e43561b81c2ad55819c46`  
		Last Modified: Wed, 29 May 2024 23:01:17 GMT  
		Size: 8.2 MB (8221828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf2b2015acc1a008fee7a0c78356d3fcd324d2f5c9d09e26ef6d3a4b3ec56a3`  
		Last Modified: Wed, 29 May 2024 23:01:16 GMT  
		Size: 18.4 KB (18414 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:37ae50a213019ffe8eaf010f119cd8486c4e60f1510d79226da53308440eee75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363410395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85645143b948b6cbb0bd9b24ad000ee53ac148bd4c1d25aaf127a0e9748a78dc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 24 May 2024 06:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 May 2024 06:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_VERSION=23-ea+24
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 May 2024 06:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ed4c12791345d3f20f66024e1f22275ce507868c508509b83dcf231b1c9adc`  
		Last Modified: Tue, 14 May 2024 01:53:09 GMT  
		Size: 64.0 MB (63994370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b34d2673967b5662ccd5c9732e884134222739b6789a4f4e83385a35d701d`  
		Last Modified: Thu, 30 May 2024 12:47:10 GMT  
		Size: 17.7 MB (17732434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecf6090bb2f37d072e5c6970a01e896738976fd9167caea4635310d034fe33e`  
		Last Modified: Thu, 30 May 2024 12:47:17 GMT  
		Size: 208.5 MB (208483593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:73dbf880116601ba714e935aeea2b197ff94067f910613a9e3bf94116d222344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8378243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06600801b77d88551a8a34d48e6f847d04b98dd4aaaca2eb93588f0c75820d8d`

```dockerfile
```

-	Layers:
	-	`sha256:7daa7d982c75955e6c494d7922002a4b68bc7e205181a133e4d5836c78364c36`  
		Last Modified: Thu, 30 May 2024 12:47:10 GMT  
		Size: 8.4 MB (8359489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b8f2e877519c20d62aafbbf1d8e5bc388d0d168d3a95a2248d1b6911cf223a`  
		Last Modified: Thu, 30 May 2024 12:47:09 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.in-toto+json
