## `openjdk:24-ea-16-jdk-slim`

```console
$ docker pull openjdk@sha256:68676639d21a09f509a1b8a40c03c8fe95190e8d086762aa0ca5147067cd7ce3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-16-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:917670faaddedde5072c9127a3e28c9f91712c13f09a8b64590acd845a5a8614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242878628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581588ae1e332425d1e9a4fdf21be9644b634dcb2caff27e08c752f407b27b0d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 20 Sep 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+16
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='46c9e29e1e700ac596a07ef1795142939bcfd687dcc7f959043886bf800a3bee'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='f42ff15af07babf02cf4dc52c121b18be22bc6f54d6b041b424687f82cdd9919'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f55d71591737b02292699c3b818022d57eb096a05e70b2db7daa5f59a52e15`  
		Last Modified: Mon, 16 Sep 2024 19:23:27 GMT  
		Size: 3.8 MB (3833454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08f5d83f5682678a346733b9cf35ac69c48c3b3e5a27f946cd3d9ca05f7795a`  
		Last Modified: Fri, 20 Sep 2024 18:03:28 GMT  
		Size: 209.9 MB (209888629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-16-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:1a3c91d06f84b0699b2aa1ded7ea73c1c06424a66dab72ff8c31de73cace9f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662cb77f03832bf7bf1404f24c5dad05a2c3543293d8414d8fed12937a40cf16`

```dockerfile
```

-	Layers:
	-	`sha256:09edcf3cd00cdd330a55a78b117391e3a23ba9582573ff9e16bce6ea6ffe9df4`  
		Last Modified: Fri, 20 Sep 2024 18:03:24 GMT  
		Size: 2.4 MB (2365660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a075db869ba90639b7f09d40b74f67cd5095c890e6c517c98b818fe481758c`  
		Last Modified: Fri, 20 Sep 2024 18:03:24 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json
