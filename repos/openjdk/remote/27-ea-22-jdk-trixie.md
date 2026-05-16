## `openjdk:27-ea-22-jdk-trixie`

```console
$ docker pull openjdk@sha256:bc1dce1eab1394e23b0c08cdcabc8bf5a83f3f1dd8fe8d2bb983a41d84886b6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-22-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:3cda599e68a656335644a11c5cd1e68fcdb811459f10fff961afed7c97e8e525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387707940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b373ad447a0640ec15cdec9e0f456695829dd6d88c9889de3837ff4699a988e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 15 May 2026 20:18:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 20:18:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 15 May 2026 20:18:42 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:42 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:42 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489983f41aab8c17c0f044d7054bd4ee3cb090893049bb2e857dd7514566dd55`  
		Last Modified: Fri, 15 May 2026 20:19:06 GMT  
		Size: 16.1 MB (16065733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48014ef100a64837390b87a4b806f0339bcd89ac6fc0d1f766f784321f8c3195`  
		Last Modified: Fri, 15 May 2026 20:19:11 GMT  
		Size: 228.9 MB (228927575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-22-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d67f96599295e2af1a7e8fc5cd23022e382bef7defcc84ff50dc803155c53555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f131f52b0b21110c946659affaf327877829e035ef1ace7b992964c639478120`

```dockerfile
```

-	Layers:
	-	`sha256:4c711ece7a20d228de4e828cf9ee90ca6646f9f4034a7f56501cd00f495792e0`  
		Last Modified: Fri, 15 May 2026 20:19:06 GMT  
		Size: 8.5 MB (8509920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d31d1a047988b2fbfbd05272a267a167037ecd830c44c1eaa492f4af9ff9899a`  
		Last Modified: Fri, 15 May 2026 20:19:05 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-22-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9d80076dde0463a98be5589e21a1545126eb12990c069e013b6c7967a79b3bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.2 MB (385239794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1fdb3a67c8e532cffd6ec00368387e0b9cb6097c42f9f3dcc943484ca3dac9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 15 May 2026 20:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 20:18:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 15 May 2026 20:18:26 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:26 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:26 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da76eb902cd1fd807fdfc9fdf934f07968a695b2274fa7e16fb34e9366bf85e`  
		Last Modified: Fri, 15 May 2026 20:18:52 GMT  
		Size: 16.1 MB (16071570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62880d7f9e77cf91c46154a8f9a25028d0ef375992348251d542ef02cca2e32b`  
		Last Modified: Fri, 15 May 2026 20:18:55 GMT  
		Size: 226.9 MB (226883248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-22-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0e2d89bbc13afa05f6fc313b6c9a12df5db8ace444d93c383b207e2910a52e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd93a3942515bc64cbbde5d6b7f60bf7b47d001f4fb03bcc00218ff062ea17ba`

```dockerfile
```

-	Layers:
	-	`sha256:01eb171273f7cf0e5ee2b12b2726fbcdd85b1c4cadada82662ad6f8648064af6`  
		Last Modified: Fri, 15 May 2026 20:18:51 GMT  
		Size: 8.7 MB (8704710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2318b337c4662a4ff9f016a317b65f63c103d429e5aba6bad29492b99d720d05`  
		Last Modified: Fri, 15 May 2026 20:18:50 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
