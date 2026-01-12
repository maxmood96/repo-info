## `openjdk:26-ea-30-trixie`

```console
$ docker pull openjdk@sha256:5bff4832b31e1da9772362295397130bd076db29ae95c99a308b86f7e5d05043
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-30-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:6c14a07564b7231e24901b219746d5c0ec87cdfb366f844a31c2f563d8110f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386712429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52f1e1b977069ecd816e7f397c459d1aa95fbf0a3c66a7bf343a0564c0a1671`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 12 Jan 2026 20:07:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:07:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 12 Jan 2026 20:07:42 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:07:42 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:07:42 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:07:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:07:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd32f4f12560b9ed87f280972337179967997615b7881f860e21edf60413c2b`  
		Last Modified: Mon, 12 Jan 2026 20:08:17 GMT  
		Size: 16.1 MB (16062660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8034e9cd31b2faa7dc34f70bfdbda02395fbddcd4b0c1ae70b14c1bee17e734d`  
		Last Modified: Mon, 12 Jan 2026 20:08:25 GMT  
		Size: 228.0 MB (227968960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:34366da62faa73ce565b71c359df90116294046451a18d5081e8faff8c32e466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd77be6eb171d2b6754e3957386457d78860d16c315f9e26898a97966e02f87`

```dockerfile
```

-	Layers:
	-	`sha256:dda8eb5bfcba3f4a34c6068cd0f6c88b51ba144c920ca8777a3f25f192e45709`  
		Last Modified: Mon, 12 Jan 2026 22:24:30 GMT  
		Size: 8.5 MB (8509979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517effe435850fbac138556c31cbf661a282867f1ce97a6a123de0cb038f088d`  
		Last Modified: Mon, 12 Jan 2026 22:24:31 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-30-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c5ad8439e60c9eb9a34ae7ec5c856ed770fe094dbeb8c4fa872ef343040be490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384212310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc367fb6dd5d574d500e5b9239530bcc7f816529ab334e6dcf4081e03abce2c8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 12 Jan 2026 20:08:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 12 Jan 2026 20:08:31 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:31 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:31 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:08:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5854558bb92c28a440afd3316378b8e1fe545e1223a9509df1737847f1ff2c06`  
		Last Modified: Mon, 12 Jan 2026 20:09:07 GMT  
		Size: 16.1 MB (16071534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab9b34b59f6c17b9ff7e65da9a3f41e24478f3d204d9d53147b23f096212fd`  
		Last Modified: Mon, 12 Jan 2026 20:09:12 GMT  
		Size: 225.9 MB (225885754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:9c29fe64f04414a124396f53691c054c96100376c2e5fc3dbf7630b44a0d9af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397a5d49b6c27523bd4ba69fbd77d3a6cc9f6645693394463a044a90da756c29`

```dockerfile
```

-	Layers:
	-	`sha256:0dbcddc27ae0afeaf680847db9af6f12dcd7d906109ffdf25436e97d48b6cb1a`  
		Last Modified: Mon, 12 Jan 2026 22:24:38 GMT  
		Size: 8.7 MB (8704769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc29d3e8359a29bb4e9e2149c95308d6b204c1e33d46d3f35694a0aab310817`  
		Last Modified: Mon, 12 Jan 2026 22:24:39 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
