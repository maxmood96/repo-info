## `openjdk:25-ea-11-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:80670477c553d189f7ff76a612f68cfe3a5f23295052b7d908a35d6637f1b275
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-11-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:49b64920d3cf16b22db7b4717ab6331a6a67ac8e3037da46c5485bcefd9ce4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243611795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2398a67dc578536f3fd418db27faf1cc6aa76139eadcae7a3ded03a9a763229b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Feb 2025 01:48:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75b418bff8cd157cb04b51e7def66cf5bf98f3350a737e0833a8ee62529ff75`  
		Last Modified: Tue, 25 Feb 2025 02:28:36 GMT  
		Size: 1.4 MB (1377215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2428037070c0a512006bbbc8cabe8560ff67260a7ca4c1654c5770857850a851`  
		Last Modified: Tue, 25 Feb 2025 02:28:39 GMT  
		Size: 212.0 MB (211980650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-11-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:0a7efd9b2c792810e0760ac43c0dd957c6a5ff81a6ff645434979ddde7ec203e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a574d464d1dc29d1f6cc73498e4c932962662c060628d00288399c84692db9e0`

```dockerfile
```

-	Layers:
	-	`sha256:b3adfc639493ec0f398e14085cc7985a90b6c2b14d63dff7f9d6f61680d64eef`  
		Last Modified: Tue, 25 Feb 2025 02:28:36 GMT  
		Size: 2.8 MB (2831053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057731344448a5c1280078324dd8d9039bf5a079e9f5c3e5c7d4c35645f78d82`  
		Last Modified: Tue, 25 Feb 2025 02:28:36 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-11-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e43f9b77839c70a40496ea48a369c1efdc1a2e6d45554d48b380e50f9aaab6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240033272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29501469d1ca4313ceadef695a260f82e630959f63caa949e834f1261b7b6e55`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Feb 2025 01:48:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6204c439a953bed7a76b34fba5d07cc86c4cf0bb198d41bd4b68599e9a4ab576`  
		Last Modified: Tue, 25 Feb 2025 06:26:49 GMT  
		Size: 1.4 MB (1361261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef32444887eb77d25871772521ec4a7d2bac6309b0807c615789e70a63b0fdbc`  
		Last Modified: Tue, 25 Feb 2025 06:26:55 GMT  
		Size: 209.9 MB (209926024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-11-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c12af5c7431faf0c785dae98f735afaea833bdee9551588dd6b27cff0f8ff781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7a06255f7105440e7cee28ccad316575a839cac060b01d8efcd7a12a018eb0`

```dockerfile
```

-	Layers:
	-	`sha256:7935f1fdf27ec62dbe55faee057a8a6c36b643ea18edd843d4be237a2d997ff5`  
		Last Modified: Tue, 25 Feb 2025 06:26:50 GMT  
		Size: 2.8 MB (2830705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c3ffcdb2343f22e42312daeabb09accfd6660ad53ef6016de37c66b575cb3ac`  
		Last Modified: Tue, 25 Feb 2025 06:26:49 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
