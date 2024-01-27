## `openjdk:22-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:d7d3d2ab221bb369df7b95de09c3ab40c117bc528123315b3a7fa9cfddd673ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:965aea6d66737b474d5c3fc238f06b1d75d7601bc6ef2562c6719b011d0f94c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357575933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d326e3159b9dd6bcdb3d5bfeb95909ab7f2626e23d20ef00de11fb14e83606`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:31:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
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
	-	`sha256:30d85599795460b2d9d24c6b87c53ec60555b601705cc83bea31632240500980`  
		Last Modified: Wed, 17 Jan 2024 02:00:06 GMT  
		Size: 64.1 MB (64139892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ac060e671815dc2aae4d2f9421d2c209d49cc889249041e8a62d838d125529`  
		Last Modified: Fri, 26 Jan 2024 23:50:24 GMT  
		Size: 16.9 MB (16945716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ee7085dbeb5d65077fabad788d87bea03e58db7acbeca827d5e923bb1c018`  
		Last Modified: Fri, 26 Jan 2024 23:50:28 GMT  
		Size: 202.9 MB (202882341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d663ab8fd1fa57ccecf70261a8c2f5bc20352dba9eaa14898b32b8b4c9da45b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6e8d057f70a4b1dd6d50428cf5caa5493d75ac12bfe5cec1a51eab27e4f43a`

```dockerfile
```

-	Layers:
	-	`sha256:c1261d5b1c560879c5ffd635ad3b28750a883976683aff89fba5faa0197efd7d`  
		Last Modified: Fri, 26 Jan 2024 23:50:24 GMT  
		Size: 7.1 MB (7116360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d52ae015157654f325f3efd008a254600e207b4f8b550fd2882e27288844db`  
		Last Modified: Fri, 26 Jan 2024 23:50:23 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b814d36329f6c848b84d4a6dde42670641fa4e713d6659cd0a77175bd2e60f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355832147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b63cc634c31f79be124ac3ef37fde6b2b0e0690c79906da1b4f8fbb8ffbad3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
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
	-	`sha256:76b4f1810f998c1f1580e2404b2e7fed8e264902d898bbe531443ea9789b7641`  
		Last Modified: Wed, 17 Jan 2024 02:58:02 GMT  
		Size: 64.0 MB (63991147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb32b79503545458e2fc627360a71ead33be25914626cc424d8226cc3b833f89`  
		Last Modified: Sat, 27 Jan 2024 20:35:05 GMT  
		Size: 17.7 MB (17728784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc035cc92f915af4fed651a698773ffdcbc8fb9963bae8fbf11ed4402674e9b`  
		Last Modified: Sat, 27 Jan 2024 20:51:24 GMT  
		Size: 200.9 MB (200937377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7de2a7e034759656c0cf363c60c3b9b3eeefc6038c5949891605df5c38bb9bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7253611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ece2dd3d4959e3a11a19d6689508b180f4ed72918a91c58ce0788856b80e893`

```dockerfile
```

-	Layers:
	-	`sha256:55f6ac25c80e70727ec7839ccf6ed3f91ffff49af5322637f5ee93e207f05706`  
		Last Modified: Sat, 27 Jan 2024 20:51:21 GMT  
		Size: 7.2 MB (7235187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9d64fa793ceaabd0edfe14430b017947ecb98dd7edd6ff71fcddc26cded208`  
		Last Modified: Sat, 27 Jan 2024 20:51:20 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
