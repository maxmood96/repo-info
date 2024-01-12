## `openjdk:23-bookworm`

```console
$ docker pull openjdk@sha256:227e3234686b2c27f257168ef1a5a65b7cb4c1f2874cf27af087b07edeef5c5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:0eea9597498ff1005acfe3241f57cd6b592eef292e1b712bf73c4343e4414bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.8 MB (357803666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a26d0ff5e0205254e302ac56d5e9211bd632bf8ef7ecd38c3a5a6e2cfe56a9a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:52:17 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:52:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jan 2024 01:52:17 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_VERSION=23-ea+4
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='9a68dc2301a1ab9d674095ba14205b79ba23dd83002077ae6777edc820e789d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a7293d34fcb6c1b9f5b0bfc74aabc4e695b0e6d6b6778172d59596b19db6e4e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
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
	-	`sha256:8d55d1cb1ffb0c7e0438b372a96cc0f23a76c21571fa3e7b7b38e3fbc66a8c3a`  
		Last Modified: Thu, 11 Jan 2024 04:44:54 GMT  
		Size: 64.1 MB (64139713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f5b1321110b2d9c2e4c1232c5e4736b9b1d701c4234813f0b4624f7a8bc4c2`  
		Last Modified: Fri, 12 Jan 2024 00:22:35 GMT  
		Size: 16.9 MB (16945659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80970c9009513088a6fa5c4d794950bc13b645c12925d72f76d2eff3b3b7f9a`  
		Last Modified: Fri, 12 Jan 2024 00:22:39 GMT  
		Size: 203.1 MB (203110310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1d35a22a478d42c13cf996719f0f6aeabf07cccc10b07098feca6caed2f36c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d9c47941659b037d1487dc3b604fa11ca767b5e49e06b2f3bb4158bf49b918`

```dockerfile
```

-	Layers:
	-	`sha256:ca68e13652114beedb259ffe167362ed5673682040e62f26c9850eac5edcfb9f`  
		Last Modified: Fri, 12 Jan 2024 00:22:35 GMT  
		Size: 7.1 MB (7116352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d219f52c8237c8d51496fb7b50313172ea64010f97cce5836272d835afc7ba4`  
		Last Modified: Fri, 12 Jan 2024 00:22:34 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9c1d7e42c1fd4e73f2d2dab7eae66d7da2a2808dd4a7f5c83afa830217a919dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.9 MB (355908443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bef74ea53cd10b8a9e884813c1430d2ba79fa74d507203963cc8e4ddbf7494b`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:52:17 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:52:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jan 2024 01:52:17 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_VERSION=23-ea+4
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='9a68dc2301a1ab9d674095ba14205b79ba23dd83002077ae6777edc820e789d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a7293d34fcb6c1b9f5b0bfc74aabc4e695b0e6d6b6778172d59596b19db6e4e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069a35492a4c5b1727f36b1184c413a96ce816d65578adaf3bce2023a1765c0a`  
		Last Modified: Thu, 11 Jan 2024 09:34:23 GMT  
		Size: 64.0 MB (63990799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428630060163e40cf9f829265e1288a72aa00079dea1b8f66ab032378555b816`  
		Last Modified: Fri, 12 Jan 2024 09:20:46 GMT  
		Size: 17.7 MB (17728761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613b8e20e239fbfe4010b6a694dacb4deba866d21b379941d2f6816ca7609612`  
		Last Modified: Fri, 12 Jan 2024 09:20:53 GMT  
		Size: 201.0 MB (201014044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5fa86b31858c56dc2b23a063022f3b13f8fae13c5b3a60a7861385afd8158d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7254087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2f349dd69ae015584855dfe3e6cefb1e4c696444fd99ad790fdcecf28ed42a`

```dockerfile
```

-	Layers:
	-	`sha256:57ef98d74c0d94c66861de14f878acf60c37db6e9f521756a89391b0a8c4761a`  
		Last Modified: Fri, 12 Jan 2024 09:20:46 GMT  
		Size: 7.2 MB (7235183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:679e1783445bcee3aa0dfa21a5a215b000e8ce21d60232222eda4911645abf1d`  
		Last Modified: Fri, 12 Jan 2024 09:20:45 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json
