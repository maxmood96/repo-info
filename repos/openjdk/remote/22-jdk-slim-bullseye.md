## `openjdk:22-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:bdd43362b58b5d60585518db92c9fad86cc17a11fa6b771db0bb860da0260d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:12a59bde0dcf0e260c277a3c9c2d9caf7073feaf123a0f7b859ca8db6091e6a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238897439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a5912c0106bc83942a9c5f663d49181b5a83695492fadf750daaaf7bbb6c44`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:51:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:51:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 01 Nov 2023 11:51:40 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 11:51:40 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 11:51:40 GMT
ENV JAVA_VERSION=22-ea+21
# Wed, 01 Nov 2023 11:51:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='cefe6f9697801dd2a7abebdbd5b7bd36ad489794589e838562da46bde434ae5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='b77e7f170973c91690aa64a028f2e991828fde5092eabc29b602e26824216797'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 01 Nov 2023 11:51:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8bcc04d7ec7c559e1809ac80f8625104e0723f3b628adcb9e7dd5ead853567`  
		Last Modified: Wed, 01 Nov 2023 11:54:41 GMT  
		Size: 1.6 MB (1584394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30595d87c91df09cc535dbcbe49959d67f8e88d5b824f86c2157048917b43e8`  
		Last Modified: Wed, 01 Nov 2023 11:54:56 GMT  
		Size: 205.9 MB (205895130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:aaf0c297387d3d614db7c0f40bc3a6d1f40466e746931c2c288b40b0c04f449d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235736727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1ccc76fb4a6d03ada9526eef7e7d9a6d0b85f3d05d4f87666bee0d00734649`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 03:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 03:22:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 01 Nov 2023 03:22:54 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:22:54 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 03:22:54 GMT
ENV JAVA_VERSION=22-ea+21
# Wed, 01 Nov 2023 03:23:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='cefe6f9697801dd2a7abebdbd5b7bd36ad489794589e838562da46bde434ae5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='b77e7f170973c91690aa64a028f2e991828fde5092eabc29b602e26824216797'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 01 Nov 2023 03:23:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c6abed9fe365e0d3d29c1e8623c6d3d6cc0edf4c4d111f36535cad5d6bfe0c`  
		Last Modified: Wed, 01 Nov 2023 03:25:23 GMT  
		Size: 1.6 MB (1567882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2959b65c06b30dd18a8cd93afedaf01e0cdf9b263a049958fbd9ed6dddea908`  
		Last Modified: Wed, 01 Nov 2023 03:25:35 GMT  
		Size: 204.1 MB (204104940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
