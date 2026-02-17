## `openjdk:27-ea-9-jdk-bookworm`

```console
$ docker pull openjdk@sha256:5450ecd65b05ac4614d93869d01de6eee687aa3c6d7fe2211f2a580eda5d22fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-9-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:2c7da63189dabd7a2c705d6bf4f1f5ee6cebcbfe9a17e14a2588cd24b7a1c3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.3 MB (382349413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5046abc51eb4a53b0556a1c337c44065b47c9252d7414baa41d325384f296a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:32:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:32:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 17 Feb 2026 19:32:31 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:32:31 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:32:31 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:32:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:32:31 GMT
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
	-	`sha256:ea43fe0738d21d89bd7e6a75bbe38c5bb6d8671e5bdf74a9c733d541dc9f080a`  
		Last Modified: Tue, 17 Feb 2026 19:32:56 GMT  
		Size: 16.9 MB (16944704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b71462c6ebfcda132dc174f5213a15d6eb66d176b52b2b2f13f2b0be9a94cf`  
		Last Modified: Tue, 17 Feb 2026 19:33:00 GMT  
		Size: 228.5 MB (228488809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-9-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f888fa9633f34c78bcaededdd14c3fbed5611bbc1e98e87c9df60ce478d8a782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeb7b92d6c45cc2f97e787e10bc460b6053762906aac002b5f69452d6214da6`

```dockerfile
```

-	Layers:
	-	`sha256:05351b95224275f33b81a8469bc31fb85686f36bfc36b3a4f57fbe8b407e1178`  
		Last Modified: Tue, 17 Feb 2026 19:32:56 GMT  
		Size: 8.7 MB (8668879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a8f457e253d5de656d387c9490ebef203065ff8b771dea0e7c82b7f8db2f6a7`  
		Last Modified: Tue, 17 Feb 2026 19:32:55 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-9-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:45b6d0a06568adb0e0e2c2995ade4589bad9f6363c397fab14a233f9cc4d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.6 MB (380613741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c87100f42d0c2d86767579f094994ea99c25c3fce978a7aad9964aa5ae9b80f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:30:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:31:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 17 Feb 2026 19:31:48 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:48 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:31:48 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:31:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:31:48 GMT
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
	-	`sha256:7e75f74f450c7a955e93bf0efdd08056ae7261f63f5d37c7ca32bb97cc6c0692`  
		Last Modified: Tue, 17 Feb 2026 19:31:27 GMT  
		Size: 17.7 MB (17728528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de10b98374016d0760fe5e9dc8843c45ac259a0dd13ae8029b76c2c8a6c0d8ef`  
		Last Modified: Tue, 17 Feb 2026 19:32:20 GMT  
		Size: 226.4 MB (226434728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-9-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0ab5378bd34510572897fcdd6cf07c81b12f62c375406bfa6820bc25e6f848db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728e47853d3f08d40ecba62d1829a82e02957dade343b922bf966420e936b830`

```dockerfile
```

-	Layers:
	-	`sha256:ab006c5a8cf8d8f25dad50004afd3024d6928ffe7b1d13dd17bc38aed84dee4f`  
		Last Modified: Tue, 17 Feb 2026 19:32:13 GMT  
		Size: 8.8 MB (8805724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c776f5cd0217e9d91719179d48facc693be7b52199904c67aa51482d1d1df42`  
		Last Modified: Tue, 17 Feb 2026 19:32:12 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
