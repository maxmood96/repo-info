## `openjdk:22-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:8ca84cf6401758dd535f81ffcc3f37ec907d5ff56e21464d375f4ed98d4ab394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:24b9b92294a8f43dc44655a7a58c669a24cc54790b004af4b5cdf30a8156ba68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238607890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738cc681e79fd5fc203eb1f939fdb65d9c5a64b97f039869c8a4a3ab70f97d92`
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
# Fri, 06 Oct 2023 20:13:52 GMT
ENV JAVA_VERSION=22-ea+18
# Fri, 06 Oct 2023 20:14:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='07830a4cc21745464a68057e8c441e98d4cd673cd02348e9791d9eafe9f3d0df'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='03432a54970a3005c521d34b44a2438ac28f8fe150bf686e28cea6ea9b2a002e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Oct 2023 20:14:07 GMT
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
	-	`sha256:52e3341c7cf7c6d5ec96f9c4988aa18d308cefc9ce11f6f018c68c3095a2a4e7`  
		Last Modified: Fri, 06 Oct 2023 20:17:39 GMT  
		Size: 205.5 MB (205475138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d4d30c40105beaeef2fe104a860f7802cbdd7c8728791fd0da5313929b648cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236739517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd30617383b36e000a80b69bdec47e19ccc22676cced330d1f5d18536480c5ad`
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
# Fri, 06 Oct 2023 20:23:37 GMT
ENV JAVA_VERSION=22-ea+18
# Fri, 06 Oct 2023 20:23:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='07830a4cc21745464a68057e8c441e98d4cd673cd02348e9791d9eafe9f3d0df'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='03432a54970a3005c521d34b44a2438ac28f8fe150bf686e28cea6ea9b2a002e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Oct 2023 20:23:53 GMT
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
	-	`sha256:740257b11c72f00182c0d5b6de6c019f9da4fa24528bd0d12b7ce198f99d7c40`  
		Last Modified: Fri, 06 Oct 2023 20:27:01 GMT  
		Size: 203.8 MB (203764716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
