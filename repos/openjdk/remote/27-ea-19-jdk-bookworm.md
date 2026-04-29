## `openjdk:27-ea-19-jdk-bookworm`

```console
$ docker pull openjdk@sha256:63245e92c6f2668348d3d78424c0f6899621b40b32f88c964d8a0f07aa17bd18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-19-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a4d9e0093a143311e6f987a9b9ad02c5400fae97046f74120f18d6d531d2b372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.4 MB (382421541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba1686cece32b44310b08c819c851a7e3e3e247cd65e1a075aae66cb8c5d048`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:34:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:34:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 28 Apr 2026 23:34:57 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:34:57 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:34:57 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:34:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:34:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcda2b4d7993820b00c5488d173051e76d01ba6b85620617ba77001b0f9e2fa`  
		Last Modified: Wed, 22 Apr 2026 05:12:28 GMT  
		Size: 64.4 MB (64396988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4fda379cb30e35bffbc7902b556e963b28fbe7c7060b43ae61115402fc6a93`  
		Last Modified: Tue, 28 Apr 2026 23:35:24 GMT  
		Size: 16.9 MB (16945770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2609649d48e07f1ca46ab875b3ea9ed840199159d6205db550a817f4d1c2983e`  
		Last Modified: Tue, 28 Apr 2026 23:35:28 GMT  
		Size: 228.5 MB (228547921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-19-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0b3a938536cb81036b0f971f10867219a006dcf3aae4fd35cca60074fdb9f919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8685556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c546f3e0ee31b6e1f07794bbb15ed6d48357a3176fbdb59aa2b38f45930de42`

```dockerfile
```

-	Layers:
	-	`sha256:cb06a273743cdce14136860f9a311465afe9b4a59183a6b217999ea8132046a5`  
		Last Modified: Tue, 28 Apr 2026 23:35:24 GMT  
		Size: 8.7 MB (8667617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a837fb159bdb4fa647328d7b05408c337e69723e1326bd23bcd83c1096d1d2a`  
		Last Modified: Tue, 28 Apr 2026 23:35:23 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-19-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0d1b1eb76f1e2ba0b81870a048267c20bde6371006d337a6da6fb551927317f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380689063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef580f32489b6c867f28786c03099d33d9594992c6da6a4cfaa997c02b9f04e1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:35:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:35:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 28 Apr 2026 23:35:44 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:35:44 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:35:44 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:35:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:35:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee2c0d424adfcb4e7c66e91946116ab34c8ed7f2c3792df96cb0bab759bc193`  
		Last Modified: Tue, 28 Apr 2026 23:36:10 GMT  
		Size: 17.7 MB (17729179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f476be60175ca3cb9d5b3060c41887e482197bf3afd253bd246740324d163820`  
		Last Modified: Tue, 28 Apr 2026 23:36:15 GMT  
		Size: 226.5 MB (226497784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-19-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2853a04e34d17c8ee672e22e5f4ae3147ae08a21889096121037a43d5b4acdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bf185faeb6b5db818fdebcd12c5dc64a56be9ada6e32aba6fc7f43cb890885`

```dockerfile
```

-	Layers:
	-	`sha256:36aac9a5a1a970685600a38e2c4b9cc0eebda5ab89c82e8cb14c84f6604e8299`  
		Last Modified: Tue, 28 Apr 2026 23:36:10 GMT  
		Size: 8.8 MB (8804462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c963d8fcc18224249a57cfd9ef56f76f8edc5843938f456000003c6c68a1dea`  
		Last Modified: Tue, 28 Apr 2026 23:36:09 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
