## `openjdk:27-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:78059068abb194ebc5975b02eea9ec5cca8a9789734cc55624f25b1283d25923
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:74f4aad15f8998e868f3a975152b8b46fe047910f747ac73bd183e92a82d1879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261238509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4f057ab97737e6cd542da9d7ff9370747ab31f02cdc2387015f788b61ca494`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 19 May 2026 23:28:51 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:28:51 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:28:51 GMT
ENV JAVA_VERSION=27-ea+22
# Tue, 19 May 2026 23:28:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 19 May 2026 23:28:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51e24780aa1639beae8c78855cda7af1cdad29c23e753f750c681cdc6f5e317`  
		Last Modified: Tue, 19 May 2026 23:29:09 GMT  
		Size: 4.0 MB (4032608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45b851ac1e480f589a7262d654135c619e1766d69368167534d286f6a7af5b4`  
		Last Modified: Tue, 19 May 2026 23:29:15 GMT  
		Size: 229.0 MB (228972358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f9154b22cfec97d77068a8dc63b3f6a1a6e9e0a10fe2c8d65ef86bb6d5b14cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f58b81b4cbb3b0663a6e773bd569a8360b2e64762822d247956e08aeffdb11`

```dockerfile
```

-	Layers:
	-	`sha256:d51fefc2185e4e6df0ec82545667e57bacf2895da7bc79aca256837daba1e95c`  
		Last Modified: Tue, 19 May 2026 23:29:09 GMT  
		Size: 2.6 MB (2648555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa7e9fa7c3108e1479ee6bd3a4ad8b9ef3bf009e3727a31974d107bd8160602`  
		Last Modified: Tue, 19 May 2026 23:29:09 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ab7ba35d2dc3c1b995a3b7115ccbe6c67e68000417dee121b515d571da10c371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258892934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e675e4322a4c1a7a8c6caee9ad5db9accada8a877db1f119ab6c34805f274da`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:32:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:32:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 19 May 2026 23:32:22 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:32:22 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:32:22 GMT
ENV JAVA_VERSION=27-ea+22
# Tue, 19 May 2026 23:32:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 19 May 2026 23:32:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc7d0d0582f7198234df2b20d87653c8ecda07a9ea08486c1e0329c4c85e0a3`  
		Last Modified: Tue, 19 May 2026 23:32:42 GMT  
		Size: 3.9 MB (3852992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb50dba349f6ca003e80c6dd8e6facfe13a3e8a12223c8233f4644ae9c8c818`  
		Last Modified: Tue, 19 May 2026 23:32:47 GMT  
		Size: 226.9 MB (226924899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c63c4ede7994fa20bf66513f243895a14444534dc85c5329d7fdf0d1983f769a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04fae3625de3068911712d532da6db8f18fdbbfdca3c70b92523e004fa2420`

```dockerfile
```

-	Layers:
	-	`sha256:6f75b5e6032664419c605107f4763b29b32daed73a02e292d5b669ff9b3fa90e`  
		Last Modified: Tue, 19 May 2026 23:32:42 GMT  
		Size: 2.6 MB (2648189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fcb06cd177e2057572815ef4f6be993f19587c8cbc7e6175d11040873370367`  
		Last Modified: Tue, 19 May 2026 23:32:42 GMT  
		Size: 17.0 KB (16989 bytes)  
		MIME: application/vnd.in-toto+json
