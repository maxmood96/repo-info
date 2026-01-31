## `openjdk:26-ea-33-slim`

```console
$ docker pull openjdk@sha256:ee85500c28bee0c67e05211d26913d54808e21ca969397b504ff628032e2792b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-33-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:420af5ec09ff45b391c69abde5ba95823a65acf60d74aca598325d16e788469e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263142962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d62cf6db7cb9347a7272076a2e5aba167f7458c563c833675f9b8b8aa05ade`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 30 Jan 2026 23:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 30 Jan 2026 23:40:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:17 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:17 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3d874c2bb4252786cd3ab529fcba80cfdb3beca489f07128f9ba135055dee6`  
		Last Modified: Fri, 30 Jan 2026 23:40:38 GMT  
		Size: 5.3 MB (5333279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0122af62331f6b74722cd2908d28a27d2843c6f7d9dbb4ed22294d41a306670`  
		Last Modified: Fri, 30 Jan 2026 23:40:42 GMT  
		Size: 228.0 MB (228035998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:47ddad2102fa9aefae5bdbf5fb08db2268b02847bb38bc0dc39b2c8914c89e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8073a43836ea625387eddee44c143cd6a1754d9d6db0922605b5d6236b3d7d2`

```dockerfile
```

-	Layers:
	-	`sha256:524e9864aa7c03372fe3691296cdc553418c397ceaaf10cfb2eda0aeed3d896a`  
		Last Modified: Fri, 30 Jan 2026 23:40:38 GMT  
		Size: 2.3 MB (2278851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff4f222f8b66e63cbfaafa3f69233ebe3c7c913bdcdd1a32bbfee8b155c8d59`  
		Last Modified: Fri, 30 Jan 2026 23:40:37 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-33-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fcdc31a0845863fc9f039ea5e7526abd73cd4674b81798d23072a14d9a0a0b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261721170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d37871294cad608f68612f233d8cb9a4fe8082381664b1fe8a3ed85b46e9a4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 30 Jan 2026 23:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 30 Jan 2026 23:40:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:13 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:13 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f0e2ae7133d06c1f6a3dbb1709df1dd803a430499874ac54078cfc0ccc4cac`  
		Last Modified: Fri, 30 Jan 2026 23:40:34 GMT  
		Size: 5.6 MB (5635664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215c107e67e7249d207e333215c6e943c27c194597e6dadcd53960166c21f3cb`  
		Last Modified: Fri, 30 Jan 2026 23:40:38 GMT  
		Size: 226.0 MB (225951464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:9203bd38ea42582d5bdad9d992368b9f578d13e374234db97321f167a6605b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa464ce24b63e7c0ee2f60378aa6f51821536dc513482d71f948d207c104d3`

```dockerfile
```

-	Layers:
	-	`sha256:06f2fc01af2acee70062a5fbbc8fe9ff1903283a8d61498230d5ca865ef000b4`  
		Last Modified: Fri, 30 Jan 2026 23:40:34 GMT  
		Size: 2.3 MB (2278537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9beb08e23aacb19de3ce6641cf5316a5fc4e832dc8be8b1ec73281529028428d`  
		Last Modified: Fri, 30 Jan 2026 23:40:34 GMT  
		Size: 18.3 KB (18275 bytes)  
		MIME: application/vnd.in-toto+json
