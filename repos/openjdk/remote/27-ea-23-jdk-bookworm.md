## `openjdk:27-ea-23-jdk-bookworm`

```console
$ docker pull openjdk@sha256:5ea14af168145d0aa52b9ac1f3f7cc7dd65f2ac14e7ae823bc9ae725dac5d306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-23-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:b7b49dfc37516ea9d479853ea0fed6c4aaea7faa5490391dc606b50ca0cb6f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382808365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a5dab57bd51a550ab6c1c5780c6aeeb15885c80a94263d86a7bef766a81db`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:09:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:10:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 26 May 2026 19:10:07 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:10:07 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:10:07 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:10:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:10:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e53d17277a91a9d192b67517c37a97e10d0eeb8f3dfe54e65425253a5e3d95a`  
		Last Modified: Tue, 26 May 2026 19:10:31 GMT  
		Size: 16.9 MB (16946238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3871f302623a5ef26e2bcba49289de30ebbbf48170af4b50182260fcf8c013de`  
		Last Modified: Tue, 26 May 2026 19:10:35 GMT  
		Size: 228.9 MB (228918870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:28c45c16779b2288350eff5f319e68bec9b99941e7b5c3d80ad01cc3c6d4a369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8685582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e0bbfbb824615b151f055ccde8449ac887a1c8b6533d53299534b871e49bbd`

```dockerfile
```

-	Layers:
	-	`sha256:3a0702cdfd6f92c99f5f2b0eb44e0f0e9bd9d49b7d6a23d16d4f7a07f9a120ea`  
		Last Modified: Tue, 26 May 2026 19:10:30 GMT  
		Size: 8.7 MB (8667643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a677bf4af2214a980695f18a9531bebec016ece4533c112424a468327616d3cb`  
		Last Modified: Tue, 26 May 2026 19:10:29 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-23-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b65ca430a66ac1584a85de4dc6f7a1d6344b265bc57700e74b27d4a91fc0f352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381087459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf3bd76adacdec4c167b445c12ac288af8d1e4fdb8b66f11168ed0e1f35a3e3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 26 May 2026 19:12:16 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:12:16 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:12:16 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:12:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:12:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f4bd30aa9ced565866dd163f8e1c2f5aad490039fc2417a88f81b80a26024d`  
		Last Modified: Tue, 26 May 2026 19:12:42 GMT  
		Size: 17.7 MB (17730381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0679206a865a77e10bcfe46663d700da8d39e4c51ae66d0256c095f4fcdf6cd7`  
		Last Modified: Tue, 26 May 2026 19:12:47 GMT  
		Size: 226.9 MB (226876597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b400127552bbc1d8b662061662ffd2169fe32d5167932767357046a0ac56a69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcf00e48ded4323a2fec2c42735099d6e54b3fb6e22ee5b9da3e62d6d9068b8`

```dockerfile
```

-	Layers:
	-	`sha256:9b5d5f3f52705d799542ef1a99e0fe54d9337c1b915f0e3a75e566ee870dd3d2`  
		Last Modified: Tue, 26 May 2026 19:12:42 GMT  
		Size: 8.8 MB (8804488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c43a096ddb370d9077730088b55ca268826d1e595cccee1b2ba439a6ff371f2`  
		Last Modified: Tue, 26 May 2026 19:12:42 GMT  
		Size: 18.1 KB (18057 bytes)  
		MIME: application/vnd.in-toto+json
