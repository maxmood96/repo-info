## `openjdk:26-ea-11-jdk-slim`

```console
$ docker pull openjdk@sha256:c3aa81e4da846b4e30bb8a6d7b1a4a4708f1bb5a81d9140e2c6c71b350781f50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-11-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:dc97065dd3ea5c48a8c0e9c6219ea1930a64f9a1fcaa6eb34caa640a12271835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255348599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55910ec5499a240cb193425db4716a96da4788dd88c12da4e04069904828fc72`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e1bb091c1cf2f7a13269bd945fe7f4d9c50b5b640c8c2e1a2874c07e2f6073`  
		Last Modified: Mon, 18 Aug 2025 18:24:51 GMT  
		Size: 2.4 MB (2371098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6394f9232c279a0e645948eede1e45e1cb4306071912a10cfbc5c20156d1e0`  
		Last Modified: Mon, 18 Aug 2025 21:36:06 GMT  
		Size: 223.2 MB (223204216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-11-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:e880edb724521e95273cf19ff7988fd4a95042a85ad0187ccb154541427b31fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57fe513dc8456151ce592fc50902f232e40dd6aec4a39207ae291c32375b0a44`

```dockerfile
```

-	Layers:
	-	`sha256:ae3d8422ec085a8a0fe97962aae2b81a4d74f4af3dffb48b9c6d6b0d1e92b8f7`  
		Last Modified: Mon, 18 Aug 2025 21:25:13 GMT  
		Size: 2.3 MB (2281656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975204884ab9a80b61398e2458aafbf5f26a7cbe87c1f57114f572ad415e65fe`  
		Last Modified: Mon, 18 Aug 2025 21:25:14 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-11-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0e2c9f476136f7ea1fe9295154343ef1bbdfb93ebf90d199ae04b017071bb5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253489396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9268b954cfe66dcb9a5e5de5808e8396d50612af10615b581226eff63deb9d2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8aafae0cffde53a4a97b3a67ecda78936d66918ef646e27519a1c2c6551a203`  
		Last Modified: Mon, 18 Aug 2025 22:23:58 GMT  
		Size: 2.3 MB (2314286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097407765727caaef3b0cb566ba89eb3ac72b9a788e99d4df6282a0fce64055e`  
		Last Modified: Mon, 18 Aug 2025 22:23:49 GMT  
		Size: 221.0 MB (221039066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-11-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:348317dd8bdbcf00c2d4011712495404beac35247f9d63332323b7a8414eaea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b808fc467a32ea167dcc77baf476acb0c3c8fb38ac857480fa297e0c14976b58`

```dockerfile
```

-	Layers:
	-	`sha256:c1c78deedcf924e47da266a96267c6c04a12f4def4b4a88d32e4964964cced99`  
		Last Modified: Tue, 19 Aug 2025 00:24:49 GMT  
		Size: 2.3 MB (2281390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14814c66dfdd6eb31510dbd72696bd1a1a8bd08364d5f374d66753b86059071c`  
		Last Modified: Tue, 19 Aug 2025 00:24:50 GMT  
		Size: 19.6 KB (19626 bytes)  
		MIME: application/vnd.in-toto+json
