## `openjdk:24-rc-bullseye`

```console
$ docker pull openjdk@sha256:2d59b615060b32af94c1c344e444473f5577abf740c5f351331d18828ecd69ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-rc-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:7b2878d58984f34ee8d6c0279988132eb65026281990de675b90c97335ee0f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351072144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4c3ef3974851e92c112541559f1ce65b60a607f763964ac793c557454f38b9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceef6690d6235041c21b9e72ef65b7064141df814b45ddd70515b4b678e87ed3`  
		Last Modified: Tue, 25 Feb 2025 04:17:43 GMT  
		Size: 14.1 MB (14071408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d56f8f75e98ffc1f74556b6a53212040b15ea2dbe1e9ff42f9f056db3e14d9e`  
		Last Modified: Tue, 25 Feb 2025 04:17:46 GMT  
		Size: 212.9 MB (212948826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:0658ec8de86b642515ee17542a9742f72d6a0ee7f2b145c4514ef2dd0b2091fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8385929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fe29d8f9eef28e398f5aabb3b63e00d9375e85ae1dd42cda933dc327e1d215`

```dockerfile
```

-	Layers:
	-	`sha256:a2c39fbc2c3e7f3fccc1b45ffb2c50c26308c13c7765e2c27c5be41c4105a6a9`  
		Last Modified: Tue, 25 Feb 2025 04:17:43 GMT  
		Size: 8.4 MB (8367899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ad0836b336ab0fca0ac5db5223f271aa99de3591bab0a3ba25ff3e3944c2ee`  
		Last Modified: Tue, 25 Feb 2025 04:17:43 GMT  
		Size: 18.0 KB (18030 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f1b8723a9c3b561a5239045f16683d2e171dc3f0ebefe0399c70ba53f8e53a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349072685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9295e557eb9c421069cc82894097972f4dfeb743a6e6a937b2915f900bc9b0f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c572ebb94bd0fa84090727060c50b8ce9e915a3c790cdbb3e5f4b0f67359fabc`  
		Last Modified: Tue, 25 Feb 2025 16:00:32 GMT  
		Size: 15.5 MB (15526396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17c2e3d89d535d44ea6af331265352ef9706f95e8af26ebdae7d83802b7b6aa`  
		Last Modified: Tue, 25 Feb 2025 16:02:35 GMT  
		Size: 210.9 MB (210898078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6fc05fef1aa44ba56bf0e2faffa1b92a23ec40b02b402f701bf52253a02b9950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8486986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792b8708f67e0699672e4f57e8329593ea00da106d1d02c10bd8dcb1414832db`

```dockerfile
```

-	Layers:
	-	`sha256:503a59231fc814671b3c280b13c08e5230faee07b92e5a1eaaf4efc09c47af04`  
		Last Modified: Tue, 25 Feb 2025 16:02:28 GMT  
		Size: 8.5 MB (8468837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66e849b607204080031d405c69c97f50669bcd10ea6f375233916c5928b2a63`  
		Last Modified: Tue, 25 Feb 2025 16:02:27 GMT  
		Size: 18.1 KB (18149 bytes)  
		MIME: application/vnd.in-toto+json
