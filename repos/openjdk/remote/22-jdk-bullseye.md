## `openjdk:22-jdk-bullseye`

```console
$ docker pull openjdk@sha256:19416f503f74d23f778b50990c99c37386f0f5637865991a0be019df6a60cd5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3f1dd6c9ebe9fc371f496019830e167f0ccc549b80999e36a84023cf2b0cf19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342328971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6255b5d68155ee75220cd21140fa1335dbf77cd7a00a6210f210c21484697dd1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Dec 2023 19:48:12 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Fri, 15 Dec 2023 19:48:12 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2023 19:48:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 15 Dec 2023 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_VERSION=22-ea+28
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='c19197168f6e8f67635539f348e7e97ebf21cacda670bec9304e59cb9e967fd1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='cfc0261560182c1fb0e8e6ab133a6300aa3da0663abdf5f195f7a664f8f7d56e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d278fc41a93b35689afe55f7bbeda81194c3ed9d7162d8adf2ed2af1e042ea`  
		Last Modified: Tue, 19 Dec 2023 04:42:32 GMT  
		Size: 54.6 MB (54595440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6f8c9998ef1e3f306065ad8baa7099b5682cacfbdd361c02a598a55fc1c56d`  
		Last Modified: Tue, 19 Dec 2023 07:50:09 GMT  
		Size: 14.1 MB (14073147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae25218096d7d96a923a10342883abba4ffc5d22259c6adf57f15565fc66475`  
		Last Modified: Tue, 19 Dec 2023 07:50:14 GMT  
		Size: 202.8 MB (202838232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:85219c33893aa719fc80fa95d6e54b6a6fff48f869898aa1467e0d1423e14f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a011750c9372119d663b3c3f6be75efe2bf02f76c550a00ad455be8e2e6492e9`

```dockerfile
```

-	Layers:
	-	`sha256:6db8359e7f294d010f6dbe18af234cf00d9807456aad632b59327273b44dbeac`  
		Last Modified: Tue, 19 Dec 2023 07:50:09 GMT  
		Size: 7.0 MB (6956084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f228f68f2df3612f39b4783c7ceec52bc2b9e63d2de81c2547d9362225f903af`  
		Last Modified: Tue, 19 Dec 2023 07:50:08 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b500e3b4a1208640fb50a6e19cbd4dd6c2e8213ff0f6d25119f97e653f3a2b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340575122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb79cdba7aaa925c5d3cc9b96606bbf0ae28378ba230c9879c90a323665169e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:59:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 15 Dec 2023 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:48:12 GMT
ENV JAVA_VERSION=22-ea+28
# Fri, 15 Dec 2023 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='c19197168f6e8f67635539f348e7e97ebf21cacda670bec9304e59cb9e967fd1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/28/GPL/openjdk-22-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='cfc0261560182c1fb0e8e6ab133a6300aa3da0663abdf5f195f7a664f8f7d56e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a9d2006a8ea812285a7be34dfc82465b2a592d6217f4d385d373c298de4642`  
		Last Modified: Tue, 21 Nov 2023 08:07:16 GMT  
		Size: 54.7 MB (54700129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc85cb84d79c3e3594b521045571bbae857e3a968aea20d3f8da0ccc3b21b10`  
		Last Modified: Fri, 15 Dec 2023 23:24:25 GMT  
		Size: 15.5 MB (15527435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c656b7ec27e160a2cb2b62d0ac136fef9c27ad26ddbd254cd2ee1d9c815c54`  
		Last Modified: Sat, 16 Dec 2023 19:18:13 GMT  
		Size: 200.9 MB (200889573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:47f6fae1574265b860f2ebf0d9b5d5cdd1db9c6965b7c1b357836d951b12943e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9951c49c68f784fe1c489004210dfe945a85669237e97ec94a8db7dc299fc2c`

```dockerfile
```

-	Layers:
	-	`sha256:55c4389b0e8375789b39cf69167177bb5ed00f5c4048d553142e1badee5c75f4`  
		Last Modified: Sat, 16 Dec 2023 19:18:07 GMT  
		Size: 7.0 MB (7043700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:260fc31d3d86e64a7e57801eeb95ed4644c1eedee614939a873c0a65c56388b7`  
		Last Modified: Sat, 16 Dec 2023 19:18:07 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
