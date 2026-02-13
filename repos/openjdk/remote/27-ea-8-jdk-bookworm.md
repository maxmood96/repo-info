## `openjdk:27-ea-8-jdk-bookworm`

```console
$ docker pull openjdk@sha256:16fe94665046103f7e12d68a1f297d0a9f245e234b449156dc4c7facb1c0196f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-8-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:647297f34cd94c9ada5276f17a3c423cfb43aace32d4ac08224a41b747df73cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.3 MB (382298424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529dee89d158c9d76694126d6639f7339a200fb81b46b23ce322cf0ebdd57730`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:01:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:01:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 13 Feb 2026 00:01:40 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:01:40 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:01:40 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:01:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:01:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efebe96a2119f14fc904cd389de93119a6814e3be8b294c68622581aae2a0ea0`  
		Last Modified: Fri, 13 Feb 2026 00:02:04 GMT  
		Size: 16.9 MB (16944847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334c355cbd7c3ddd53215dadb76b37aee2bbe90253534156e270d3271313769f`  
		Last Modified: Fri, 13 Feb 2026 00:02:08 GMT  
		Size: 228.4 MB (228437677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-8-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:78a7e6c04de59b8830ef0849dacf10d13a0ee88c68093e86abc85748c0ee8e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c8730ee5e38c1f3c95edbf991e7c40bb7eb9b89f77f3c2d743c9bf3be37a99`

```dockerfile
```

-	Layers:
	-	`sha256:20114ae3b99364c90d0b6687c1d6e6aa9418c315edf6845f0eaf79c451a53b04`  
		Last Modified: Fri, 13 Feb 2026 00:02:04 GMT  
		Size: 8.7 MB (8668250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d81d5eca4097905e7afd49f0e8bc72757063d6717305be950363c9f1c4df3a4f`  
		Last Modified: Fri, 13 Feb 2026 00:02:03 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-8-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:02aa21dba47604e32a7c0a9c6a5d7f8a975396fec938bd8491a72eb59ed5e953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.5 MB (380548311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16735e06d6908adfe4a1e7aace35e9cc40322648d838e545555df8f6652e73e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 13 Feb 2026 00:02:51 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:02:51 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:02:51 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:02:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:02:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bed88fa10839f20d74ac80e484e672f1620c530d35452cd181dbff554ee36f`  
		Last Modified: Fri, 13 Feb 2026 00:03:17 GMT  
		Size: 17.7 MB (17728489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ddc685d67cca1a45a286bae5db21c60bb1cf82a9f97afaf90a55de51b5bb4b`  
		Last Modified: Fri, 13 Feb 2026 00:03:21 GMT  
		Size: 226.4 MB (226369337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-8-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9efd132c5a529d1e26e89d8a8414c70bb459d4e59b2cc4f44d52cfcd1d1a83a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2276737ffcfc75d45fb406edf70b1e7164274de481b157bf8f98b2c547bfd3c4`

```dockerfile
```

-	Layers:
	-	`sha256:062e2d1e2ba8fcb562bf9f7587dba39d93395eeb660a52ab8880f19bda8d65d0`  
		Last Modified: Fri, 13 Feb 2026 00:03:17 GMT  
		Size: 8.8 MB (8805095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e50c6ec20258b4df16c6e3d07a9cf5fdf57d06c7518200f1b24fd02e0ec131fa`  
		Last Modified: Fri, 13 Feb 2026 00:03:16 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
