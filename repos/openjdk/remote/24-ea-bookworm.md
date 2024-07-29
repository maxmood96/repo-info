## `openjdk:24-ea-bookworm`

```console
$ docker pull openjdk@sha256:5633da8cc83c9ba82c981917b8ab9e4a8dd1d934b289ff90a25b3e5b0296b906
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:115b16497eb97154ee2b876293462f6c6cdafeccf9f5b1f103768a3edf8f30c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366532290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b062ce8416a0747694faa4446f5b4a273029516904844917d35a32331668d81`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5c011bf8deaf18b8ec1d88b3905f795ea72359a2e0d98b47e61fac0d7aa3b9`  
		Last Modified: Mon, 29 Jul 2024 16:56:36 GMT  
		Size: 16.9 MB (16942969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9436051f786e92460afd84569f3f85139c1e72212cc8e41c33c160985bf98f`  
		Last Modified: Mon, 29 Jul 2024 16:56:38 GMT  
		Size: 211.8 MB (211841251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f75a0ade1905404ba533adf9f582ed9a20fc1411dd92b2130b53978cbbe6de6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8276432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c157eb288b9d1b6a2e6ab22e7dbca65fc55181ef0d7925262f9ae7dc6f6a70`

```dockerfile
```

-	Layers:
	-	`sha256:5dec1494e6489b95d186856c320a5c2b490c47244e48253edf0526b7fb5d4c05`  
		Last Modified: Mon, 29 Jul 2024 16:56:36 GMT  
		Size: 8.3 MB (8257986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12c43ed1d54448818bf7b9a508211b84b18d7b1227f46b4813dd9aae42650a4`  
		Last Modified: Mon, 29 Jul 2024 16:56:36 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6b0b340fad2d70e1c870f094e3b1d4d6125b5a04b100e257e53a61646430afbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364613086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5202d2a95e27c0338f9a6e9f5003baed5c08a5674d31b6226ba20e76b00bbb0a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad2e5609f4bf13e28a549241365ce86413b647e67b95cba7c36a2233342908a`  
		Last Modified: Mon, 29 Jul 2024 16:59:05 GMT  
		Size: 17.7 MB (17727179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511c50ef2858e4e6ebe61571d2a7cb9e7d9a53bbe4d4b8723493a4ee59e98d56`  
		Last Modified: Mon, 29 Jul 2024 16:59:09 GMT  
		Size: 209.7 MB (209710724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:017d9da26df373e503d8126a57017f1a9a29cbe75372bf760841e959035203bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8414433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878bbe64baea0b43a07f1a3395a3271da1a9015eb59baacf14cad18c1e6780d2`

```dockerfile
```

-	Layers:
	-	`sha256:d51aed105b7cd75be98ea78c71781a31234cde759f1513a1eaea05660343641a`  
		Last Modified: Mon, 29 Jul 2024 16:59:05 GMT  
		Size: 8.4 MB (8395647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c69a5afc8c07eebd966f0dc53795d9bb29e9f7c04b7e6f9016a184ec41d756`  
		Last Modified: Mon, 29 Jul 2024 16:59:04 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json
