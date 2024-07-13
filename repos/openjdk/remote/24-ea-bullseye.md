## `openjdk:24-ea-bullseye`

```console
$ docker pull openjdk@sha256:00fd827dc1113f85735166b325b4e854541c1efb7b17b8aa416fc5903cdaa0d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:d3aaf1b656b83eb71bec19d22df44dde56ef4ec818ffe8f21fcf4e0c6b6b30df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351126321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eade7ee68cbb823b472247bff046ee928994547c21ce868082b57f3b27fd8ae`
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
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 12 Jul 2024 06:52:24 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='85969884f11f2863595c13dff1cb6f6d94149bbe5188c34f0a7aaa284a545a27'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c719648382b7e5d564dc1d39d4408890d92ce5484fd46a5ef338da7380684ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
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
	-	`sha256:7b78387be2fb71301dbd94ee92d1c44c4c8c9a885913f88b25718af5dae31dcb`  
		Last Modified: Fri, 12 Jul 2024 21:57:19 GMT  
		Size: 14.1 MB (14071345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda5ebee9a71b83f3ccdd1a0d581d56c3936f54bad20a43e479e7042816eae3`  
		Last Modified: Fri, 12 Jul 2024 21:57:22 GMT  
		Size: 211.6 MB (211620805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c3d7c8619ecd500495be30cbb540e444f6d4abee00e706023560687d3c9b7f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5575dc5d13ed5ae7d2dae035f1ed24380c230e8f0039047bc0885fae05f280a9`

```dockerfile
```

-	Layers:
	-	`sha256:ce1f2ffe93783f4b9af38302bd955d6c9d6d22676e6bcc752a3208ea5fb2f33b`  
		Last Modified: Fri, 12 Jul 2024 21:57:20 GMT  
		Size: 8.2 MB (8157352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b269201878c8dc8dd00f0a765e209250073e7fccd23f8b9eb7cb716714579d07`  
		Last Modified: Fri, 12 Jul 2024 21:57:19 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:09801ec96ce3e5efd3e22424b528734a43e9af94d8661fc6fff44045608a0f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349190729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1d783e01dff67144a8fba65383513a9cb6d3e47caa711aa18184c87f686792`
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
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 12 Jul 2024 06:52:24 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='85969884f11f2863595c13dff1cb6f6d94149bbe5188c34f0a7aaa284a545a27'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c719648382b7e5d564dc1d39d4408890d92ce5484fd46a5ef338da7380684ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
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
	-	`sha256:30dfa44008957cc8fd0311b330bc8a4da6e8eee0daf21b187e8f5ca1278b356b`  
		Last Modified: Fri, 12 Jul 2024 22:08:50 GMT  
		Size: 209.5 MB (209498578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e3bc64b6d55aed7f868196f574b07dca3ffc6e5ce9656f60eef4c8dcf6dd0796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e6f581be2a985de3b8fa3f8cd89bb454c8671589784101658abbc0b632cacd`

```dockerfile
```

-	Layers:
	-	`sha256:c44714fe8f3057da3e218623a6aa6c8dac530652f4a526b87c1e164194f59549`  
		Last Modified: Fri, 12 Jul 2024 22:08:45 GMT  
		Size: 8.3 MB (8259062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01689ad4201d336b705986ab9ae81685fdbd793d09118c2ed641dd9b055f2141`  
		Last Modified: Fri, 12 Jul 2024 22:08:42 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.in-toto+json
