## `openjdk:26-jdk-bookworm`

```console
$ docker pull openjdk@sha256:4e329e195bb7f38424c03a30c3f8a98062ee4d9cd7719bbf926fe95844a25907
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:0146f1fd8bebf7acb15c846c85b9f316fb2d77108c77c90bd87fa397dc60ae27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 MB (379628728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9b77a021eebf23a7a4a53e5f76722ec7edcf09d4a19271588cfef191cee0ef`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dc770b7b4289b5b5f08ef2e589de684a6e8e695a4db23617bf68e9a4889528`  
		Last Modified: Mon, 06 Oct 2025 21:06:04 GMT  
		Size: 16.9 MB (16943577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7f23e848f940058091c33c18ab00a42a907bcecd41e87ac970983368fa30a`  
		Last Modified: Mon, 06 Oct 2025 21:24:36 GMT  
		Size: 225.8 MB (225781307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef82582f50eab7ecfa4c246b7d9c7dc703a22905bf2cf965122b7826c0637404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8689956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7e7bd55dc0745e6793b099b0d382725fa8d73e9281a0282ad249caf4089fb9`

```dockerfile
```

-	Layers:
	-	`sha256:4b7777723e4268ce8deacb606783e28e5f13396c08726e7f8cd608ff28f60406`  
		Last Modified: Mon, 06 Oct 2025 21:23:28 GMT  
		Size: 8.7 MB (8671339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752251ad3f06848082f9fb6e0320a0cd3e2bce27b000caf41f2606199d3c6d4e`  
		Last Modified: Mon, 06 Oct 2025 21:23:29 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1165a7ff069b6ddb7b0f1e49b39ac70182cdd575799d0b0f927a869e743d76e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.7 MB (377650011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a8f3edb7d0ef96aa7db6f032f5553dfbdfeba69fcfb57fb874db6dc7a4c55a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 26 Sep 2025 18:48:12 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='0a80f3aa3279fbcd36b9247a873bc99b3688ce092a970c08ff3788e2fac99351'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='d12fc689cf8b2e7c1b503472b988320ad15693d9b40c3e877e9f78aae6fb82a1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5763f6df4ecef7e1040e72f0fbf9d26d9930f9c94f3059efed4815adcd5639`  
		Last Modified: Tue, 30 Sep 2025 02:17:31 GMT  
		Size: 17.7 MB (17727609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba8059d7cded30bd7ea903e96dd450ce2ff1c0bcf2a77fea13fb3520d326614`  
		Last Modified: Wed, 01 Oct 2025 11:01:53 GMT  
		Size: 223.6 MB (223597544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3edbce86164c10f2c26fd4b70fc70e0ac0958fd453bbca095aa765179eb3319d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8826969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63730ed806b4cdc016ed6cca14c0dd6dbaa214f43ad209813026e7514fa35424`

```dockerfile
```

-	Layers:
	-	`sha256:efd9748f603d05cb53dc9c5b6484f28eb241b0b0182d5b7692d2cdf11261b532`  
		Last Modified: Tue, 30 Sep 2025 12:23:28 GMT  
		Size: 8.8 MB (8808208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789892f002f23f15515729c0a87f9b41d007bfd888ebe24c22aee59a67432f38`  
		Last Modified: Tue, 30 Sep 2025 12:23:29 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
