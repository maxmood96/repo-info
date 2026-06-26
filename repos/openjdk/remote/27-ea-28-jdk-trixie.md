## `openjdk:27-ea-28-jdk-trixie`

```console
$ docker pull openjdk@sha256:d787bcc4869221640e4e41599068b730cdce6c285b9586f62a50b99d3f231fc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-28-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:616bc2f1f25b246e4566a4f89448633c679870043254d39651b7e76928ddaa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385892659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cbe415af33664c2257a050517b081555cdaa39d0168f4631c74be5001c3fc2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 26 Jun 2026 17:48:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 26 Jun 2026 17:49:04 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:49:04 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:49:04 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 17:49:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='45707add322e7be16c9eaf4e6f15febf5bd06baeab88aea73d3a89fae0d7bcd7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='1fe32bfb8b4a3533d1cbd2199cbdb9c62d72032b409da56d58135460a7e0c5a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59c84a786323367a79d4959142649bb24b16c989bbaae7f273550b47325959`  
		Last Modified: Wed, 24 Jun 2026 01:41:50 GMT  
		Size: 25.6 MB (25634938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d0db852850114cc79598cc8ab1ec19da54691d9e3267288bb3458d7488f125`  
		Last Modified: Wed, 24 Jun 2026 02:28:58 GMT  
		Size: 67.8 MB (67778134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae82026f79267d1af37fde6c8f64dc16afb317087774f778c5d39356fc6016f`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 16.1 MB (16065638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77404d4a735e63f8bb0e3387b8790daab3ae089d3c547b55b6dd4f49a0882cae`  
		Last Modified: Fri, 26 Jun 2026 17:49:33 GMT  
		Size: 227.1 MB (227096694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-28-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:9ea1ec0b952bad4c81116137df43845c35b3182f98071bf61865f7f10bcbb0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ea7b7099bde9bf24196f9e1b95f7531fed507be04a2d2e819b7eafbc3e6314`

```dockerfile
```

-	Layers:
	-	`sha256:332ac8d0f18fb91ecc3ec2b158d1d68e577f4d81861bfa73ef677bbfbcad5a7f`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 8.5 MB (8508895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0df14a903922caa8d97202d9474561ebf6ab073ff9a0e08870c70e2c78ac394`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-28-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:89138041bcb1a286eba0856a8a3bd172836a8efa35b9f38cf94f65ed4c1769c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.4 MB (383437112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b935f92743d0d65344399c31c0b8ceda7207fb19c0dd837eedbfa60e3a93ad60`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 26 Jun 2026 17:53:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:54:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 26 Jun 2026 17:54:09 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:54:09 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:54:09 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 17:54:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='45707add322e7be16c9eaf4e6f15febf5bd06baeab88aea73d3a89fae0d7bcd7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='1fe32bfb8b4a3533d1cbd2199cbdb9c62d72032b409da56d58135460a7e0c5a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:54:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe059c57e3bc40ea8086d6be574927bed6c0a000b182f3354b758009265e197`  
		Last Modified: Wed, 24 Jun 2026 01:45:26 GMT  
		Size: 25.0 MB (25026863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf605f6b62a65326644e598c84134d29702579734c83dfca4cedf5dad7fb6d3`  
		Last Modified: Wed, 24 Jun 2026 02:35:43 GMT  
		Size: 67.6 MB (67592645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168a992d9b6a7b2baac71ab5ec7dc627b01402214d08503b4c9ebdcf715236da`  
		Last Modified: Fri, 26 Jun 2026 17:54:35 GMT  
		Size: 16.1 MB (16071352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4b583f2106cd909e25d0fa0f5ba4e624f7d24556a561a6d829d573997e22b4`  
		Last Modified: Fri, 26 Jun 2026 17:54:39 GMT  
		Size: 225.1 MB (225067857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-28-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ebf81598b7b2f75372e29e8345916bf17c59a8bfd862168d39ef1182793fbcd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf634ab3e13fa4c56bdb3c637bfa4e1d5b2dfa0f3fee50a4b6a29589e57ef379`

```dockerfile
```

-	Layers:
	-	`sha256:039e6d4ef8263f8676512722d824b5dc4e5fa7cc2bd5017a302aaf35e7e4c8ce`  
		Last Modified: Fri, 26 Jun 2026 17:54:35 GMT  
		Size: 8.7 MB (8703048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43a98873c0c44a07f95223b9932551f69e1c4d2c45b4dac7a0b206a657ea656`  
		Last Modified: Fri, 26 Jun 2026 17:54:34 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
