## `openjdk:27-ea-bookworm`

```console
$ docker pull openjdk@sha256:92ba54179a26b7318dfe280c666bc61afb50cd6a2c2700be96a3f19c42e70ca4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:1c5cf49cff276d9f7f56ca27565d577dddfbc04c226c6a8408e2194633f5a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.0 MB (381976291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2487f3949002f4161517c82f646409c9797a79707b8f9a80677d312d62fe6aa6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:04:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Dec 2025 00:04:06 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:06 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:06 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7c01867339ff2562e4fc3244c06a462f2b81591779f2f2bfbc09d859b85f1`  
		Last Modified: Tue, 16 Dec 2025 00:04:43 GMT  
		Size: 16.9 MB (16944759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b84449d06afc4cab55dde373574cf0eb0a5434ccc8f37798a373105eb32f1c`  
		Last Modified: Tue, 16 Dec 2025 00:05:09 GMT  
		Size: 228.1 MB (228124939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0870f449d401637e90ebb5c90cc3a63b3043b752ec3e2bb390f773592a29fa4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815c077ba908c094382d57ab7dcab58005ed3aaad9e55c0a2162daa6d0c83311`

```dockerfile
```

-	Layers:
	-	`sha256:36c163c58181bdb8cc98a7f44863bcbb8a5b60cd80ad7f83f7f496f8effe0590`  
		Last Modified: Tue, 16 Dec 2025 01:25:53 GMT  
		Size: 8.7 MB (8668226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10ca57ac249c83f33addf6c66ad98b57a8cedc4f52ba1d135683c6a20742c9b`  
		Last Modified: Tue, 16 Dec 2025 01:25:54 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ea79e43b6b654e9fc7bbdbdedad11d17ff4ffb1670da02d8e12c72154531cd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.1 MB (380110588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6afc4215e9806cf5554298a5b3bf1c250cca50ff751cf114e6e478d5cbea12`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:04:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Dec 2025 00:04:06 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:06 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:06 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f918f3a1d9e98b262e03e793e6afccdfe01032834d505b52336f3251372dfc8`  
		Last Modified: Tue, 16 Dec 2025 00:04:44 GMT  
		Size: 17.7 MB (17728486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f37ddc61d00c32c52e2ac78389588ab54aac1d5bf4a9b61811a3084084ed92`  
		Last Modified: Tue, 16 Dec 2025 00:04:51 GMT  
		Size: 226.1 MB (226053295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d2f87989823d3b723d1a144a78ca0e2620df0d2405386c792c701c9484a29898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58fa6a300ced348b3fd85d45744b8034c7389f2a45f6f7b86dff4f2bd64e98c`

```dockerfile
```

-	Layers:
	-	`sha256:b310a5b8fdf38304c8c565644f68abd8c834a9466795121e223dec380ba9d55d`  
		Last Modified: Tue, 16 Dec 2025 01:26:02 GMT  
		Size: 8.8 MB (8805071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b813db32023b639fa03d777a54c05d081a196cccffdf8431992fa016803994ed`  
		Last Modified: Tue, 16 Dec 2025 01:26:03 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
