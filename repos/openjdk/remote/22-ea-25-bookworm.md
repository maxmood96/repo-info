## `openjdk:22-ea-25-bookworm`

```console
$ docker pull openjdk@sha256:d04d855ff8d2f6ba4aaa2d18028202a20c2892df987cdad9324e13425c064b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:22-ea-25-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:33c1cccf23549142496c670987b54777afd18cfd332cb57082685234b2eb578c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359143378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b7f54bc3163bb31fb56e22dca53d1c422dd4b22e32a481de8979cd44b3c6a4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:52:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:53:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Nov 2023 00:20:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Nov 2023 00:20:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 22 Nov 2023 00:20:47 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Nov 2023 00:20:47 GMT
ENV LANG=C.UTF-8
# Wed, 29 Nov 2023 01:45:42 GMT
ENV JAVA_VERSION=22-ea+25
# Wed, 29 Nov 2023 01:46:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/25/GPL/openjdk-22-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='0f98721a88a1dd380773adbf29dd79df25be9b69045c3266f913ecacc5e74d3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/25/GPL/openjdk-22-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea5fc28e7b6ed0a5da04b4740a35d8dd26bb68a48a516da2d002359d817ba35c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Nov 2023 01:46:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1a8ca91d35598fbae8dee7f1c211f0f93cec529f6804a60e9301c53a604d0`  
		Last Modified: Tue, 21 Nov 2023 10:01:22 GMT  
		Size: 24.0 MB (24049172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a767d1d12e57724b9f254794e359f3b04d4d5ad966006e5b5cda78cc382762`  
		Last Modified: Tue, 21 Nov 2023 10:01:41 GMT  
		Size: 64.1 MB (64130771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a396ac387a82e939e9a1b9845b83c0159c426a633b2f5189dc13174c2b16846`  
		Last Modified: Wed, 22 Nov 2023 00:22:10 GMT  
		Size: 17.0 MB (16951784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1fd331710a7fe78ac4ec1e9dfe5dda2714c7a1b60361643db232fc8a81dd3c`  
		Last Modified: Wed, 29 Nov 2023 01:49:43 GMT  
		Size: 204.4 MB (204429426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
