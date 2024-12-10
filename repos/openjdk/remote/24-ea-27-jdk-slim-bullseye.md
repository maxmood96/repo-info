## `openjdk:24-ea-27-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:bb44a71a10963152e73e295f4491488ff76cf7081916dc5c465ec6e114f5621a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-27-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:c57a51dc8dc4573bf1dd2098e7f40a6f11ace6508845264369f6fd2596501aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244524042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bf4f223d4803b8033eb5264d4f8d50a9a60e8d249375a1a65ade5c7bca096e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c44ad36e3f4093ee1459fe4396af03a5453779a4e0df1cc0f386ac1b7c7de3d`  
		Last Modified: Mon, 09 Dec 2024 23:30:42 GMT  
		Size: 1.4 MB (1377219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e021c8b76a8143ec807faa64986126d892842d7bc6b6b92652c5e297d133fd`  
		Last Modified: Mon, 09 Dec 2024 23:30:47 GMT  
		Size: 212.9 MB (212894179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-27-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6720f94223db1e0c846d54c0678480d806b8fa9d319b45ece8e60f086873f847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76fee8a5337325675845e2b62db447546babc145376b81578f1223fb60372a6`

```dockerfile
```

-	Layers:
	-	`sha256:1be19dbf1fb39c0f2fe7b7d7f9b5c9b39ac4e3783589d8f4e49248d9533627de`  
		Last Modified: Mon, 09 Dec 2024 23:30:41 GMT  
		Size: 2.8 MB (2830879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c39be580a88397973791d646d48780a62b9eb778179ab7d99afbfebd7b90c74`  
		Last Modified: Mon, 09 Dec 2024 23:30:41 GMT  
		Size: 17.6 KB (17569 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-27-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e98b0eb377407cb27b5f4f83d977609ce96a5f1cbf3e81a8a2668a01ef298e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240955698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7194eccb267bfec18bb5ff44b771e50a5074423eb7b4f6dedbdeb15a4840d71`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7ad6e84f249b4b319e4c8cf12e7929732105f68e6f8a67945acfd605733bd`  
		Last Modified: Tue, 10 Dec 2024 01:31:31 GMT  
		Size: 1.4 MB (1361283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48329509bd3042db591a5e0ce957cee9d3cae4b4bc2e11fd95194a0dd7f8219`  
		Last Modified: Tue, 10 Dec 2024 01:36:18 GMT  
		Size: 210.8 MB (210849492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-27-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:61692de9624f31484e247f1993f1a2f6e1a9b9ab6dcd9ebe2fe9f1c00c48cedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2546f9d6bd519c07e3cd350720fdf14e0c657dc31bfe41797354416d7ca2e369`

```dockerfile
```

-	Layers:
	-	`sha256:33bc2f00d6089dea9b7d4673fbbb3d09b162e0ed00204c29d62119dca8091b30`  
		Last Modified: Tue, 10 Dec 2024 01:36:13 GMT  
		Size: 2.8 MB (2830529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e31c1715337dd55e0520a1d64d3cc5b6ca977dac6ea21b88c71f1c7972ec035e`  
		Last Modified: Tue, 10 Dec 2024 01:36:13 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
