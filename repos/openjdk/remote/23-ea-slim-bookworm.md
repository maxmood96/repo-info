## `openjdk:23-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:8ccf101abe2bc791be6399edfe7ef29a07a97a40cc65e4a5c9b4d0e6fdd098e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:4e5175248f38411b248b141ec38d1974effb5548061d14d2af72cdf2db00a25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236301192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289fee3bb01ec537769b46c645d6611d0aa899ffe46370628d5cd2cc5023aef8`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:52:17 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jan 2024 01:52:17 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_VERSION=23-ea+4
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='9a68dc2301a1ab9d674095ba14205b79ba23dd83002077ae6777edc820e789d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a7293d34fcb6c1b9f5b0bfc74aabc4e695b0e6d6b6778172d59596b19db6e4e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c4a523dcc804ef708a7e16d8a131ff97547d3f82e625d074bdc615e038a1a4`  
		Last Modified: Fri, 12 Jan 2024 00:22:26 GMT  
		Size: 4.0 MB (4014814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8aa0d8463d4c0c4206262cfe416281545b35b0a068645c22289310dac31b894`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 203.2 MB (203160457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c2e8d9925f1fe096b5f82599fe0281431ed7fb487306e397ded9297a1cf74da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea5a53d6cda5505e62029652812d28f975cdb0a0f707f955ac7d44fb035c093`

```dockerfile
```

-	Layers:
	-	`sha256:a0a67d89c45b9d3faacfd5263c7faa3dbd64bc543e5b58783033830100421fff`  
		Last Modified: Fri, 12 Jan 2024 00:22:26 GMT  
		Size: 2.0 MB (2037175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63fdd45944c1b997a4fd1a80de16915c6f115cf5e552ebb401fccc18801737c`  
		Last Modified: Fri, 12 Jan 2024 00:22:26 GMT  
		Size: 19.3 KB (19327 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:00e9b1625468b9f91eb8ddadb234a5caaa28c87b819c1f8af764e41a01d811dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234040485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e2469d4a43b9c052edf868f7b6516d59c80657e03ca9b5d13570ec5aed961c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jan 2024 01:52:17 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_VERSION=23-ea+4
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='9a68dc2301a1ab9d674095ba14205b79ba23dd83002077ae6777edc820e789d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a7293d34fcb6c1b9f5b0bfc74aabc4e695b0e6d6b6778172d59596b19db6e4e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2614bd11b588c96b15909791ce0a1d4f2faa851a036310cc2fe1b2deae203b7`  
		Last Modified: Wed, 20 Dec 2023 10:22:09 GMT  
		Size: 3.8 MB (3819909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac4f8fb9f70cd420c12f323b74f3916b308af7db983e5d4ffe875431ca8a20d`  
		Last Modified: Tue, 09 Jan 2024 02:20:04 GMT  
		Size: 201.1 MB (201063307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:304318a00f81500a6d61a9c7dd0ff69c54be0aa49212a2ee0a75259849767076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2055739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548af11bdbc75c3918cf73eb3aec6ae6b9567c87cc76804416dd6e2ac32b22b2`

```dockerfile
```

-	Layers:
	-	`sha256:8018d49bbca908e70e28671f28a396fc146bb0a470a5b59b783720682d456198`  
		Last Modified: Tue, 09 Jan 2024 02:19:59 GMT  
		Size: 2.0 MB (2036553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bb2a5ec81f104f0cc13b4b19ba76abe2381a6e7fa253ab8a92b6ffcaa9f680`  
		Last Modified: Tue, 09 Jan 2024 02:19:59 GMT  
		Size: 19.2 KB (19186 bytes)  
		MIME: application/vnd.in-toto+json
