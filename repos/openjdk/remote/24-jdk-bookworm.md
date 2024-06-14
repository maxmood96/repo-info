## `openjdk:24-jdk-bookworm`

```console
$ docker pull openjdk@sha256:2d6907b379bbf6e92057705513a991d0fb063dd07a9a304f40f60217d4022849
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:ec25d0bf908bbf658b364c3b18949231385b029f450a4e1f9c0d5e183a1cd66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366152313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93b9fe65805fa7a6cc7dc381f65c32e2854be2c17ecf1482899cd53760ccc9c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:43 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Thu, 13 Jun 2024 01:20:44 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 13 Jun 2024 18:54:09 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:54:09 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_VERSION=24-ea+2
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='5219b8df6c8c43be5dab2d1ab5251df85610360ab22789e497ee05c66fa4c7e6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5632c71df051ca5b6640c3c2a09ca3dd2b3dd131ea632906bd0eef7033323223'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3873416e6a335157d669c6193a256dfb289331d669d87f200e4eed1f19f9ebb9`  
		Last Modified: Thu, 13 Jun 2024 03:49:40 GMT  
		Size: 64.1 MB (64142031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c8bd1928bff7ea7f11f1ecb96164e0a75b78411dab94028af282e81ec9ff6b`  
		Last Modified: Fri, 14 Jun 2024 01:01:14 GMT  
		Size: 16.9 MB (16949397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66687d74c6e0025d99be974a1c68d5d6a927641fd5882f212664bcf6c62686d8`  
		Last Modified: Fri, 14 Jun 2024 01:01:17 GMT  
		Size: 211.4 MB (211434229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c7f1ea6bdfc28c830336428f9c760a3f0bf48171bb88c2053fca682b14074857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8240265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05219db7e2be182939c54dff88bf5e108e4ddf328ed98899216622290b1a9f81`

```dockerfile
```

-	Layers:
	-	`sha256:d2992a08e01310fa1bdb39a8dac816cd070cbb956f62028166ad05cfa72b4ab0`  
		Last Modified: Fri, 14 Jun 2024 01:01:14 GMT  
		Size: 8.2 MB (8221819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e7576d7c32f49e3c17f415d19006969d8db3f2736b889bb2a5b70be988f2e9b`  
		Last Modified: Fri, 14 Jun 2024 01:01:14 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1f793ba1c700cd8514f57b338acd7a21f9f16a1e3fa9b5911a13ac6c2556bb44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364238746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f161130ad29fbeda783b62d69c769df58cbff23c2ffa58f280afdd6fa2df1f5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 13 Jun 2024 18:54:09 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:54:09 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_VERSION=24-ea+2
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='5219b8df6c8c43be5dab2d1ab5251df85610360ab22789e497ee05c66fa4c7e6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5632c71df051ca5b6640c3c2a09ca3dd2b3dd131ea632906bd0eef7033323223'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84230ae22287ffb8cab5a4fcdafa2c2117dc175cf922927e4f3cf7dac065a66`  
		Last Modified: Thu, 13 Jun 2024 19:55:37 GMT  
		Size: 17.7 MB (17732451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4852339c8138feebcbfa509dfba326c640f923b449d2ba8986ec6a7b51562296`  
		Last Modified: Fri, 14 Jun 2024 04:06:13 GMT  
		Size: 209.3 MB (209311586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d507cb3dc67ebb45df336b4ce775cb989ae5b25bc01ef4facd8118e343cedb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8378265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8973c8bd539c4f4a651bdef4af0f6d89c1c82b9fd2507bcc7c738d3cb4a078`

```dockerfile
```

-	Layers:
	-	`sha256:ad78b5ebe0fd234f859b0929fe5df2ee064c108231d0458d6e3edbed191e4f28`  
		Last Modified: Fri, 14 Jun 2024 04:06:09 GMT  
		Size: 8.4 MB (8359480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3838034d787c5cd5c3ab0f90b4fb60646cfa555bf71f57ccebd20f93b7982135`  
		Last Modified: Fri, 14 Jun 2024 04:06:08 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.in-toto+json
