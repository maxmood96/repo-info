## `openjdk:23-slim-bookworm`

```console
$ docker pull openjdk@sha256:4467ee318470e89c8a91fd04f4cb41a7101023f587dbe9929e2f0d6318c5fd2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:eed24e858bf5813a0bc5591903b47ceca276c9d0fc9e9613fa694867adb55104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244406915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c182d1a45789d9a53dfdfb2759f2821d3c0fb8b0497482e00c0817661e124aac`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba0b1964aeb5d6d568c0cc6ebfca97274114ab20d09fc9af4a69fcd1941d8dd`  
		Last Modified: Fri, 14 Jun 2024 01:01:15 GMT  
		Size: 3.8 MB (3821800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33f2268b0e9bad7945071e607d4899a795143b2cbc691e2976843538f63f44c`  
		Last Modified: Fri, 14 Jun 2024 01:01:18 GMT  
		Size: 211.4 MB (211434685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e0df2a9f5cbd068c5e567d22be52acefcf81023c321044155b1e40a431fb043c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8404de55bc7170344ead283df2b817021fdce8d93e5165c24917381e1b7056c2`

```dockerfile
```

-	Layers:
	-	`sha256:6a37a85740ac92f0592dfda4440a4b9fb86c015950c2da44fcfeea58008b2c59`  
		Last Modified: Fri, 14 Jun 2024 01:01:15 GMT  
		Size: 2.3 MB (2346316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3245fafda5608d8b1d9ad2898ec11f2a2863458b91f0d6194e9fa8e8a8589257`  
		Last Modified: Fri, 14 Jun 2024 01:01:15 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2061970985599b77bbe407a7689f9cbe335c7ad571e9912491a8ea0cc8fdfef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242138126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fae2ee072eacd34e56a44fff08604a4e56176ccc6cdd986213112fe611d413`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb960144e9a3234b18ad0a695286d60905b47d016807f2c30ce00e0acd5b3ab5`  
		Last Modified: Thu, 13 Jun 2024 19:56:32 GMT  
		Size: 3.6 MB (3629819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a33d401c4eeffa6d2bbe228d09862e2bd3077241a3127d7602362c0fb08c99`  
		Last Modified: Fri, 14 Jun 2024 04:12:24 GMT  
		Size: 209.3 MB (209328641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f56164bfca0ba3e052671f24712436eea44d8b7b6440729769e540c2b682b687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f479feb0646de06cee5146a86c6c644d01d1709502313d6a3a62b848935d922f`

```dockerfile
```

-	Layers:
	-	`sha256:2a4fcc5a3bd45dbb2208ca0995c6e14b725c92389bf392e9d6967fc423faa03f`  
		Last Modified: Fri, 14 Jun 2024 04:12:19 GMT  
		Size: 2.3 MB (2346670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5848b418500144bebbfd134759246b6a01be69651bc1b9e93b061c3b27672e1`  
		Last Modified: Fri, 14 Jun 2024 04:12:19 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json
