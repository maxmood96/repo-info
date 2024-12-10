## `openjdk:25-jdk-bookworm`

```console
$ docker pull openjdk@sha256:7886392373760ab1847e394e39f469f43556d86e876f0b95a5f7251f9483ae72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:6bbdaadb8f121fdc3faa479c3cfd8e05d2728b8e5b6926510b4d7f730044c82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366671223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0e1c93f8eaeba870d05e2ea12d8bebc038b2f66c90966719bbc850178e9dfb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c700e8ee8b405198fa470a301d6ce8311f88d46b1b2f8af1b06cf20fa79f62`  
		Last Modified: Mon, 09 Dec 2024 23:30:34 GMT  
		Size: 16.9 MB (16943039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03cd15b19884e91a3595c4f1385eda38db4aba87b65f595af53629e863adcff`  
		Last Modified: Mon, 09 Dec 2024 23:30:36 GMT  
		Size: 213.0 MB (212973590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8054cf30c3ba4eadb2c65820d777332d02c74ba1d2cdfea880b28e1cdd59031e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8466398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71571ee74c0a58e1c611a3b9b5f320a0c3cb3baff4786650397e111689fa836`

```dockerfile
```

-	Layers:
	-	`sha256:13e80f360751e4313710c53c4245b33fa54d8187ea303490c877e365c27a0b11`  
		Last Modified: Mon, 09 Dec 2024 23:30:33 GMT  
		Size: 8.4 MB (8447797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0868734fd862a9f0004913a8d697d6a36e28cd276839c42daf732fa7431090ca`  
		Last Modified: Mon, 09 Dec 2024 23:30:33 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9c3e7565caf72dcfa640b35036fd6737df8f1605584a98e62e6ba87058748cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364730019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778062e6755d0345a6d09b650c453f797dbdf291d7a7892242aba42e069ce2c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133b2b6add979b2154435e8ffa765b9f6bf91b9c32635e0e18067f8505b1f4e3`  
		Last Modified: Tue, 10 Dec 2024 01:28:50 GMT  
		Size: 17.7 MB (17726651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a059f3345211ce8031fd1922bc4cd025721084e65e0d809314401aca480aa3d`  
		Last Modified: Tue, 10 Dec 2024 01:28:54 GMT  
		Size: 210.9 MB (210924023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:116201138cc59fa41099ea5056df94c0aafd13b59e7add82fe80538bb4a4ca97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8603576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b412de00d41da050a78293a07747529eb9e4209c543444daf1810c178438294`

```dockerfile
```

-	Layers:
	-	`sha256:1ac403186615168253da2cb62fcf632fb4408b308c300940d920795431b54f5a`  
		Last Modified: Tue, 10 Dec 2024 01:28:50 GMT  
		Size: 8.6 MB (8584832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c12483f824514b2d62bd760cb24418d9a76afd30da703707ba4c956c72cc666`  
		Last Modified: Tue, 10 Dec 2024 01:28:49 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
