## `openjdk:25-bookworm`

```console
$ docker pull openjdk@sha256:b61b0e8169fab95791ed192529316d038c6900cda1c7b2d3d8a515a0e85dfd05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e1a4c31b831652619ce6e2e73aba21b21f1e93cfeb417dc14b5d4d381705894f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365694340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c33b37dfcf2f1dc137d1e9615e7f61e0b910c27acf51c1ec6bc5931ac6b9d27`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255774e0027b72d2327719e78dbad5ad8c9cf446d055e45be7fc149418470bae`  
		Last Modified: Tue, 18 Mar 2025 00:18:51 GMT  
		Size: 64.4 MB (64396484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a7c6e66ecb583fa4ab182712c676a28f9459afce2acab9178dbb58ea2ff742`  
		Last Modified: Tue, 18 Mar 2025 01:13:25 GMT  
		Size: 16.9 MB (16942997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad68f993f0d5af7f5acd02126e71900180e585fae42a808666824358c572462`  
		Last Modified: Tue, 18 Mar 2025 01:13:30 GMT  
		Size: 211.9 MB (211875885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:46e92d6f91f1db6b9edecedddfdb0dfbf8be1ea0defd923ba0156b0f6cada6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8450569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66feeaab84e0826aa14cf36eba998338979c45f0b61e4d96d3e1700cc2b9cee6`

```dockerfile
```

-	Layers:
	-	`sha256:b8be04f0269b019938b4c8853625f0ff8e3f7dd024c546b1c502884bb81478c6`  
		Last Modified: Tue, 18 Mar 2025 01:13:25 GMT  
		Size: 8.4 MB (8431951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aeef0a149616a51d8c049039f86e2c206413e98cc30fe9e52e981dc9b452fb8`  
		Last Modified: Tue, 18 Mar 2025 01:13:25 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9b9f46231d70e07f58038bfc36020276f8412cf49740eb226a6de42080340b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.8 MB (363764966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6192341fea43542214e04f3217d1087cc5eb8efe40b60aea63c50ad59af1ae48`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106ba329b49f3a9b20cef55d874fb509ab821a658fc215b000644c96c40384d0`  
		Last Modified: Tue, 18 Mar 2025 14:39:42 GMT  
		Size: 17.7 MB (17726763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add8366f85bbf869781479fa744402d2e335f8cceb21a24f0cd095d1699b965c`  
		Last Modified: Tue, 18 Mar 2025 14:44:45 GMT  
		Size: 209.8 MB (209833208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b7b7cc95303a3fdbd4f54324be84dcaee5c0854aee981dcdaa19a96a1d04e5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8587580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b22a1b11118d0cc0eef64d20dec6b4e6d0a0852fa55119f311e1edbdbc22aa`

```dockerfile
```

-	Layers:
	-	`sha256:3998a8d0490155cfe0c77c6cff1b9230306944814c1152702da0b2c69d7f92fe`  
		Last Modified: Tue, 18 Mar 2025 14:44:37 GMT  
		Size: 8.6 MB (8568819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab1eecf290602f9924e4010f59f921847698f391adb0b194e11baf8ded20c311`  
		Last Modified: Tue, 18 Mar 2025 14:44:36 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
