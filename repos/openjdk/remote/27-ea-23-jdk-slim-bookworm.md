## `openjdk:27-ea-23-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:920e4f7b1c1a1c6b726b4f05397625e45d8d765dc6ae5ac1778d13ba71eb9a42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-23-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:9ee01c1b12b6e0b5a1e9a4aab0131807e7578948c64555a2f08301da95d9fbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261232859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625c00a95c930e27f626cba12f9baeb4eec59dfad97968a2b82139ffb922b95`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 26 May 2026 19:09:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:10:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 26 May 2026 19:10:08 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:10:08 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:10:08 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:10:08 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:10:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5db2c120e8867cb57e39ddf2417feabbe30c5acbd0293e4a2aa03572edd056`  
		Last Modified: Tue, 26 May 2026 19:10:26 GMT  
		Size: 4.0 MB (4032612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2020d8da64d6bdd6bb5c198dea496c7114a6751da16829dd4760d8d5d0883c21`  
		Last Modified: Tue, 26 May 2026 19:10:32 GMT  
		Size: 229.0 MB (228966704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-23-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:077c93a4cca9f464822c5ca9b1a6d08b64c9541214349d8df94e8181dd5c8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdba69956d717c375f228e76f726d710e2125ca7829bae60bb41f20f34f1376`

```dockerfile
```

-	Layers:
	-	`sha256:aff21ac6208c81679af0d20b4dc9c60cc7de58ee6475d3c459fec176e6edd67b`  
		Last Modified: Tue, 26 May 2026 19:10:26 GMT  
		Size: 2.6 MB (2648559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b1623e6ac9d3f2cc02ce3124362ee3d104e9cf59af3936a8021d1ece575ae5`  
		Last Modified: Tue, 26 May 2026 19:10:26 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-23-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dad2d93acd6778318e64b1896df7a45d53f30945a75cacf763bebb66fba4bcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258892705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52148750f9e70d3c059ebc5cbec73ef05cbe55f9c67f73b1741f39977bc523b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 26 May 2026 19:12:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 26 May 2026 19:12:18 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:12:18 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:12:18 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:12:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:12:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a755d0e284129736281477f2a50cf1e25969d22d640543eab0c7c4a9e5b0c3`  
		Last Modified: Tue, 26 May 2026 19:12:38 GMT  
		Size: 3.9 MB (3852934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4ab2bc989ff6a926eb0df4eb93823d02da815e0e9eea0e6153e1110c6296e4`  
		Last Modified: Tue, 26 May 2026 19:12:44 GMT  
		Size: 226.9 MB (226924728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-23-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:89cc7571e5c959c00cd032367c9e481f0a756ce454cb1b4617f8bb48b5744697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6961072786ed8a3c4e1cb3f786282daf88686b97c893b6dcd377f22fdfb04dca`

```dockerfile
```

-	Layers:
	-	`sha256:16760d75ba887fb629c23c91b8e2aa9618e0ed22c9d28b8d41d80b51e52cb9a6`  
		Last Modified: Tue, 26 May 2026 19:12:39 GMT  
		Size: 2.6 MB (2648193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96984f8b3228e6b2737d59e46b80bbf340b583b0d555eb0bbdda8e602f84ab91`  
		Last Modified: Tue, 26 May 2026 19:12:38 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
