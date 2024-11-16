## `openjdk:24-jdk-bookworm`

```console
$ docker pull openjdk@sha256:0e3df426883c34b294546134717739320a10c6921eadc51f356efe4de8f27316
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:4081788b40873a6cc4c1e6ffe1c871d1532bb59c995681e021b19499da975ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.2 MB (377182143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c67fafbf82de78f57430bb86c7c5998f76e198ff54388425c3e14b9fb70650f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d036a7e919560942a57d1ce372e2668e31f65a6c9ab6030813d5f0af018fc963`  
		Last Modified: Fri, 15 Nov 2024 23:04:50 GMT  
		Size: 16.9 MB (16943074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce44f15e042a114eeacef53173832a805eeb20e8fdf29b908673ce1ce626fad`  
		Last Modified: Fri, 15 Nov 2024 23:04:53 GMT  
		Size: 222.2 MB (222213652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e49c9ccb2df1f952c2c7d6337cc7e6a25e48ec81c72e1481817ea532ef60668c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8463864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0333a8b02302407a109567dac11d39288c55e007ac1a15aba49f8e86d4515d`

```dockerfile
```

-	Layers:
	-	`sha256:bec8a154ef2d09ac44f12aac9a7783d8e06354b83b003fce7f90d5475eae3e7c`  
		Last Modified: Fri, 15 Nov 2024 23:04:50 GMT  
		Size: 8.4 MB (8445246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dedc6769f618993a964f8c41df73866011326ec7411afeaf85c845dfbcbae08`  
		Last Modified: Fri, 15 Nov 2024 23:04:49 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a4660c71c73a99c03b08a1c39d4afc80b19dc54cde6ca29277acded2a1ad92af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.4 MB (375425310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c874b6b82db7e345a67f535b8ac8e28115c7b724de38028df334b7696ff9f504`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da77587964f4bbb2b7c9115b16a9fc672b4ae417c45bc0d66fbcf77843a55d8`  
		Last Modified: Wed, 13 Nov 2024 09:12:01 GMT  
		Size: 17.7 MB (17726633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e40e8f7abef780fd0e58bd324a53994d56b73e962f90adb9ee001995a0a8ba0`  
		Last Modified: Fri, 15 Nov 2024 23:11:06 GMT  
		Size: 220.2 MB (220165523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7a7727eece83ad0ab552162c9f8f33721469c51d80928d24b875e45ecbd868ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8601042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7de019fa3dabc893336b9a2d2a0bbdb5a720f19d70e8a3b6cf6795555eb71e`

```dockerfile
```

-	Layers:
	-	`sha256:334a512f1b9ac4fbc97f718194e38b19121ad3a809ef5724faee6c410e48fcf5`  
		Last Modified: Fri, 15 Nov 2024 23:11:01 GMT  
		Size: 8.6 MB (8582281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f77fad04e8e1f9a5a6abeb8be8c9b547ceaa588e6060e3f01713e62534238df9`  
		Last Modified: Fri, 15 Nov 2024 23:11:00 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
