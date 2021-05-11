## `clojure:openjdk-17-boot-slim-buster`

```console
$ docker pull clojure@sha256:56c5bdb1412538101fa5c29015a4f5dbdee1b83a900123cc4e9b0bed7a9690ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:7b90e409b606ff4a9a6d55acc661b00f903b7177869e1ee509748bdfa6c1e97f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275910135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09934a232a7b1544b772e24b40492b0902351803ee3f89a790d86e3bfb99466`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:44:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 12:44:50 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 12:44:51 GMT
ENV LANG=C.UTF-8
# Tue, 11 May 2021 00:15:34 GMT
ENV JAVA_VERSION=17-ea+21
# Tue, 11 May 2021 00:15:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2a923efe7bd6c682d5550551a16dadfe8057b0106e0b4b4aad2aa56b8bed4c19'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb389fe6915c9e70e639db6ab630342a5ccc275f5a06aaded43321eeea9ba6ee'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 May 2021 00:15:53 GMT
CMD ["jshell"]
# Tue, 11 May 2021 01:28:53 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 11 May 2021 01:28:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 11 May 2021 01:28:53 GMT
WORKDIR /tmp
# Tue, 11 May 2021 01:28:58 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 11 May 2021 01:28:58 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 11 May 2021 01:28:58 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 11 May 2021 01:29:32 GMT
RUN boot
# Tue, 11 May 2021 01:29:32 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf4c47c8c6124c3089f3ed26410da9870ba18dd4bc68331e2b7e853116a6cad`  
		Last Modified: Sat, 10 Apr 2021 12:54:28 GMT  
		Size: 3.3 MB (3268764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb80c72a96b420bbf07f0cdaeaaab1859c2f04cec313dc4312e8107eca41433`  
		Last Modified: Tue, 11 May 2021 00:23:07 GMT  
		Size: 186.4 MB (186401638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c24957159b796fbbaf6eeac0b22f91ec7ceee7b401e962ad55eb009a548099`  
		Last Modified: Tue, 11 May 2021 01:33:51 GMT  
		Size: 279.7 KB (279695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f7d8ea7cfc276b707feaba344faed42cff4f1a17076439ea95a275b393bbe7`  
		Last Modified: Tue, 11 May 2021 01:33:54 GMT  
		Size: 58.8 MB (58820665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0a19e450a757483556df22451ac60929b74cf1cb5f8ca91da2c7a1515f9c1a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270605524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739782b4833423a411cf2793fe8939e643405b4bcc5081d46dfafc140b18c05b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:25 GMT
ADD file:b24da7eb23eeae04e00d0e45da29a89fe8f992e8dcf4ba482afb907b8015b7bf in / 
# Sat, 10 Apr 2021 00:41:28 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:31:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 01:31:15 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 01:31:16 GMT
ENV LANG=C.UTF-8
# Tue, 11 May 2021 01:46:12 GMT
ENV JAVA_VERSION=17-ea+21
# Tue, 11 May 2021 01:46:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2a923efe7bd6c682d5550551a16dadfe8057b0106e0b4b4aad2aa56b8bed4c19'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb389fe6915c9e70e639db6ab630342a5ccc275f5a06aaded43321eeea9ba6ee'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 May 2021 01:46:41 GMT
CMD ["jshell"]
# Tue, 11 May 2021 02:40:18 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 11 May 2021 02:40:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 11 May 2021 02:40:20 GMT
WORKDIR /tmp
# Tue, 11 May 2021 02:40:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 11 May 2021 02:40:31 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 11 May 2021 02:40:32 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 11 May 2021 02:41:07 GMT
RUN boot
# Tue, 11 May 2021 02:41:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:15cb40b9c4df1a06940dc2a154c3be46844241235c1a091afa70da0ee2dc811a`  
		Last Modified: Sat, 10 Apr 2021 00:47:53 GMT  
		Size: 25.9 MB (25904582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ed82b9f1018dd9b8a3d8ed771ba8773bd33481ce655abab47d10bd3034f05`  
		Last Modified: Sat, 10 Apr 2021 01:37:31 GMT  
		Size: 3.1 MB (3118914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11d8fd64baec0ee00d154286dee2bd77466e042e6aab4916de26401821337c8`  
		Last Modified: Tue, 11 May 2021 01:53:12 GMT  
		Size: 182.5 MB (182481831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d352fe099b68aff8f8bcbb3980714d6028149e33cea8f2bd4b3b0e84029a2e`  
		Last Modified: Tue, 11 May 2021 02:45:06 GMT  
		Size: 279.6 KB (279614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b96746201522552d9468c66a51861fa9d00c5fdfdf4e9244da825e39e48204c`  
		Last Modified: Tue, 11 May 2021 02:45:10 GMT  
		Size: 58.8 MB (58820583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
