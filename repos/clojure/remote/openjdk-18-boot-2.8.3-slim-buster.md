## `clojure:openjdk-18-boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:fe8f2e905f615f14eba387a6db019f2f59c917b3b6f67a7a135b52e4951af2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:10d58149b9073cc62a1d8543cf7cdc2a0507136c7fee5fcf67277d11c98fa86a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277754262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a1e61fb43761186fa5a9d90ebe6570aa31b0674794aa9ebabd629b4db0b009`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:15:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:15:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 28 Sep 2021 09:15:24 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 09:15:24 GMT
ENV LANG=C.UTF-8
# Sat, 09 Oct 2021 00:52:34 GMT
ENV JAVA_VERSION=18-ea+18
# Sat, 09 Oct 2021 00:52:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='425b4f9afe439b4690593e5f78e27b6687525114a66f652c285a7dcca95b1961'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='af5b0d66cf7c4f7450066fd67dbb0d48c17bcc5ab8ddb105cf7fe66176427f87'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 09 Oct 2021 00:52:54 GMT
CMD ["jshell"]
# Sat, 09 Oct 2021 01:33:02 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 09 Oct 2021 01:33:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 09 Oct 2021 01:33:02 GMT
WORKDIR /tmp
# Sat, 09 Oct 2021 01:33:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 09 Oct 2021 01:33:07 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 Oct 2021 01:33:08 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 09 Oct 2021 01:33:50 GMT
RUN boot
# Sat, 09 Oct 2021 01:33:51 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49190af1e362ddee7f9a92cbf321a9b1444ccbc631019b5ebcc582e4ef2ec3e9`  
		Last Modified: Tue, 28 Sep 2021 09:35:40 GMT  
		Size: 3.3 MB (3269563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258c0cb75d8406288efe2acc907913d091aafbe66e5837cbcf0e724b46db792a`  
		Last Modified: Sat, 09 Oct 2021 01:02:50 GMT  
		Size: 188.2 MB (188238101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b667bf7f6e0e1909cf39a561aee183a62d50c05bb7cec911b397fd84b0235bc3`  
		Last Modified: Sat, 09 Oct 2021 01:42:15 GMT  
		Size: 279.8 KB (279756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91499ac76f27aceefb2be2bb9b659962fc78c15f3caede9e25aa02e3170e2a7`  
		Last Modified: Sat, 09 Oct 2021 01:42:18 GMT  
		Size: 58.8 MB (58820848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89d72f0138853421ab7e52fdf0298ec2b15cfd523dc0ccf1471e8bde5ed627ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275295881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70137b4ca06cc5655b74e6e91b357d308f1d07cd6913702c3ed0a18a555f07b6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 05:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 05:43:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 28 Sep 2021 05:43:46 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 05:43:46 GMT
ENV LANG=C.UTF-8
# Sat, 09 Oct 2021 01:21:22 GMT
ENV JAVA_VERSION=18-ea+18
# Sat, 09 Oct 2021 01:21:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='425b4f9afe439b4690593e5f78e27b6687525114a66f652c285a7dcca95b1961'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='af5b0d66cf7c4f7450066fd67dbb0d48c17bcc5ab8ddb105cf7fe66176427f87'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 09 Oct 2021 01:21:35 GMT
CMD ["jshell"]
# Sat, 09 Oct 2021 01:59:03 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 09 Oct 2021 01:59:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 09 Oct 2021 01:59:04 GMT
WORKDIR /tmp
# Sat, 09 Oct 2021 01:59:08 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 09 Oct 2021 01:59:09 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 Oct 2021 01:59:09 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 09 Oct 2021 01:59:32 GMT
RUN boot
# Sat, 09 Oct 2021 01:59:32 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f844c3c3d3fdf0c62ff77a82ed24a2a010ad55e3206255c75275457b868825`  
		Last Modified: Tue, 28 Sep 2021 06:06:17 GMT  
		Size: 3.1 MB (3119080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ea9d6faeaa3671b30c5a07dc27383c38d7a3d334fc6d4e0968b3fcdc331be6`  
		Last Modified: Sat, 09 Oct 2021 01:37:43 GMT  
		Size: 187.2 MB (187161723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0142d7940fe680e7ac1aca9f9bc82fed00a17d905ebb5ed356b1eac128b97e57`  
		Last Modified: Sat, 09 Oct 2021 02:12:08 GMT  
		Size: 279.6 KB (279591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdaac66a7d9e09a7d8a0833db3ebc2603527bac19e48c45fcd40f12f80798e83`  
		Last Modified: Sat, 09 Oct 2021 02:12:13 GMT  
		Size: 58.8 MB (58820448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
