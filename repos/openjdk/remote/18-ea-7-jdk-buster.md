## `openjdk:18-ea-7-jdk-buster`

```console
$ docker pull openjdk@sha256:cf9884e2ce93348bba67dfce4c7f2bf38f2b68f77ef77a88bab87f393fd403ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-7-jdk-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:69be2f92bf7dc0b28d78493e1ec2e4b24646353546af06eb4c1b9a555450b958
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321674590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee937b3ea14f172a34eab32a321260871fb3c2c6bddebed485d47d6bc8e38f`
-	Default Command: `["jshell"]`

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
# Fri, 23 Jul 2021 21:21:04 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:21:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='03f895bdf47691e44e9b269eda74f407715e97385b0cfb60304bcfda29f589a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='bc3dec6f82541afbd83e9b5ba6ae70541206accd7d815dd171fd36c93a90fe3d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 21:21:14 GMT
CMD ["jshell"]
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
	-	`sha256:3c6ae8b7e92c177566f49294374bf7e5273650754c935d820d5489737ea399b7`  
		Last Modified: Fri, 23 Jul 2021 21:27:51 GMT  
		Size: 187.6 MB (187646347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-7-jdk-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:92bcb9f5c687349c2cba1476fe67acd5b4a18ad1704ef9b7a3da08ee40ab7c8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320137776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacf0984bd98c0871d455371fc8b270f1aa305c87df599e864e52f4e845a8f8b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:59 GMT
ADD file:3e8e075f08a6b727602af05c539f43648a48663cbb3a88eeba310cfc32c01d78 in / 
# Thu, 22 Jul 2021 00:40:00 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:16:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 05:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 05:15:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 22 Jul 2021 05:15:12 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 05:15:12 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 21:41:27 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:41:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='03f895bdf47691e44e9b269eda74f407715e97385b0cfb60304bcfda29f589a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='bc3dec6f82541afbd83e9b5ba6ae70541206accd7d815dd171fd36c93a90fe3d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 21:41:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d272b0d8f7c4fd0caf0ef022ce544cfe3800e349a73b585f82837e6526a4247e`  
		Last Modified: Thu, 22 Jul 2021 00:45:18 GMT  
		Size: 49.2 MB (49222109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fabd82f026fa10e0e0341fa3d6d3112de04413ea6c46e72bcc1dca40d924aa`  
		Last Modified: Thu, 22 Jul 2021 01:25:00 GMT  
		Size: 7.7 MB (7694906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0193c0cdceae23cd0e13721651d74f409440171fe8a1c8b521616b6ed29db6e1`  
		Last Modified: Thu, 22 Jul 2021 01:25:00 GMT  
		Size: 10.0 MB (9984335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967a8f1385966af47c9f250997e3158c319d498adc004c91570f770ceac5045a`  
		Last Modified: Thu, 22 Jul 2021 01:25:24 GMT  
		Size: 52.2 MB (52167528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176877461d089b6f2c205b71c8892552af1b56d6cd599f6db980e3275e7f589c`  
		Last Modified: Thu, 22 Jul 2021 05:29:29 GMT  
		Size: 14.7 MB (14673538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942f98b25db62960e9353e5cc63f439d311219bbe88579c79a65243b306a280f`  
		Last Modified: Fri, 23 Jul 2021 21:53:47 GMT  
		Size: 186.4 MB (186395360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
