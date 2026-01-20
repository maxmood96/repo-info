## `openjdk:26-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:82ca79ccc53f26a17cb1f8a11656d9dce7523c390692330f409dc9cf28289c28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:606eded06abb5fa7e9118ae2e90a96ebb8b6ad223939594f1818c157a745613d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386717375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a724b16479f3466902d0c1f778ec1b3b5ffc1a9e8e082e38bbb50ebd1e46bd`
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
# Tue, 13 Jan 2026 04:53:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 13 Jan 2026 04:53:09 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:53:09 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:53:09 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 04:53:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 04:53:09 GMT
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
	-	`sha256:74f885500cf54fdd521cc61052aa9f9a0332ab5a3d20a6d6e1f6d520d6f0ee13`  
		Last Modified: Tue, 13 Jan 2026 04:53:38 GMT  
		Size: 228.0 MB (227968710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d5bc77304d2a6bebc6f523983143bad913eaf6d4ec7ae954130d47fb3916b127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5bb3956625370c151eb25c41734b19ef7e1c24ee105a56e5dc6fa4b59825bd`

```dockerfile
```

-	Layers:
	-	`sha256:8c37fbfcd1b1b260302a6113e2cb937f6f497e422783768ef8d1cfb7d3cf0c80`  
		Last Modified: Tue, 13 Jan 2026 07:24:30 GMT  
		Size: 8.5 MB (8511018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91d3f26150c3015e43d34ea9268b94d4a88f0fa3f62a4239df608b96e37ef326`  
		Last Modified: Tue, 13 Jan 2026 07:24:31 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6223363b1649108ad0694612d01967da5928e3598b1c785ef1eb856a1de13240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384219483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe92627413bea0a01d03c0e7a9956b6a39b6c17e74f62db24d015e7954b1e3d`
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
# Tue, 13 Jan 2026 04:54:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 13 Jan 2026 04:54:39 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:54:39 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:54:39 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 04:54:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 04:54:39 GMT
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
	-	`sha256:2d8a45b0539424626ad163eb14fb89156ba0450e344bde42e7d990408e94d822`  
		Last Modified: Tue, 13 Jan 2026 05:18:15 GMT  
		Size: 225.9 MB (225885757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d57a89bc1daaaac8541ae6e0502268ab1aa9fba3ece4ea2ceacad8659bcfa790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6d1d36cd3e26062bb7625e7f959ec792c133c8caf14c50e7a38061d3b4be39`

```dockerfile
```

-	Layers:
	-	`sha256:a8732c7d0214b38da4bb3f0db83256ab3a0993db7354ea886709d24754a3e935`  
		Last Modified: Tue, 13 Jan 2026 07:24:40 GMT  
		Size: 8.7 MB (8705808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357c6e5d939870ee570f0d90ea7d0ae789855bd5622135d424c5d2a8610e8874`  
		Last Modified: Tue, 13 Jan 2026 04:55:04 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
