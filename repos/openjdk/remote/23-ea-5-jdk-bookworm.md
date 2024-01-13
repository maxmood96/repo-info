## `openjdk:23-ea-5-jdk-bookworm`

```console
$ docker pull openjdk@sha256:d64ac47a967167357682b31015423f486b00ad4ea2d6c4e3d24ecf804f03e072
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-5-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:34bfd627bb03dac637a7f4ccd1ca7ac332d9099e56f14c829601a7b1754cbc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357868377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2d4e86a6df7159ae1e45ec5312357b2d053d1b75eaa4e8017416beadbf82c0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:35:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d55d1cb1ffb0c7e0438b372a96cc0f23a76c21571fa3e7b7b38e3fbc66a8c3a`  
		Last Modified: Thu, 11 Jan 2024 04:44:54 GMT  
		Size: 64.1 MB (64139713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421b1373c4f22a38fb8d16b0045e6ecabd1369e85ac568d7412e80c0a2fff3c5`  
		Last Modified: Sat, 13 Jan 2024 01:07:16 GMT  
		Size: 16.9 MB (16945685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ac346737b78021a0bd480229bc5f2c2ab6aa135b386d0e2a9320c8bd5a27c2`  
		Last Modified: Sat, 13 Jan 2024 01:07:20 GMT  
		Size: 203.2 MB (203174995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-5-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce537764c5a9a6c24c922432a84dd1cef6198c66f484c060d1cf8d9acd969c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aee9deb6768c5f16b9f1a4004f95c5dcbbcdcd7f5f579b77bdb06b48eb75182`

```dockerfile
```

-	Layers:
	-	`sha256:b992e3ccac3d09610ce84224777566d71726843bb34a46c2ffc1bb91ced4e2cc`  
		Last Modified: Sat, 13 Jan 2024 01:07:15 GMT  
		Size: 7.1 MB (7116352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa28d43ceff24bd39a2f3e8de6dc781eac608c759ba797ab3a7187a9ab387cfb`  
		Last Modified: Sat, 13 Jan 2024 01:07:15 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-5-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9b03f2567a117df7f28b12177b2ef7438e9fec96e59c2632b0c05e1c55f62c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (355986026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11143d0c7657ae912626db321355ad72d8fd40a29e9df7d5a6f4b7220b70f447`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:25:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069a35492a4c5b1727f36b1184c413a96ce816d65578adaf3bce2023a1765c0a`  
		Last Modified: Thu, 11 Jan 2024 09:34:23 GMT  
		Size: 64.0 MB (63990799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428630060163e40cf9f829265e1288a72aa00079dea1b8f66ab032378555b816`  
		Last Modified: Fri, 12 Jan 2024 09:20:46 GMT  
		Size: 17.7 MB (17728761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a2be2b4f46b7c8f02865f97fea887dd58aafcceb527e6d3a0764c9febe8637`  
		Last Modified: Sat, 13 Jan 2024 01:39:45 GMT  
		Size: 201.1 MB (201091627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-5-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7fc088ea6dfdc6d712a338951b492f761e02bf0b448e59cdbeefd1fdf6c19c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7253590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4fed2c0edf9c6c2a5a36d8c8f2f4aee4b3c1ff4a4d8c1a64ff61a7a8f714ac`

```dockerfile
```

-	Layers:
	-	`sha256:d9ff7e7f4cb9f8691193110d6ee701766890b9bd187d2f295a8b20bd0722bc45`  
		Last Modified: Sat, 13 Jan 2024 01:39:40 GMT  
		Size: 7.2 MB (7235183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4adba910e1301f4f6b7a9025cf6b9292c3ab58273b7e843e2df7bd625586797`  
		Last Modified: Sat, 13 Jan 2024 01:39:39 GMT  
		Size: 18.4 KB (18407 bytes)  
		MIME: application/vnd.in-toto+json
