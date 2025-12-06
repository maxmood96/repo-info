## `openjdk:26-ea-27-jdk-trixie`

```console
$ docker pull openjdk@sha256:ff16c84ec00fcf9d6abf940a01520f301bf4fc2ccf9258867bc23f9ce606293e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-27-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:197cf8e0b4217dafe31f63795d658c87358c42454fedf342a41f6e8ea6215c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386684553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b99d884693f5bf4de4eec78f4fa7f6c2450e51823b1d6b39ff4afb8abe9b15`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 06 Dec 2025 00:34:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:34:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Dec 2025 00:34:39 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:34:39 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:34:39 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:34:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:34:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b7c8d62ec7ae85bf91ccf7d7fe9286baf469428005b936821b15210777eaba`  
		Last Modified: Sat, 06 Dec 2025 00:35:16 GMT  
		Size: 16.1 MB (16061675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225b6b2a4fab12d8eefc64b28dee37de25b72fe7899a87d8f052c14a8d0db3ee`  
		Last Modified: Sat, 06 Dec 2025 00:35:22 GMT  
		Size: 227.9 MB (227940419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-27-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0f0b58c406950a6b4f0e71e018de80ac42e100fd858d876617624d1eb2210502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9f091e568b74c3d1e784bbaf34ac4bfa6a80445748127728e1723970eea727`

```dockerfile
```

-	Layers:
	-	`sha256:dec68fdddeee68a6cd84e46a0d79e181d26ccc97d6663112a9e036a622520c3d`  
		Last Modified: Sat, 06 Dec 2025 01:24:31 GMT  
		Size: 8.5 MB (8509943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52213551b56413e3776142ffb81cde8ed5fae04247f24ddd60ee8b7bc6ed0a50`  
		Last Modified: Sat, 06 Dec 2025 01:24:31 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-27-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:89282bccfa4b48c775d1163d89b0d87897f67c78bba72b60e839e6654444ee10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384183716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd77686bdef6a6a5def38110defcb82a64f6cbcaeb71ba436fbf9ea0c76f2d5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 06 Dec 2025 00:34:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Dec 2025 00:35:07 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:07 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:07 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:35:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e5a045efdd16964b811f88ea169e4d3647bcd0f16d91d31504f6ae39917162`  
		Last Modified: Sat, 06 Dec 2025 00:35:48 GMT  
		Size: 16.1 MB (16070871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec9c35c3bce63c322fc5e29ae53dd4e526df502e4ffeffa0607b3af06a7f2f6`  
		Last Modified: Sat, 06 Dec 2025 00:38:02 GMT  
		Size: 225.9 MB (225856840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-27-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:6a7d238cc1ac23a7d52634029318ae9a0636b5c8a0a0f9fa85064f0f341a3b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2b60d714e04811115dafacd5b702c50b2fa5be3f8bb82aba848ef62d9e83a5`

```dockerfile
```

-	Layers:
	-	`sha256:92bcf5d3c8064df10845d74b1fe4517393c1b68692161885cbe81e9976555dd1`  
		Last Modified: Sat, 06 Dec 2025 01:24:38 GMT  
		Size: 8.7 MB (8704733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01de88c8a8dd686b4096f6996dce1b72af584af1e3e58a23561eaf841e711ac`  
		Last Modified: Sat, 06 Dec 2025 01:24:58 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
