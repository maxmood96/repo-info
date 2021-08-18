## `clojure:openjdk-18-boot-buster`

```console
$ docker pull clojure@sha256:ec597a4ad93b28a295b1cd7c4bbc70b28065b4026d9aa993d8b0c7e6f1a4d99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-buster` - linux; amd64

```console
$ docker pull clojure@sha256:5d9c8f600decdc0dce1a92be59b1922938945bfbb2d4145043dd5e5e7a103e39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.4 MB (380431298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5796fcdaa329afc4898973e3f1d85a57a1fc06547b587b3795a9ff7a6a51e8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:12:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:12:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 13:33:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 13:33:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 22 Jul 2021 13:33:13 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 13:33:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Aug 2021 17:27:04 GMT
ENV JAVA_VERSION=18-ea+10
# Fri, 13 Aug 2021 17:27:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='f02c5e52c193b349688216e85ab6fb67548861e93d96dd454f74881abfb696b2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6a6ba79485e560d0d7687152a2a1dfa92cbe80871f16eb24b52e01274f9f4f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Aug 2021 17:27:15 GMT
CMD ["jshell"]
# Mon, 16 Aug 2021 20:24:43 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 16 Aug 2021 20:24:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 16 Aug 2021 20:24:43 GMT
WORKDIR /tmp
# Mon, 16 Aug 2021 20:24:44 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Mon, 16 Aug 2021 20:24:44 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 16 Aug 2021 20:24:45 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 16 Aug 2021 20:25:04 GMT
RUN boot
# Mon, 16 Aug 2021 20:25:04 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040670e5e559fd936db175530ad4c1dd014bd25b2bf25ea19fa20554fe2d736`  
		Last Modified: Thu, 22 Jul 2021 01:19:54 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073a180f4992853fa3dd8da604e7b041bc8ea92157749d042c0853312f178f6a`  
		Last Modified: Thu, 22 Jul 2021 01:19:54 GMT  
		Size: 10.0 MB (9997222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf76209566d0c8d78df205b09e6e5b52ff7f10cb4e1c03d9336ed7dd2decd919`  
		Last Modified: Thu, 22 Jul 2021 01:20:16 GMT  
		Size: 51.8 MB (51841203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4de66c57277180420b7663842bf72269ceeb8ddb3b87e83d9d5a4b708ac740`  
		Last Modified: Thu, 22 Jul 2021 13:43:09 GMT  
		Size: 13.9 MB (13921248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf28cbe84e179afe37b71e900696a26c014994de5713503c8da37ccc9d95fc7`  
		Last Modified: Fri, 13 Aug 2021 17:33:17 GMT  
		Size: 187.6 MB (187575629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a943f5f59bb2f9bc5c172ebb20926da27bbce757034d4e271cc9a21847067`  
		Last Modified: Mon, 16 Aug 2021 20:31:39 GMT  
		Size: 6.9 KB (6923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e87e78ccef8c600d2af8c3a2fb8e8406a1fa9435b4d8cbdd0bf179dd32b4b82`  
		Last Modified: Mon, 16 Aug 2021 20:31:42 GMT  
		Size: 58.8 MB (58820503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9ae771fe858c9a2494f1f3a4cb33f03328bcde3ed5c991e6dda53bceea427e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378900847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f03a471ad5f0fc4805e6322efbd63585270c254c74ed1f8923d06f3260818f`
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
# Wed, 18 Aug 2021 03:06:43 GMT
ENV JAVA_VERSION=18-ea+10
# Wed, 18 Aug 2021 03:06:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='f02c5e52c193b349688216e85ab6fb67548861e93d96dd454f74881abfb696b2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/10/GPL/openjdk-18-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6a6ba79485e560d0d7687152a2a1dfa92cbe80871f16eb24b52e01274f9f4f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 18 Aug 2021 03:06:53 GMT
CMD ["jshell"]
# Wed, 18 Aug 2021 10:31:17 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 18 Aug 2021 10:31:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 18 Aug 2021 10:31:18 GMT
WORKDIR /tmp
# Wed, 18 Aug 2021 10:31:24 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Wed, 18 Aug 2021 10:31:24 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 18 Aug 2021 10:31:24 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 18 Aug 2021 10:31:42 GMT
RUN boot
# Wed, 18 Aug 2021 10:31:42 GMT
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
	-	`sha256:8d7a1041bc23edfae4d0ab54b43cdf5f38213f37e4e5d928a57bbb7f704a38e0`  
		Last Modified: Wed, 18 Aug 2021 03:18:10 GMT  
		Size: 186.3 MB (186330282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca265694ac86bae93fceed24340a886611ab99c5e563fc2d57958e670a6b24f`  
		Last Modified: Wed, 18 Aug 2021 10:40:06 GMT  
		Size: 6.9 KB (6922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454fd3ba0ef12dba2b66cdf4a968bbc5eafcb01eb93484f77e9bd49f7c39e15e`  
		Last Modified: Wed, 18 Aug 2021 10:40:10 GMT  
		Size: 58.8 MB (58820295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
