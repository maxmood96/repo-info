## `openjdk:28-ea-2-slim-bookworm`

```console
$ docker pull openjdk@sha256:fe129c7e29cd57104409e80f01baf6a8fd3fab8c7e3375475d2249a5af58e990
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-2-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5f30deb8e9bff3961e7e02911c57564af81bcc88286fd144b89cb56ecbd48cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259821233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382cc7c125d34ba1941073613542ae9f4ee08b690c9b522e0dc425e804c07db0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Tue, 16 Jun 2026 23:32:53 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:53 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:53 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb91402955e497e9730e0f9ceb620049dde5f642aa2f4d7d30922b7893b97697`  
		Last Modified: Tue, 16 Jun 2026 23:33:14 GMT  
		Size: 4.0 MB (4033006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717e845c029dd5216c1376b65c57caaaed71c14ab7662bcd4d8bf5441b24d4b5`  
		Last Modified: Tue, 16 Jun 2026 23:33:19 GMT  
		Size: 227.6 MB (227550603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-2-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c623b482bdeb1c5550cfa24d2c0361f4c7dac6b6386df1a545dc8fda9783921a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa57fd7d2e487cdd4d3aadbadeee007572d93637dc26e55300deef1152fe1f`

```dockerfile
```

-	Layers:
	-	`sha256:c83fdad54ae5a629d5604e2abdb91c251590d99c3e16302bcf0877d1c01f2a10`  
		Last Modified: Tue, 16 Jun 2026 23:33:14 GMT  
		Size: 2.6 MB (2647280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d9ee0b65b46a83f7ccf809ae047d87660de028ef26ff2051b77813ac66ffe39`  
		Last Modified: Tue, 16 Jun 2026 23:33:14 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:eb2294f3d3c771e7373f659ecf99d661487321486ebe66b0fb436bc75e4d11ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257550559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab2b7d5ce0f8e78092cbd1166406cba202df0c5fdee48cfddd0927cbf6bfd32`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Tue, 16 Jun 2026 23:32:41 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:41 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d350784fca1b924251e08257d40da337480188354a7cd45b461316ea3545386`  
		Last Modified: Tue, 16 Jun 2026 23:33:02 GMT  
		Size: 3.9 MB (3852829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d7434cf1f7a7e2a85cf01bdca97751154c8a61983a53c632515244c08e141`  
		Last Modified: Tue, 16 Jun 2026 23:33:06 GMT  
		Size: 225.6 MB (225575423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-2-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e598079953aa8a70f4951db980a40ac500546c140bbe9560961ee502d62d5435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b54d32db7f4dee46aac6e738aca6cdae5528a12f47260624de70379a38c78a`

```dockerfile
```

-	Layers:
	-	`sha256:cfb3bc4f7c26a1669ff09f75ea72fefd3d2f20f8fdd81220831485a86616a32b`  
		Last Modified: Tue, 16 Jun 2026 23:33:02 GMT  
		Size: 2.6 MB (2646914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3ec144786c2fc8c88325bc4dbdcaacb807a992f258b7a36aa1b281595488460`  
		Last Modified: Tue, 16 Jun 2026 23:33:02 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
