## `openjdk:23-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:25ff8ef889137d61dfc95e1606ed3d909be0573fc315064560a7d97192caf542
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:dc3c1469468f6c778611589a879cc226b776286da66fc76145b9a486b00b2e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366103919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a10315c68094bbb10a8dedf0472ce4cfd13531c21aa786e7766f3e674f288f9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:43 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Thu, 13 Jun 2024 01:20:44 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3873416e6a335157d669c6193a256dfb289331d669d87f200e4eed1f19f9ebb9`  
		Last Modified: Thu, 13 Jun 2024 03:49:40 GMT  
		Size: 64.1 MB (64142031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923497218248ec3acbdb5d993e7549549bef0535dc62623a66d1d60540a8b1c0`  
		Last Modified: Fri, 14 Jun 2024 01:01:20 GMT  
		Size: 16.9 MB (16949367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d096009e14b0a42f5516b5c513d0e93b904dbb43bb4b513cea86733befdcb79`  
		Last Modified: Fri, 14 Jun 2024 01:01:23 GMT  
		Size: 211.4 MB (211385865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2df4c4c918f2d70d4317d792b019114ab02ae1d4b7cf19ba0bbccf57465673c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8240290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb456566b4d183934b45d2b2cd88bf6befe4a6b6ce6929db50fae990de1d2ec`

```dockerfile
```

-	Layers:
	-	`sha256:3f43a2cba3b582e55b63163bf91d792f4bd3d214e20fc924d93f285015f59066`  
		Last Modified: Fri, 14 Jun 2024 01:01:21 GMT  
		Size: 8.2 MB (8221827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc690925fc9d288f9a926936313a38198ba897b020bc40b7c56437a4e302a37`  
		Last Modified: Fri, 14 Jun 2024 01:01:20 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f4aca4b7392c9ba79f94591ecd659c3b5448bd12688c8c1cc9661f518f1065db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364204174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd6a0ffa9f3d48effeda2eadf9aa8f497aaa22c86d58a179b9e800e6ec7902e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84230ae22287ffb8cab5a4fcdafa2c2117dc175cf922927e4f3cf7dac065a66`  
		Last Modified: Thu, 13 Jun 2024 19:55:37 GMT  
		Size: 17.7 MB (17732451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dd69fa5125181aeaed356db1de90950fb0f08de02ca8ca3ad0d23e3c0a4202`  
		Last Modified: Fri, 14 Jun 2024 04:11:37 GMT  
		Size: 209.3 MB (209277014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:08c8b45037c3c1448e83e934d4ca5f45c13d476657aecacaf7c4ef6c807e27c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8378291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5b6bdcf836c57c23ab46c7b3ea5cf3ce5e6cda8cee410c4cac363507fa96a9`

```dockerfile
```

-	Layers:
	-	`sha256:093ca0ebc15eb23954df9ce259c4af67bc8cbf0b009208a6b94b115fa83dc3b5`  
		Last Modified: Fri, 14 Jun 2024 04:11:33 GMT  
		Size: 8.4 MB (8359488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c633dce7d59b7a18af44d5378e3386192174b3dad79db9eaab15a7a5029c0a77`  
		Last Modified: Fri, 14 Jun 2024 04:11:32 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
