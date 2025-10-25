## `openjdk:26-slim-bookworm`

```console
$ docker pull openjdk@sha256:49b054f744892145da7780c9dcc38320671fa8ab2d43603bd1c26188fe7a2919
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:6416b6e1f27286671877d6c42e8407c98b87391e811372ca52178ee4d14d93f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258158173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55a39729edaa37ba87770a673643ab67becceb2f86c03f79e95e37f58f53708`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 24 Oct 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Oct 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='3189ce7f96b6fb0b69ce1e8ca7bc626aa30009023f9e2ddf7faeaa5ddf9e8626'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f2d4dc408e6fe82574fb9ad9cff97da63a897a887198c666cb1bd0987fa690c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78486af54288f120a4c57b8de0b057d75605645f0ada9072efaa9922d5806e71`  
		Last Modified: Fri, 24 Oct 2025 23:26:32 GMT  
		Size: 4.0 MB (4027342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ad5ca0dd9a093a7db7a677fa60fc418b9ac5aa124884e3955ef495b2b6741b`  
		Last Modified: Fri, 24 Oct 2025 23:26:37 GMT  
		Size: 225.9 MB (225902510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d04d92d4d34f0c6d4aa3919caf9da0b137a97f19049bee13732110cc89b8c778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01989d59008feb169f7ec4ec364649899d7ec2bc4e3fc30f0e0f0707c4d349a3`

```dockerfile
```

-	Layers:
	-	`sha256:495b976d2d8067b36dd1b8ccdfc7692e3c2ad28fb95706e335c885f4310984d1`  
		Last Modified: Sat, 25 Oct 2025 00:24:13 GMT  
		Size: 2.7 MB (2651699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c45f9f27eca14043904f7757eaa3ffa4116f149bdeae1669307a381698369499`  
		Last Modified: Sat, 25 Oct 2025 00:24:14 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9637b582dcb840e0d3791ed333466fa3aa4f3d14bcf1b1524f115c59c4859543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255695442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304987b4c35c5cc33f8ef92c01f96c467b440cefd680e58482080d5a8ac12ce6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 24 Oct 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Oct 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='3189ce7f96b6fb0b69ce1e8ca7bc626aa30009023f9e2ddf7faeaa5ddf9e8626'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f2d4dc408e6fe82574fb9ad9cff97da63a897a887198c666cb1bd0987fa690c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a0def938f4d48d6fbc28adbc2e23c744fa814ba18a37f40c1e9be072384916`  
		Last Modified: Fri, 24 Oct 2025 23:25:55 GMT  
		Size: 3.9 MB (3851394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8c926d72984544e0eefa21fce60c7592a5fe031dbb6d658dafd08fae609c00`  
		Last Modified: Fri, 24 Oct 2025 23:30:30 GMT  
		Size: 223.7 MB (223741858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1c71f43c82c9610d5e7bc1d7c63e517522a2ec05a5f188e7ab1c37e1702d0072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5051bdf04b632c4b14009e0167af796f3f84b1d7e440fdc97219375074440af`

```dockerfile
```

-	Layers:
	-	`sha256:fa2ec8dace298ff6b38f5d48299e3e5dc7c22785edf435fb2c382042664387ea`  
		Last Modified: Sat, 25 Oct 2025 00:24:18 GMT  
		Size: 2.7 MB (2651357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:925a44c78f41c14edfd3458a99645e72384f1d1a9ae69a476464ce25883aecaa`  
		Last Modified: Sat, 25 Oct 2025 00:24:18 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
