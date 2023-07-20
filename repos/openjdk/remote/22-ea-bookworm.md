## `openjdk:22-ea-bookworm`

```console
$ docker pull openjdk@sha256:f4522e8ccb81f2dc127c758ffc86e945e4619cfe6700a3186dc039cbf9aebe98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:6e77858f05193e025d3a247b2cdb16e45bc8a0751401ec2660d1d595866f1235
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.6 MB (359593750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db519ecff227ef1461fb53472244b4b3ece1dca9dd299d11c9cf83c931efe77`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:44 GMT
ADD file:5d17ca085473e890bd6eca4abf6d324c3181f80692523b83ef25d1c42576b99f in / 
# Tue, 04 Jul 2023 01:19:44 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:28:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 17:47:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 17:47:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 04 Jul 2023 17:47:54 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 17:47:54 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jul 2023 20:22:44 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:23:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 20 Jul 2023 20:23:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d52e4f012db158bb7c0fe215b98af1facaddcbaee530efd69b1bae07d597b711`  
		Last Modified: Tue, 04 Jul 2023 01:24:39 GMT  
		Size: 49.6 MB (49551432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd206bea61ff3e3b54be1c20b58d8475ddd6f89df176146ddb7a2fd2c747ea2`  
		Last Modified: Tue, 04 Jul 2023 03:51:23 GMT  
		Size: 24.0 MB (24030593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2320f9be4a9c605d1ac847cf67cec42b91484a7cf7c94996417a0c7c316deadc`  
		Last Modified: Tue, 04 Jul 2023 03:51:42 GMT  
		Size: 64.1 MB (64111613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe2eadbbcddf082c22d3a63d0dabdea67e8dca87688709258efc404506be95b`  
		Last Modified: Tue, 04 Jul 2023 17:50:58 GMT  
		Size: 16.9 MB (16947014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3d368416e50ebc1610df4de90e7cf655d7a70bdd5ebbd6219685a67f9bf18b`  
		Last Modified: Thu, 20 Jul 2023 20:29:56 GMT  
		Size: 205.0 MB (204953098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1f5b7bcb6f04cc13a1a87d39d2694dd6f1922568f2064ff8ed1aa6d84ae7bf9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.1 MB (358120429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856e07287faa3a538192faa624d7c35fed4722a748c771e9b1d8c70f04a6c45a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:26 GMT
ADD file:ab1761d899751c4d24e15179fc9e7e7ac3fb83798ee37ca13d6a6ac44fbeded3 in / 
# Tue, 04 Jul 2023 01:57:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:54:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:26:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 04 Jul 2023 13:26:30 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 13:26:30 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jul 2023 20:06:57 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:07:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 20 Jul 2023 20:07:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:42cbebf8bc116ba1aed7897e2d0566bf49da9d5c70be71b6a7cb07805d2f5b7a`  
		Last Modified: Tue, 04 Jul 2023 02:00:57 GMT  
		Size: 49.6 MB (49572781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0518ec57568a70561f7c04650f9554c88dada973f54d88e36f65b0796d35de`  
		Last Modified: Tue, 04 Jul 2023 06:21:03 GMT  
		Size: 23.6 MB (23569546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356172c718acf9930d9465b170864319079e2d2ebac0ddef781d64e85789531e`  
		Last Modified: Tue, 04 Jul 2023 06:21:20 GMT  
		Size: 64.0 MB (63984075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b194d600b7f300615aada88430a937774f4f19a53f70de68b85504b8cb5bfbf3`  
		Last Modified: Tue, 04 Jul 2023 13:30:27 GMT  
		Size: 17.7 MB (17728896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1992f13095c778962a0c4b92ccc051fbb82545a2e02ed8e6856ef0f749bbb9c`  
		Last Modified: Thu, 20 Jul 2023 20:14:02 GMT  
		Size: 203.3 MB (203265131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
