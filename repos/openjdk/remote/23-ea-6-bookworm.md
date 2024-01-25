## `openjdk:23-ea-6-bookworm`

```console
$ docker pull openjdk@sha256:8ab27d13e66154b9a64d64ec59e6cc225549adf6aa658fc4a1af4225c022bf8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-6-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:1a1f5496188fdac924d41356c6f386650502f301afa4a9c4229df81fa2ab7962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357873084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cba62cbabb8b741ae6b73ccfb925f8ee242db75a535ce0e7523f4d6408d1d9`
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
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Tue, 23 Jan 2024 20:18:23 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 20:18:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_VERSION=23-ea+6
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='5163a8a077bfb1cb60e6b4ade06959b0ecba73399a509a5e83f8f9df5cebd140'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa7e954bb29a17c5d0095c4ce94275bfe53383cb8aa7f14894d352e9c00110c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
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
	-	`sha256:9a577dc800fe8a1d404e948cd14eebe2283aa960ffc44a4851e9c36e730616f4`  
		Last Modified: Wed, 24 Jan 2024 20:56:55 GMT  
		Size: 16.9 MB (16945700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b1cf7f3ff9736663dbbd7b8078a507f0ce78a480ff2a2ac030635d38094316`  
		Last Modified: Wed, 24 Jan 2024 20:56:58 GMT  
		Size: 203.2 MB (203179508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-6-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8a3f863883cef05ace61e75f4c407baca9cd41fcd8424e6a048d5ee0cf6af350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208cc7be8e1ff9fae89847914739ecb4b26a8560b0a051341f583df8fe87a295`

```dockerfile
```

-	Layers:
	-	`sha256:c126eea7bcbd81a41362c79cdac13c7e6c18404577a6988622e131aacdb6fd64`  
		Last Modified: Wed, 24 Jan 2024 20:56:54 GMT  
		Size: 7.1 MB (7116352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:596f36782294c5441ccfb4c8f3f741bf8c3e890a1d9085fcfdf3835f9316bcc4`  
		Last Modified: Wed, 24 Jan 2024 20:56:54 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json
