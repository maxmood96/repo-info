## `openjdk:25-ea-18-jdk-bullseye`

```console
$ docker pull openjdk@sha256:79ac51418f087d77c79a03138fe76eea926ea2453376fd3525e2a58f32d4b732
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-18-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:d3d199264f80e01b665d0561e7c75c1b98516ef4171fe16ead19d3f9f1273749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350316236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408aec9b9ee47b2bf0f3dd6b223a745d02a4f98aa41783740455562d144b2d92`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2246f1023f09275e01841c5ed822aac7c0a009d6f1c7c996024f81fac4ecb5c8`  
		Last Modified: Mon, 14 Apr 2025 22:58:50 GMT  
		Size: 14.1 MB (14071443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb8a75e330022f3f8b225fb1813a8b2a0156ced0c067cbbe55e0582b34fef2`  
		Last Modified: Mon, 14 Apr 2025 22:58:53 GMT  
		Size: 212.0 MB (211977602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-18-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:44e3d4fee9c8be71f4fec0e1e9741a8bce342da69077cf3da03450425f95b535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b5eb223a39a5cd329c0bea04cd2f5155e27eb74fd245980ec87519fa6e77c1`

```dockerfile
```

-	Layers:
	-	`sha256:10c12e29c44d5a4814a2f14fd44ec2629f0ad860de8ed58254a3878678efb8cb`  
		Last Modified: Mon, 14 Apr 2025 22:58:50 GMT  
		Size: 8.4 MB (8366136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a46f1ff27097d5e15d0931f72f5807f6e326cb25d2b062331853330ae73073`  
		Last Modified: Mon, 14 Apr 2025 22:58:49 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-18-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:01b09d08d373094fad4e01a54da983e6cb647e7be7584fb877c789231bc4e594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348173281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e780e89363bdc2769adc599881003d4b0593ce92f202d617ae62ae4b0d68d56`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b8d0e9b235be5e2e0be479250427b87473f356403cb62123cb458aeafa672e`  
		Last Modified: Mon, 14 Apr 2025 23:02:55 GMT  
		Size: 15.5 MB (15526571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03664ce001c8b738db74458b5a204d32984b4f365b60af7671299fe7b525a98a`  
		Last Modified: Mon, 14 Apr 2025 23:03:00 GMT  
		Size: 209.8 MB (209793393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-18-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e2d411c95b5456aa8ae5bba06ad9e7b4e308ebe020fa23b1073d0591d5a5d389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8485858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c780806b05d9061674d2018b744d5addc7482f9b1d9cf7dd939f018819a09b`

```dockerfile
```

-	Layers:
	-	`sha256:962d5d1e6ad9dcd2caea1b1af692d1117ec25989569233e0d8d64ac64d183d37`  
		Last Modified: Mon, 14 Apr 2025 23:02:55 GMT  
		Size: 8.5 MB (8467098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c585d212df31b983dace39d8100e98c9c0a9dee13739f0a59399c3a9d77b2b3d`  
		Last Modified: Mon, 14 Apr 2025 23:02:54 GMT  
		Size: 18.8 KB (18760 bytes)  
		MIME: application/vnd.in-toto+json
