## `openjdk:26-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:761a9c242bda520c7dce57ed631d5cb0ae1d73a8e175446ba9e58fdc4e6a43f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:727f3b7c1e5ef3df681943d426752cb138edc5dd97e975c968ad17e274fbc02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.8 MB (381803738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8faaf244eefb66970a685114656b621026d921497250d1a15ea233864d260f0b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:44:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 30 Dec 2025 02:44:28 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:44:28 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 02:44:28 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 30 Dec 2025 02:44:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 02:44:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858b7813255a9cb57d05f02b50978e5b5965b0cfc040288fa29905cdc65ad9a`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 64.4 MB (64396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d4fb1d4c76fcdb906e98b265a6ee4da576c551147d8ea96b138f8b4029f3d5`  
		Last Modified: Tue, 30 Dec 2025 02:45:04 GMT  
		Size: 16.9 MB (16944651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd2a50885dfd94aadcbf8bad69bfafac0a3e91a4cc273e2cb59158b8129a5c3`  
		Last Modified: Tue, 30 Dec 2025 02:45:09 GMT  
		Size: 228.0 MB (227952857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a376b8a789b6b9adea3c708a2b4256c90b97e2ed9f24eb422e7008feadd8416d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800d01722130984d944c85ec019755dcc582444a956ac033ee1c8b2d72371e3d`

```dockerfile
```

-	Layers:
	-	`sha256:670b7bb8cfcc73593e9504fb5c58eea870a2c283c14803344fb4202483fdfe07`  
		Last Modified: Tue, 30 Dec 2025 04:23:58 GMT  
		Size: 8.7 MB (8668236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb88f34e886c8b71d31ad5a3e7f60d4f17218114b7d011327b4f79f0235ad976`  
		Last Modified: Tue, 30 Dec 2025 04:23:58 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ef4c6afb8dca58aa7171a4c2f487216352073cf38821e865c130b7200a476f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.9 MB (379917547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6ea6451bb3e3ccd1a949892900fd42cf4499d9b970ed3888d122c96b6d005f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:42:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 30 Dec 2025 02:42:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:42:17 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 02:42:17 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 30 Dec 2025 02:42:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 02:42:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0f830954e4032c2c8131a98736d62914df466de0582c1b613910232ab43fe7`  
		Last Modified: Tue, 30 Dec 2025 02:42:55 GMT  
		Size: 17.7 MB (17728350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a3f13925fdafff37302051fda9c8abbf52bc89c88b63e04f1641fc0478f3a5`  
		Last Modified: Tue, 30 Dec 2025 02:43:01 GMT  
		Size: 225.9 MB (225860502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ea1446d3ccc3d4bf9241244f8672f2fa0e0f0bed2cd6d1914b6715282abdf3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ac3e1910ef81414252943ee140584de69ceb90c9461bc9362f471e0317f3bd`

```dockerfile
```

-	Layers:
	-	`sha256:9b319a51c08b76bce6c85bd1c5b37d76c06db845c0e4baf703a3bef5a2e66356`  
		Last Modified: Tue, 30 Dec 2025 04:24:05 GMT  
		Size: 8.8 MB (8805081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7811f6415aeb94fe117eb81ebb2f5fed6f5868a3d8092cfd58fb12decc6562e8`  
		Last Modified: Tue, 30 Dec 2025 04:24:06 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
