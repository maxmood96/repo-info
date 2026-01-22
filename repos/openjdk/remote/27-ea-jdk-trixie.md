## `openjdk:27-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:56208b61d67d214785c86e1ed340cadfedaaba068ce0d36c84e684560937d00e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:2f2bc9983c2b75201adad31181f81b403dd9eb53e54427c7ca49b88dc617df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 MB (386937351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8c071065947771eb20ff665c9a88a06d318a46a634dbb0492d7e7b499c7898`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 20 Jan 2026 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:46:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 20 Jan 2026 18:46:51 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:46:51 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:46:51 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:46:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:46:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddef0d4d56402006705701bbbe84ff7e6564ba645cd7958397bdbcd6791bb7c`  
		Last Modified: Tue, 20 Jan 2026 19:31:18 GMT  
		Size: 16.1 MB (16062910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9848311b6fbe0fec7297104ad5eb53295209ab0aeff18a7103b435d488fa34ab`  
		Last Modified: Tue, 20 Jan 2026 18:47:19 GMT  
		Size: 228.2 MB (228188634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:187ceebe1ebcf5846e5d343f1c99818c0ddb4cb9a2f4f2e0ab98482294b7aa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65538e8a2fc9e85724d75af1ef8e1509ad711b35e8e5f47f137d9d76f4e2db1a`

```dockerfile
```

-	Layers:
	-	`sha256:92958e9183892fb91200b29685f381e4e42220a20c584e1868a357ed15cd4195`  
		Last Modified: Tue, 20 Jan 2026 19:26:43 GMT  
		Size: 8.5 MB (8511010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3771f95e9cad32449e63d2bccc714b483f7cdde132f70285dfed728544a41e37`  
		Last Modified: Tue, 20 Jan 2026 18:47:14 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:aced90d7a7e8e0ee4dccdb63c567e0e9c9a9e7dfe4561a63aa5bfb68c889007c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384457990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e15d2d0a9e440efd4084d747da7240f82414ec2fd7707c5a36b7ddb010fe3a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 20 Jan 2026 18:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:47:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 20 Jan 2026 18:47:41 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:41 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:41 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:47:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:39 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3357879be610cd88f919c5e23bf95567a64e6be6b25c362185a4012e0b2862`  
		Last Modified: Tue, 20 Jan 2026 18:48:07 GMT  
		Size: 16.1 MB (16071431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f0b0390a8d951567a1ecdca527c6ef79f6feebb21ce94eb423be054c76b5a6`  
		Last Modified: Tue, 20 Jan 2026 20:03:54 GMT  
		Size: 226.1 MB (226124327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:8f979fd139bdbb98ed677ec0ce44da0e982fd33dab0a26de4c82dac52d9c89fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d2f01ae8f2a7e4c6586d3b434a0b9ae945e386ca1e0600c6d75dc6d6d66560`

```dockerfile
```

-	Layers:
	-	`sha256:67ea643f78a415a6ee6ec2b9ec25ff0d316324ef4f962b08645454e24804849c`  
		Last Modified: Tue, 20 Jan 2026 19:26:47 GMT  
		Size: 8.7 MB (8705800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d421479f8fda1bb480d225294c8bae1d8918bde88181a630ae97a72cd074943`  
		Last Modified: Tue, 20 Jan 2026 18:48:06 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
