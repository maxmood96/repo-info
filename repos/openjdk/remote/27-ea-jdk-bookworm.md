## `openjdk:27-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:99d098a3b54e3a3f516cbd839d790a97d6fd7d27ef70d34cd5bbec0e32b560de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:246da42781dbe1275687edce9b0f7d5d0e39ba6873098faf0b722296a1a018e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382620100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329c5f440a1863347c73a06cf484bac1142a67f73254c78c07cc14b56c957020`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 06:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 06:19:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 22 Apr 2026 06:19:32 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 06:19:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 06:19:32 GMT
ENV JAVA_VERSION=27-ea+18
# Wed, 22 Apr 2026 06:19:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 22 Apr 2026 06:19:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcda2b4d7993820b00c5488d173051e76d01ba6b85620617ba77001b0f9e2fa`  
		Last Modified: Wed, 22 Apr 2026 05:12:28 GMT  
		Size: 64.4 MB (64396988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5029ea5a984ca382b7a4e1d4b647358e8c92c647997d843f5291ebba6b2c070f`  
		Last Modified: Wed, 22 Apr 2026 06:19:53 GMT  
		Size: 16.9 MB (16945851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d11f374390a323b60e1ada8a655ccfe6db949debdae98e92f08201177ab8212`  
		Last Modified: Wed, 22 Apr 2026 06:19:59 GMT  
		Size: 228.7 MB (228746399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c8d62d560a90dcdb1bcc76237bb8a42a2a16c4c6da09a8634920fad2cdd570aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8685556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7a49398409323d13667ccab1aa6bf35a6d89487f96e9f898680d899aae3792`

```dockerfile
```

-	Layers:
	-	`sha256:37525ac73c814fefe0e43e7d37edbe0500c213a53a3a4c6ea80cacba6310eec3`  
		Last Modified: Wed, 22 Apr 2026 06:19:53 GMT  
		Size: 8.7 MB (8667617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3677af998d57a0fc3541937b9f0ce79aae7b16ae498a60fc46285a16892ace6`  
		Last Modified: Wed, 22 Apr 2026 06:19:52 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7fb73202b9e30a93a6c6812d3b30f7955202a8702e3b2ee477206626968db1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.9 MB (380885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c83bcb28b52b9f5d3d932b5fdb7a7c208862b450398a5c0a91db3fac25c96b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:18:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:18:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 22 Apr 2026 03:18:43 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:18:43 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 03:18:43 GMT
ENV JAVA_VERSION=27-ea+18
# Wed, 22 Apr 2026 03:18:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 22 Apr 2026 03:18:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6c1b8b184364a826f2161a30292bce63f190c904d52be4102575e6226d12e2`  
		Last Modified: Wed, 22 Apr 2026 03:19:09 GMT  
		Size: 17.7 MB (17728884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48178854da49ba3b04c972eb9a779b3f01f7777fcf3a22c77097c13374d64a`  
		Last Modified: Wed, 22 Apr 2026 03:19:13 GMT  
		Size: 226.7 MB (226694754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c5ea3900d591b3861744a441d152abde2c2be7864a7b354de32761bd72b482ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1765021e90e0dcc1c839b0bfbf7ace92d12611aa97656bd08bb1509eb275c720`

```dockerfile
```

-	Layers:
	-	`sha256:e54443b38dddd5daeb2fe634f2d15c1b2f2e377044898355e9d6a31c7b08e374`  
		Last Modified: Wed, 22 Apr 2026 03:19:08 GMT  
		Size: 8.8 MB (8804462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27762e412b167a8a4c56edce76cb5ffd71df1a8c6b787d29fea5eb3c2ffc3322`  
		Last Modified: Wed, 22 Apr 2026 03:19:08 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
