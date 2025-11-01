## `openjdk:26-ea-22-jdk-bookworm`

```console
$ docker pull openjdk@sha256:c9319dfe023fca23d38305cc2d5f5e89a800cb99dedde6ab9d12d235d8f0e904
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-22-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8796092f31c0e7960a8b25d0d9b91b93c075b560c604f4e82ba84d134ddb09ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 MB (379764586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51134019225369f67834c22cc10384a7e9bf50467018936375bf7e709099c4e4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:29:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:29:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 31 Oct 2025 20:29:45 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:29:45 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:29:45 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:29:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:29:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8958db98e70e74768068ebc61b717e6650a5a7b990c5759d4e362979edaa2`  
		Last Modified: Fri, 31 Oct 2025 20:30:29 GMT  
		Size: 16.9 MB (16943686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8a533a955850b01b394bca6fe055dc945d651cc864bef54602b87f6b5d8a79`  
		Last Modified: Fri, 31 Oct 2025 22:02:58 GMT  
		Size: 225.9 MB (225915034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b4c40fa18b2c960e97d503356262f4fb84c92bdd9becc7939095a3c389ee1e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8688036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a058d34d698404aab0d3a4fce0e9d6ee8919c31c00bd93317d50e7a7a7a8985`

```dockerfile
```

-	Layers:
	-	`sha256:4a507615c456e033b9e177ce7ddb98ca1d32d1083bf9b6e1bc9626d549186f6e`  
		Last Modified: Fri, 31 Oct 2025 21:23:36 GMT  
		Size: 8.7 MB (8669461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb4a6ad8cc53e947e5dde5ff0a7c7f4340361b063834ca14dc67c0237a6bc783`  
		Last Modified: Fri, 31 Oct 2025 21:23:37 GMT  
		Size: 18.6 KB (18575 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-22-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:083a8c73dede0dbd1206026e818d19dfe4a53ad78c9749f78ff31697cff50850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377823838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a7b30a2a1f6595a9917e87cefcb896f408e892e84ee77d4bd19b273554d8ec`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:10:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:10:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 31 Oct 2025 20:10:35 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:10:35 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:10:35 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:10:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:10:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0ea05bd7174a18ac3895ea91a48961fb104f855d052d8f4d03b8f86ee6c001`  
		Last Modified: Fri, 31 Oct 2025 20:11:24 GMT  
		Size: 17.7 MB (17727736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1fc2d99a325b3e57282656740371b84e9f5ab4a5b4c5c5290de62ca9665452`  
		Last Modified: Fri, 31 Oct 2025 22:01:53 GMT  
		Size: 223.8 MB (223768184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:6d42b34a0dc2315baa8b3dce8660532dc7739327002bdda397dd6b6ed7db0384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8825048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7078e389cf2152353a7e063f1f476da63594d9850e15f2e0b3b317315d56f194`

```dockerfile
```

-	Layers:
	-	`sha256:06a6663c2dfe2f3c932861ec7ef28ba0d47e1272fbf3c0e4796dcd29090f2ac3`  
		Last Modified: Fri, 31 Oct 2025 21:23:45 GMT  
		Size: 8.8 MB (8806330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c2c98c8b704dac431473bc71b77df845d9f6c631303ba0ee3c5888c1b92adf`  
		Last Modified: Fri, 31 Oct 2025 21:23:46 GMT  
		Size: 18.7 KB (18718 bytes)  
		MIME: application/vnd.in-toto+json
