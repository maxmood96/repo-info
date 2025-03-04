## `openjdk:25-ea-jdk-bullseye`

```console
$ docker pull openjdk@sha256:dff473d5d2672a5746a9eee29fd7429bad382039d92849d593861a6a0a4f012a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:0c782ac8c70c21b5f5291ffd65e961eb8035a7471bc7f5994da3552695ef7277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (350021684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d829c6b47d8dec457fe23d835a18a6cc9fea4e10188c5e1d3314159f05c5748d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76c449e309fe3074edc84cc6780748f4bbd14003b0dd0f0b4c0cfc778377434`  
		Last Modified: Tue, 04 Mar 2025 21:57:09 GMT  
		Size: 14.1 MB (14071384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e9c31b66d5742c2616c1372a6e123eed436eb053276ecc1dfec6d45d95b869`  
		Last Modified: Tue, 04 Mar 2025 21:57:12 GMT  
		Size: 211.9 MB (211898390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2f551da0d0eae840a1428bb82eed6f0d616a3827ce1eaa7aa1ccd3c55fe40008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8382792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e265ead5a6069e6847103947bc5f730fc29966f19dd6abc4d1f4855a0f5419`

```dockerfile
```

-	Layers:
	-	`sha256:e7fdddbdce80cd59d1210a52beadce17ed74506ac6d588ed66e32ce35488dd16`  
		Last Modified: Tue, 04 Mar 2025 21:57:09 GMT  
		Size: 8.4 MB (8364174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6d2f77b65e07679a0dd9759e78180efd6fe5841e35e8ffc60f281eb33cf2ba`  
		Last Modified: Tue, 04 Mar 2025 21:57:08 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:02365e19bf15c57e9e686c8f7b694aca229c04f17ba304c6ca41c3fe985b86c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (348009424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7195c7d2efe9fee75ee8afe41b6605e38a2fe7488644f526894f570f9aa073`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf95751179ceeac4ea644db1dd90515fa0e5e23d699d7912b3443113e442ce8`  
		Last Modified: Tue, 04 Mar 2025 21:59:33 GMT  
		Size: 15.5 MB (15526257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8bf00e27c37e7096d31d99a35e3002714c636e69c72924186e5db589ccc675`  
		Last Modified: Tue, 04 Mar 2025 21:59:37 GMT  
		Size: 209.8 MB (209834956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ff0c6213890e13ba808d57357b0b3ea5a33a3db5c72d7d939171a849b2602324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8483897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca295d61473c67c31c88cdc8f125daff8f170ef6f26b3d0269b357f48c7d094`

```dockerfile
```

-	Layers:
	-	`sha256:d9f4b0466bf9654f1942e167b2c5197f09be9e727a05a87ac41286c79de79876`  
		Last Modified: Tue, 04 Mar 2025 21:59:33 GMT  
		Size: 8.5 MB (8465136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6243485c6c29d411a3ba4fe7eaf00b86bfa01744dd212ae1da95b1c81740c811`  
		Last Modified: Tue, 04 Mar 2025 21:59:32 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
