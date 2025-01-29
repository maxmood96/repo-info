## `openjdk:24-bullseye`

```console
$ docker pull openjdk@sha256:1664694507b8a09587be5127016ed1b1c0a663b5473418e332a104aacba43938
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:aa619df6caf01465537ddf3542c4219144da19b26210105edb21630c4e76d251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (351007303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2191cd0d8c6ff78ea5e6e7d27d0846b9dd136ac974afe292e086255a7f1d1d15`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d363a1dd2d1714709c84ac8d050f51e921efc51885c202b336cc24f61e3186`  
		Last Modified: Tue, 14 Jan 2025 03:18:11 GMT  
		Size: 54.8 MB (54753534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46f2a556686de9bb3e8dac35f569b759fead52ead2c28384f0f46fb55a54520`  
		Last Modified: Tue, 28 Jan 2025 23:28:23 GMT  
		Size: 14.1 MB (14071349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e3742aebeb964780fcff9d68c69bcdce518f723fb18007e8e19ecaa9a27330`  
		Last Modified: Tue, 28 Jan 2025 23:28:26 GMT  
		Size: 212.9 MB (212884894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:eb86bb71d9b5dc0bb9298dd40bc0d4ccff766eebd5c303ac654a970304c34be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8383402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aef85b89649739fb386a3328bf308eea46fff9cbd92c0fcf026418385a4bc02`

```dockerfile
```

-	Layers:
	-	`sha256:30a07b4f52363dc768467de6a494d8dfe537d49b21201b5b797464cf57223c0e`  
		Last Modified: Tue, 28 Jan 2025 23:28:23 GMT  
		Size: 8.4 MB (8364785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9912f8946b1e2bea8c0733ee5a3a52a427cf0e15096cc62f943ef0f561e48546`  
		Last Modified: Tue, 28 Jan 2025 23:28:22 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f672721a642322289f6ecbad634ad871d26b3679576ebe590c13503636c339a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349017005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e59999248ee4ebc9c4a01dadfd38421676cefa12d1e579efaea40a0d4220f88`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d131bb45427773e6afabd46e2adb4b244b25d4dabe87133f23082bb3234e33e0`  
		Last Modified: Wed, 22 Jan 2025 02:33:12 GMT  
		Size: 15.5 MB (15526310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30f86c894139a6debc1f5c8830e9ab263817ff018e41aa221151fb3d5c5a514`  
		Last Modified: Tue, 28 Jan 2025 23:41:27 GMT  
		Size: 210.8 MB (210847940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2cf2ac78274dd5d371ebb1a9d1af42e722202e5947f3e167bb5973d53afb1ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8484508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b545cde25a25e7fe3abb31c40c35310c32da2d68f78ead269b3bc1204c83a94`

```dockerfile
```

-	Layers:
	-	`sha256:61bd4c759596991d04df560318171deb6acf5d99387f67984adf0f6c7bb50578`  
		Last Modified: Tue, 28 Jan 2025 23:41:23 GMT  
		Size: 8.5 MB (8465747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ee3bf98d15efa188ef6aade0ad89dc76c170d549500ed1088b4db3c2ab26cf8`  
		Last Modified: Tue, 28 Jan 2025 23:41:22 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
