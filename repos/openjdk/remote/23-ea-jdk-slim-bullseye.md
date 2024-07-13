## `openjdk:23-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:288f2e6ae8633cb749ca2be6feb8ac8d0408fbd9abf1dad6cda15e15a9467795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:0faadd46e2a46976c29f18ff8bb5cfb62d759f91821f6605e4bc854a1bc6822f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244468511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb1e0512af19035e7a1b6d78a374bed7081d9579ed9452a1544e63912772b2d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21cbd2407f785b10cef0680b2c88b6d63585c16fe2c766b568ea284dbcd5c21`  
		Last Modified: Fri, 12 Jul 2024 21:57:25 GMT  
		Size: 1.6 MB (1581821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b841b5b2c42e02d6eabebb3a04b374bf069094d975128b71d5ade744c5451134`  
		Last Modified: Fri, 12 Jul 2024 21:57:30 GMT  
		Size: 211.5 MB (211464406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ce43896bf33369c2a10ba21810a8853772a94252ef786a29bd537b67f5f3e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e322eed4d868b9fa40621fc806f3cf4d876c0b1a8b3b6c4d906ec06dd14553ec`

```dockerfile
```

-	Layers:
	-	`sha256:d5f3c43a699866622ba6248df945308b94f019c40daaf1e13800f3e51cb2c384`  
		Last Modified: Fri, 12 Jul 2024 21:57:26 GMT  
		Size: 2.6 MB (2638497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff51e1a35b05e4928cc1c3f15d51cce99ebfee54be5d8fa9439dee4bd091ff1`  
		Last Modified: Fri, 12 Jul 2024 21:57:26 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:231bef05a413708250aa5199c9beb43f1320837244a8319731472c5f7c3160a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240987670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addc3c731edecaea98b7eb43762de54ad937efbf936ba00f9ad2e117dd55a1c2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9481a8d2d3f3b38231f6c31bd2dc38c7c315578dd58eb8e02ef7320a34d44efa`  
		Last Modified: Fri, 12 Jul 2024 22:09:40 GMT  
		Size: 1.6 MB (1565925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4f1d2b05947afb48638c03c657ca85859341dc539de0c9638b3754af20d0c6`  
		Last Modified: Fri, 12 Jul 2024 22:14:41 GMT  
		Size: 209.4 MB (209352130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5e62329cc50ff3cfa556af8f02e3e172f3f4d61db85c20de513fe0d8dbea1010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d0b88f131ba1796fb83526d4277b940d5934f74c932fea2c8b91f7376859db`

```dockerfile
```

-	Layers:
	-	`sha256:816c661fe4c870e8417eb964c66537233d22e97797f5f88932be2f965fd73ce0`  
		Last Modified: Fri, 12 Jul 2024 22:14:36 GMT  
		Size: 2.6 MB (2638773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c751a9b623c709ab33203138bb09b71c7689ed916549859e15ee83de0f8d87`  
		Last Modified: Fri, 12 Jul 2024 22:14:35 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json
