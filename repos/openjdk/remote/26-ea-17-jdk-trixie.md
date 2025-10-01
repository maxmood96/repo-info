## `openjdk:26-ea-17-jdk-trixie`

```console
$ docker pull openjdk@sha256:a2163a71267784a2352250aa465eb4c161c97194c0485d2b3b0b2f6172b8325f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-17-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:a73979145617be41103091820112694419339d0b09b8d677b0dea134c6a587d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384458604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5331d514cbe2a9ad77fd10cb1c2301943dc9a1cab38a8b7d0919434e47de3a99`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 26 Sep 2025 18:48:12 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='0a80f3aa3279fbcd36b9247a873bc99b3688ce092a970c08ff3788e2fac99351'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='d12fc689cf8b2e7c1b503472b988320ad15693d9b40c3e877e9f78aae6fb82a1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ac1bfc6035235053592393992cf7231e6b01b55806ebb7de9f4e74f7204f93`  
		Last Modified: Tue, 30 Sep 2025 06:44:25 GMT  
		Size: 16.1 MB (16061154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61f47700821e8b06a45a1897bed43af1f25ac93f03150d63a869922c2293395`  
		Last Modified: Wed, 01 Oct 2025 01:09:17 GMT  
		Size: 225.7 MB (225713065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-17-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:c3137f27b44d23f31d0dd62211efc0495b316606e535dd79a34b33ea13181360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8531556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d286418095475081557ec7b266289f8b20c259ec2bf5fa9865c20e11f45a93`

```dockerfile
```

-	Layers:
	-	`sha256:0973028276d4a9828336bebbbadbf53d3934530741fa4969cf81231de1ee40b2`  
		Last Modified: Tue, 30 Sep 2025 21:32:50 GMT  
		Size: 8.5 MB (8512972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0299a73b9c705a70563fb333e682c8435e14ddadb725e1814bd5199612ab7bd`  
		Last Modified: Tue, 30 Sep 2025 21:32:50 GMT  
		Size: 18.6 KB (18584 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-17-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cbdabac305744a899a9b46a17094107f984b9d6a78eefc64d48fa1dd36185189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381928176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e567e84cda9127a035c0b73fca00cb8d3ab87e6b8a84699075eac64536d753`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 26 Sep 2025 18:48:12 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='0a80f3aa3279fbcd36b9247a873bc99b3688ce092a970c08ff3788e2fac99351'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='d12fc689cf8b2e7c1b503472b988320ad15693d9b40c3e877e9f78aae6fb82a1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c9631087ef516f060328537d417f223e1f264c968e39186895696e78090b7`  
		Last Modified: Tue, 30 Sep 2025 01:20:15 GMT  
		Size: 67.6 MB (67582977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ca2247774c1071b538489bd0d8c540711fe4fcb7a29146f7c7ac4204ceae7`  
		Last Modified: Tue, 30 Sep 2025 02:17:30 GMT  
		Size: 16.1 MB (16069974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fa95da301183556cd3429260f4b69169f96a3b1dcc501d838b29aaf1a83361`  
		Last Modified: Wed, 01 Oct 2025 12:15:10 GMT  
		Size: 223.6 MB (223610160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-17-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:8c3547345334625b9b26cc5f2d8ad2ace60b60716637bcbc064e2462cfef5e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8726513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5e0dc9377e6b2a002de7614e942de1426fa3d32008544cbbbf35eb10d5268b`

```dockerfile
```

-	Layers:
	-	`sha256:bf139ec8f6a4752bb26533853b5ef10e4794fcc48f21e2aa937d778cc32b115b`  
		Last Modified: Tue, 30 Sep 2025 12:23:48 GMT  
		Size: 8.7 MB (8707786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad368877c3293d721c355d13821cc57a30eb9f4249220805924f10371e0cac3`  
		Last Modified: Tue, 30 Sep 2025 12:23:49 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json
