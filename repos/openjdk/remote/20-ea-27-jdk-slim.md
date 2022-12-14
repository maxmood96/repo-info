## `openjdk:20-ea-27-jdk-slim`

```console
$ docker pull openjdk@sha256:a23d258686ff5b2290461ebf45041f4d125aa7fd9522c6a8a2049bae47166822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-27-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:51250a8b1edb3efda6b92dbd0f164b72d646fcecf17da7146ed66e46395ffa89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231465203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8074b43c600dc0ff291fed7b11a02de88113c0512fdab3f4c2cef02fb441972`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 05:06:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 05:06:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 06 Dec 2022 05:06:08 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 05:06:08 GMT
ENV LANG=C.UTF-8
# Mon, 12 Dec 2022 20:58:25 GMT
ENV JAVA_VERSION=20-ea+27
# Mon, 12 Dec 2022 20:58:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='fc3bc8e77b3b556d06a55cf2c2e5510c94359858d5c691b38575aa164eade92b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7828ad1bee0c3e813c02057353eca047c86f3799cfe3c76cbe21b15d57b239bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Dec 2022 20:58:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca06928f532b9db5daaeea1a6cfedc2be5faa3421714209b828baa3f96741b02`  
		Last Modified: Tue, 06 Dec 2022 05:11:13 GMT  
		Size: 1.6 MB (1584014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e25cf4006fc4058d02e675dc4b08069dc646c656dfb3f06082e68ed6dcc10d`  
		Last Modified: Mon, 12 Dec 2022 21:03:39 GMT  
		Size: 198.5 MB (198468337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-27-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:54e3a41274d25173ba93dcfcd8ebc35d6326bcfac5d035f89629b5c1b1ceccb3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228586059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc493ba464a312563aba0d8fe7240ee4ebfd1fda64869fa1e43a9d5e4d27959d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 04:27:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:27:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 06 Dec 2022 04:27:21 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:27:21 GMT
ENV LANG=C.UTF-8
# Mon, 12 Dec 2022 19:54:03 GMT
ENV JAVA_VERSION=20-ea+27
# Mon, 12 Dec 2022 19:54:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='fc3bc8e77b3b556d06a55cf2c2e5510c94359858d5c691b38575aa164eade92b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7828ad1bee0c3e813c02057353eca047c86f3799cfe3c76cbe21b15d57b239bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Dec 2022 19:54:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e352a64899d702442b046fd5b4919ea4eef3df76860668bc610c2162af8eec`  
		Last Modified: Tue, 06 Dec 2022 04:32:15 GMT  
		Size: 1.6 MB (1567461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7b6959ef562230384d38ac3caf86b931fa2cf150c9181727a862fc6cfe00df`  
		Last Modified: Mon, 12 Dec 2022 19:59:22 GMT  
		Size: 197.0 MB (196958278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
