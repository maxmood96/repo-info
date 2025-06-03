## `openjdk:25-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:2113323438cbda76e1248e6d032c633840dfaa0ce59bd9e32a10934e9520a540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:24a78a0e23020b1d70c934ee56ca2e01245da94fa94957e9645001ba06ae50a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.6 MB (376561075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a591dfdf315682302f7d79a4b694e7d89e13800bdb2d4884b96ce8a54212e31`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e94f08ac5af4d35b95385e958655be2d6d0ec6de73617dd75463870a254dd38`  
		Last Modified: Tue, 03 Jun 2025 13:47:56 GMT  
		Size: 16.9 MB (16943316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a95e5d31ee3f80c10de673bcfd2178af2d912ac80f3029547a97f4c5cddb715`  
		Last Modified: Tue, 03 Jun 2025 13:48:04 GMT  
		Size: 222.7 MB (222714021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b98ea8cdd5b2b2135374fb84d6d192c5ac6e18ea642bbf6a97e9df4e2b2594c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8487879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6214a32d938d7498b01ceeb7568c7092ad1ed4233f604c52f2bdbe09f1d254b2`

```dockerfile
```

-	Layers:
	-	`sha256:33cea6d41583dab89932ed63936017856396d0a0fdedf17f7c1e2e06c092c573`  
		Last Modified: Fri, 30 May 2025 17:37:42 GMT  
		Size: 8.5 MB (8469261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ea284d16b74e699f19a6a60807285a3467b3123c683c24b5fb430339448f48c`  
		Last Modified: Fri, 30 May 2025 17:37:42 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4a8abd1b9f70df6e134b9ce6ca8ae43a7773f70c1a9692f1c22f2fa821d3ee76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.5 MB (374473292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc5514b7328850568a2be65935bf03248d339e98241dba373959a22dc7b4561`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f99ce5ffd12a32009f9a69c70db4a1f19481d9b1f6ae3dd3f54c6168bf416e`  
		Last Modified: Tue, 03 Jun 2025 14:41:59 GMT  
		Size: 17.7 MB (17727154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe53c482a107013b3992054f3dd5004c8622f8ca7ee7788213ea0519951af3`  
		Last Modified: Tue, 03 Jun 2025 14:42:11 GMT  
		Size: 220.5 MB (220505570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:6d0a42afc758345ff465264cd42aa101adb7fe14a30288d72fa98d743877a82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8624890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a860f1574e8bec266d8aaf48f552a9c1ab86db8360a1c1dd22b177b82b1e01`

```dockerfile
```

-	Layers:
	-	`sha256:65a266ea07e438840a13ebe167de49308918c7fcacc4707a3e0c55fc6065eab2`  
		Last Modified: Fri, 30 May 2025 17:40:22 GMT  
		Size: 8.6 MB (8606129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dcc926239a84e4dcaae11b6781f0893671ab926269c7c511955d3bd8094065d`  
		Last Modified: Fri, 30 May 2025 17:40:21 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
