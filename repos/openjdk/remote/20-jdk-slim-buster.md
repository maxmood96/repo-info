## `openjdk:20-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:9dc91cf770a140eb40843a5e829409aa6aafbc6f8c71029d82bdb2b9b29d0a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:f4555518a4677a1af61b91e7172d67405b46125095b425b751046dcd2914fdaa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228888431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc43cb3cc147689b9f951effb473710999fc50a7c3c356bddcfb350e447fae50`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Dec 2022 01:21:18 GMT
ADD file:30180333dcb9028c0d2776f05042f6f309238b100863a050f3981fb80604e871 in / 
# Tue, 06 Dec 2022 01:21:18 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 05:06:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 05:06:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 06 Dec 2022 05:06:57 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 05:06:58 GMT
ENV LANG=C.UTF-8
# Mon, 12 Dec 2022 20:58:59 GMT
ENV JAVA_VERSION=20-ea+27
# Mon, 12 Dec 2022 20:59:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='fc3bc8e77b3b556d06a55cf2c2e5510c94359858d5c691b38575aa164eade92b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7828ad1bee0c3e813c02057353eca047c86f3799cfe3c76cbe21b15d57b239bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Dec 2022 20:59:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6eab20599fab240a56b06125a77b4921dd39662d3b9f9008da7306531772a1d0`  
		Last Modified: Tue, 06 Dec 2022 01:25:52 GMT  
		Size: 27.1 MB (27140356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9669963fa8087b26171d843ba42c25760333a213b886c3b12289e827c22c574d`  
		Last Modified: Tue, 06 Dec 2022 05:12:29 GMT  
		Size: 3.3 MB (3275939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ee7bd9c996efb1e0ade7c265cb9e2f031803c0991c3274aba68fe5c4c06eea`  
		Last Modified: Mon, 12 Dec 2022 21:05:08 GMT  
		Size: 198.5 MB (198472136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:74047cece46885ff99551025f984ae2cc97f72d23ea500f0e753c42979e66d22
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226010415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39850b6084fedbdb4a070a6fcc9a9dff1ffb4f3365fc4a988f496ee3000807d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:28:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 06 Dec 2022 04:28:02 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:28:02 GMT
ENV LANG=C.UTF-8
# Mon, 12 Dec 2022 19:54:34 GMT
ENV JAVA_VERSION=20-ea+27
# Mon, 12 Dec 2022 19:54:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='fc3bc8e77b3b556d06a55cf2c2e5510c94359858d5c691b38575aa164eade92b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7828ad1bee0c3e813c02057353eca047c86f3799cfe3c76cbe21b15d57b239bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Dec 2022 19:54:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ebe9071c02f951926aefb5793b954b3398b0073a3c4a5b8ce0984c4f12050`  
		Last Modified: Tue, 06 Dec 2022 04:33:26 GMT  
		Size: 3.1 MB (3129343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0152e0ef556bf62fd5f055d934d6fb1e722c94cce2aa67bf57be50ff948f19bc`  
		Last Modified: Mon, 12 Dec 2022 20:00:36 GMT  
		Size: 197.0 MB (196966121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
