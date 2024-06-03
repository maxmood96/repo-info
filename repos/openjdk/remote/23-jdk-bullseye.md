## `openjdk:23-jdk-bullseye`

```console
$ docker pull openjdk@sha256:177a02a9d8ab30da72b5a8f859fbaa1329d095d5b54c4d7f65a4ecb90eacd373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:261529d18c9aad89524d23e70d9edca13ae1ad4cfa6cf4a40ae0cb8c0cd64e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350814650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca61f39e00747788a94fe2e4cef564bda952d03aabccd94b1b3bbbafe79fed5b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 31 May 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+25
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='155a1386301d0ac6cd1ce5769b31f550bb400d652f4211454b9988bf25fa173d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b00cd1591ad9727c48c07e598f57cdec15fa40b605ae712b67f35f221534d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9862156c5ba6d6555a4b9081c2005389e1856711085b337ab2d556cd426c521`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 14.1 MB (14072835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee4410891ab3284939b3ff5d27f32ba599369033a09da49d08a59135c456ca`  
		Last Modified: Mon, 03 Jun 2024 19:01:05 GMT  
		Size: 211.3 MB (211287944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:14b5302310f8a45f873f3b2ef3df016f3e00acf4ec5abd60d4d794c1389677eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c675e51362a3eab4af5d977520b17b670630edd026308bf90dc6299195ed0dda`

```dockerfile
```

-	Layers:
	-	`sha256:afea6fa15864c99c653139b206d10c5c2a55e1b9ac0d4e52115e71e677fafab2`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 8.2 MB (8157321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a40c65ee67706b60f495b683077384066593d269dd71271b0b8434df201d053f`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 18.4 KB (18414 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:60e92a783141f6682ed808d485fc26f8168c26522b44b740cceecd6ea3c90e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348187252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bd4974cde5ca3d8caaf2233ca34b199005edb2f26721849b20a91d6df2bf00`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:45:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 24 May 2024 06:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 May 2024 06:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_VERSION=23-ea+24
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 May 2024 06:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691cb555e773cb93573d3bc043d7cf17af1d4819163089dfddab3f4cc971718e`  
		Last Modified: Tue, 14 May 2024 01:53:53 GMT  
		Size: 15.8 MB (15750525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce352085291a4828eefe3a8fe5557c610cb7e308cbe4a56a62e0922171dc1c`  
		Last Modified: Tue, 14 May 2024 01:54:08 GMT  
		Size: 54.7 MB (54696093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d585a8f14175d4efbc32ded99c930a961a2585f0303352d224e14578d00ede37`  
		Last Modified: Thu, 30 May 2024 12:49:13 GMT  
		Size: 15.5 MB (15527075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c93b341606d47ef03ac6ede40c521cb770f001c79e2c939bc2caa2a999bb62`  
		Last Modified: Thu, 30 May 2024 12:49:17 GMT  
		Size: 208.5 MB (208474569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c8ed1b1086fdfe16cf75213847bfc8d63c8022e6805f58e490a69cbe8d408752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c036e32917ddee0ff612a82132480c13c4ae0084fe7f84ad268fd7a8a9bf6569`

```dockerfile
```

-	Layers:
	-	`sha256:3e98cfbfaef32d0c95d2f8efbb7bbc39ef201c8359941162505c4b0c721f968c`  
		Last Modified: Thu, 30 May 2024 12:49:13 GMT  
		Size: 8.3 MB (8259032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f6abee42b29ec8cfa2c33463ceb6e565594ccf20bcde065cf105b8d82fba66`  
		Last Modified: Thu, 30 May 2024 12:49:12 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.in-toto+json
