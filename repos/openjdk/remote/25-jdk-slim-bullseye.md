## `openjdk:25-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:4675c01204ecb9c7fd45a7a98644b7131900dcfc9bacdf6a492cefc50a236562
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:eeeaa9fecf627f895f6fcb6309879f29ecbe7ce00667dc5ca51119892b1f48d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243868756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd770b881c9802971e1e4813e510b3534be6374cd1b0e886b1a5f47407464c5d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c56f6ea38d31ce1b4e4135ab9a84cec57e779d3549caa20877d88838ce9f5`  
		Last Modified: Mon, 14 Apr 2025 22:58:45 GMT  
		Size: 1.6 MB (1581831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf3c051f23e8558a6786283cfb0ba200047c13427f4222a9c06670cb5fa903`  
		Last Modified: Mon, 14 Apr 2025 22:58:48 GMT  
		Size: 212.0 MB (212029506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:1ccd80625df4cd9f80e6f60eeafc0e8d168d6f28a765e4adf77d0497117f7f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cff553a32e36f5122b8f020725fe9aad03fb2ccf85e3b368a16ed7ee028f363`

```dockerfile
```

-	Layers:
	-	`sha256:ef3793f9428f9951df681fe5931ce1c61dab67274957ec4a497214e8a965847e`  
		Last Modified: Mon, 14 Apr 2025 22:58:45 GMT  
		Size: 2.8 MB (2829207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33643011b0a2592776fdcc66ffa5c9c3b1872148a0dc92e2da51cccb9b68bde7`  
		Last Modified: Mon, 14 Apr 2025 22:58:44 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8353445ded2bdf5dbc7f15e5239800f23f4fea2259a22f64392a31f1973589f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240161146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77578a3b66c56bfbdffeabb82395b18a52ef9ad70449fdbf3caf7413c6aa6e0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609a7e4368bd79410cad3a425c733de39f59e4e41157ea12172a4ef1e0bee0d9`  
		Last Modified: Mon, 14 Apr 2025 23:03:48 GMT  
		Size: 1.6 MB (1565936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d0fbc765960b02f176f1ef6cc0d541b19d95cfb3b520ae478e1009267082b7`  
		Last Modified: Mon, 14 Apr 2025 23:03:55 GMT  
		Size: 209.8 MB (209845712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:98198007229cb4edefa745c15a94f70235dd6fdf58947689c0aa6914ee2d5cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8221eeb5aae8021f0f77382d46237fcc2c848de09a0c9daa91dfcc4bee5b3a`

```dockerfile
```

-	Layers:
	-	`sha256:0463b1959b2e7fb55a031dd335cb950a2075e99b623de6919fa32be5eb033c5c`  
		Last Modified: Mon, 14 Apr 2025 23:03:48 GMT  
		Size: 2.8 MB (2828859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31091b9db009c916c3ac425ca71ac5f5f30cc71b4e770d39f411a24ef5e23e25`  
		Last Modified: Mon, 14 Apr 2025 23:03:47 GMT  
		Size: 17.7 KB (17711 bytes)  
		MIME: application/vnd.in-toto+json
