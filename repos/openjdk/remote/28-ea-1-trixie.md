## `openjdk:28-ea-1-trixie`

```console
$ docker pull openjdk@sha256:6fe5b2a24c1e04589914ecb0e732e9d84fe52fc27a043cd5d132dac558235a5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-1-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:488c0a89435e6187fd3a8b9a17b788a3f540854b6e13cd5b2ea7f2dcf2420254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385933053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985380e244a18f86decbb479f8fc477ab9c17be27343a167bdcb82b39ff52932`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 10 Jun 2026 20:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:16:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 10 Jun 2026 20:16:38 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:38 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:38 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9dfe264b62e3d63906376b1d59a0352115c11480a4bfe43b7a80c3da6cc262`  
		Last Modified: Wed, 10 Jun 2026 20:17:02 GMT  
		Size: 16.1 MB (16065769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bc370603586f69a2e9adba7ad768d36bf44555072b45d40290e3f83748ee2d`  
		Last Modified: Wed, 10 Jun 2026 20:17:07 GMT  
		Size: 227.1 MB (227145014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:36d054b409ca76c75c3d994267f24ec9f3e70eba3e13648751a8930fea259435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5aa1cb7180999df145ab72c41b48f9130e54a9b83398b6f316f8a99b9276a64`

```dockerfile
```

-	Layers:
	-	`sha256:ed6daa62b511b72af9f63cdbc29f4d335c7e051c15d09eaeeabb455f4530f39f`  
		Last Modified: Wed, 10 Jun 2026 20:17:01 GMT  
		Size: 8.5 MB (8508775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:673e6ee815034c0aee7f1fb8e8a6828fc9c1f02f2cdeee13d9dbe96a8f81b3aa`  
		Last Modified: Wed, 10 Jun 2026 20:17:01 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-1-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9ea83d66d2ab000e423178f6faee5797781ce7c7d0c9f88c8d6e9b2d034ade2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.5 MB (383490470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c74d195a71bb1c3ed92cbeb70f2b4db612e55892b6894803c587555b8e5979`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:18:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:18:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Thu, 11 Jun 2026 03:18:50 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:18:50 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:18:50 GMT
ENV JAVA_VERSION=28-ea+1
# Thu, 11 Jun 2026 03:18:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 03:18:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2e427d8856f71d8d3667d1c4d9274b8aca2bd9d228387c51c211909e51263f`  
		Last Modified: Thu, 11 Jun 2026 02:22:21 GMT  
		Size: 67.6 MB (67599934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0104a7a6f0bb87d6ef1d5b06fb7d319e3e8d88f2ff6717577f0124ff73ed20`  
		Last Modified: Thu, 11 Jun 2026 03:19:15 GMT  
		Size: 16.1 MB (16071341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caa7f31af8b492b20680a306e4044820d5c72a45d89b3d720f9017790721793`  
		Last Modified: Thu, 11 Jun 2026 03:19:20 GMT  
		Size: 225.1 MB (225114115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:6b541f7187573bac110b4724354d11e4480b9f7b6a30fc2ab7e31d6d4c915d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb2d0736b2791cc9ffd09df4f08d8b44e02d4c8e1ab7d0905dc2406922f1781`

```dockerfile
```

-	Layers:
	-	`sha256:716f71849d2219b6ab786c393e931b50db0c5aa698b97885aa660194c9785785`  
		Last Modified: Thu, 11 Jun 2026 03:19:15 GMT  
		Size: 8.7 MB (8703036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeef5041fcc6b23ade92439144f6c465e5530dec2a308707ca2cd76966720278`  
		Last Modified: Thu, 11 Jun 2026 03:19:15 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
