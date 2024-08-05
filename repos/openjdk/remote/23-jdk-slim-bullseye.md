## `openjdk:23-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:4fd877f24481954ba4eda67b8697765eaa3da356282685566a7440f4af550cd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:5cf4b473609bc994bf88b5763f209055f9aab719d8ade9c24ce6ecb340fc2e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244488950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9a1bec9572365d89da779aa9fe732cb1c37c13ed2333d4abd76fad4ff68613`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Aug 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+35
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='5387c8da8acb4261265c12bb46cea856c248d70bf9d64164019b74ed96545655'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='d5765b057a4eca4913ddd3d661e0ecd9cb182d4ad79359a645e427bdadd574d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b816d03eb7a35ad5c51e98ffd1097b17040f2e1d7aa1bada14682efa9c27d`  
		Last Modified: Mon, 05 Aug 2024 18:57:50 GMT  
		Size: 1.6 MB (1581855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e76de3cf126a6620d9e4f92a90708125595b814f4f43f728b127e4b26a464d`  
		Last Modified: Mon, 05 Aug 2024 18:57:55 GMT  
		Size: 211.5 MB (211478765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ea296669c26c99c8db765434e86ec4babc7bf7d4719f661e0e66ee00017d56f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2676531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a28462c2662a1ab512709117fe77f128f1ee8e1a57e3fa36b09e3c31a0c1b90`

```dockerfile
```

-	Layers:
	-	`sha256:4651b8aad3e44f31217403135243108ad760374b336d21b85bdf4aa05a7a2a0f`  
		Last Modified: Mon, 05 Aug 2024 18:57:50 GMT  
		Size: 2.7 MB (2659174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa673418f0b5befd1571649d98e3eca93b0827f1d8a082c664e589eb9ce64cdc`  
		Last Modified: Mon, 05 Aug 2024 18:57:50 GMT  
		Size: 17.4 KB (17357 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0c57926c69efaad38d934f461824a86357429ef15bf05ea5b5269245acf04bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240982005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9d8cc628d63b0e4aaca4f4cd4561a3ae64e729c7643eb9f41649a3613b7277`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Aug 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+35
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='5387c8da8acb4261265c12bb46cea856c248d70bf9d64164019b74ed96545655'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='d5765b057a4eca4913ddd3d661e0ecd9cb182d4ad79359a645e427bdadd574d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3bd1e759a916e6497c78e1f9bc18301b82c1d8c089d5cd721ebc3c2f5e7f3f`  
		Last Modified: Mon, 29 Jul 2024 17:01:58 GMT  
		Size: 1.6 MB (1565920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116f8a437258039d834fd3db62527aad1bc00981a16a3960e2c034e8578fb78e`  
		Last Modified: Mon, 05 Aug 2024 19:16:08 GMT  
		Size: 209.3 MB (209340002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:368521db9a9ad55e41a57d0d8bc383fb9e6b7144f195ad9d64f9fafdf9b66d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7086d98bd4efae0c342d08148ff5fd15ba8417509736aaeb5ebc4b04b54952ea`

```dockerfile
```

-	Layers:
	-	`sha256:a6a7ebdcf5a804717a4213b8e81f1ddb19f5c87ebd8bf4d1b1b8f8ed7b82db7e`  
		Last Modified: Mon, 05 Aug 2024 19:16:04 GMT  
		Size: 2.7 MB (2659450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91e4da461822912f72abbf795a03564af0b2dca1584782458cf3279f2c4e93a`  
		Last Modified: Mon, 05 Aug 2024 19:16:03 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json
