## `openjdk:22-jdk-bookworm`

```console
$ docker pull openjdk@sha256:6ea0e912ee729fc2d3f5585e9e1e6b546f4adf5861b3245242e37cc5660c3e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:042e1b9265d6b622bd8173d7b22257e38a5ff23bead9dae4ab0bb2b57de263c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357545778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d05db9b28b4cdbf218647a69b68a87596df0cb2c90aa6cbe0bcacd33d14b6b6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:32:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de22c0f5cd2ea2bb6c0524478db95bff5a294c99419ccd4a9d3ccc9873bad9`  
		Last Modified: Tue, 19 Dec 2023 04:41:08 GMT  
		Size: 24.0 MB (24046123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917ee5330e73737d6095a802333d311648959399ff2c067150890162e720f863`  
		Last Modified: Tue, 19 Dec 2023 04:41:27 GMT  
		Size: 64.1 MB (64131542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e44f67950d10bc084dc8ac29813c354ee73a92f614ca88dda30b6a7a9031b7`  
		Last Modified: Wed, 27 Dec 2023 21:53:51 GMT  
		Size: 16.9 MB (16945657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961c23f9bfc1bbc451366a2647fdf34dd4b53b882a6831ac4ab74375c695cfa`  
		Last Modified: Wed, 27 Dec 2023 21:53:58 GMT  
		Size: 202.9 MB (202860877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c3a42bb42b2742fd51b60504cbcf6da42c606f903751ae406dc7431ff8e2a6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6b8138b6c0e8a91751a8f036828fec2c0a6bb8776ccfa69d1cdf11db6b42c5`

```dockerfile
```

-	Layers:
	-	`sha256:f7fc9f4050cfc5ab3282020fb3f0c027e1048b63ad08afc8ee1f280f1c619a92`  
		Last Modified: Wed, 27 Dec 2023 21:53:50 GMT  
		Size: 7.1 MB (7116360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f7b029570e7a85616674e342e4d0fd3b3b93e4148b8069ec7b6c75f1c3ae7b6`  
		Last Modified: Wed, 27 Dec 2023 21:53:51 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2612c8aad8758e827d5169e79014e3f709891e44337379ec5f45273ed76d8e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355804733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff655ff31a44f7298d40f6ff26063d555da02897945b4df9d08aa6372766457`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:34:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c641d36985b2db859fc64c43a6dbf7c25cdf73e5d16d107fab1d95a840bb4e1`  
		Last Modified: Tue, 19 Dec 2023 11:42:17 GMT  
		Size: 23.6 MB (23582271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd8544b6e15c7a4096b1f48a67fb5bed2efba509fca597f1c164b582ab01c02`  
		Last Modified: Tue, 19 Dec 2023 11:42:35 GMT  
		Size: 64.0 MB (63988289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f4486e748ebca87a82800520024d71377305cb16a0c8e2cfdd5de9220f3e9b`  
		Last Modified: Wed, 20 Dec 2023 10:21:15 GMT  
		Size: 17.7 MB (17728700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1601a8aaa98b1723efb789163588fdc4e46da8d1ba79bcf543ac92e15d531379`  
		Last Modified: Thu, 28 Dec 2023 05:06:47 GMT  
		Size: 200.9 MB (200913214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4024d2815cc2f634289704b1ae73f5a8830ae7498cd8af6e2b0a1700213f9ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7253611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b09e54bad64ea059a7e40ae00bf0ac20268ffd4882c529826031f8afc9c7bcd`

```dockerfile
```

-	Layers:
	-	`sha256:4d249362b8264815aa6f8860840fcdd4983033788c8aaa1c13ca61c449ba4c8b`  
		Last Modified: Thu, 28 Dec 2023 05:06:42 GMT  
		Size: 7.2 MB (7235187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd00e733cdf006ee3edea4fb45ccbef86dee00fbf97bd7038728d9477a40fca5`  
		Last Modified: Thu, 28 Dec 2023 05:06:41 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
