## `openjdk:27-ea-4-trixie`

```console
$ docker pull openjdk@sha256:9b3c9dab9235175b77718e179374d7bc14efe2d9e0ac2999cf03939919d69e3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-4-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:a98891c5f78c35d14fc200e081767f617201c5b050e3d409012649d9c35dab3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.8 MB (386779643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6cf4e7f98adab6a00e51bafeca8529f0be667928ecc87aca2b4eae34ad6caf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 12 Jan 2026 20:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 12 Jan 2026 20:08:39 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:39 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:39 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:08:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e71b21dbac6b4cd3d09fcb642e345ddd14f9f7fa21157d46d6f01af6f688d9f`  
		Last Modified: Mon, 12 Jan 2026 20:09:18 GMT  
		Size: 16.1 MB (16062743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4807e57ac0375e60507253de0bbae60c7c6261451c8bf0fc93fbfc3416830628`  
		Last Modified: Mon, 12 Jan 2026 20:12:39 GMT  
		Size: 228.0 MB (228036091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4873f3bb4a9e6c87a74a885e54c11d3fdf633788d0e1fd08b6ec6ac7ccc94ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d386f67774c7d8bbdb061707dcaeffec936d187777f0c6970b2b615847d9ff`

```dockerfile
```

-	Layers:
	-	`sha256:ade335cd90194962b8afc7490158e140ef0d05d8ed283321f4ed2e3088c85c07`  
		Last Modified: Mon, 12 Jan 2026 22:27:06 GMT  
		Size: 8.5 MB (8509971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f665dc7f58bfaeb8f8682446ba834247b2dc5ccb947481c299f76b1a5de4fe`  
		Last Modified: Mon, 12 Jan 2026 22:27:07 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-4-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:93d325fe591f280b78cc7c4658c55eea4532c5a0a9d8e355f93b3ed74dbbdd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384286083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b8366366b02b02e2c29060048afa92eca8d515824d7931a0b0889c99d6a0c2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 12 Jan 2026 20:08:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:09:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 12 Jan 2026 20:09:16 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:09:16 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:09:16 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:09:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:09:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5854558bb92c28a440afd3316378b8e1fe545e1223a9509df1737847f1ff2c06`  
		Last Modified: Mon, 12 Jan 2026 20:09:07 GMT  
		Size: 16.1 MB (16071534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d266f691b548bf1b5ce879d0e7d3cbbd7d50bff5ba57090109fae0b9eaa54f83`  
		Last Modified: Mon, 12 Jan 2026 20:10:10 GMT  
		Size: 226.0 MB (225959527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:3a61755e13b917cc999a9af0de0d8a3ddb0ba7b8a9f393b8804417e39dcf6f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff706ec39abcc1d3a5b9a3eca7c266460e6c183c6139a6b866df47edf2ded4d7`

```dockerfile
```

-	Layers:
	-	`sha256:2f16285fa828f48db084d9718180fb6bb4dec4c86a654b9a792ebd3ad73957d1`  
		Last Modified: Mon, 12 Jan 2026 22:27:15 GMT  
		Size: 8.7 MB (8704761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c06653cee40945089316416fe22d9c814f258f00144e3c97f8fe287118270bf`  
		Last Modified: Mon, 12 Jan 2026 22:27:16 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
