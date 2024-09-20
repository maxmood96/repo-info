## `openjdk:24-ea-16-jdk-bullseye`

```console
$ docker pull openjdk@sha256:f36271942d1f7f18267dd6a43a25defef2f73d07cbb25d7ebe9d8cfe1cfc93eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-16-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:b1e284029ea014c304192987e25e01c7c13010f27b2764e2ecd231022baa5607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351652496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4b5a818a899981158d020097fe606032a2d8481d0337327eb2d1baa460d25d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 20 Sep 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+16
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='46c9e29e1e700ac596a07ef1795142939bcfd687dcc7f959043886bf800a3bee'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='f42ff15af07babf02cf4dc52c121b18be22bc6f54d6b041b424687f82cdd9919'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df08a7b1a9fde0710b3aed31e021fde9ccd93b661758366f4823b4a0af1efaa`  
		Last Modified: Fri, 20 Sep 2024 17:57:47 GMT  
		Size: 14.1 MB (14071314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7c909e5d276c2686c826587eb8f88971d3e681daa1319548d171c1ad2ac520`  
		Last Modified: Fri, 20 Sep 2024 17:57:50 GMT  
		Size: 212.0 MB (212009432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-16-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:4f75049760379b1da64d4d73ba9338cbc46f89eff1b8c07d72ae6fcaa3ef36df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87140a376bff5b1f0f0021d24643dcd816a2de90b0ff4548e25fbf09012d525c`

```dockerfile
```

-	Layers:
	-	`sha256:3e2976a1903e6b84b3316419fb81f7fa37ef399288b7cfb0977c10274966c7b8`  
		Last Modified: Fri, 20 Sep 2024 17:57:47 GMT  
		Size: 3.0 KB (2963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cb7db610e7b6dd8c59a2c978370c1fd5c81fe599c27e960de0d19c37d71b147`  
		Last Modified: Fri, 20 Sep 2024 17:57:47 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-16-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c0c40c252673394c41175872ccce4c1ca3e6b8b3ca04f0f435ec95388d4381d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349669031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875372456cf39207e63d82a27fd16b53c4984e66b144c1ff1e4923b4f6057e43`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 20 Sep 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+16
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='46c9e29e1e700ac596a07ef1795142939bcfd687dcc7f959043886bf800a3bee'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='f42ff15af07babf02cf4dc52c121b18be22bc6f54d6b041b424687f82cdd9919'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47b2b01e7ce009af5fa97c531d3c10731cde5c693d8574b0416f64f36c47e6a`  
		Last Modified: Mon, 16 Sep 2024 19:24:34 GMT  
		Size: 15.5 MB (15526332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a91423be1afea6f7dfb687e64371a1828982158d561e8acdbbc83627d4d32a6`  
		Last Modified: Fri, 20 Sep 2024 18:04:33 GMT  
		Size: 209.8 MB (209827919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-16-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:fc463e118e14e04dbc4e644809d181aa06c899c74b17225eed115e6482e99c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8314423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0798418cdd5820b519f8eb80910f944d70976640cc103922c34fab68b77aab9`

```dockerfile
```

-	Layers:
	-	`sha256:c926a1df10a624f347abd702e8c6ad751a0c0a3677d3b22d929df75951234921`  
		Last Modified: Fri, 20 Sep 2024 18:04:29 GMT  
		Size: 8.3 MB (8295620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:393d82227dd9f702214331d7897a316d5331f2ede65bcfe9b9c600c4821e363d`  
		Last Modified: Fri, 20 Sep 2024 18:04:28 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
