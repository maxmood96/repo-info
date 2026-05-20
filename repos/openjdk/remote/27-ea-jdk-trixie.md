## `openjdk:27-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:6052232379228bf2cc7853970e64d1ad7650eecc11f290c82f1730aa66a5fe4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-trixie` - linux; amd64

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

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

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

### `openjdk:27-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:666c84d6795a20cc4c39b6a6022bc925de4c3f74ba8e988e70e551ac574ba63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.2 MB (385245215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de36f78d69a0022843cdb3e0a436ee67dd7ee6245772b11057f6b1b705c05a0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:17:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 20 May 2026 01:17:14 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:17:14 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:17:14 GMT
ENV JAVA_VERSION=27-ea+22
# Wed, 20 May 2026 01:17:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 20 May 2026 01:17:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c1c66b190cccf0414ba51dbf14a1d9c497fd347b86d5c3c5efbd786b9c0ca`  
		Last Modified: Wed, 20 May 2026 01:17:43 GMT  
		Size: 16.1 MB (16071338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359b4722f9c02d2849e92e0649784e0d6a3b2df47f5ff3259620c8d32a456387`  
		Last Modified: Wed, 20 May 2026 01:17:50 GMT  
		Size: 226.9 MB (226883202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ab749a8a173d9b9e655571779f1ab9e829cbb8d8d67f3aba0b4aa36c89e04640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266df30ac97d10dca1ae6096c6c6e57fb09575f33dbaf6db3fd0a6b62edf7f7e`

```dockerfile
```

-	Layers:
	-	`sha256:0d0298bdb0073a965495a968172439b108c61a7dfa4ed3302fe8ff4aa55b6051`  
		Last Modified: Wed, 20 May 2026 01:17:42 GMT  
		Size: 8.7 MB (8704223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846bbd8a527bfba46fc0378256c379f0342fd72801a0baccd375ebbbd9057c08`  
		Last Modified: Wed, 20 May 2026 01:17:42 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
