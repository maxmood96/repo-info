## `openjdk:24-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:a50d1872fdda93dbb80bb4d682ac8c47c063afc27f7d9bc32d3be17e2453f16d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:01f4c195957e80e45a365850a62b6a3fbf49a0ea90f1fe777764adbfe93a70a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367197120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d356dda04f587244ba57be3c67d86f9e04bea5144082892610bebde70b01d8eb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 27 Sep 2024 06:48:27 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 06:48:27 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_VERSION=24-ea+17
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='983faf25eff38b5b396afabd191a91b239a1d803a0dadd01863861ecf731f034'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9eb980b4f1fde9c2387e0fab6b91b6f68cb109e3ddd43eda0013d9ee345f2dc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f0752e2f6d985e3b2e91465fc1226a60c1e5931ea75481d4a967f1d012d283`  
		Last Modified: Sat, 28 Sep 2024 01:01:23 GMT  
		Size: 16.9 MB (16943004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e90a01fb0eb8567f5a02f83f45a2d8786520df956828199a1db867f0107e98`  
		Last Modified: Sat, 28 Sep 2024 01:01:27 GMT  
		Size: 212.3 MB (212253693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:64b267f54d820769c2b0326e546df5020f7acaa94e637cbf9c654fd28245e524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8421979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ba2bac77b39e71e3ceee2d20569b1efcd74e6fcb8f5f23add5703290fcc30d`

```dockerfile
```

-	Layers:
	-	`sha256:6b555cdf982d3417d0fa6e54173ae7918f0b2376444f3bf0749ddb0086595885`  
		Last Modified: Sat, 28 Sep 2024 01:01:22 GMT  
		Size: 8.4 MB (8403516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c50b2fd67278f9569df464748ab0057d20de2f3ff7a5dfde1b9e78c59583e0e`  
		Last Modified: Sat, 28 Sep 2024 01:01:22 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:12b5cfbf14230bf23f571fe0334d8109cef181b43501d674cc0510f8135e0366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364741409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9085e8b67fab56cac619aab67e018b51db917adc605b031078c6c646260de7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 20 Sep 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+16
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='46c9e29e1e700ac596a07ef1795142939bcfd687dcc7f959043886bf800a3bee'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='f42ff15af07babf02cf4dc52c121b18be22bc6f54d6b041b424687f82cdd9919'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b6f012ccff6ca072ee648eeb669eb5d011cf0f400da82a947223b15780d28e`  
		Last Modified: Mon, 16 Sep 2024 19:22:31 GMT  
		Size: 17.7 MB (17727278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31dbeb8bc791108d6395a74548e6b62e04634f49bfe692fbc96964eb35d202a9`  
		Last Modified: Fri, 20 Sep 2024 18:02:35 GMT  
		Size: 209.8 MB (209836762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2f02e889a1e3a2ef4e530ca2d22a5572c37551ce81f35cdf858a4fb764998a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8413843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fc2d5c9b492469d2bb5c5a8996fd872a52fa4f16759123509dbcd26882ebf3`

```dockerfile
```

-	Layers:
	-	`sha256:9b2b81c0072c4f72b3352139fadf3b3e16b0b6e661e4aa1378afd762edea6c0c`  
		Last Modified: Fri, 20 Sep 2024 18:02:31 GMT  
		Size: 8.4 MB (8395040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cb4aa44e4c7afbd35ba1c328cef714e47ea03f3b56678843cecfcab90fba12`  
		Last Modified: Fri, 20 Sep 2024 18:02:30 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
