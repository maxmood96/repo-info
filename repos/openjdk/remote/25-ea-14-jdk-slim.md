## `openjdk:25-ea-14-jdk-slim`

```console
$ docker pull openjdk@sha256:8614b0ae3cc9a4a5527d1b1132a2ada18cb59d88e68fe17359d4ba482d9fd9ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-14-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:fe230f29540ee7d6a769a78523b23bad237d5bd03bbae2ce3c07b8b4ad3ab37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244153050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3bb0a1dba26606213c8a8b0644118e1672773ad1b1b32de1c288c4cb715b6d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 15 Mar 2025 00:48:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f87136f9741f81a970f10817cf043d3f4b06b066c4fb0a1b1111b5e82e13733`  
		Last Modified: Mon, 17 Mar 2025 23:15:31 GMT  
		Size: 4.0 MB (4018438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afee552b597bfc4ecc858420d298096b7be890c338b7b90c0c01564868430cb6`  
		Last Modified: Mon, 17 Mar 2025 23:15:35 GMT  
		Size: 211.9 MB (211929747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-14-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:07b18dd61a85ceebac76576f0ba7aa9ec6d55101679d1925f118ae6c1d12ef6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba331f2968a782ea92e253de107527b401dcc23f765192b2168b64f9efd23d11`

```dockerfile
```

-	Layers:
	-	`sha256:3c99ce5752ac52362a8fffaa8ac3eec710ec6067aaa2ad8a7a2b1985d2473f5d`  
		Last Modified: Mon, 17 Mar 2025 23:15:31 GMT  
		Size: 2.5 MB (2533916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c845d856d594082c77d4a5074240bb47d00cb403855811d30b4aae89b9fa82d0`  
		Last Modified: Mon, 17 Mar 2025 23:15:30 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-14-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4e9849e1473541d254f7f22ad0b56384d78055a99cbca5241fdba76eb1667d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241760248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f28d3f83c217170488e490676fe99b79b7bc1b6662fed596f3639d2202b3e0`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 15 Mar 2025 00:48:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c91501ca16261bf18e11c6d5d732a4f4ddcae8f195acbb862662770301eb4b`  
		Last Modified: Tue, 18 Mar 2025 03:03:03 GMT  
		Size: 3.8 MB (3833739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e292b3440741a325144fd6d04905162ee04e627d8f87e31d6ce2f04442a1e3c7`  
		Last Modified: Tue, 18 Mar 2025 03:03:09 GMT  
		Size: 209.9 MB (209882472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-14-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:2993a342f35e8781b41881d5b73fcd851cb6f54c0a9bbe6f76515c4f9f9bb775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567863b75f75aa3e986132fb60a27c199a6ef3e486f98f8378064f6f36ff103a`

```dockerfile
```

-	Layers:
	-	`sha256:ceccac97580439cfce654e24d04f573436f100261f15fe9e67298d3c8143076f`  
		Last Modified: Tue, 18 Mar 2025 03:03:03 GMT  
		Size: 2.5 MB (2533646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d2fe4c350b3ac1aef2d7604d1590ee05f8044218eb51f09b583ffbe1bb9c2d`  
		Last Modified: Tue, 18 Mar 2025 03:03:02 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
