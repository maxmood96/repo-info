## `openjdk:28-ea-1-jdk-bookworm`

```console
$ docker pull openjdk@sha256:ba467f122ff4feb4990d4cbc8992ab2657f8e2cd88c6ae30e357621a30abaa84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-1-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:ebe4d4c8ea2320051e00a54e74d4441dc45dd03a099920a45c506ecddc553e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (381030838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb76cce86fa0c5b2d6bb2afb796474de7c95677a2f6251b5cb599d6016f7af7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:16:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:16:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 10 Jun 2026 20:16:56 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:56 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:56 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ceb74de907c9d70ebccc284b5d0b815f189a0e5b7f48fda85d81d554dd45df`  
		Last Modified: Wed, 10 Jun 2026 20:17:19 GMT  
		Size: 16.9 MB (16946717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04344f2351a86b9d2dda190445d0ccd5764f65dc3fa0437e3be8cc1db79d936`  
		Last Modified: Wed, 10 Jun 2026 20:17:24 GMT  
		Size: 227.1 MB (227140864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4c03796c7528f387c0c482fcd5fcfbae59543b5edcc45a9de8b65c4f2fe8d357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8684266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ef673f1460d6cac855910edb14177b9bcf7c0bd9474fa0711220010cb10141`

```dockerfile
```

-	Layers:
	-	`sha256:cf4c935ba4237f43e9503d3a2369edd5cb4219c67d87bcc3c11e75e5a14fa50c`  
		Last Modified: Wed, 10 Jun 2026 20:17:19 GMT  
		Size: 8.7 MB (8666344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e6737d8315d2962bd0a9378baff837c196aab9bd51f2bdf32cfb983d0b617b`  
		Last Modified: Wed, 10 Jun 2026 20:17:18 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-1-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:13f08d3e386ddb9e0268bba1f6f41e8241b2f10bda3c7ddccc70c20123f4dc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379331416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb98d4deac9526aed2ca7ee985af85d92cf54bb98885abe6204e9365632175b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:18:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:18:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Thu, 11 Jun 2026 03:18:58 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:18:58 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:18:58 GMT
ENV JAVA_VERSION=28-ea+1
# Thu, 11 Jun 2026 03:18:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 03:18:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba7f71e6b05c3d50d8265b1b8430c05f4e125d59bd4ad677e27eb47f8c9306e`  
		Last Modified: Thu, 11 Jun 2026 03:19:23 GMT  
		Size: 17.7 MB (17730230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b591b16ea9a0ea50e560c1effd01d86b05a9941fd995b6c1e088564518ed9f20`  
		Last Modified: Thu, 11 Jun 2026 03:19:28 GMT  
		Size: 225.1 MB (225110996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b700819e7afa8b6f5ee1b41caf9229fc10e2d68b43e057b3c43d5f77ae57f323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8821248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1403d50316d9918fe0f46c6f44165cffdb11df45b34e55a37072fe7f5c51f5c`

```dockerfile
```

-	Layers:
	-	`sha256:ebb59b9c8bd9837495431ef7c3cab7ee3d7f3f8d364fd057bb6a1985561fd865`  
		Last Modified: Thu, 11 Jun 2026 03:19:23 GMT  
		Size: 8.8 MB (8803207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d605f0dbe2a41ab57bafdada9cc05f8d9f72e0a8aa160073ff84603296dd8da`  
		Last Modified: Thu, 11 Jun 2026 03:19:23 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
