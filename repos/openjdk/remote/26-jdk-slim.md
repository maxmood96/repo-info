## `openjdk:26-jdk-slim`

```console
$ docker pull openjdk@sha256:4ead9499598f0619575aba5c7e45a128156b4a3aea95522e85f589563d9189ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:46d7d7a8f937c4f1bdeec5232810ca7aaf04e61924edbdac007750da3c6be6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255346812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aece7a4a18bd083b0fa6d268703bdf4f96e56e74831019220ff7ddbb5011cca1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 12 Aug 2025 17:48:34 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:48:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_VERSION=26-ea+10
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='09044ebef2f1122e484e84df3a95605462c66caf6fb6363a6b3bb70cb6dba3db'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ffacf32c82e822c5ffb1400e05a279b08ddcc3f2c5538d01bf79f31c2af0fb2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da6b356553dde33a62c8200d69e45905bd367e945d18425ee6ea7dfa2bf5a6a`  
		Last Modified: Tue, 12 Aug 2025 23:39:36 GMT  
		Size: 2.4 MB (2371048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cc866c79fa8660e924442ee20b3390f45629ea6cbe49585839b4c7b294e469`  
		Last Modified: Wed, 13 Aug 2025 00:38:45 GMT  
		Size: 223.2 MB (223202479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ddfb560ce3e953d0b177a7111c63721e31835fbdecee3d490cfcae5be84df65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df13b9523e3bceb4d0d9320eb528bbb6680d6292476e8f77ba2676bd1ff7c695`

```dockerfile
```

-	Layers:
	-	`sha256:87f29272edb3c54ccf00bac5f550ceed75cc56faff5368c7a6aadeaadfdbe4e9`  
		Last Modified: Wed, 13 Aug 2025 00:24:45 GMT  
		Size: 2.3 MB (2281656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8591a3fe86d3a5eec0e226ae91bed93462036140d8cee15f8d6ea1aa4f426aa`  
		Last Modified: Wed, 13 Aug 2025 00:24:46 GMT  
		Size: 19.4 KB (19411 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4099e3ca263cb32173ad2cc9cd407fa9107a72a315494a321ca8b7f75f255cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253471748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8ef3cb05bc7bb5267e6b8315d62e4f6342717570d65d3a0f8cae62f75b5eee`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 12 Aug 2025 17:48:34 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:48:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_VERSION=26-ea+10
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='09044ebef2f1122e484e84df3a95605462c66caf6fb6363a6b3bb70cb6dba3db'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ffacf32c82e822c5ffb1400e05a279b08ddcc3f2c5538d01bf79f31c2af0fb2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512919f072a673e9dab75fcb7614cb9cd2c9167ebea194f8f30082ef4e0d0348`  
		Last Modified: Wed, 13 Aug 2025 08:19:57 GMT  
		Size: 2.3 MB (2314200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e866eee1344a230171d1cef09ae1c5b2e6f8a5f03be1f6d87f887a656410f9`  
		Last Modified: Wed, 13 Aug 2025 09:28:51 GMT  
		Size: 221.0 MB (221021504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:e2d3175a96aaa833533f0f9b93039ac2fa98ca72c935df605287aad225668c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e968c2d016c9482fe6b80470d36cb4096468816677f37b73bd11c3851d99d9d`

```dockerfile
```

-	Layers:
	-	`sha256:801b80ab200159ade56203c43dfa3e4c8ed5a1917beb968fe49502db8bee5dcb`  
		Last Modified: Wed, 13 Aug 2025 09:24:04 GMT  
		Size: 2.3 MB (2281390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de0f88f809b138bd6b20bfbaa2906646a49f1d07cd258784963d1dfb7ce5fa9`  
		Last Modified: Wed, 13 Aug 2025 09:24:04 GMT  
		Size: 19.6 KB (19627 bytes)  
		MIME: application/vnd.in-toto+json
