## `openjdk:24-jdk-bullseye`

```console
$ docker pull openjdk@sha256:e5613b19c8c26e4083a886c710e7f0d266dde75b0f8627e454fcf330f860b34b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:229765f3c6ed0e7f20af7a2a996da73c66b92dc94d1be4d296cc571c0d996853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (351002344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145309feafb2ff275f069acef77574cc6e06518b06595f927f1e0584d55944e`
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
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
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
	-	`sha256:80932cdaa8c9400ca5a6f7f8ae1126d31d51d4f21a4514c1d8911971580c5dd1`  
		Last Modified: Mon, 08 Jul 2024 20:56:56 GMT  
		Size: 14.1 MB (14071377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8804ea197f02f7efd381ec9e5a5bae4c217cda039499db6d00b8a5fa93401`  
		Last Modified: Mon, 08 Jul 2024 20:56:59 GMT  
		Size: 211.5 MB (211496796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9a2c553721fc3f003da624218bed5a1ae95f340dd17d64f115ad20f76305b73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a29375444737dc76544f3e041fd31d46edea78c934f04f7f7103011ef703aad`

```dockerfile
```

-	Layers:
	-	`sha256:628f38a24a5fc7f5f50ad1121df36cc71a64951a5cb75a5b75aa5f55d7906806`  
		Last Modified: Mon, 08 Jul 2024 20:56:56 GMT  
		Size: 8.2 MB (8157352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ced67127f13682a3ec845a73f9c54b7c93e95982326cd90444fdfd96b9fa3aa0`  
		Last Modified: Mon, 08 Jul 2024 20:56:56 GMT  
		Size: 18.4 KB (18445 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7e76a566ae9b40fbde4e615bc3d606271976284a248995b7d1c11f025e8d0c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349057373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff6fc8789b85cb54e79f8724d36d80f1548ce90d02065a4f05dc890b1dd9c1`
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
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
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
	-	`sha256:ddc7d1e28c547cc9851a874cc742840712e2256f0ae225576248132254a36b15`  
		Last Modified: Mon, 08 Jul 2024 21:01:14 GMT  
		Size: 15.5 MB (15525950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d0ee58f8ae7310163e5c052ffc9c6a25a99abc60f200731e07ffb3880a8ad7`  
		Last Modified: Mon, 08 Jul 2024 21:01:25 GMT  
		Size: 209.4 MB (209365148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2910161529558df03e44eb80d1e03811f8c4e3902b6153ee34a8285c73baee8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d190c78535ef1a392d7aaa87f3bd90523cb30612b8cd307fa81ef1682d4a657`

```dockerfile
```

-	Layers:
	-	`sha256:6ae5ecb374a77fe74c4052030ebcac2c492954f79740dd107b2ce87b29c891d1`  
		Last Modified: Mon, 08 Jul 2024 21:01:14 GMT  
		Size: 8.3 MB (8259062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef041bc67f1c1e2d15622b459991ac49c3ac9104212a647a8cd1eb5c80d5a8c7`  
		Last Modified: Mon, 08 Jul 2024 21:01:13 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json
