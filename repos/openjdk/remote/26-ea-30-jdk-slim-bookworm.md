## `openjdk:26-ea-30-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:374ae83ab3a10151b5f39d9780b056ea9fa9e8586157ac9ef8358c3b0a4407bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-30-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:521544200275b4f7af6aff544935b9b4f0e7078f557dcc5db3e00ffa5026603a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260270694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94941359c99e18cdaf1b49805fb7b8ab9a16abf84e846521c834bba3c91c22b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:43:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 13 Jan 2026 02:43:22 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:43:22 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:43:22 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 02:43:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 02:43:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be79aa08c99b03fe0420695fada2be0a811d3a39b8b79125cfa8860dbb403238`  
		Last Modified: Tue, 13 Jan 2026 02:43:53 GMT  
		Size: 4.0 MB (4028170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61974d566ad2129243ceafc14f1704e945e1adf25e60ae7626c054f5dd89df9`  
		Last Modified: Tue, 13 Jan 2026 02:43:47 GMT  
		Size: 228.0 MB (228013952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c3a8b8ff1ee1df085901e25e22f36a0d33f388c9c84c928901037e0c91b2cb20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1447ccca1a5f96f5aec4a2c295585841a0693ef9b9e770a49eee4b8331e61b`

```dockerfile
```

-	Layers:
	-	`sha256:199db90b487943e5a3fafd7c9a09d6d99277967f7448401504bb7f41e3d91446`  
		Last Modified: Tue, 13 Jan 2026 04:24:19 GMT  
		Size: 2.6 MB (2649799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58649d1ea0032b0f50100d2a5726334ffe4a223e7014cb0ae317036257499837`  
		Last Modified: Tue, 13 Jan 2026 04:24:20 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-30-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1f8d5c05d3c21024fd1a92a715a02edf7c444d96d12f7874f6fe382b2a5bd5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257894453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65b8c30fdd9239b7bb83d5c395267031fae77e8b4ab972091312e574c8d9c59`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:47:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:48:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 13 Jan 2026 02:48:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:48:06 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:48:06 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 02:48:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 02:48:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a64051c025e692309b366f8a7639ab33b49d83096184e41be931f50ab34e62`  
		Last Modified: Tue, 13 Jan 2026 02:48:39 GMT  
		Size: 3.9 MB (3852006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fd50428fcd5534438c06e56b7f319b6dbc8403807d9741abc03d04aba303c1`  
		Last Modified: Tue, 13 Jan 2026 02:48:32 GMT  
		Size: 225.9 MB (225934558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7ab7a995fdeacbd831ea0a7c3ed733084912743a5b1820f7f8549f9065d23c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31dac1f28e65fa91dd4a63be333191613e6e0f76179d3214310e39c0b5ce39a0`

```dockerfile
```

-	Layers:
	-	`sha256:a4ef8b0c5360736ee5b613ad4cffd0d2cee15de7e817af07726a29227f2138ff`  
		Last Modified: Tue, 13 Jan 2026 04:24:25 GMT  
		Size: 2.6 MB (2649433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc4bb339f7bf194cf3d1ec1217f08acb4fd0c4dbfa74b4fe8e92bba424ed896`  
		Last Modified: Tue, 13 Jan 2026 02:48:26 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
