## `openjdk:26-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:da407067134113f3e04dd4405986e42a7c918a5121eb0b2f5c7154f4fea10d8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:dfc811c6d73f62e532b6af53af7e589921e277152d77961b6cba4a36017ca1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 MB (379630225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204f44a918980340af66fa8d13210442c0ca123f1be3255e3f3153598448d06`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
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
	-	`sha256:bc9edfe97502242f87c2fb3c7f191b23aae13dd46c804ebdd82a3c352ca60a09`  
		Last Modified: Tue, 21 Oct 2025 21:37:14 GMT  
		Size: 16.9 MB (16943624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cf290383d896c216fbd37ad750e2ee7f90eac046e73b2280858738a1b8c157`  
		Last Modified: Tue, 21 Oct 2025 21:37:29 GMT  
		Size: 225.8 MB (225780735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4ea703c23c8bf3d12c1bafd84de11a02454c5c82d6317993093de2a6042c0b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8688708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e360909a28edadf6b69e284ece1776755864cea053b93e0b3e0575a7ce158493`

```dockerfile
```

-	Layers:
	-	`sha256:3149fddb0e5db988658e71de86b5a3bf085e12d759a2c4a87846d519379efd47`  
		Last Modified: Tue, 21 Oct 2025 21:23:33 GMT  
		Size: 8.7 MB (8670090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f4432e313005d9babf24860e975d4e39af59b30191744db4f0f35121c67fb0`  
		Last Modified: Tue, 21 Oct 2025 21:23:34 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e85c5bd170c33141182216b27425f6cb3799d7e825346c2cb2bcf206dc6bc3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.7 MB (377693617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d17dbcc9c66e1aa4d269454161334263629341f24c9293648f03a1e6db5f25`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
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
	-	`sha256:5f31d04ab929957224fa000bdd23e6e972b2d8500aa9bd3efc384fa137cd0f10`  
		Last Modified: Tue, 21 Oct 2025 18:14:22 GMT  
		Size: 17.7 MB (17727630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60f8d92eaf968105f6a43624cf380dad6ccda3bf02a93692c16a6a1607978a9`  
		Last Modified: Tue, 21 Oct 2025 21:37:55 GMT  
		Size: 223.6 MB (223638069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0c88e0da5425a5ad69dd445efe866bac9b9640073cbc091c9d36a6ebb9f6e95e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8825720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfae61a9a16dc35224bc40dde9423e31e5dc8bb8ffd5ef2a298e09051fd8bba6`

```dockerfile
```

-	Layers:
	-	`sha256:d4da1e38ae02ca3aa6d8dc5c5ba5873c8528b7c993b0ed7132378218a28ab5bd`  
		Last Modified: Tue, 21 Oct 2025 21:23:41 GMT  
		Size: 8.8 MB (8806959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57ce6d4e251a4b09efcd5f23f071514eeca85ae66dcadd96bfe9a21ae52b9773`  
		Last Modified: Tue, 21 Oct 2025 21:23:42 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
