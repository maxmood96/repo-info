## `openjdk:23-jdk-bookworm`

```console
$ docker pull openjdk@sha256:a5103a9b3447eb706080e92b1c303c151e6dd72b46ea4884872c64b857b76b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:25277b211d86df1be39d388992e00147186f6fcaee49198ed217dd58bee6f3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357613672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464f56a3974d6a21e09016f4321ebf957eb121926f0555235164c90713ff873b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5245d215a06cdcb5cdfbd2f3f28dd45f4ff837952fe60ccf39a81028ac73cc9d`  
		Last Modified: Sat, 09 Mar 2024 01:49:16 GMT  
		Size: 16.9 MB (16945890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcffc3470904d6b2ed4173b32740feb204b01ab362b16663513ade6dd3fe946b`  
		Last Modified: Sat, 09 Mar 2024 01:49:19 GMT  
		Size: 202.9 MB (202928272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ca005534e4da2f88b148c2476e9eef4d299c3e6135c62c859fbb19a3188d979f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8248108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292b16cc54f562a18f26032886dd4e55d8edf22cd748342ec1d33cc4893f27a3`

```dockerfile
```

-	Layers:
	-	`sha256:f5cc5eccbbd9390a349360e6f4bce8c9fd2ff0446e683a2477c4803ae0fbe8fb`  
		Last Modified: Sat, 09 Mar 2024 01:49:16 GMT  
		Size: 8.2 MB (8229201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0fb53f066eaa8e8475b52aa86f4f3d1cb8893e3fbed89d00b46e40e705fd90`  
		Last Modified: Sat, 09 Mar 2024 01:49:16 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:95bd6a27bd35e46f41bad336962ae707445c8f6f41f60e3473ede38dc3494e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355693073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8385e35598e3a34b892c71b7f3958712d4b01042764b15d10fcf8f27e3b7ec2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178a6567d064fca050e5c1a2e8dcde52ec79e420186d812482f616cb428d30ad`  
		Last Modified: Sat, 09 Mar 2024 03:58:30 GMT  
		Size: 17.7 MB (17728916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2859a61b88b5011b3e2f9e5e082375fef2cae66e43602a38e7eee343648f6d46`  
		Last Modified: Sat, 09 Mar 2024 03:58:34 GMT  
		Size: 200.8 MB (200799506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7253a4a25a81922a2aed918ec3acdbd0059cd17fff07158502bbcdf9dc69e086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02325b122b2f2299200eade42504d18c7fb76825047f0cc075f1797df310badb`

```dockerfile
```

-	Layers:
	-	`sha256:1b5519ec84200fd3b1d2bb5617d9c69b753e6330ce9dcb1ce9208655bfd6a673`  
		Last Modified: Sat, 09 Mar 2024 03:58:30 GMT  
		Size: 8.4 MB (8365838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f97213ea3cc307eeb1a099d86a28aeab1b70187aa9f72297221329e214a4933`  
		Last Modified: Sat, 09 Mar 2024 03:58:29 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.in-toto+json
