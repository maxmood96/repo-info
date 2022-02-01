## `clojure:openjdk-18-boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:a6d2f5282cb043a2fe64eed04f64e52979953f2595a0fc5996ec8fa8c6dd9d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:070897d6c8a355e7332636d2c2db66818e33a479f18b6c82b4da5757b3026d05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278575731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ffee6bafb07dab256b34bae7a98fdd7e7968c0f4eeaebae3d576496726c17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:19:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:21:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:21:10 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:21:11 GMT
ENV LANG=C.UTF-8
# Tue, 01 Feb 2022 03:13:45 GMT
ENV JAVA_VERSION=18-ea+33
# Tue, 01 Feb 2022 03:14:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/33/GPL/openjdk-18-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='01f7265aafc4325b507fb6f033881dba83b8b510fc0a70f1e0a9d0aa619b2c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/33/GPL/openjdk-18-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='467277bda5bacab0ef3c18247e1e2f9f9fe6e025510954a8eb95589c752b620c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Feb 2022 03:14:01 GMT
CMD ["jshell"]
# Tue, 01 Feb 2022 03:47:14 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 01 Feb 2022 03:47:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 01 Feb 2022 03:47:15 GMT
WORKDIR /tmp
# Tue, 01 Feb 2022 03:47:20 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 01 Feb 2022 03:47:20 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 01 Feb 2022 03:47:20 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 01 Feb 2022 03:47:49 GMT
RUN boot
# Tue, 01 Feb 2022 03:47:49 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 01 Feb 2022 03:47:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 01 Feb 2022 03:47:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa8d0f5eb646a53df0b867301afa43404e868c540fdf170240578844dfd0d6b`  
		Last Modified: Wed, 26 Jan 2022 09:43:10 GMT  
		Size: 3.3 MB (3269688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932a6f1fc5e51e33c1c998a6fb2c746a0943c48bda0827225577c494c269ae25`  
		Last Modified: Tue, 01 Feb 2022 03:28:38 GMT  
		Size: 189.1 MB (189051411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b596c8d477b41cdbb597ae5b410bc8921b31dcc55481be2c8bd925b646cf46cd`  
		Last Modified: Tue, 01 Feb 2022 03:55:45 GMT  
		Size: 279.8 KB (279778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e82406f4215f416eb30e8d80eb2523b3bc020c9f66d0ff80d515969a61e4794`  
		Last Modified: Tue, 01 Feb 2022 03:55:48 GMT  
		Size: 58.8 MB (58820717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c760a71e2b3404110ac1297f3dc39a9bd19dfc273c921e8586ee4140c8c93`  
		Last Modified: Tue, 01 Feb 2022 03:55:45 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:39ed873f6a42b55e6ba68fc739703f2abe8df6d77f901fd20a2086aa7ee24203
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275699009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40693aaebdb13db2d37ee0e8330c533ffb02cfaab67f56433ef2f559d77a89c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:53:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 05:53:13 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:53:14 GMT
ENV LANG=C.UTF-8
# Tue, 01 Feb 2022 02:48:10 GMT
ENV JAVA_VERSION=18-ea+33
# Tue, 01 Feb 2022 02:48:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/33/GPL/openjdk-18-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='01f7265aafc4325b507fb6f033881dba83b8b510fc0a70f1e0a9d0aa619b2c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/33/GPL/openjdk-18-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='467277bda5bacab0ef3c18247e1e2f9f9fe6e025510954a8eb95589c752b620c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Feb 2022 02:48:30 GMT
CMD ["jshell"]
# Tue, 01 Feb 2022 03:30:45 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 01 Feb 2022 03:30:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 01 Feb 2022 03:30:46 GMT
WORKDIR /tmp
# Tue, 01 Feb 2022 03:30:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 01 Feb 2022 03:30:52 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 01 Feb 2022 03:30:53 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 01 Feb 2022 03:31:34 GMT
RUN boot
# Tue, 01 Feb 2022 03:31:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 01 Feb 2022 03:31:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 01 Feb 2022 03:31:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a5c9716b24a17043a5d8ede1303daffeaaa07ff0393fa14caed54f01154833`  
		Last Modified: Wed, 26 Jan 2022 06:14:50 GMT  
		Size: 3.1 MB (3118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d764a3665ce0e4520007891588ac2eef778912e096587be1d9b5a8058ef3a1e9`  
		Last Modified: Tue, 01 Feb 2022 03:09:02 GMT  
		Size: 187.8 MB (187772177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449d9f01f332989335b680811c60ad35495b3d1fdef0e881d3a5d8021be72df3`  
		Last Modified: Tue, 01 Feb 2022 03:43:17 GMT  
		Size: 67.5 KB (67524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7daf5e661fe4c0aa1f6a7c427b01a2168d7581cf96ab1eee86a6fcc063810b`  
		Last Modified: Tue, 01 Feb 2022 03:43:22 GMT  
		Size: 58.8 MB (58816828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2d05fa06c369f8aa3f653d3492090a8788808916b00744fc79157ab1ec3cfb`  
		Last Modified: Tue, 01 Feb 2022 03:43:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
