## `openjdk:26-jdk-bookworm`

```console
$ docker pull openjdk@sha256:2841664c999db80684ba551bd2e2d56d7741dbe893abe7fc0458d0bcc8fc94ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:7829a023c3e67f2408b87f5ca46b9f2fddb2963bc1147ec8ece3aef753f43f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.3 MB (377280667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c895676bfcc20b65e17bfe7efb472c3ac320dcdae24e8bfcd89d761cf8f0e6b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 12 Sep 2025 18:48:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 18:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_VERSION=26-ea+15
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d8fa7cffcc38d68ed218fa285958e163c48a9b0d5c968c0c8859cc0a36e0baa0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='955e3af91d63b89cb5eecc00503ca439d96a9d2cf645e38e4079ed65c5486ff2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5073558d5a5274440fddfe987f56645dc90b8b84481e9e3dc858ac3311e33e`  
		Last Modified: Mon, 08 Sep 2025 22:13:51 GMT  
		Size: 64.4 MB (64396915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccd34a1b095cef11eafa0313b987a89e62054c0f3edc7908ab05807b627ced0`  
		Last Modified: Mon, 15 Sep 2025 16:58:05 GMT  
		Size: 16.9 MB (16943606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a794300a64b1abab7d4012e5597b35ca24556b8155fb85f3b3a27b3b5603d8`  
		Last Modified: Mon, 15 Sep 2025 18:42:01 GMT  
		Size: 223.4 MB (223433540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f2fd4b2c84cdac0e2671d8ae1c3d9c0b1b514ab29fb8451fcb3e5510b578bef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8689956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deadb2982d1be9184538877825b03f39b479b6d5f6a60f780485b56ec9c1c281`

```dockerfile
```

-	Layers:
	-	`sha256:91bc46a833c48569c5a3ce23071ee9c2131a418143d3b80c290f402724edd1f6`  
		Last Modified: Mon, 15 Sep 2025 18:24:05 GMT  
		Size: 8.7 MB (8671339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c555803a67bdde7f43860b2fbb0f06188315c00ea32832a6513a38946c71b6`  
		Last Modified: Mon, 15 Sep 2025 18:24:06 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0d32cf7b911621007abc119c63939a1f04a70d83fc564f17bcb401acfa8990d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.3 MB (375325358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867715178c8615ffcaa50c658a3f1c8c0f2b4f15543c456204cb0125f117721a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 12 Sep 2025 18:48:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 18:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_VERSION=26-ea+15
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d8fa7cffcc38d68ed218fa285958e163c48a9b0d5c968c0c8859cc0a36e0baa0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='955e3af91d63b89cb5eecc00503ca439d96a9d2cf645e38e4079ed65c5486ff2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133142790bc081eb3e5455996df5c3f98df543c5a224c3643437a19d4d6a7d93`  
		Last Modified: Tue, 09 Sep 2025 02:12:12 GMT  
		Size: 64.4 MB (64371181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b594ed1a9ad2712ed0c002f568515520a3b29257b0e407f9cca36952f3ae77`  
		Last Modified: Mon, 15 Sep 2025 16:57:57 GMT  
		Size: 17.7 MB (17727715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd8302379a3e63e7734e6f9c604fbd31eb2863157488d90a523172cc8c3a618`  
		Last Modified: Mon, 15 Sep 2025 18:42:22 GMT  
		Size: 221.3 MB (221272654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:08c89af6a9912e047164836e7f7c92d3ba4c7988fac2cdfa9a9684fb526fc6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8826969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803686267ac6aa275b78c4974a4ed2c381d7a83cddf661b67d419e5d3f16cbbf`

```dockerfile
```

-	Layers:
	-	`sha256:aff13cedcab121aefc7992f0f72e8e5f1a8bb6107aa88cbf5e1aaa0363926a81`  
		Last Modified: Mon, 15 Sep 2025 18:24:15 GMT  
		Size: 8.8 MB (8808208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc97b21318108de868c15438c33d43ec41312dfdc11ee430b8acabeaf48f767`  
		Last Modified: Mon, 15 Sep 2025 18:24:16 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
