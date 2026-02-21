## `openjdk:27-ea-10-bookworm`

```console
$ docker pull openjdk@sha256:a0f891930e0af31e1af6c74d492ec1a5b584007969090fa67a693724f31d2cdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-10-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:2cc7c0e9b07dcd0bc23267d124ed505bd02ac657bfa4787a3fd9126bdf5e0595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.4 MB (382365022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913659c195d1f3eae088c7ee3f60283d629c829c4b4f534da8ccbaa614aeb175`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 21 Feb 2026 01:29:49 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:29:49 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:29:49 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:29:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:29:49 GMT
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
	-	`sha256:7047dd5ecdb4943342ba315978d34127c3ebed98f287f6abb38c697a7579eddc`  
		Last Modified: Sat, 21 Feb 2026 01:30:13 GMT  
		Size: 16.9 MB (16945129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5c53016bc8dd8dceda4cd5e6d200691cc455be16289f5227fced519d4c4cfd`  
		Last Modified: Sat, 21 Feb 2026 01:30:18 GMT  
		Size: 228.5 MB (228503993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b8ff429fbaaf60ada1073b1b4d29378e7d59c01d68e01c69c6696737a859186d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208c39f6f3766734da875d18d26479b261a4ce48cce53fa575b14296d38a4c12`

```dockerfile
```

-	Layers:
	-	`sha256:625f8dd8cb29398b12c6996f787de2f1403064f8f1eb87b3ff13bd283f861601`  
		Last Modified: Sat, 21 Feb 2026 01:30:13 GMT  
		Size: 8.7 MB (8668885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec4e1bc588ec38b1257edc1bc6511de2631f684cbce7f6b72dab247a59cb53da`  
		Last Modified: Sat, 21 Feb 2026 01:30:13 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-10-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9c73380e3bc7bb6f243e09a368f09145e78fb93106a56b210b15cbb7bf3cfeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.6 MB (380630313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b33ec16bded90ffe173365ed3b193dd1590a087ef9944657708b5da6865f31`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 21 Feb 2026 01:29:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:29:58 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:29:58 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:29:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:29:58 GMT
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
	-	`sha256:36b6939610282b9f96a411ba5e171b633862b3b39ec7287b629571c424cddad6`  
		Last Modified: Sat, 21 Feb 2026 01:30:24 GMT  
		Size: 17.7 MB (17728963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a4946fcd827555056d5ad3788822293ef07536605581bb29a625515eefa815`  
		Last Modified: Sat, 21 Feb 2026 01:30:28 GMT  
		Size: 226.5 MB (226450865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:33c6ed1baae1b676448b991101fa3b5627557c8b3376f3fef03e070943b07b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba824a9d56a866f514a03b3c5ee7978016a5fc2796e2aae2259a4d1cc22589e`

```dockerfile
```

-	Layers:
	-	`sha256:198cc752c6674af29db1643322a1863e246421cb960ddfe57faddd76f08918ae`  
		Last Modified: Sat, 21 Feb 2026 01:30:24 GMT  
		Size: 8.8 MB (8805730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d58a1ff609a8ba4e8754512751df38498e71ae928977de8f9397c110e5cfeb`  
		Last Modified: Sat, 21 Feb 2026 01:30:23 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
