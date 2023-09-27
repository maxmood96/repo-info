## `openjdk:22-ea-slim`

```console
$ docker pull openjdk@sha256:8a858a91ac54b678a45f6ed4c3a6b63cbdfc889a2327747886cb209e5589abd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:a38f9c48c5833777ff753903a40fc309ab2c6d766cb19712169efcbdc85cdfb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238561995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3039c1727ee3f3d1b03c1b74e2988178920528782079508f5c968057e1d3129`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:40 GMT
ADD file:a1398394375faab8dd9e1e8d584eea96c750fb57ae4ffd2b14624f1cf263561b in / 
# Wed, 20 Sep 2023 04:55:41 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 06:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 06:16:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 06:16:19 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 06:16:19 GMT
ENV LANG=C.UTF-8
# Wed, 27 Sep 2023 00:41:56 GMT
ENV JAVA_VERSION=22-ea+16
# Wed, 27 Sep 2023 00:42:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/16/GPL/openjdk-22-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='4bea3daa0a5dc0234dad8381ffb3322598e7f88d6190b21ebef4d01327b266ab'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/16/GPL/openjdk-22-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='34b3154d77f547b0b75d3bd2d534b38af115c75e2b395f1994c9adf923a8f3c3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 27 Sep 2023 00:42:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a803e7c4b030119420574a882a52b6431e160fceb7620f61b525d49bc2d58886`  
		Last Modified: Wed, 20 Sep 2023 05:00:22 GMT  
		Size: 29.1 MB (29124705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4972576c83dad66aa1e4f6d08e74f9e551e721a7cb2dc5370fe8da1af5b11e8`  
		Last Modified: Wed, 20 Sep 2023 06:18:48 GMT  
		Size: 4.0 MB (4008047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500fb4078ffa9fe7780274b6b45acc28493581f116d2a37f10a5904ce47d55dc`  
		Last Modified: Wed, 27 Sep 2023 00:46:20 GMT  
		Size: 205.4 MB (205429243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:252b12498eaa30789a06b1a6ac5529679d7686af1a9600c147d7b4be688e2203
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236724545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e451cbb653a4bd1c61ce2c3f0f4f8280ff9fd41303d115d1a7e3d039fb943db`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:13 GMT
ADD file:ec1a6e0aedd76c8fdc8544775f8b553f58950e9435f5cfe919f39374e222cfbb in / 
# Wed, 20 Sep 2023 02:44:14 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:57:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:57:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 17:57:26 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 17:57:26 GMT
ENV LANG=C.UTF-8
# Wed, 27 Sep 2023 01:09:44 GMT
ENV JAVA_VERSION=22-ea+16
# Wed, 27 Sep 2023 01:09:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/16/GPL/openjdk-22-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='4bea3daa0a5dc0234dad8381ffb3322598e7f88d6190b21ebef4d01327b266ab'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/16/GPL/openjdk-22-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='34b3154d77f547b0b75d3bd2d534b38af115c75e2b395f1994c9adf923a8f3c3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 27 Sep 2023 01:09:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e886f0f47ef56fcadb6ecaf2116056bbdb273e0afe07ed034498b198d386c04e`  
		Last Modified: Wed, 20 Sep 2023 02:47:36 GMT  
		Size: 29.2 MB (29157221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190c8d653feddc1553f480657f5813ecd07f1979c94ef5b5afa2b7c9c278ca4`  
		Last Modified: Wed, 20 Sep 2023 18:00:57 GMT  
		Size: 3.8 MB (3817580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7410e9674b0238c2042c514aec9d0c9052c96731218ce221699c2d1e02a91cba`  
		Last Modified: Wed, 27 Sep 2023 01:13:06 GMT  
		Size: 203.7 MB (203749744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
