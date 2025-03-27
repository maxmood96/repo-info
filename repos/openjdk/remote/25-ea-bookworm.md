## `openjdk:25-ea-bookworm`

```console
$ docker pull openjdk@sha256:2c7bb414c127d1e027a056aaf0272807d3f675c81a9e334aac337770e723594c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e1db53f9efda8b2a99d5916a9aa6f21a5c3e9c2738dd5d474658a052abc64a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366110460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa95647fdd4d9c32652f8701886c22389a634d08be79f4b3e82b1bbf188cdf82`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
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
	-	`sha256:52a52a4d39a4f777243ff463648aad9cddd254d5835562939ddc1f94c63948f0`  
		Last Modified: Thu, 27 Mar 2025 20:45:48 GMT  
		Size: 16.9 MB (16943108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e0b93954c66cd779d5cffcbb694938a63dc5d15c86c0471c09002ed688c4aa`  
		Last Modified: Thu, 27 Mar 2025 20:45:53 GMT  
		Size: 212.3 MB (212291894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2034dad06b5b662f07d9fb5b07b8c04b4055b5b77920cb8ebf7e9442307cb435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8450569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001e187c0edd6689f52d8c8f0c9fa4e37a98582af53907ccb34fd4373cf0966f`

```dockerfile
```

-	Layers:
	-	`sha256:dbbe032b4202c369110f811ac97d78c956577323827d1159ea8c3a202808f577`  
		Last Modified: Thu, 27 Mar 2025 20:45:48 GMT  
		Size: 8.4 MB (8431951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd5260f2bd379de5b91e8592e6e9a5d262be16c022925000b5ce9673649f9f9`  
		Last Modified: Thu, 27 Mar 2025 20:45:47 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:132beae612d3414bbf82c323aeb70381b91fc6e0e8e3a9d5511a0ab5a41bccdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364119639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db26c9949c5aa1a369f6ad7c8f74a2570d294e2a251646fa835877b7e7fd7401`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
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
	-	`sha256:6a39eb638671aca31c31cec258c0f6a91f693343530bac472c906e3b740ca00d`  
		Last Modified: Fri, 21 Mar 2025 17:25:37 GMT  
		Size: 17.7 MB (17726818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeae898a6b246b2366474ae227ebc2065610d8d3476ac8f07a19c0ba714209c`  
		Last Modified: Thu, 27 Mar 2025 20:47:22 GMT  
		Size: 210.2 MB (210187826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:cf90e060100d9427c9c1cd9ef34faf15e481c75f6a2409c2f61b145ad86ae234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8587580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cef5fb06f5ad9ac63d7531e34c8e410c1a70e3f815e0aa35b4dedc166c9e09d`

```dockerfile
```

-	Layers:
	-	`sha256:27b803df49683cf316832c37610b5cf16ec94fd50d505f39d59a6ad87eb12336`  
		Last Modified: Thu, 27 Mar 2025 20:47:18 GMT  
		Size: 8.6 MB (8568819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20dab810ef8c551cf40b5c9029e0bb5971cf81141a9d5d2b3f1f8eb02892c44d`  
		Last Modified: Thu, 27 Mar 2025 20:47:17 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
