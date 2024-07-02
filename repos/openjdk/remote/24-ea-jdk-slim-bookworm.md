## `openjdk:24-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:d41720342641faf68e62ae6f6e85f2ee2cc184bc4f880733249fd3c572f21cf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8e4ad9182a60653b2a17357cc995ef14ebf4dddf9162695c8bd25a2e6523752d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244620557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4ac785f3d5ff7a11fc4631dd8424de6b13d3e3f45809994869f76ccc37afa4`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:52:17 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 29 Jun 2024 00:52:17 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_VERSION=24-ea+4
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='64aa493b28493a2d223626bdad774640cb148b0d52f392b081b2776532a980a0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d0b65f191528ab241b4e238568e52fa7199975b4f4b7badcf58a279b1fac426'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e26aeb8fb64e6e8a34aa523f6e2af3894a6b5cc356fd935b1a59e91df591fcf`  
		Last Modified: Tue, 02 Jul 2024 03:21:05 GMT  
		Size: 4.0 MB (4016757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023f3b8ff8b56effe4f5de8cc1264321f30172c221098defd326195d37b7b90c`  
		Last Modified: Tue, 02 Jul 2024 03:21:08 GMT  
		Size: 211.5 MB (211477522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:118471702214ae6180dbbcbbee1f75c472bf1a27d3910bc87d446b4b8bc3d677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30462148ad35e4a329b2867b57f2947caa277bd665e09a4d3cabf81f077e976b`

```dockerfile
```

-	Layers:
	-	`sha256:d9b9359d318144d87b33266b9796a1b5cc59cebfcf3f7381ee8783d5e8837fd7`  
		Last Modified: Tue, 02 Jul 2024 03:21:05 GMT  
		Size: 2.3 MB (2346333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b892cf268bfba368c4192604916dc931763ecfa1113611f4eed78fb4833969`  
		Last Modified: Tue, 02 Jul 2024 03:21:04 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:36f9d097f55ee7fdf083b8ea77546a7cbac9fd97383afee3fd06ef3cf75107e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242192160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0957633d665daa57ec4dee8e68a0e8bd2e8b20b4bce2684337afa0c10782f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 21 Jun 2024 18:52:10 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:52:10 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_VERSION=24-ea+3
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='dad750c864049dba95a01fa89ad1c52c3b702ba87c3c865e5e64fa624f9e3de0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='4a5515c226db56008676461bef7443163ccfe369415342136b8d9691ecd5130b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb960144e9a3234b18ad0a695286d60905b47d016807f2c30ce00e0acd5b3ab5`  
		Last Modified: Thu, 13 Jun 2024 19:56:32 GMT  
		Size: 3.6 MB (3629819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcfaceb429c0c97e5d759a7a0c59891f1f0f37911fecea9fd81f29eaa1c4420`  
		Last Modified: Sat, 22 Jun 2024 06:18:38 GMT  
		Size: 209.4 MB (209382675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:39ccedc48d9efc04908ad9130a0f3c42ee2314c3650f701f190d4bc44fe7a806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0011daf88210bcb08c358b9af2351ef2ec72e73879d65cc78663927044462f60`

```dockerfile
```

-	Layers:
	-	`sha256:960b2c4a3dc53bb942621b16e72dbe009b1ac39926e8c894874aaf5f2267c6d9`  
		Last Modified: Sat, 22 Jun 2024 06:18:34 GMT  
		Size: 2.3 MB (2346659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c353519b0bc1643346510852f8f09f1ae160b9f4387780a7830ab2dd2fb00ff`  
		Last Modified: Sat, 22 Jun 2024 06:18:33 GMT  
		Size: 19.6 KB (19617 bytes)  
		MIME: application/vnd.in-toto+json
