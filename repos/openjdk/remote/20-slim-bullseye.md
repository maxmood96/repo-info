## `openjdk:20-slim-bullseye`

```console
$ docker pull openjdk@sha256:981127c7bcdaec74d2c3c665d35011e8fdebb5e866d797eee1a24cd441aa7f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:700d1988e4e2ef8579e4374d2d7275a0f075ec4bfa8af67bde551c4c10c9f25d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231466549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e6353e2a3f7241bf8cdffe6f84fa1d66321215dc4c4f9aad73d9dbb1050517`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:10:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:11:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 21 Dec 2022 12:11:58 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 12:11:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 Dec 2022 01:22:19 GMT
ENV JAVA_VERSION=20-ea+29
# Fri, 23 Dec 2022 01:22:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/29/GPL/openjdk-20-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='c8ef212d37d809927edc8f7c4100bc4606a9680ad1646975f365c7fdb2442eba'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/29/GPL/openjdk-20-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='af77c5e0a7ee15fe98e6ed22e007788db669de2637bdd2b6c321144d8a37b260'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Dec 2022 01:22:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc03ebf496347487b6180d378e9c5769b292b90df671ddc991422926d0809fec`  
		Last Modified: Wed, 21 Dec 2022 12:17:41 GMT  
		Size: 1.6 MB (1582327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92594eb32a08f7f6fafec5fb35c5558ebe159583da78e595e6db3a31c689a782`  
		Last Modified: Fri, 23 Dec 2022 01:31:50 GMT  
		Size: 198.5 MB (198487279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0f8c5aea43125f1c5fbc1e8eea7f26387416438f6bbadd7ebada72ab2d2adfcf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228603027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8f5fef83c61c2fcdb6d42ea88352a48b07b4cd175cfef1881c20c0983827ff`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:53:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:54:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 21 Dec 2022 03:54:52 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 03:54:52 GMT
ENV LANG=C.UTF-8
# Fri, 23 Dec 2022 00:42:00 GMT
ENV JAVA_VERSION=20-ea+29
# Fri, 23 Dec 2022 00:42:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/29/GPL/openjdk-20-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='c8ef212d37d809927edc8f7c4100bc4606a9680ad1646975f365c7fdb2442eba'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/29/GPL/openjdk-20-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='af77c5e0a7ee15fe98e6ed22e007788db669de2637bdd2b6c321144d8a37b260'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Dec 2022 00:42:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d25ec39ac4d8c95008c4cae68bf15b8d0f09df7a1b2b0b0c892724ec59abbd2`  
		Last Modified: Wed, 21 Dec 2022 04:00:05 GMT  
		Size: 1.6 MB (1566279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab4a0830a9ecb8f62f89a79596b5da4f24dd6be489f34b88d8b9f51b64aaf9c`  
		Last Modified: Fri, 23 Dec 2022 00:51:07 GMT  
		Size: 197.0 MB (196991976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
