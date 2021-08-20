## `clojure:openjdk-18-boot-buster`

```console
$ docker pull clojure@sha256:9a0653c6ffe7c72b879bbaf9373593c05fadc4d76b15f9c2369fc56c8879fd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-buster` - linux; amd64

```console
$ docker pull clojure@sha256:a0d1c9ddb4d685e08fd5785207dbfd81b299ae6f20dacd1d49315c3935abc85c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.5 MB (380457148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860dd3269dd451f50d90697d93b219a952cda1d3e1804d4ef9ff96907df77db8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:20:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 09:21:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 07:03:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 18 Aug 2021 07:03:15 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 07:03:15 GMT
ENV LANG=C.UTF-8
# Thu, 19 Aug 2021 22:29:04 GMT
ENV JAVA_VERSION=18-ea+11
# Thu, 19 Aug 2021 22:29:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='593243ad4eb9339cec9d7675ff01fb4d7b816c1b1f68d4e54d0dc4f99d8f55f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='8efa12ef6e1acab1a4cc5dba5a45dcb828fa0265e409cd0cf2e8e9eec4ad8f0f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 19 Aug 2021 22:29:15 GMT
CMD ["jshell"]
# Thu, 19 Aug 2021 23:09:52 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 19 Aug 2021 23:09:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 19 Aug 2021 23:09:53 GMT
WORKDIR /tmp
# Thu, 19 Aug 2021 23:09:54 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Thu, 19 Aug 2021 23:09:54 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 19 Aug 2021 23:09:54 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 19 Aug 2021 23:10:18 GMT
RUN boot
# Thu, 19 Aug 2021 23:10:18 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4099a935a96edef1e9378de34e314d07fb3aea1b7205774055a1fa44a3819f4`  
		Last Modified: Tue, 17 Aug 2021 09:30:37 GMT  
		Size: 7.8 MB (7833079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2960d83651b1494b4da6c97686e79cc760aa90a75948eed56786726f86928`  
		Last Modified: Tue, 17 Aug 2021 09:30:38 GMT  
		Size: 10.0 MB (9997209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffd4e6385927b79e4d4daa2d00523e766502eed6dd1934e1eda583d348abd8b`  
		Last Modified: Tue, 17 Aug 2021 09:30:58 GMT  
		Size: 51.8 MB (51841042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b08ee8efd6a18f94b99c86dc6397c94dfe2940b06244f88b90d3bbba2ac2e`  
		Last Modified: Wed, 18 Aug 2021 07:09:09 GMT  
		Size: 13.9 MB (13921228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b03a35a10aa84723fe76e0abbac5ac58371b0dfc31b74af69932b60f6f7afa`  
		Last Modified: Thu, 19 Aug 2021 22:35:26 GMT  
		Size: 187.6 MB (187600910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b8ac99054919af8d768a6570059dbdf3e2c9e65048ea6e254eee3fad8c9d31`  
		Last Modified: Thu, 19 Aug 2021 23:14:44 GMT  
		Size: 6.9 KB (6921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0ff014ccd06595b6d63e38d27ed4795fc00568b2abd41fe14d77dc179e51b4`  
		Last Modified: Thu, 19 Aug 2021 23:14:47 GMT  
		Size: 58.8 MB (58820558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d31be480accafc2327e42e3b61b1e624a3cc2e401446f33a97944b26e21c05d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378908391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6bc73ad7b26c9840f89e5d2ed3984e4576cdbe160e32e2274fc2f18d9b151e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:16 GMT
ADD file:9e7d801ba29c50f7388cf80395faef75e0b4db056e16d1117293539bda895467 in / 
# Tue, 17 Aug 2021 01:46:16 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:53:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 07:53:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 07:54:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 03:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 03:06:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 18 Aug 2021 03:06:43 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Aug 2021 03:06:43 GMT
ENV LANG=C.UTF-8
# Thu, 19 Aug 2021 20:41:35 GMT
ENV JAVA_VERSION=18-ea+11
# Thu, 19 Aug 2021 20:41:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='593243ad4eb9339cec9d7675ff01fb4d7b816c1b1f68d4e54d0dc4f99d8f55f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='8efa12ef6e1acab1a4cc5dba5a45dcb828fa0265e409cd0cf2e8e9eec4ad8f0f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 19 Aug 2021 20:41:44 GMT
CMD ["jshell"]
# Thu, 19 Aug 2021 22:35:40 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 19 Aug 2021 22:35:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 19 Aug 2021 22:35:40 GMT
WORKDIR /tmp
# Thu, 19 Aug 2021 22:35:41 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Thu, 19 Aug 2021 22:35:41 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 19 Aug 2021 22:35:41 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 19 Aug 2021 22:36:00 GMT
RUN boot
# Thu, 19 Aug 2021 22:36:01 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b721438f56fc7c4bf10a9f9ac58d22b52d97c50353a44f531fb5b7a70314e642`  
		Last Modified: Tue, 17 Aug 2021 01:53:52 GMT  
		Size: 49.2 MB (49222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268ad76519936dc02d53171a3a4ca6eea0fc0b8a93e97cde6138071fe0422825`  
		Last Modified: Tue, 17 Aug 2021 08:02:23 GMT  
		Size: 7.7 MB (7695203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c93fd903c94bd33e20edef5822d935ca9efd856e0b3d41b0849c1df8ac81a09`  
		Last Modified: Tue, 17 Aug 2021 08:02:24 GMT  
		Size: 10.0 MB (9984343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0eab8670a99c796e5d1a5613581de4cf56c052c3ff83593ca70565c7c45683`  
		Last Modified: Tue, 17 Aug 2021 08:02:43 GMT  
		Size: 52.2 MB (52167867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ed51ddf3297ab19b10c82281594f0c6df9c6fc34f05e952ec2ae05b89314c1`  
		Last Modified: Wed, 18 Aug 2021 03:17:55 GMT  
		Size: 14.7 MB (14673573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74b228ab245518a68c2aa24dea378fee779db31a07ed570bfdcd6e76bb871cf`  
		Last Modified: Thu, 19 Aug 2021 20:53:08 GMT  
		Size: 186.3 MB (186337668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b81e101e4a08541dba5843b3be188e87f8e575c24b98b1cae1fabce70aee82`  
		Last Modified: Thu, 19 Aug 2021 22:42:18 GMT  
		Size: 6.9 KB (6923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ca26525aa947bbe948d8cbf11a27dd97024cac483376bbe4c01faafb5085b3`  
		Last Modified: Thu, 19 Aug 2021 22:42:23 GMT  
		Size: 58.8 MB (58820452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
