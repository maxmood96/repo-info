## `openjdk:24-ea-1-bookworm`

```console
$ docker pull openjdk@sha256:e9c6019d0d571f0a00d6ad2a61644c387f22b8374bf276fed44bd79b79c421b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-1-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:595a2f88cfc5393cbe8e412471020d772022a4e2c2793a2c25ba7738005207d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366172480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50c696d20244188f1f08b560e4d7232c1998a2e2c267d092ca5e0b9b93772bc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 11 Jun 2024 06:58:53 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
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
	-	`sha256:9da8d5b3a58a1f848fa18222bb8bfd3292706c834aaa383fc3cc021c03ebcae3`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 16.9 MB (16949340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b89e226fd4b820bf247d0b0ee671164e81b509b338b67f425de02af93c2fde6`  
		Last Modified: Thu, 13 Jun 2024 18:29:48 GMT  
		Size: 211.5 MB (211454453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-1-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:95935efd2581d4ee2fe694332fca75308aeac9496de0e49ab4bc977ecece052b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8240263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896869d1be0b40c73cffb79a277360c408efb0515970101c9688b67c88edf52`

```dockerfile
```

-	Layers:
	-	`sha256:eef5208bcc5e5bb9336287e0660f09abba9850d09f168a35f17f1b1dbca04360`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 8.2 MB (8221817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae838b3d9269d0df4e049e683025346e6a2beed9c7ba66934c14cf453e0a36cd`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-1-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:573136ce136b6f25f0848c40e23cd0ea42f5536f1076b63904dd2cee2239b764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364261416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f9c2af230466fb24ff42e60745c9198bdf72f31bda8a21d77f10c886c4b04d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 11 Jun 2024 06:58:53 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
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
	-	`sha256:cbf0bf39f17ad05e4f2c1c840b669305607cf0f0edf1fe98449cd46dc48c656b`  
		Last Modified: Thu, 13 Jun 2024 19:55:44 GMT  
		Size: 209.3 MB (209334256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-1-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f1301a97a4e1923e215782df9abfabcbfec1f2390dbd5a52706ee04c93f963ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8378263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e1a2d21476640b911bb0f59e09c49ee80adcc1fbe42e77bf4c52736b83f699`

```dockerfile
```

-	Layers:
	-	`sha256:63c782369833eb38b4b49eceaefec91dd9c990ad87210a06ac339d9307d9e8c1`  
		Last Modified: Thu, 13 Jun 2024 19:55:37 GMT  
		Size: 8.4 MB (8359478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1bb90c5e0228a0e4bbdb70ee3ed50751088f8876047a1db193e57d06e23e08`  
		Last Modified: Thu, 13 Jun 2024 19:55:36 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.in-toto+json
