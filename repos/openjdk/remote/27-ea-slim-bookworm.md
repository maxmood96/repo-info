## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:21ba9517ed360594c1aa0172d19563a74a270a72efd15a7bf40ac758c4429865
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:b9ea30d8c4e392ca516a7bba06d10113d60150f1ea2e71c2652187fb6043a83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259387373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ceb247646ad4451a3e882d9070b7977166ded0f181a8951a68c376dab2c426`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:46:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:46:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 24 Jun 2026 01:46:39 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:46:39 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:46:39 GMT
ENV JAVA_VERSION=27-ea+27
# Wed, 24 Jun 2026 01:46:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Jun 2026 01:46:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68be67116a3b05f9f874c6f009c6b28fd75ab5e390d47a888c8113c51dee173a`  
		Last Modified: Wed, 24 Jun 2026 01:46:59 GMT  
		Size: 4.0 MB (4032937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ced4af3e32ceef0191f4349b1b95123bb83d55146dd5151126f26f66b5a6a04`  
		Last Modified: Wed, 24 Jun 2026 01:47:05 GMT  
		Size: 227.1 MB (227116797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:623a0fe3018c6fd836bd5eb84b989c400888d18d38f77dddf33b1de697e637c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f61cdcea60cdc51eaddb4a435fc88be4d9605b8d40c6d89422c3244fcfd9d9c`

```dockerfile
```

-	Layers:
	-	`sha256:128bb10f363801f5cac873113fb101ccb089f7c3b4193e9e8236e6b6f1d3b256`  
		Last Modified: Wed, 24 Jun 2026 01:46:59 GMT  
		Size: 2.6 MB (2647290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89c1f25a7590dc39e08199e7e48cf581e37136fd8b0828ee208186be0f34e06`  
		Last Modified: Wed, 24 Jun 2026 01:46:59 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:04b761feb70051c480dcdef5710efe5a8f1d08a0d807976f5404948dcfe5d915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257074241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf59b5585c6ea91bc4a73f89ca1907c486ce8dd8621ac5675115cc1f7eb23f4c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:49:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:50:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 24 Jun 2026 01:50:08 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:50:08 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:50:08 GMT
ENV JAVA_VERSION=27-ea+27
# Wed, 24 Jun 2026 01:50:08 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Jun 2026 01:50:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889c781161a8a7977563bd2ae17c2f225e39f2fb177afdaa2f240deca6ad35b7`  
		Last Modified: Wed, 24 Jun 2026 01:50:28 GMT  
		Size: 3.9 MB (3852863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c36c6ce1a216985ca21c70618225c335319bd4f72f1b49f63f1101174d156c`  
		Last Modified: Wed, 24 Jun 2026 01:50:33 GMT  
		Size: 225.1 MB (225098960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:184fd7786777ed9028a198af48f8dfce2d28d584d86ec97fcefbdb347b858d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f021dc19eeca15b2f141cfb451795ec6f4006ca68f25f1fdecd0484564b4461`

```dockerfile
```

-	Layers:
	-	`sha256:50e3d7c15459132db0e3777b3cda1104e4f3f85673617b6dd2707de380cbd660`  
		Last Modified: Wed, 24 Jun 2026 01:50:28 GMT  
		Size: 2.6 MB (2646924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee1022aff4064a3783dd237f52d03f6ac931590ea8a93f335696f16f09d660e`  
		Last Modified: Wed, 24 Jun 2026 01:50:28 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
