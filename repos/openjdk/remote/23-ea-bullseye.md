## `openjdk:23-ea-bullseye`

```console
$ docker pull openjdk@sha256:51e274b50cfad556dae3ef43ca60b66350834ffadebba19a60ad024ef2deba7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:ceb8a9a4df0ed82eb729b1eb1ddd750c78ddfeff6d26e790c7377a3e26e01b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349503758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e95bc76b0708a618bc186cefbfff01877a756fceab5bbf03ea6f437a4c3357c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbeb8ef1d906919c518d52a9eb71cedf1ee5c3247b6ea106571a6252d5a4f05`  
		Last Modified: Wed, 24 Apr 2024 04:22:13 GMT  
		Size: 54.6 MB (54589380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b01d217406aa03f6648130240d372b0b57301d5632e80a7b8e80409f9b21ad`  
		Last Modified: Mon, 06 May 2024 23:05:43 GMT  
		Size: 14.1 MB (14072915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46c0f3940e3b0ba35a52ce5ed9c2911941bbeacb70409c5b11f57a7fe5de484`  
		Last Modified: Mon, 06 May 2024 23:05:46 GMT  
		Size: 210.0 MB (209977314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:4a31d9f7ccb34807908fda4ce2aa7c6fc861e482b05b365a3c52ef501275564f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f75ba6c325671a105cd21ac9b9ed8a68d6e9b48fa9039f811c4b9a3c75cc9a`

```dockerfile
```

-	Layers:
	-	`sha256:dd81821df7770fc851b181bd55768b484dc9f6e662180a3ab5abd7b970d63d2a`  
		Last Modified: Mon, 06 May 2024 23:05:43 GMT  
		Size: 8.2 MB (8157316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce1a8ea99a13f495fbcb6d3e20631fbb0d8003b43b383964db0523527c72aa5`  
		Last Modified: Mon, 06 May 2024 23:05:42 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a3257a9bdaff32378020940d3f0a8dd5dfc3d5718e8e4a83f5e065f05bca0242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.6 MB (347573198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299efccc1f6b5b63a15bcf418dabbbeb250f35a9d411a5e9eb1621da16cee101`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36972983386f768dbeff5de37af34ed4e2f59541b2e3c43575f29758c3591923`  
		Last Modified: Wed, 24 Apr 2024 08:42:45 GMT  
		Size: 54.7 MB (54696233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0446d6e932dad24b117d4f43160b02390e795232709aebc002c1d7a3f1630918`  
		Last Modified: Mon, 06 May 2024 23:51:34 GMT  
		Size: 15.5 MB (15527262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6879bf272b907fa58e86575d20b4a77021e03d5248b2f770affa52a6f6793aa`  
		Last Modified: Mon, 06 May 2024 23:51:38 GMT  
		Size: 207.9 MB (207859121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f50e4baf09ac568a59d1d87770f6cf311a490eec921b98167c0a4b03ac27cdba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7369aad5319a0246c03af8be5e9bfe7a4f990b172c7a7485599296c6e57490f`

```dockerfile
```

-	Layers:
	-	`sha256:cc9d60e5908891df0a6f126946575e02007ba24ced12458bd0c3a79cc0ec1c19`  
		Last Modified: Mon, 06 May 2024 23:51:34 GMT  
		Size: 8.3 MB (8258961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a606840ed194a64a000ee962fd3b09c98c09e1b4cf1a1ff24d5ad4afdecca3b`  
		Last Modified: Mon, 06 May 2024 23:51:33 GMT  
		Size: 18.9 KB (18925 bytes)  
		MIME: application/vnd.in-toto+json
