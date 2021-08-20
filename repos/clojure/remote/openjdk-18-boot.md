## `clojure:openjdk-18-boot`

```console
$ docker pull clojure@sha256:2c4db38240978b6ea5bb57104023b426b3f96e404321c0906bcd5f95c103079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot` - linux; amd64

```console
$ docker pull clojure@sha256:8b7aa579dbf0c966b580cca078f4b25fbb2761d46b7ff9d813a4cd09e47561cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277382497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca81bbd3d304dd41494940cbbfe9ef274a35a900909fa16ec8d5fe8e6156430`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:53:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 17 Aug 2021 06:53:11 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:53:11 GMT
ENV LANG=C.UTF-8
# Thu, 19 Aug 2021 22:29:20 GMT
ENV JAVA_VERSION=18-ea+11
# Thu, 19 Aug 2021 22:29:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='593243ad4eb9339cec9d7675ff01fb4d7b816c1b1f68d4e54d0dc4f99d8f55f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='8efa12ef6e1acab1a4cc5dba5a45dcb828fa0265e409cd0cf2e8e9eec4ad8f0f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 19 Aug 2021 22:29:35 GMT
CMD ["jshell"]
# Thu, 19 Aug 2021 23:09:17 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 19 Aug 2021 23:09:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 19 Aug 2021 23:09:17 GMT
WORKDIR /tmp
# Thu, 19 Aug 2021 23:09:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 19 Aug 2021 23:09:22 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 19 Aug 2021 23:09:23 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 19 Aug 2021 23:09:46 GMT
RUN boot
# Thu, 19 Aug 2021 23:09:46 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427b7134c0c7b2e1d9cc703e20a84b850cbbf34ef654cfa0db710678a99da78b`  
		Last Modified: Tue, 17 Aug 2021 07:00:00 GMT  
		Size: 3.3 MB (3268768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e628b12479503916e24674a2a918dadb02e86ffbe093a0e7382ad9d1afb7c2c`  
		Last Modified: Thu, 19 Aug 2021 22:36:04 GMT  
		Size: 187.9 MB (187867380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dfa27dd6c8dd8ba2d8d641193236415424dd1c76d7973d684424cdf90c41ef`  
		Last Modified: Thu, 19 Aug 2021 23:14:24 GMT  
		Size: 279.8 KB (279769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7c2c079305a0203aa93875a8310fbaaeeea830d9499d02f074369179ee49b`  
		Last Modified: Thu, 19 Aug 2021 23:14:28 GMT  
		Size: 58.8 MB (58820595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:60f5961cfa9d2c141d875b083611b0467d11a11da96a997857630c7997b00db5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274737768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ce477294647888f923eb5e335daae59b78f1a74c48e45b15e48fd2e0e52634`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:04:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:04:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 17 Aug 2021 06:04:06 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:04:06 GMT
ENV LANG=C.UTF-8
# Thu, 19 Aug 2021 20:41:51 GMT
ENV JAVA_VERSION=18-ea+11
# Thu, 19 Aug 2021 20:42:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='593243ad4eb9339cec9d7675ff01fb4d7b816c1b1f68d4e54d0dc4f99d8f55f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='8efa12ef6e1acab1a4cc5dba5a45dcb828fa0265e409cd0cf2e8e9eec4ad8f0f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 19 Aug 2021 20:42:10 GMT
CMD ["jshell"]
# Thu, 19 Aug 2021 22:34:55 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 19 Aug 2021 22:34:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 19 Aug 2021 22:34:56 GMT
WORKDIR /tmp
# Thu, 19 Aug 2021 22:35:00 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 19 Aug 2021 22:35:01 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 19 Aug 2021 22:35:01 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 19 Aug 2021 22:35:29 GMT
RUN boot
# Thu, 19 Aug 2021 22:35:29 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82a27af984eefbe6b82ccb775aead56e92f82cf16d079218087ebe132125cf5`  
		Last Modified: Tue, 17 Aug 2021 06:15:41 GMT  
		Size: 3.1 MB (3118861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937780d44fe5eb665a71c71605ccd575fca3517f672bab075e89f18fe34cf797`  
		Last Modified: Thu, 19 Aug 2021 20:53:52 GMT  
		Size: 186.6 MB (186603707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8eb2ede806270637d2c0d2c743c2356431d4ce09f1d03fe97824b498929c1a`  
		Last Modified: Thu, 19 Aug 2021 22:41:56 GMT  
		Size: 279.5 KB (279525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75e9f27c1b0eea4a91e84c69cfae4e177d964250c665bb8aa39bb98bd6844a6`  
		Last Modified: Thu, 19 Aug 2021 22:42:01 GMT  
		Size: 58.8 MB (58820603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
