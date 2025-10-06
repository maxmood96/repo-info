## `openjdk:26-ea-18-trixie`

```console
$ docker pull openjdk@sha256:a0ad45af5e5d547ad13d04f152b3007345c8a1559179aa4d6cbe9664444a2d59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-18-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:ad36ff98ea76730e72a07765c067749869ba10252c0a3c8adf78058aecdad2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384525623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1deac5747722235122f53412ff8acd561893c1ba085e4f488e7e46f56d173d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c79e92bf13b17085d9c245a2755ca9e3935d5c702b18b0cf035d06477fbf57f`  
		Last Modified: Mon, 06 Oct 2025 21:05:12 GMT  
		Size: 16.1 MB (16061337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7337f2ff7ffcc458fd8996592cadcc6476ad907e16a5731bec67cfe6e741fd94`  
		Last Modified: Mon, 06 Oct 2025 21:09:59 GMT  
		Size: 225.8 MB (225779901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-18-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:3501c7a54630b5203aec141d068116adbbec1e24cf758fe881196f4a10dbeafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8531556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6338e8c00e900d0d80925b3794e99c22ad8685b644fa12073f1f50a4756af997`

```dockerfile
```

-	Layers:
	-	`sha256:835b2b0f0221668f7719dd9190f6b053eb5035ca21ef211dee3afcd629e3551b`  
		Last Modified: Mon, 06 Oct 2025 21:24:16 GMT  
		Size: 8.5 MB (8512972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a7aa7b126b714271c9de627eeb71977ea507e8297894a2a49b0bd3f61ed2ee5`  
		Last Modified: Mon, 06 Oct 2025 21:24:17 GMT  
		Size: 18.6 KB (18584 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-18-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6228a7389656b73b300b8debcc36d743ffdbd173beba751c4dbdac52c50b2f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.0 MB (381964173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2cac4fdd495e5bd860f19788f8272f0d1d79d7985c339dc113daa9f3580725`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c9631087ef516f060328537d417f223e1f264c968e39186895696e78090b7`  
		Last Modified: Tue, 30 Sep 2025 01:20:15 GMT  
		Size: 67.6 MB (67582977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe899ba0c19fb03d9bdde2ba727ae71ae6cd21be1bb42cd64b6aff505d005564`  
		Last Modified: Mon, 06 Oct 2025 21:07:29 GMT  
		Size: 16.1 MB (16070462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf4bd688a1d7887b2ccd76fa590c0b83d55ca8449840b3f229854d0c3b49381`  
		Last Modified: Mon, 06 Oct 2025 21:07:22 GMT  
		Size: 223.6 MB (223645669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-18-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:cb9456a60d01951fc1c3b05dc792d7d70af646c60e7f84c070bae43ed01f9f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8726513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684d6c5a7a82fadc670689ee9b565c13075cc79a3ec27fd5798e47600ee3729a`

```dockerfile
```

-	Layers:
	-	`sha256:e4ad51666f1d1bae43a493d84fc2b72f356c3e22a3904054f902a87a94fc7a05`  
		Last Modified: Mon, 06 Oct 2025 21:24:29 GMT  
		Size: 8.7 MB (8707786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1794e6852f98f1b1ff00ab53b64c57b4dbda7484a23d2a47264d906474e0a9f8`  
		Last Modified: Mon, 06 Oct 2025 21:24:30 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json
