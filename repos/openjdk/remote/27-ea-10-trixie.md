## `openjdk:27-ea-10-trixie`

```console
$ docker pull openjdk@sha256:2df92347f414f34414b83b064f4062404755e0704b59fdc0fa492eba0b7688ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-10-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:f6bbe2e48278d445da429af1eb4b8f1eb4f4ae5e4c069ab6116c065460d765bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387262599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bcdfc7ab944b2044d643fbe7a68a9c83da38e31256ca8419f0e560fb09817c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 21 Feb 2026 01:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 21 Feb 2026 01:29:26 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:29:26 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:29:26 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:29:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:29:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e2021c4c8bd1a46b34d9608a9381afdc333600ee1ef3c94306ecf7373e1956`  
		Last Modified: Tue, 03 Feb 2026 03:29:16 GMT  
		Size: 67.8 MB (67787365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e50ea2a1214f038cb62da5cb2d9843480b1f05c3c135b9037713cd3474c9a5e`  
		Last Modified: Sat, 21 Feb 2026 01:29:50 GMT  
		Size: 16.1 MB (16062954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412006d837c18c064a69f76d59dcb514a2240a7deb55b0911f76935ac5349dd4`  
		Last Modified: Sat, 21 Feb 2026 01:29:54 GMT  
		Size: 228.5 MB (228505318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ebd772804fb1d449e008ddf7027807d5e19182294ba193042dc68f1c1d61903b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9414b269ca138492011f965ffb9addf088f387789dd9474d258402b17ee8a1`

```dockerfile
```

-	Layers:
	-	`sha256:e75085b8b9976af26f6ab0cce7e97571d33da9f7e74bb7b85ae1be146f467d48`  
		Last Modified: Sat, 21 Feb 2026 01:29:50 GMT  
		Size: 8.5 MB (8511024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f756cf708d0dc535346e9f1c73583e7bafcc38761bf23579f4264bce6f59c0`  
		Last Modified: Sat, 21 Feb 2026 01:29:49 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-10-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4c56acf1937ab0c79a626847cb0c209f0c8cbc9835ad963706c0870d99ebff13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384793955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5401dbe05ac9446601865565734ed6055563f89be3d6c2ca210845d635e478d3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 21 Feb 2026 01:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 21 Feb 2026 01:29:07 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:29:07 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:29:07 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:29:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:29:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8128ce97ccffb1094b6eafc78b5827499d0496944f3d357e222bfc29f01968`  
		Last Modified: Tue, 03 Feb 2026 03:47:30 GMT  
		Size: 67.6 MB (67593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3f181f4c4b7f57169f4067e3075d2794071ede5a895f288194a37028c50042`  
		Last Modified: Sat, 21 Feb 2026 01:29:33 GMT  
		Size: 16.1 MB (16071814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6536965605e62c1183d30914c5deef37309aaa969076f78fad56a84800d4d9e8`  
		Last Modified: Sat, 21 Feb 2026 01:29:37 GMT  
		Size: 226.5 MB (226454431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:b7030a1dfe8193ba519e6cb03c094b1e1b9180619620e59dd09a2623f1f8ddba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd445938f34cea4c37ef438fa2fdb040d99105a16bf9aab55bff8253b25e7b3`

```dockerfile
```

-	Layers:
	-	`sha256:8c5b0865459ef02df2b0d2f24d2f33ad23e5cb54fe422f49e3095f81bab2b604`  
		Last Modified: Sat, 21 Feb 2026 01:29:33 GMT  
		Size: 8.7 MB (8705814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:425914787ace581ff53aa15fc61fa3652bc61025a9e701bd660c30e5c95e98c2`  
		Last Modified: Sat, 21 Feb 2026 01:29:32 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
