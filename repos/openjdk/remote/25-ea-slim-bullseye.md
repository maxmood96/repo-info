## `openjdk:25-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:a61e1771832254508c465c4e0ca691256b5c2f14acdbea89cd3cd58c73c99586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:00341d2678808d85184b5f17b907c1914ace28aac754eaf41c9ab9c563b6d47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244243490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087e4c8cf68653925744a259f78217899c165bc8e555ae47ed2e49acf154b3b7`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Apr 2025 00:48:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60082729ee2e5a047f47937e29dcebe998e105ee54f8336595724c1ca5274d80`  
		Last Modified: Tue, 08 Apr 2025 01:28:15 GMT  
		Size: 1.6 MB (1581789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f1500a2b2707412f4736ace013461994986f0bff2aefcff9b46d152b540240`  
		Last Modified: Tue, 08 Apr 2025 01:28:20 GMT  
		Size: 212.4 MB (212404282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:d0274d99782b673b446f7603165bff6cb69cec409470b6a2e3ccf0cd163f0d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0184621899218506e723351c3175959d837d3a0ed0479521f99b448cf8ca659a`

```dockerfile
```

-	Layers:
	-	`sha256:88bab67c3288a85d35975302c0903550a73dd4fb94bc93bf88834a2e56777d04`  
		Last Modified: Tue, 08 Apr 2025 01:28:15 GMT  
		Size: 2.8 MB (2829207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7a7affb9f437cde33ec0e6c8701ab77438cb705b4f2384120d5ef4a084a4121`  
		Last Modified: Tue, 08 Apr 2025 01:28:15 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:84ba3e4c19e069067adfa7b66cf513a9d3905c8a197c47ca9f08555f25f04077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240546876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59a6f9cbd95ee29f0b7f55aa499b26cc010abfc38e05bc5fc80fb822d32bcda`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Apr 2025 00:48:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd8ddc11358b8be92d6647d19ae01fdcd8bbb7e11671d67d6b207b21db4044d`  
		Last Modified: Tue, 08 Apr 2025 06:49:23 GMT  
		Size: 1.6 MB (1565963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e85df68367f071f0e295cf8e5ea1e0989982cde3c863c9d440802ada1ea0e0`  
		Last Modified: Tue, 08 Apr 2025 06:49:27 GMT  
		Size: 210.2 MB (210231415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:281ed60226ba61f3cad1d132242516a645cd033815f9a27db9c42935a75234fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0735919b750acdedd32f309c160061248a8817283a1e09e566d755c68499b576`

```dockerfile
```

-	Layers:
	-	`sha256:f0263b1620a198475318ea41880e8caa4809a45b21e70b637e240803f2ffe695`  
		Last Modified: Tue, 08 Apr 2025 06:49:23 GMT  
		Size: 2.8 MB (2828859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3174113256f8c6b4c788df1c6da9a2ba3f9ebebcdc35fc9109430fa1b2cbf71`  
		Last Modified: Tue, 08 Apr 2025 06:49:22 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
