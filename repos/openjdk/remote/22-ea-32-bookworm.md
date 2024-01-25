## `openjdk:22-ea-32-bookworm`

```console
$ docker pull openjdk@sha256:fda9142c784f30665e8090f8e8d0356cc116f01a02d9f726f39e9a46dc31f8e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:22-ea-32-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:12057b9b06ff502f9f260c58da9a9fc7692204289bc685f9508ebe471d79417f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357575743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59bce079ef1489f4cc1b6b1840d6dd46b04df6dd3abfd7074b142660359e5f5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:31:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 23 Jan 2024 19:48:26 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 19:48:26 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_VERSION=22-ea+32
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='7ac0b8815f22c852796fa13b7680e07fa1dc340aa93f5e2bf1c5502337d952d6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='7c565754b2926817c1779683d6b8f1975a94a8731fad35a670ea669a77aea182'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d85599795460b2d9d24c6b87c53ec60555b601705cc83bea31632240500980`  
		Last Modified: Wed, 17 Jan 2024 02:00:06 GMT  
		Size: 64.1 MB (64139892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf0e0403cd0d84e0c0e51fdfd1adb1b1920cb43c3887dd0e881a2e26630cdef`  
		Last Modified: Wed, 24 Jan 2024 20:50:15 GMT  
		Size: 16.9 MB (16945727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadcefd27554bf4b48bbf3f7cd20b4742c458887e59d951a0016d42129939dd2`  
		Last Modified: Wed, 24 Jan 2024 20:50:18 GMT  
		Size: 202.9 MB (202882140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-32-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:77f1ecf13a6a97eacaa8754962b00bb51fb9f12893adf86658683bcf800e6427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2995bbf8003e82e7f9eefe5a2597da98a9b87e80b2628224821e9ef0080dc7`

```dockerfile
```

-	Layers:
	-	`sha256:f77d0681e0ef6b6694c5823ab7c2e4acf2033f778c335de389460a2ed5afc9d2`  
		Last Modified: Wed, 24 Jan 2024 20:50:15 GMT  
		Size: 7.1 MB (7116360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb1d56c8389e7d87edd74813c06b52424d8782e11aa8425d426719acecc9f020`  
		Last Modified: Wed, 24 Jan 2024 20:50:14 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json
