## `openjdk:24-ea-jdk-bullseye`

```console
$ docker pull openjdk@sha256:ca93269fabf0615675883c3741653354a97fb6ffdcdc840f26f77b27403afddd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:2374f6b2a7ffdcd911c6bfd68248620c29490aef9df12e6409475cfae37a8862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350972365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdcc9ffcd500b50bf43870592c25f39b2e2fc915e9b9f664176ebd64f4b405c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 11 Jun 2024 06:58:53 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065842589d7a62a96a08c1acc0bf9e7c0b5442f2770276be18328b755d1ffb99`  
		Last Modified: Thu, 13 Jun 2024 03:50:44 GMT  
		Size: 54.6 MB (54589356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770e6b7857e265222ac43e88bbd456c3751729bc4786a62c9d5ccd673e203192`  
		Last Modified: Thu, 13 Jun 2024 18:29:38 GMT  
		Size: 14.1 MB (14072708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c33703ed09e700cd2eb12692180113f8477860a2b7e5434d3d9d84f1928e24`  
		Last Modified: Thu, 13 Jun 2024 18:29:41 GMT  
		Size: 211.4 MB (211446277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:baec3b58789759e89070dd66884a5af5bd694fdf123f74f3957440d5ad7dd91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724be6380c5efb62f3bdff64d637bd1b1d3801b423468202401307c6fc85f59c`

```dockerfile
```

-	Layers:
	-	`sha256:7ba79905e260afe35b1be936a5c94cb5afee4c06868831284ed51217a0101967`  
		Last Modified: Thu, 13 Jun 2024 18:29:38 GMT  
		Size: 8.2 MB (8157311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e666639dd7992bde556c849b07372dafc1e7a590eebec369f789cfb15a0d7c`  
		Last Modified: Thu, 13 Jun 2024 18:29:38 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3c10d890b60d1a007a472990f71d775f7a25a9a2bfe2397014c0676d4c57af95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349044617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5341895bde82f26a0cfc54003d225f00df5bca7d69c98257ea3e3f8c0e8198`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 11 Jun 2024 06:58:53 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a7ca076c1ea04622ddf9f43ff2f138f6c50a40118747a45d2618cc64591d6b`  
		Last Modified: Thu, 13 Jun 2024 01:31:29 GMT  
		Size: 54.7 MB (54696375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd7f584b580345af496d0447ef316f31823141d25e04341e36e0f1361c508b3`  
		Last Modified: Thu, 13 Jun 2024 19:57:35 GMT  
		Size: 15.5 MB (15527068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acdb529a81cb9a9917d33b617998e64b210067c8983db6896e07d7b6b21b289`  
		Last Modified: Thu, 13 Jun 2024 19:57:39 GMT  
		Size: 209.3 MB (209331126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ff856da8bc8cfb7d46bc935ee3f44b17edbcc80d0c4b2958000968411bbbff38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebe792d2fd2fd70f9f76b9a7099d42c0ce9f874831e9d6bbc0106bd27dd337d`

```dockerfile
```

-	Layers:
	-	`sha256:4a4d78b1dcb201b9ec69f50ac15ff1fb7c45b0963d627eb3146d4a5cc497ae25`  
		Last Modified: Thu, 13 Jun 2024 19:57:34 GMT  
		Size: 8.3 MB (8259021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4549c44607505c10200d6eea0a57d325190137b5c209504e518bee810e4f64f4`  
		Last Modified: Thu, 13 Jun 2024 19:57:34 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json
