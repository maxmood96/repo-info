## `openjdk:25-ea-slim`

```console
$ docker pull openjdk@sha256:6766a20eb12c9f9feafb3ee4fa42a90ae74fae5d06d76efe87677c26e38e10bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:eb75abf82728ae02d9272d000c7dae005319467e4539c3f3707f88418319511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244657892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c499a0cb456a53e89cfbf62c4757860f5b9a0f8ad0a6e08ab0a3d96deef2da`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Apr 2025 00:48:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca122714a8d7c7287faa7086c69faa956faf2093e47ac466b528f0cfa903990`  
		Last Modified: Tue, 08 Apr 2025 01:27:13 GMT  
		Size: 4.0 MB (4018372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7f27accf3214d3c95b787149af80556dfbf94c2943f44b35d03f865a7a85cc`  
		Last Modified: Tue, 08 Apr 2025 01:27:17 GMT  
		Size: 212.4 MB (212412261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:21e98dedc48d53ce16e707515d2cf5f7af65a0643693af66f7938ac418ff761c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0965d432dfb0e9cc3b6fb47d5b6cc555ef0901bdd8275db8a07a74d819ec0a40`

```dockerfile
```

-	Layers:
	-	`sha256:4c13462e803cb1b5725410bc092824edd50f26193801b61ca44320a5fdac453a`  
		Last Modified: Tue, 08 Apr 2025 01:27:13 GMT  
		Size: 2.5 MB (2535252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4718ad3ff91badfbd7d57d20ee837ca63d75c4e31cfa467177b5aa3320df7eda`  
		Last Modified: Tue, 08 Apr 2025 01:27:13 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e5134329f167b34a628ce597e7057e8f16b77e742522705a58349814f4a57aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242137267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f921e9691481e91e7a5fb62db7977b0fba6327a9529fc5663d02b0ee6fc080`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Apr 2025 00:48:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a61f67c692cc9d0787a601589a3e96be1ca8b7a3708d566354a3ff2f42f55`  
		Last Modified: Tue, 08 Apr 2025 06:48:28 GMT  
		Size: 3.8 MB (3833774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4428458cae161346e7dbe4f850c066f7bcf30189938d4c1a3e1c95c06702100`  
		Last Modified: Tue, 08 Apr 2025 06:48:34 GMT  
		Size: 210.2 MB (210237173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:06799ccad320333067915f1530e9648ba34c9b28618f311538b2a5a692133522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39fd118929f5788ae5be37aee5473d8477f644f4d2c65e02b2716e57185644c`

```dockerfile
```

-	Layers:
	-	`sha256:76098bf66bef5b24494ef4d2b1529f8854c01b6884127bded061245a1c5b209d`  
		Last Modified: Tue, 08 Apr 2025 06:48:28 GMT  
		Size: 2.5 MB (2534982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:150233cb77be8e5b5ca98c6ce5f28c15cff526a0ab4881077f26e4687207c737`  
		Last Modified: Tue, 08 Apr 2025 06:48:27 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
