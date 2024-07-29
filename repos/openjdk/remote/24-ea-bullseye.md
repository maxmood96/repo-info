## `openjdk:24-ea-bullseye`

```console
$ docker pull openjdk@sha256:41b4d8dadee4206b25199dcee2bc22b94bb7b14d368e3c16fea9d5efd2c73691
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:a9a5a45105e4706765b65ae79618f5c6c2522a1e5ff636a1b85dfaa00cf68658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351339221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4389f1bcbdb8ad72def1518cf9f6097e2596538efe1367af819b17529e118d82`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f91e8777f7997982c6dafd7babc5e4ce362e7a33244678f20f0d0df7282f390`  
		Last Modified: Mon, 29 Jul 2024 16:56:35 GMT  
		Size: 14.1 MB (14071331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add819c7c936eac23eac403d486df6d31871ba31ae46eb0627adb0645dbcadc4`  
		Last Modified: Mon, 29 Jul 2024 16:56:38 GMT  
		Size: 211.8 MB (211830489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:84148866d026dd196322dc6ddf8cb22e6e4418f4e17bc49ee366bb1f239e4440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8212348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12361564ae943af616c0a79357fdb405b8d7e88f0e67727dde8be350d23aa39`

```dockerfile
```

-	Layers:
	-	`sha256:4e834e34e01f391e3e66382ca693dfb0fc3a0ad915f5c6432ed0fc9b68c86372`  
		Last Modified: Mon, 29 Jul 2024 16:56:35 GMT  
		Size: 8.2 MB (8193902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68b3038db2bb0e927392cbcb9822c5d1644996628f1fe82645767a1e8f14f5c`  
		Last Modified: Mon, 29 Jul 2024 16:56:35 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f8e21b1dfdaef3bed6b645cd877c4abf5cdae7518310028c0aa20ab73137d56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349404495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0669c4d57f2add89f2a666ea46074ecc44fa23d7d67bcf0230ed1ac98a5f181`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d2fc617cf24604b5fb20d3ed6e8d19726e946ac82ce538dc06fc0c823a93ca`  
		Last Modified: Mon, 29 Jul 2024 17:01:08 GMT  
		Size: 15.5 MB (15526258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0863c1d66f8e78f2f0ae00c838fa881ea8f993179aa747adef4224b5e8fe524d`  
		Last Modified: Mon, 29 Jul 2024 17:01:12 GMT  
		Size: 209.7 MB (209703927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:77b70d7d96808912a8580a0a47fb3a3937b5cf5f6a170533e5092cbbe84928ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8314398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105abb77b03ea3d469c3506bf944b8cefdb5dad2a3f0b357f2ef61ece5432f41`

```dockerfile
```

-	Layers:
	-	`sha256:bbe72cbfc56781772c838eb9fccfe0740b5af2c29fd7932f0b1cad9741e4d85f`  
		Last Modified: Mon, 29 Jul 2024 17:01:08 GMT  
		Size: 8.3 MB (8295612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fbaaa845ffd722b6c749541a2c498231bef988c347cd60116b07eeb9ac4556`  
		Last Modified: Mon, 29 Jul 2024 17:01:07 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json
