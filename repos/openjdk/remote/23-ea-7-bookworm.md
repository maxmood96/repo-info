## `openjdk:23-ea-7-bookworm`

```console
$ docker pull openjdk@sha256:4327b3cfde622fe06c7529cc7a1dd68f9712da52444eb8a43cc00e6288ea9f2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-7-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:f72860c6d1f37c3f1099e1e9770a82d48fae902f1fc616427c0c9bc81ad37e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.0 MB (357959949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4a6625ddd3d6183621af361db1620ddfc34769121c604a060d013cfa5c8064`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 01:56:28 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcae9c3a5744a78b84d0b11591ed6305d62e78d5e8238d263cb447e0ca2161b`  
		Last Modified: Wed, 31 Jan 2024 23:55:31 GMT  
		Size: 16.9 MB (16949145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31511551f29eb52ba5bb2b475507cc1fa9ced33c6a3398679cea131a7e3eb1dc`  
		Last Modified: Wed, 31 Jan 2024 23:55:36 GMT  
		Size: 203.2 MB (203234639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-7-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7369963c878a27bb28e12d11b2fc25e292d3cc881e72c6f960e969b254081ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c584151d844e8bc5cabac45caea9dab889d425aa8b8f9d97d4d5975b0aaeb969`

```dockerfile
```

-	Layers:
	-	`sha256:d89fdf14c17f1768a363eac176968990fed3425c412c7f1cd8c8bb93234c4da7`  
		Last Modified: Wed, 31 Jan 2024 23:55:30 GMT  
		Size: 7.1 MB (7116352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec033cfd4db84d7a93057984c9236a2d225d3eb6bbf90c2e07e7845511f14f30`  
		Last Modified: Wed, 31 Jan 2024 23:55:30 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-7-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9c64b49b17dd58877fd83628c91a23a5b39dbc48c6508e985b95f4afc5e84509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.1 MB (356066252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75381e72493f4c13c879ffb6ac2e862c5e987a87c617ab336330be77406ad60d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 01:56:28 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5985ce67cc9b5be13bbd1d05bdaef8d5b3eef2c56ba38018645982e475f95a`  
		Last Modified: Fri, 02 Feb 2024 14:12:30 GMT  
		Size: 17.7 MB (17732244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f794b18d4ba1395bb32ea8eef4963959589b8adaebe481d8d7ecf7bc1e543e76`  
		Last Modified: Fri, 02 Feb 2024 14:12:35 GMT  
		Size: 201.1 MB (201137456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-7-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:966ca04567be3b9fff1df73d910d79f84bce7d4fa72838719693733920d54c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7254087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62899d091e191f9ab1179ae1c5ab5e9afbdb50fd471ec873146ff432fc3ce180`

```dockerfile
```

-	Layers:
	-	`sha256:9efd30f39043a375dace96680b922db91ee2dc5665a901ecc9c682e8c39f5e9b`  
		Last Modified: Fri, 02 Feb 2024 14:12:31 GMT  
		Size: 7.2 MB (7235183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf522a10223e9069b262773db403070fbcfdb2e1dd4ee1281f42bea861fa720`  
		Last Modified: Fri, 02 Feb 2024 14:12:29 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json
