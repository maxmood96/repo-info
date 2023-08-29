## `openjdk:22-ea-12-bullseye`

```console
$ docker pull openjdk@sha256:4b962dcfd86cbad0a457355a65a36864231d1a217b924536bb21e665a0dbd91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:22-ea-12-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7cf32f6a05c577fe867174207d0be69f1c996e100e8b741a7b0f29dce6717ea9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.0 MB (342963561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d428146eeabd65526d2b5b7edde488e6095238807d26cff9d258879e64d9ea`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:23:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 04:12:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 04:12:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 16 Aug 2023 04:12:56 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 04:12:56 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 00:11:58 GMT
ENV JAVA_VERSION=22-ea+12
# Tue, 29 Aug 2023 00:12:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/12/GPL/openjdk-22-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='e46c5ea4f8d5c55ba96ac2116faf9e31aae6f47c5317733d7dcdfdb8689ccddf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/12/GPL/openjdk-22-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='92ab4cea6b4351893b5ce66ce559b3b98b138e7eb96c3acaba52b98747904443'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Aug 2023 00:12:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abd0588cbb35597a784666f0dc97746829b8b4b730b73e8781fb90678ffef22`  
		Last Modified: Wed, 16 Aug 2023 01:39:26 GMT  
		Size: 15.7 MB (15746520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a8864a846a08e10fbf877e73678d1f0803227b00a1b16d9ba948070c6e58f6`  
		Last Modified: Wed, 16 Aug 2023 01:39:40 GMT  
		Size: 54.7 MB (54676094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a6fa7848bd18db73961a31c8f10f1948f4b05eee7d26cbad70e22f41dbb7a0`  
		Last Modified: Wed, 16 Aug 2023 04:17:16 GMT  
		Size: 15.5 MB (15529238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da969782e6107fd7df5eaf1ff421ce5a9d5b73d6053a541ba0248f0b83783ec`  
		Last Modified: Tue, 29 Aug 2023 00:15:52 GMT  
		Size: 203.3 MB (203306930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
