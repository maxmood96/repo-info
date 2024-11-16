## `openjdk:24-ea-24-slim-bullseye`

```console
$ docker pull openjdk@sha256:d1b1d78d9541c1cc064a7c99de8f8dba0f5d6978725014134215cd887672f02b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-24-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:575d0686925e1d8cc10fc4587c65a2a6b8e945fdd255bc400c99769d0066d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255089136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d300ee28d669573d23e7498d5a2339874c963915ff6e515b6f2222869a0b5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dddf5531d6584c76ba3e4ec715d85a7cdf04231293a83a8a3b9397bc663766`  
		Last Modified: Fri, 15 Nov 2024 23:04:44 GMT  
		Size: 1.4 MB (1377332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa3ae350ea23c259f4cca6dcb8f796155941dc218afba9e82e21624fd28a65b`  
		Last Modified: Fri, 15 Nov 2024 23:04:47 GMT  
		Size: 222.3 MB (222260243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:08ef50e5ecb85e1a8ffce1b0a24c49872e058927fe16ab603745c63ac5c7e333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6754523f1e6c61c84d180c2ee6a34638522eff4f8f2ade4bd19ef7b80b76d83`

```dockerfile
```

-	Layers:
	-	`sha256:f2e83cebb222eb882b51d8b2b3b381916cdb1be4499cf68502825d623475af7a`  
		Last Modified: Fri, 15 Nov 2024 23:04:44 GMT  
		Size: 2.8 MB (2828943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fd9c2f539c43381a7e551cebaf2655d0442bc3315f140fc96cf3d14269ffe3`  
		Last Modified: Fri, 15 Nov 2024 23:04:44 GMT  
		Size: 17.6 KB (17569 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-24-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7187a28cd9a16b197e60009f0a63e5e734812388e5a151b4205e664e13a83e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251665929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380c712b55d0aa1629b9066e296f4d6547e7397353028e47affd11982fc342cd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8956420fad8a33c8d0ab8fce67143e196e496b54a2ab0a2d2bc4d9a2ad45`  
		Last Modified: Tue, 12 Nov 2024 18:45:19 GMT  
		Size: 1.4 MB (1361337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be64777411a41b9208c087cadd150197414a7653725d39b287500227e56334c`  
		Last Modified: Fri, 15 Nov 2024 23:14:02 GMT  
		Size: 220.2 MB (220212992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2c0ca3e637641068ad9529987fd76b6bf92e91d784aa1dc52533005bc6a98f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8bdc643f7c00931cce8b7e30cbc6511d9035e264d3ed5372506736f776a5d4`

```dockerfile
```

-	Layers:
	-	`sha256:1e932df5010a30e91c2fb5cdb4fc5a12785e65794c3c97af02d77358a74f5dd3`  
		Last Modified: Fri, 15 Nov 2024 23:13:57 GMT  
		Size: 2.8 MB (2828593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c04f1915a058bbc4abfbe54d38134d63bfe32256997b603b7504f8ac339dfba1`  
		Last Modified: Fri, 15 Nov 2024 23:13:57 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
