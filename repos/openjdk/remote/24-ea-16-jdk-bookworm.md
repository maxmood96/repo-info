## `openjdk:24-ea-16-jdk-bookworm`

```console
$ docker pull openjdk@sha256:1019ec775a352807469d8bea649d144a92c2798a2fab30404d29ef810e433ffd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-16-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:27ec7eae350345e18a11bf044c43e41b50e30ff2695d13eee3902dd324b55530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366715581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c79314787bdbc20b3c5e96cf325ce5ad43a0c98fb1a9897a9abb175ad0d1a5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:55:22 GMT
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1663cc1d7adf6f469414161970adc436efa5a907da7e2f623d5e8a201a65d1`  
		Last Modified: Fri, 20 Sep 2024 17:57:43 GMT  
		Size: 16.9 MB (16943142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2154a32b3c873fb27e132ffd7c6b399f002ee287377e087e5a6a4b6558596`  
		Last Modified: Fri, 20 Sep 2024 17:57:46 GMT  
		Size: 212.0 MB (212014566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-16-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b3b1928725e795a326c2551f6903b0c62263c3f305a559606b2dd7766c9cd3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f04dc98b63b34ad6002cdcb750e69bb30eb4353852e0c1cd9f08a388badecb0`

```dockerfile
```

-	Layers:
	-	`sha256:7b5cf9ff30189bd69fbc70566c6b029db556af948964e5b8bcf446ce5125a643`  
		Last Modified: Fri, 20 Sep 2024 17:57:43 GMT  
		Size: 3.0 KB (2963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c356e75397025ddf10caa8f4eacc96c1996b48f2d40fcc81c66cd759d90775c1`  
		Last Modified: Fri, 20 Sep 2024 17:57:43 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-16-jdk-bookworm` - linux; arm64 variant v8

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

### `openjdk:24-ea-16-jdk-bookworm` - unknown; unknown

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
