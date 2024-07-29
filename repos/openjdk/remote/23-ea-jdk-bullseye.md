## `openjdk:23-ea-jdk-bullseye`

```console
$ docker pull openjdk@sha256:cd3b77d136ffdd6c611a3421427c0e3424234bb2e87557fb4997616800f9d515
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:e9f96b4020e399ce3ec5c1f406b6499ae625e11f77b2e3af0e6b9ff4035ccad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350933990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539b618f1caa42bf57d50c0fe499bc5d3d1be8fdf9eef70b83e6ab0c441bad42`
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
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
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
	-	`sha256:c076566ac0276b65def1bdfd8c557aebce08fc4211b1e740617c6327c02c6828`  
		Last Modified: Mon, 29 Jul 2024 16:56:47 GMT  
		Size: 14.1 MB (14071305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607ce9b5a22b6888a4e4e2a75f947a4b05f41fe25dcd980a06be134e5a41605d`  
		Last Modified: Mon, 29 Jul 2024 16:56:51 GMT  
		Size: 211.4 MB (211425284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f29980e5185c1ccc4609507a68ed37f45837c29a433a08674850f9435544672a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8212373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9876265a0232a3bd24455ffca462d66e261876d812f7daa7f5b7439f29287653`

```dockerfile
```

-	Layers:
	-	`sha256:902d7bd2aa31227e8c2b0e53a25b9cae977a1b5139d60deb02f7333dfdbe04f5`  
		Last Modified: Mon, 29 Jul 2024 16:56:47 GMT  
		Size: 8.2 MB (8193910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2122558f88977e0bbea2e56b583b2cc1bf29330894665a2a50245e33ff7674a3`  
		Last Modified: Mon, 29 Jul 2024 16:56:46 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2846485a7002c08f0fdee05466a454e77f0016be7f3abd8cf07a3e5c1b85f48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348988415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25752f6fc7b56ca41bd73c2759694e152b489b3c475e17d99b6138f2aa17b93d`
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
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
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
	-	`sha256:9f24090511e2b016f97b363b42aac56a26e49bfee69a7f802544ffe7e10d3cf7`  
		Last Modified: Mon, 29 Jul 2024 17:06:16 GMT  
		Size: 209.3 MB (209287847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:dd22f98433576490e4d1f394b4a705ba821ec978df35dac74c4ed72cfd6f9a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8314423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c81f02f60eb12b5c0aeda5066e3392833e7b5cfc30d234abeac2fd3b0dad51`

```dockerfile
```

-	Layers:
	-	`sha256:154c9dfa146a0b6767a634c57476d33e6bc1764cc66cab8a7aa10ddd1ecaafe1`  
		Last Modified: Mon, 29 Jul 2024 17:06:12 GMT  
		Size: 8.3 MB (8295620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b099904f55ad7b18428f8c7109b54fe7acf8c5d6f94cc25d962d71a33116d6`  
		Last Modified: Mon, 29 Jul 2024 17:06:11 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
