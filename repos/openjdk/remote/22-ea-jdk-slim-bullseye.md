## `openjdk:22-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:6b96e646eb8c56d85463184a244f7c7eca9c2d1f848ba56940f9295d0efb7968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:b9785c8c9bd6878684ad2302c704b5a60444ffb7c58fb75276ff54bfbbf5a59e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238454608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46ca0d131e6eb82845e63f0a8cbf92699ededf679f8d2af2b5fba55b844a00d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 06:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 06:16:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 06:16:45 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 06:16:45 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 01:30:00 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:30:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='2e079b8de8557b2bfdf2c548f69cf0c8ed9a94e7a0460dfebbebb4bf936dea8b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5b70d1b43017fc00355d38e8f5c5f96d161033968968f76777189ffff3b5ff0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 03 Oct 2023 01:30:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6450b6ea4fa89bead82ea896a53e3dfc6ad66d97a14a9f56241d71c097c8e0e1`  
		Last Modified: Wed, 20 Sep 2023 06:19:33 GMT  
		Size: 1.6 MB (1582466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1501c4f8d42f3f54620769779410ff8ac91411895fcae579afcb2638a6eb7f23`  
		Last Modified: Tue, 03 Oct 2023 01:34:13 GMT  
		Size: 205.5 MB (205454431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ecacc81eca673faa4e938c2212292393895497a36926521a446a5f40cf540c5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235397101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c04b1cf1effe67f0ac3b840d58899a40f4e52a0235cc0afb422a365c9d52275`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:58:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 17:58:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 17:58:12 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 01:34:11 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:34:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='2e079b8de8557b2bfdf2c548f69cf0c8ed9a94e7a0460dfebbebb4bf936dea8b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5b70d1b43017fc00355d38e8f5c5f96d161033968968f76777189ffff3b5ff0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 03 Oct 2023 01:34:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3cb87782f1498c5adbce22d6724eb58d2770ffdc0c184aa7d27ca35e61138f`  
		Last Modified: Wed, 20 Sep 2023 18:02:07 GMT  
		Size: 1.6 MB (1566445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38472cc19d29ed43980fb7527641094a7a45d6997fc15c4c359547fe70ba1cc5`  
		Last Modified: Tue, 03 Oct 2023 01:38:04 GMT  
		Size: 203.8 MB (203767787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
