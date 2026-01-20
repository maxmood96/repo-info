## `openjdk:27-ea-4-jdk-trixie`

```console
$ docker pull openjdk@sha256:388010bc58020ba1b0065a50b16501998d46c9ec8191708470fc70c007e60c8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-4-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:8b824d2d290cb8463f86ebcd16dd5b1b18975137a188a02aeecdee6bca282e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.8 MB (386784819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae7c1d26d9d64d23966d8fa8d89a4d48f0f8f92610170e95e3a77be24abe1c2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:55:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 13 Jan 2026 04:55:23 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:55:23 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:55:23 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 04:55:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 04:55:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67111ea63bfde460488eb23e1f1baef8d99f352c068930664b18614193cb977`  
		Last Modified: Tue, 13 Jan 2026 04:53:45 GMT  
		Size: 16.1 MB (16062858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90a482599b7b3485c2f57d68aba4bda6173dab53417c5af7b4b715aae7e16df`  
		Last Modified: Tue, 13 Jan 2026 05:18:13 GMT  
		Size: 228.0 MB (228036154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d7f5de24343fd4eeda20b3e37cb4e1aa1f71f64f80aecd1d863ae6b55fb6fe2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a834d01b4b4aca7b5bac15bb636eb166866dee08897be10d0b3d0479a71b35cf`

```dockerfile
```

-	Layers:
	-	`sha256:4f851ea1f71b8824b2d39f1d5cb16ce9be04b15b78663e73bbdb64c9d16cc2d8`  
		Last Modified: Tue, 13 Jan 2026 07:25:19 GMT  
		Size: 8.5 MB (8511010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc2571f7a0509b1f3b77da5af7dee5ec7d1e822a772a735b5e8528f3c3b3bbb2`  
		Last Modified: Tue, 13 Jan 2026 07:25:20 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-4-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d5bb9faa3f0c76faaeb5154008a686e3154b3a64c6dcb9b54d750544425e093f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384293245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6393f13f3c75b557bca1c597927931f643243df8d3889a4c97474c11f214a4b0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:54:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:55:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 13 Jan 2026 04:55:36 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:55:36 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:55:36 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 04:55:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 04:55:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911bb8418a5b38eedfe35eb7a6d1dca887e2610e8b28f43ffaf4603c1665e858`  
		Last Modified: Tue, 13 Jan 2026 04:55:17 GMT  
		Size: 16.1 MB (16071494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999a16f7d009d3446fe3397c6d75027f4edeeea5bc2da6a39e228eee79cf30c8`  
		Last Modified: Tue, 13 Jan 2026 05:17:40 GMT  
		Size: 226.0 MB (225959519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:fdda62be8aaa6b735baad50e49c166924896d9e274b3cd1b0ee4f294ccfe4a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84cde3234c2ba65e4a0aa8ec28fb35d444a18ab7f582731fa980c198249636a`

```dockerfile
```

-	Layers:
	-	`sha256:cb180598829fb70f9646feec51215d13324afe4ce40d0b9d21f19bcddb6b2e12`  
		Last Modified: Tue, 13 Jan 2026 07:25:27 GMT  
		Size: 8.7 MB (8705800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f310ee0fe092632994c2d772887aedd4b1b67aed77b5ac564715f8ff022d732f`  
		Last Modified: Tue, 13 Jan 2026 07:25:28 GMT  
		Size: 18.0 KB (18014 bytes)  
		MIME: application/vnd.in-toto+json
