## `openjdk:26-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:7bef6d512df7037b9170612c2860c32d6bccb23902020d8b13c3346dba7c3ecc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:3fa0d995d59448c1d85844ad0ba46f12b7aaf3d07fca31a2ce3cbbc619278455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260238222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfc34cfda3a742b8ad18a0c944e0d20dd5b5d4c83e6bc0d13a9e2d5c9cf087d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Sat, 06 Dec 2025 00:34:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:34:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Dec 2025 00:34:50 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:34:50 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:34:50 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:34:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:34:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d01a85cfe5ec195a2e8496a23771a1b7635e6d16eb217603ce52051886dd11`  
		Last Modified: Sat, 06 Dec 2025 00:35:23 GMT  
		Size: 4.0 MB (4027342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126bf9a3812b523742d7402ede65bfd95f56bf97090101d608e0d58cef7c1771`  
		Last Modified: Sat, 06 Dec 2025 00:37:54 GMT  
		Size: 228.0 MB (227982431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:58ab5101f62d2cd86931a2978711618659ff7967357aff01d8915350d0129682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8c3dc3b6f1f94398ca2606cf55903655aa13a3af72540071bf033ab5aaab31`

```dockerfile
```

-	Layers:
	-	`sha256:213f847d069244f0e678c93fc0cb82c300ae0619ec62e6857a31fa5761b33c32`  
		Last Modified: Sat, 06 Dec 2025 01:24:18 GMT  
		Size: 2.6 MB (2649789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7061ea810682ad2ab77ece418231cd2a75434cb342d37ee4205cc73d5377fa78`  
		Last Modified: Sat, 06 Dec 2025 01:24:19 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e96078a719aa2e716d3799ed7e7005a9c2e4ee948774a5b29cb35922d0e9ab9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257857366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9474fb72d48851b87aa23d9da396c28aef65378c8473b1f10745a6347f57231`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Sat, 06 Dec 2025 00:35:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Dec 2025 00:35:28 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:28 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:28 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:35:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdfba0e4ce9079fda5a3c8b5c6a8b8a81d7a4e093b1a86e119d8d7c1d38553c`  
		Last Modified: Sat, 06 Dec 2025 00:36:00 GMT  
		Size: 3.9 MB (3851416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cf55785556c20049c249de932758d690c0bf7dd0c5eae7e4388cf27a858b1c`  
		Last Modified: Sat, 06 Dec 2025 00:38:43 GMT  
		Size: 225.9 MB (225903743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a51516b2ed1c925fb303dd0e1e8a60f60a3a0c30da4385edd1f445f167b1b375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ceb77826e4f038987f89b083458a37ad9a1ffc206fbc85e3a67d19316562cb8`

```dockerfile
```

-	Layers:
	-	`sha256:06154441118d2ed9115c74072c13318cf620949bd937f7579429d0e35f8cab4c`  
		Last Modified: Sat, 06 Dec 2025 01:24:23 GMT  
		Size: 2.6 MB (2649423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d31ce525f1c02e898d02e7c583ea2021c252d794e78f354c2a2a72d996ee1f3b`  
		Last Modified: Sat, 06 Dec 2025 01:24:24 GMT  
		Size: 17.0 KB (16989 bytes)  
		MIME: application/vnd.in-toto+json
