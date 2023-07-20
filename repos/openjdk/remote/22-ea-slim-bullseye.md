## `openjdk:22-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:5e23a8501dfa153361ef4926a5dd5e715cc50a40f8c5888a9aa4332bd32683f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:c147b2c1234165af060cf31a6e951cd6d440fd7cac8421a9dcdf39cc958e6834
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238212211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a9317732f6d6b51da1277733f30c6d58257b197a2eb22cf3de14a37baaf133`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:53:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 01:53:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 04 Jul 2023 01:53:20 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 01:53:20 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jul 2023 20:24:01 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:24:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 20 Jul 2023 20:24:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae78b1797b5f8b06d429ce740e570a94adf8b155152e2e3faa83a259c83894cc`  
		Last Modified: Tue, 04 Jul 2023 01:59:02 GMT  
		Size: 1.6 MB (1582468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c845bef324078e1af90f3bd7348f5b1cd57f2d6eb12cbe71aae245f381e29ba4`  
		Last Modified: Thu, 20 Jul 2023 20:31:39 GMT  
		Size: 205.2 MB (205212355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ce463b028d591c0ee7635f645d1dc29a806951f3c40e48580b0db56be1aa1e9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235156042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7c89f2cd106ab5243f948c4047a8178c080fefc9ecfcdbe38766275c8c0eee`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:27:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 04 Jul 2023 13:27:58 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 13:27:59 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jul 2023 20:08:12 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:08:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 20 Jul 2023 20:08:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb66ab3fe3ab74b42fe268bde056fcbee783ef1979718ffa94fa05e09805b822`  
		Last Modified: Tue, 04 Jul 2023 13:31:59 GMT  
		Size: 1.6 MB (1566385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c94a1e5c39e478eeab2bbb904d1986a000149016dad4a003d7f49248e90f01`  
		Last Modified: Thu, 20 Jul 2023 20:15:43 GMT  
		Size: 203.5 MB (203526700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
