## `openjdk:26-ea-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:d03b77f66df3ff37be1665c34b32d4d9d19d735aa4e5c0aaec993db699e0e6d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:70e046a0c18699d70b21538a5c48dc86fe303d9fc1df1c2b61001d560465b8b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.9 MB (259928970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b8c703def07990eacc57676eadecf263b5a9bf13489cd09aba448c1e819657`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 01:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:08:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 02 Dec 2025 01:08:30 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:08:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 01:08:30 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 01:08:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 01:08:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd73ef99b5c07706d7e76125a59a5392893f44ecb7e573bf6f5bf1ccd68e8dd9`  
		Last Modified: Tue, 02 Dec 2025 01:09:16 GMT  
		Size: 2.4 MB (2371041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfe3a914a3600c91737d6ca7b67ec42b63909e529216ce28031a6d86a91b80c`  
		Last Modified: Tue, 02 Dec 2025 04:35:00 GMT  
		Size: 227.8 MB (227781445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:5cde288cb1e1e14ff756b2c0f29037688a65bb7b8ad405e3d29f414459a2e78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3237fc27a97d1c8fad2e33fc17c866bca325949c4d50d3e074f4b17fdb6c905`

```dockerfile
```

-	Layers:
	-	`sha256:5ea2b75d046f64b9a054028983148d236e41fe63689e2436452ed64024073b65`  
		Last Modified: Tue, 02 Dec 2025 04:24:09 GMT  
		Size: 2.3 MB (2278789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1c86ca9d32294650a257db22d8387c507bf7c603b85307fca6890ef3aad37d`  
		Last Modified: Tue, 02 Dec 2025 04:24:10 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:29d7cad643f1263994d26ceb1049b579e46400d1cd1dfeec09d47f961d4c0aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258157353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8c60f9969b68e8c80e71b34e6fc864cbe09abb336c0e8ef71fab759c97c308`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 02:32:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 02:33:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 02 Dec 2025 02:33:03 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:33:03 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 02:33:03 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 02:33:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 02:33:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f6fb0223ce6c2ca0cd284cae4ac57d2807cac52a938014b0507b85b7052780`  
		Last Modified: Tue, 02 Dec 2025 02:33:31 GMT  
		Size: 2.3 MB (2314105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d4190d275cb2f47957289db6b85cd8b6cf7c2a12f0aaf65a50282ae68dc2be`  
		Last Modified: Tue, 02 Dec 2025 04:39:38 GMT  
		Size: 225.7 MB (225704638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:33a65073980245035d9391c32776958a36f9bb2732246f684ce9d3aac10383cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6fc215606496e04d7c15f7cb4b17c537d2af17f35e9a8c7aac92a7ecc4b89`

```dockerfile
```

-	Layers:
	-	`sha256:59e3a32997c55bc984c7cf86ec73326f033b5198461426b20347501e91c88a20`  
		Last Modified: Tue, 02 Dec 2025 04:24:14 GMT  
		Size: 2.3 MB (2278475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f811d111e25ab7408f4b393e82b52f45bd8a87277182de219a7488b0b6d3b4`  
		Last Modified: Tue, 02 Dec 2025 04:24:15 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
