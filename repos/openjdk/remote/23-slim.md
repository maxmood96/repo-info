## `openjdk:23-slim`

```console
$ docker pull openjdk@sha256:50ef01ed82401fdd77f590f46fa1b458f865cd4ea002c8eba8b6dfbfc2896d98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:ea2f85c3a3cf9e7d9da3dabd4d029aa3a348b881eafda165c15f3b983c2abbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244623628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a971b4cbd730b8cd014ad18d789e7f66e508830d80f5b9eb61e6d6a48db498`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Jul 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 20 Jul 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+33
# Sat, 20 Jul 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='d44748cfdec1fe164da0725a95fb05f7e4b94070a669f2688f8604154d14df5b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='e25276d4f0cf9fb6f67b3a1be8087fbf0cceadfa33cab8ffc17e99c83e105e74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21effac48f4048f3c6a6f560d07b4aac04474c9f164efa77c1d836790c5ef8d`  
		Last Modified: Mon, 22 Jul 2024 21:00:02 GMT  
		Size: 4.0 MB (4016765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662ee20a2bfc2b46a77e61b67bbbdc408ff3c2504e59cab10992a185cc0d321`  
		Last Modified: Mon, 22 Jul 2024 21:00:05 GMT  
		Size: 211.5 MB (211480585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:87a22daec969dec94352bf1e9a9edb93746de7cf62035c203ef4ac4462869bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115ee9aa0a8839a117bfd358b9690cfd7b0173a65aa6a4a6ce7bc9a3d3571745`

```dockerfile
```

-	Layers:
	-	`sha256:70f18d08132cc36258282c24b74f7357bc02f764480211351f0756296800f195`  
		Last Modified: Mon, 22 Jul 2024 21:00:02 GMT  
		Size: 2.4 MB (2365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b7f1f7dc1a41bd84269bffd346d09e84dd43cce72398de32eb45089830cc2f6`  
		Last Modified: Mon, 22 Jul 2024 21:00:02 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7558be6d4035794ceab5d5839bf98ebeb66eaf0233c91a82345515caf80540fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242346086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8040dd488ee57147b9d01d48e2c119ae9781e6e741b2f6516636d12cff4324b5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0370b31cbe4825d7532c88b6301fd41a3b91f7ca9bfeb28d0c0a0d92748ce685`  
		Last Modified: Fri, 12 Jul 2024 22:07:40 GMT  
		Size: 3.8 MB (3829944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e7161887a181224b301c5facf9e52b87a2edc877d4ec22616e89dc3b346be1`  
		Last Modified: Fri, 12 Jul 2024 22:13:02 GMT  
		Size: 209.4 MB (209359579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:a79baab4369265b968533f7c3e3a08b5597a35a654bbe2354028cd486786eda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f54d587ef7d7aad38eb53a40d7465c7f93232af61e92d3819bab8a1f8a020a`

```dockerfile
```

-	Layers:
	-	`sha256:8712c1e86dc1c704cea5d55a6e8c06a5671d456c32c88aef6aeeffe722c00956`  
		Last Modified: Fri, 12 Jul 2024 22:12:58 GMT  
		Size: 2.3 MB (2346699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61e453cc1b1bf96ffad92d69fcee14b543ac260cd9c74fb972235431efb1e522`  
		Last Modified: Fri, 12 Jul 2024 22:12:57 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json
