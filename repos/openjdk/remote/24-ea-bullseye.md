## `openjdk:24-ea-bullseye`

```console
$ docker pull openjdk@sha256:d64ac918c42c606809429127ee97c9dbfd6866aeccb0d6a0c73fe4fd7294b0e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:bd35a6027179a6bb3b63bf024fb932328bf7a9ac4aa7e581f7de04034453fc60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350985711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3741c35741b03d801fa37a48fa0711fe90824ad802a19968b7b869280ef00183`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee26b7a209f9a26720207792b237af3e19c0efeed8695e1e630fcd0feef9230`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 54.8 MB (54753708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c9d348fd8b7b86f2c6e58d8e3b786c83d4d740aa6b2be8f92a75adac1a0db9`  
		Last Modified: Sat, 11 Jan 2025 02:29:52 GMT  
		Size: 14.1 MB (14071391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d340dc6fd651d5a508e59e1a942b94e41228f174e10231653c3d839e503fa8`  
		Last Modified: Sat, 11 Jan 2025 02:29:54 GMT  
		Size: 212.9 MB (212863362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:d5a3878be9815a06d03cd9c48e547c2bcd4a7a8159d897faa05aad7f5fdc92bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8383402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a546ea11d3ab954507e900332f6a69c7b41af5feb6231ef7796c8661ee3ca7`

```dockerfile
```

-	Layers:
	-	`sha256:729cb42570c6babdb843e45471cf393ead8fa95e3b794528def2179fed8c02e3`  
		Last Modified: Sat, 11 Jan 2025 02:29:52 GMT  
		Size: 8.4 MB (8364785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e9b5fed248fd5cf5b2ae83db7484193b9468bba01187a80620efc5fb5e8c61f`  
		Last Modified: Sat, 11 Jan 2025 02:29:52 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:990c60abb859c1ee330679e6ed17591d06353f6d5e733d9680ef8506b03b5a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348988609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d908a470acff23ea7cd1e110efdcfcc208d7dc9dd88fecf1171703701dbabb8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76479c78354ea5a5c0b1b7532f5adca25103a796405e3d01dfeeb0e9af4b21e`  
		Last Modified: Sat, 11 Jan 2025 03:18:56 GMT  
		Size: 15.5 MB (15526432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9d4c2be87b3722b0ff5924111697cebfb1ae425dd30d351061e9d4da8b30a4`  
		Last Modified: Sat, 11 Jan 2025 03:24:22 GMT  
		Size: 210.8 MB (210820030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:4341784f1a31dd446acd9e1c314554b7944818031cc7341846533b98d7682c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8484508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d69481d5a06dd99c464af7ccf9bda1eb8f2aabea5c09077ea0860a4c21b26e`

```dockerfile
```

-	Layers:
	-	`sha256:9cc566a4eb4f6269ed388e23fba499e1a37fb7ab134a5666a59d1099ce677a66`  
		Last Modified: Sat, 11 Jan 2025 03:24:18 GMT  
		Size: 8.5 MB (8465747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82a249b7f5d3a622f7e0b38debb8f982c992cc306a636bd9404e33e7bd619240`  
		Last Modified: Sat, 11 Jan 2025 03:24:17 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
