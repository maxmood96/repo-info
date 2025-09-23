## `openjdk:26-trixie`

```console
$ docker pull openjdk@sha256:5d55d5dbc0cfcc5023b60c702c0777547ea2f3f1452bd020ea0eaaa080478dce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:ca1d0b072a5aff7e8cebdde1a9f9c832c32dfe3192a60944f8034a2261975992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382202141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e886397455075f8447ad268778d43c8101048d19c75ef581d78a5696c284ea2e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 20 Sep 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Sep 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+16
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='87ee3d9cfd07f66858b6e519b07d2f23375fb1c1827faeebce6580c31045879f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='116ea44265700afbfe2c15b751ef9e34921fa449663ac0dfb439adef9db9c379'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a98f7495bee3e8e6943da9f52f0ab1043c43eb1d107a3817fc2a4b916be97`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 67.8 MB (67776756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc41d7c96806442d7ddc8e81659e0f56ade88f7ed6e28ea3f07c8fd6c61dc135`  
		Last Modified: Mon, 22 Sep 2025 23:43:07 GMT  
		Size: 16.1 MB (16061431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dda876411523c3812f7d244ee2ce50f136291f4d8dbd6fabe41a9aa0116932`  
		Last Modified: Tue, 23 Sep 2025 00:35:09 GMT  
		Size: 223.5 MB (223470788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:bc45924b3c278d5f8e8581203d251cdd70a2d14a3b86e80c9a5fe4cda179bf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8531556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddb17163f973ce9fe625f048776fe077f6baf6b885e073931f30ac81e4011f7`

```dockerfile
```

-	Layers:
	-	`sha256:42e621628c0bb8e7275a285e6efbd96f1f24488659fb324c1a56c2151fb836b0`  
		Last Modified: Tue, 23 Sep 2025 00:24:27 GMT  
		Size: 8.5 MB (8512972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f3ead27370e366ef9f6b12f45b3713c70925fc6831d8b56dec2d943ddfd4f2c`  
		Last Modified: Tue, 23 Sep 2025 00:24:27 GMT  
		Size: 18.6 KB (18584 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2a55397526e60dbd4bbad7397a5428b5596b222df5730a44ce2ff69e0c6604a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 MB (379641323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbacd0cb09905ba6431ffa423857b22373e651030a0f601dc2f76815e37eb0d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 20 Sep 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Sep 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+16
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='87ee3d9cfd07f66858b6e519b07d2f23375fb1c1827faeebce6580c31045879f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='116ea44265700afbfe2c15b751ef9e34921fa449663ac0dfb439adef9db9c379'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd36c08acb8bfd3ecaef97bc215303e9b1c59f47cb418c4692d97f29cb1b17c`  
		Last Modified: Mon, 08 Sep 2025 22:26:04 GMT  
		Size: 25.0 MB (25015321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fd600967e6c49c98883d12d3ca7ba50395f75eb436373e95780141122745a6`  
		Last Modified: Tue, 09 Sep 2025 02:13:16 GMT  
		Size: 67.6 MB (67583121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5690f33c0dd077f2ed099720005b21f3c6dadd584d94f0198a998da37b82d9e9`  
		Last Modified: Mon, 22 Sep 2025 22:11:24 GMT  
		Size: 16.1 MB (16070521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3239586df44c8e86e746e84dc4ccd25faef44e4125879aa140a84b294130a89`  
		Last Modified: Mon, 22 Sep 2025 22:13:45 GMT  
		Size: 221.3 MB (221328614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:5d376d4130751b4b8d5956f43663dd338451b513f5340d6cb696cf805d56635d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8726513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8742578468781147cb7273ba9d75640f6bbfc9feeaa1c1814411949a635c051c`

```dockerfile
```

-	Layers:
	-	`sha256:e51beb617bce29548df08c69470ba6f69781d676471c62885c15e03268a74c00`  
		Last Modified: Tue, 23 Sep 2025 00:24:34 GMT  
		Size: 8.7 MB (8707786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5173463086f4eb6c7f5e79dbe439908157c58eb40d215eb4482dcb241e9f937b`  
		Last Modified: Tue, 23 Sep 2025 00:24:35 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json
