## `openjdk:27-ea-20-jdk-bookworm`

```console
$ docker pull openjdk@sha256:3758bdcfb40da31940426208a046f27b93dad5a65d961bd4a4fbd62066ebded8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-20-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:14eff914813ddc87b4f291e77c7705d77d196e5783c37d8ca0792de1e5fda510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382460013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5589d55ee4c1444ac642d8f155cc1591477e016cbe20547289feac09834b0eaf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:04:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:04:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 05 May 2026 23:04:49 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:49 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:04:49 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:04:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:04:49 GMT
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
	-	`sha256:adc71f2f55d0a867c9dddf3ba50d4d937e48462f934863bf60e3a913bca68118`  
		Last Modified: Tue, 05 May 2026 23:05:18 GMT  
		Size: 16.9 MB (16945706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a382b618c7a5833030f9cd2baa0dd16de8631dd08b321ba6db06d3c4224ee532`  
		Last Modified: Tue, 05 May 2026 23:05:22 GMT  
		Size: 228.6 MB (228586457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-20-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:59eaae8cb1e5f7328113949eec097cee2471dbd434fa90dba33c9b993fb8d9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8685556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d799e69e1f0631ed52876b48c83a2ba6f00d53a1e16683e5eb002df4c5ccfe`

```dockerfile
```

-	Layers:
	-	`sha256:5a8c31cecf645d1ddf778b379cf95fe7f2eeb8b46c84f5b13aef669dd8adf791`  
		Last Modified: Tue, 05 May 2026 23:05:17 GMT  
		Size: 8.7 MB (8667617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1de80cca09928aaef24860a338a734cce13ad5a8173c4733ed4958773b740b`  
		Last Modified: Tue, 05 May 2026 23:05:17 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-20-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3831670d276bb6e92a4fe6ee96df25315ddcb6acee1704511c1dcc98d579d7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380746164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f7f5955f138402548e1ac068ceeac09d72535e19d2366967e4488fa9473e10`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:04:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:04:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 05 May 2026 23:04:49 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:49 GMT
ENV LANG=C.UTF-8
# Tue, 05 May 2026 23:04:49 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:04:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 05 May 2026 23:04:49 GMT
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
	-	`sha256:4e58d88203c49b40c428e5f8ce4a83a5081db4ab40baa5ce72f8786eb459b2ff`  
		Last Modified: Tue, 05 May 2026 23:05:15 GMT  
		Size: 17.7 MB (17729013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4326573d4e03a69b8f827fbb9f2c14b5259704ae67cf85cce710056872940e2`  
		Last Modified: Tue, 05 May 2026 23:05:20 GMT  
		Size: 226.6 MB (226555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-20-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9be217ec4d836ad40a3af48e9c54a937ffcf792d5fbdf88234a7cac174719c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d0a245ac6eb26f6e6b036e57a69cb680c51310cd34f0650d81ad230646e54f`

```dockerfile
```

-	Layers:
	-	`sha256:a16c0ec6996c4a6ba0a807ff46457250c3d77909403b1589293bf8bcad35a892`  
		Last Modified: Tue, 05 May 2026 23:05:15 GMT  
		Size: 8.8 MB (8804462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0232abbc014433e8dfd6ad511efcffd7ed52c41341db5c1eaf7cf38c2641e839`  
		Last Modified: Tue, 05 May 2026 23:05:14 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
