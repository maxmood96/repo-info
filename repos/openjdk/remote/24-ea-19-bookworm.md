## `openjdk:24-ea-19-bookworm`

```console
$ docker pull openjdk@sha256:82380cde36c7065c7334e40dbcd67b69008f8d1e57f4a40bf8a37891e820f59b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-19-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:000c5c5258889a2e3ba1a75b9f9ded3db366d9495887950ff6f23336aa297d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367304483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32ee7e4250c964ed89e162927202696f3c38674e6112ca8a8528550a73b379e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 00:48:11 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["bash"]
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 11 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='b283aeaeda2e1fb83a01a61a370e2e95e217a00aa3a51641d1b65244b60b05f6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1f125899b06296b1948e650bece4c424c5ac572793c9446bac6f39c68a4545fd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb9009787730d617460a4d70305e3c54a79f79dadfa6eb7c73ffc8d7d78c16`  
		Last Modified: Thu, 17 Oct 2024 02:59:49 GMT  
		Size: 16.9 MB (16942969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80029f298e2932704fb9e439bbc8508b04928907696281b9a82bae49478ed91f`  
		Last Modified: Thu, 17 Oct 2024 02:59:52 GMT  
		Size: 212.4 MB (212360323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-19-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:869175595c8040e72e250817ed88c697fe5663e1fc7fb3102401f73b741de16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8422017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b8868f7010c4f606c011105c77692cc044a733dbd10f71d2c7f0f071f6ba41`

```dockerfile
```

-	Layers:
	-	`sha256:675ef22377827313e49c49056865babb38c02e82ebe197e16b55b352c072071d`  
		Last Modified: Thu, 17 Oct 2024 02:59:49 GMT  
		Size: 8.4 MB (8403516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf1902e7f6081aa97ef483fb73871258aebedb777683706c82d2099d981eec8`  
		Last Modified: Thu, 17 Oct 2024 02:59:49 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-19-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:929522e5df8654fdd7b931b652ef00ed108168da8d1277dfeafe70f7ddc69a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365505770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825c24a31112a692bb9b702d5b70800a7f7593af39b058c53e7e61e0565656a9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 11 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='b283aeaeda2e1fb83a01a61a370e2e95e217a00aa3a51641d1b65244b60b05f6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1f125899b06296b1948e650bece4c424c5ac572793c9446bac6f39c68a4545fd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdb6174757e63a9a678b86a6e14ffba178a5a7bcf8c6ad7be2972588bbef8bc`  
		Last Modified: Fri, 11 Oct 2024 19:26:56 GMT  
		Size: 17.7 MB (17727210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7bd8345b9c572eeb3690dbdd1db94aa33915e29e23467b04b2670c253df5dc`  
		Last Modified: Fri, 11 Oct 2024 19:27:01 GMT  
		Size: 210.2 MB (210249935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-19-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3539d09567b94f928b1b81135996122a4c9a530e5b72e490531a1b5f3143d782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8558566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b108ad957faf540b61f4f4eccbf247947eae3fdc77414253524c884d5c7d8175`

```dockerfile
```

-	Layers:
	-	`sha256:e9dd5bdf8184c1f1b0af28626f1b608890e5f5ebbb5d201b3050ad772feb2d3b`  
		Last Modified: Fri, 11 Oct 2024 19:26:56 GMT  
		Size: 8.5 MB (8539928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c567adf790b0e7627881241a046fa23f9849b7b4d74a4264bad2db0b89f8a02d`  
		Last Modified: Fri, 11 Oct 2024 19:26:56 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json
