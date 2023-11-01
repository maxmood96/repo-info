## `openjdk:22-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:36cecf568412571e426dde75e83b4116222eb61d5e4a0d6953ac7f2c613e88fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:f1fd1d3332c659724422a8af9ed6dd248dc81f145b6112bbc62ac2c0627b68da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360344091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575e7060c54e1d919590e0424f305cb9e6a4239b86047fb62c394de65233c945`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:52:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 00:52:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:50:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:50:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 01 Nov 2023 11:50:32 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 11:50:32 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 11:50:32 GMT
ENV JAVA_VERSION=22-ea+21
# Wed, 01 Nov 2023 11:50:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='cefe6f9697801dd2a7abebdbd5b7bd36ad489794589e838562da46bde434ae5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='b77e7f170973c91690aa64a028f2e991828fde5092eabc29b602e26824216797'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 01 Nov 2023 11:50:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13baa2029dde87a21b87127168a0fb50a007c07da6b5adc8864e1fe1376c86ff`  
		Last Modified: Wed, 01 Nov 2023 01:02:01 GMT  
		Size: 24.0 MB (24049147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325c5bf4c2f26c11380501bec4b6eef8a3ea35b554aa1b222cbcd1e1fe11ae1d`  
		Last Modified: Wed, 01 Nov 2023 01:02:20 GMT  
		Size: 64.1 MB (64130415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97135b4a132821de70b5d1180269f8a89c06ca476b3d02709f674d75da34eb1d`  
		Last Modified: Wed, 01 Nov 2023 11:52:41 GMT  
		Size: 17.0 MB (16951833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bd7ba9c0d0daef3670da83af846f992c3824a38a48534ea9b7e030988449f1`  
		Last Modified: Wed, 01 Nov 2023 11:52:53 GMT  
		Size: 205.6 MB (205630672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a4530dea9f096f47fbb41017bf11a31b13f7f835d84f56a9c782476e588ad5af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358763370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2784f75b54aa954b98840ee2b830065a9b2dd336eb9e6d61e9b767a794e24e2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:04:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 03:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 03:21:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 01 Nov 2023 03:21:48 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:21:48 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 03:21:48 GMT
ENV JAVA_VERSION=22-ea+21
# Wed, 01 Nov 2023 03:21:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='cefe6f9697801dd2a7abebdbd5b7bd36ad489794589e838562da46bde434ae5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='b77e7f170973c91690aa64a028f2e991828fde5092eabc29b602e26824216797'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 01 Nov 2023 03:22:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d826ee8aa65e56e167f0e27fa65cfc065687a7ac6c360787d5940d8b51f0cf1`  
		Last Modified: Wed, 01 Nov 2023 02:13:39 GMT  
		Size: 23.6 MB (23584896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198068495d09b6865e75ce28d5d5d5de39897b8325ada63ba80eca884ad5666b`  
		Last Modified: Wed, 01 Nov 2023 02:13:57 GMT  
		Size: 64.0 MB (63994018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459caeca6f2dabcdd676f48943e8a6f36c3bf3fb165acf2bdab551ecf3414f6`  
		Last Modified: Wed, 01 Nov 2023 03:23:46 GMT  
		Size: 17.7 MB (17733531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6fea50f876f5212f29f38ca7d6c21ff117a84cdbd51c8c32a4bdb8e5437abc`  
		Last Modified: Wed, 01 Nov 2023 03:23:57 GMT  
		Size: 203.8 MB (203838272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
