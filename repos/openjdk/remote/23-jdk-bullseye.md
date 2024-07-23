## `openjdk:23-jdk-bullseye`

```console
$ docker pull openjdk@sha256:69ec1aea1ed32007fac7cdcbf2fe320a3e227cf40e03571de2a8ad982e3cad63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:d1aaddcd7a577247b7282a36072cbd764529c207285b798bc3f6cc24830bdc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350930808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217e6c6b6e02b39390447b41c714d045f7cdb5130c477eda4788bc0dd01a68f9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jul 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Jul 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 20 Jul 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+33
# Sat, 20 Jul 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='d44748cfdec1fe164da0725a95fb05f7e4b94070a669f2688f8604154d14df5b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='e25276d4f0cf9fb6f67b3a1be8087fbf0cceadfa33cab8ffc17e99c83e105e74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da238dd9d1f579bf4f3cd6589e3ab75747f8ea35be2bf50403f8f3fafa942eea`  
		Last Modified: Tue, 02 Jul 2024 02:01:35 GMT  
		Size: 54.6 MB (54588637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b3238c0509c6ff2874fe4ef33f961d0f59b5cd4367d113541a3a4ca972cbe5`  
		Last Modified: Mon, 22 Jul 2024 21:00:13 GMT  
		Size: 14.1 MB (14071307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d62e693cca03041d541482da485eb4d444b08e04bffd5d2e4b149e568f63b42`  
		Last Modified: Mon, 22 Jul 2024 21:00:15 GMT  
		Size: 211.4 MB (211425330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:502f0581365fe620320e966c598aed7e001d08c4c766cba546adac0961d0ee17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8212373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743aeae947b6fd00db3520caaee6fa3ec49bf15d9c003ec86e81aa0c6837ef16`

```dockerfile
```

-	Layers:
	-	`sha256:6437a465a42ea3323edb252ea3a29f75d8f661ca5f900b8e126b389e6da191bd`  
		Last Modified: Mon, 22 Jul 2024 21:00:12 GMT  
		Size: 8.2 MB (8193910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9ce30fb5ba9cba2a5392f780964bb44665f04d68a354e54bb4feb229d48e375`  
		Last Modified: Mon, 22 Jul 2024 21:00:12 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:595ff7b6e98b5aa101142d9c1674f35b68f5bb7ddc52a165f0b0b975cb8052c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348993210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fb60ccd4ebd1576a09c4014d057af37ff452a2625b2386472ba294278b8967`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d5c261e2789f3ec0c616ba4eb68b8f090db8b916e2deb059a486d6a5bc72c9`  
		Last Modified: Fri, 12 Jul 2024 22:08:44 GMT  
		Size: 15.5 MB (15525876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2bf51c9de98b780fcb06f6bcafa7f609c2186996ac6e7b7255e2e365c8625a`  
		Last Modified: Fri, 12 Jul 2024 22:13:52 GMT  
		Size: 209.3 MB (209301059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:15218aeecbf46404e8e8dbdc73bfcda7c6390b90ca6ee9d5733e4145e27d329b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3f2b8cdd12504ab7d5f0adfcb1110b66d06047814a97fdeea3599e3afc29ed`

```dockerfile
```

-	Layers:
	-	`sha256:1f609a7287728319ff443fc9fbccc17b44fc3b1ddae8f27f81ac05a6e5158ec2`  
		Last Modified: Fri, 12 Jul 2024 22:13:48 GMT  
		Size: 8.3 MB (8259070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3829100ffa59a9e9e1a3e69c1b644552ade1923767d61265bbe03a333b08152d`  
		Last Modified: Fri, 12 Jul 2024 22:13:47 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
