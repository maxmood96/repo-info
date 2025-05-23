## `openjdk:25-slim-bookworm`

```console
$ docker pull openjdk@sha256:b50ca3b3fb711522fcc3aaa8d4c04ae153e51e3c91842272ff02412e465ca43e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:7a3e8656e4887431d539657c877404dd90ee485ce9541ebf8be7c41dae2dd500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d616770ac313450d7bc324154bc7da1279eb5927a46c914a24e74a7dd56dc1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7675d1f849ab3084d4a189e89426666a40bb13f7cec18811ce3ee5a631cc4c`  
		Last Modified: Fri, 23 May 2025 19:55:10 GMT  
		Size: 4.0 MB (4020003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77697bbe7706d5a24dd932074cb4533054d690bd6e6586d2005292ff56eacaa9`  
		Last Modified: Fri, 23 May 2025 19:55:13 GMT  
		Size: 214.0 MB (214039938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b49c65d1c04b9a2ac32763a7aaa43008076ea35fdeb43c20cad5c4b76c654190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef95d0887a5d34545bcb7972a9c3b8fcb4050a40786d7f7db37195c234947f21`

```dockerfile
```

-	Layers:
	-	`sha256:3fdfd6aa7e06f4ddaa809ff62ee0055ff881d178f245c8a0014a153676f20c3b`  
		Last Modified: Fri, 23 May 2025 19:55:10 GMT  
		Size: 2.6 MB (2552703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722bfc13b6e567749dff8239a97be75886626bd5c82bcca92583f0988c1f53e6`  
		Last Modified: Fri, 23 May 2025 19:55:09 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cdea1173d8233641c1222024874fc0cf210f60aeb1bd4da08a0ed327d0676746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243713585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8123e64a7158ffd0d14f1acf1e232c103c1ad51a40ca5f261040c38239a22590`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534846ac900e03a1a9681c93961912f7790334b9daba4996c1c1fb5a858bff00`  
		Last Modified: Thu, 22 May 2025 03:34:20 GMT  
		Size: 3.8 MB (3835231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c687215a706fe81ce31f2eb1f2426d194b69de9bbafb78b882993905067f9c3`  
		Last Modified: Fri, 23 May 2025 20:07:18 GMT  
		Size: 211.8 MB (211813074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3af939f0f389cb176c0c1c8fbc36a6c38fbd161acb4d6ce23070286e6b5a9d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81fc613b69b93fb8a34995f9fec8f3d49e227d0483abedd8a26c505c45c653`

```dockerfile
```

-	Layers:
	-	`sha256:761b9f81ce64f6aec25dc95df1fb807d9a84df6c6411cd9df92078796ab56704`  
		Last Modified: Fri, 23 May 2025 20:07:14 GMT  
		Size: 2.6 MB (2552433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc57841204d1133ebac041d2efd3317b561bc66cc2a7a39459c818132269e9ad`  
		Last Modified: Fri, 23 May 2025 20:07:13 GMT  
		Size: 19.7 KB (19656 bytes)  
		MIME: application/vnd.in-toto+json
