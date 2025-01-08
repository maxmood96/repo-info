## `openjdk:25-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:34183ca27693cc261f3d668de18067f3086e3e186f6a74aff808b8547c0d9378
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:581f6bc62f890bcd16f2888d02a3edb75e0eb7246b53a96e937550248bd33b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244708507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c633b455c8ea3a8d2ca7154414dda540ceefd969dda7b43ca2b1c474366370`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 03 Jan 2025 19:53:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:53:11 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_VERSION=25-ea+4
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='57eb4b2610608286fb271949bd4f1acb9ce6d550325d0797f445c1bd0587de50'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='2ebebc0344b40c03cd47ecd8936fe2aee3f0624e5e2463340054d7174b3f4e1d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Wed, 08 Jan 2025 02:30:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f4c2db8aaf4b9cf21329634fe8a8937fb0038271f4e02c7ade551dc540d5af`  
		Last Modified: Mon, 06 Jan 2025 20:28:01 GMT  
		Size: 1.4 MB (1377220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11956e835fdf92399febf45a5e63d3c89f3c47a186b34ab147ba3ad019a1ee8b`  
		Last Modified: Mon, 06 Jan 2025 20:28:04 GMT  
		Size: 213.1 MB (213078644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ca865b23b08142f4a2b1b53466aa27cc824150566e3b349e26a1f7263edd0a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fe218c748385fcdc59bbfb85881f6fc5cbf0cbbe3571909d5e514ef23ab4f9`

```dockerfile
```

-	Layers:
	-	`sha256:64a662f68af91c4460d123430eb36af3700c9232d4d3c8a0434aa91606407cd6`  
		Size: 2.8 MB (2827914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fda5c13a4ffec5099db43812a4456a751a666b303823d85d2ef132067e586d5`  
		Last Modified: Mon, 06 Jan 2025 20:28:01 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b1d2b5967b1091512198f00f62aef78ff071bee55a524354a288f18194c4ac4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241133869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e21ceddef84419f25755365e0032606fda8494a765ad3d067ffdf8bbc0579f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 03 Jan 2025 19:53:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:53:11 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_VERSION=25-ea+4
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='57eb4b2610608286fb271949bd4f1acb9ce6d550325d0797f445c1bd0587de50'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='2ebebc0344b40c03cd47ecd8936fe2aee3f0624e5e2463340054d7174b3f4e1d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802af25e15e1605893bc7f616bdceb6df54d42569f2584718a22b15a94ff45a7`  
		Size: 1.4 MB (1361263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cd6f74a6c0205f4f53b923b5a72fdf42359e7232e3d2203e34d7ea6a5e3910`  
		Last Modified: Mon, 06 Jan 2025 20:32:45 GMT  
		Size: 211.0 MB (211027753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e4047b258e3c59c6437f87c3c2c1023658983e809dd8b5e5fa1f914edc92b8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc6e93d636d87d4f3abf957a67105eabbd98cc9613a4780a25543f7a83238ea`

```dockerfile
```

-	Layers:
	-	`sha256:eb07b37bc580d942311c081c2840ce09b6db4ffe9023a67ef406cc182f39b0f7`  
		Last Modified: Mon, 06 Jan 2025 20:32:41 GMT  
		Size: 2.8 MB (2827566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:831f1e6fa7d90e179c6122cecce5ad6c84852c948ec34716b29dbbd5a1695be1`  
		Last Modified: Mon, 06 Jan 2025 20:32:40 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
