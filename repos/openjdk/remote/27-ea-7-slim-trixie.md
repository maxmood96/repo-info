## `openjdk:27-ea-7-slim-trixie`

```console
$ docker pull openjdk@sha256:7750dd311dc2e6aaab04d1e4815780a8595dc0e2b9674b8bd2c9cdc615beb243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-7-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:c861e188570420ed30a3a1619e3a48967013aed4257f92b2921c431f9b112fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263517573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e2d936e57641c043061ea7b11ace47e160e80d34af3e66e576f41445e83599`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 30 Jan 2026 23:40:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 30 Jan 2026 23:40:30 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:30 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:30 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4a0605e4f788be139bb9d856cfccfe5d195d3f629d308f0c5a7b306d16a71`  
		Last Modified: Fri, 30 Jan 2026 23:40:51 GMT  
		Size: 5.3 MB (5333330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8d379628723a773e7127ce41f83793a629ec83f58ccda16b5d6bb8595d9d01`  
		Last Modified: Fri, 30 Jan 2026 23:40:55 GMT  
		Size: 228.4 MB (228410558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:80208cb1040c67892d4a8e5a1a5ca19bb4f9070c87bbda6906a2071b9fc88f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840b746638ebc314288b3465a6a0f30d03758657d63512a5c5217d30af6329c`

```dockerfile
```

-	Layers:
	-	`sha256:97a88d01be95b1f5576924fb98a6ebc4915b29288c33081d58686605cbdba374`  
		Last Modified: Fri, 30 Jan 2026 23:40:50 GMT  
		Size: 2.3 MB (2278218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043fe4b143cbaabc0a1537f8620662abdaaac9c43040712ae035cd0dcbc67f74`  
		Last Modified: Fri, 30 Jan 2026 23:40:50 GMT  
		Size: 18.1 KB (18087 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-7-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ad73b3ca3dc771ed7064c2cb7247fd703981e086c53def40011344d372796f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262111838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb812f58445059b65c2aaab093d37caca1a67a97fb4f275deb5156e9cbc0d6e7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 30 Jan 2026 23:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 30 Jan 2026 23:40:26 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:26 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:26 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587c1ffdd4e9a15e1ec9faf5d6909877512b94980663eb556e8ad1cf148c3c91`  
		Last Modified: Fri, 30 Jan 2026 23:40:47 GMT  
		Size: 5.6 MB (5635682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cee6a661fd6dc62e013490fcb0442eda787f711c0ef0176054cab69704badc`  
		Last Modified: Fri, 30 Jan 2026 23:40:51 GMT  
		Size: 226.3 MB (226342114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ec3f6e512b9444ca2fb07ef3cf54bf2da997b00a1dfd8dfd780108c413029158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de5d3f3ca742daae71b3260b409629dba6a4ad044b59e5fd1bd6ecb501fbe49`

```dockerfile
```

-	Layers:
	-	`sha256:f9598aa117591b01e7380650c15ed47fe7c39c17c8ba06f146d6b84c8198a992`  
		Last Modified: Fri, 30 Jan 2026 23:40:47 GMT  
		Size: 2.3 MB (2277904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c116870090c2c75e757cb3f6c5b5f48347864572d07eb7443f58aa7b346c7b3`  
		Last Modified: Fri, 30 Jan 2026 23:40:47 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
