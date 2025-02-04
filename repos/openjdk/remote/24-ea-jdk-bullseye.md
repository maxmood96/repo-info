## `openjdk:24-ea-jdk-bullseye`

```console
$ docker pull openjdk@sha256:e78ae78698ffaddc8212f64caf88a0fabda79cea89d7f372600498a7667e93d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:579ab73dbb63199ec95d926be1c0a6f860919b0883eb8ad895e9f830c9a8bd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (351044331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d26915a869eb21c7c5791466a13cb0502b4c57b36c1c5c8d7328e8381a4a89`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 31 Jan 2025 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d49c0df93307a9bd06c9ca7b35ce6d068246a0938d0802933910b42574c173d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='ffab3ade32683a348fbb81aef96107b38545d1df7daa4e7ca81fe0f6775002ea'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef636a0bd6959031b388f04d2e48646799b8fde7c1b8a70713c98292e07db64`  
		Last Modified: Tue, 04 Feb 2025 06:14:41 GMT  
		Size: 14.1 MB (14071419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575f54a56148996d56876755c3343dae07b87a0a9109a2f4e5418a19389fc3c3`  
		Last Modified: Tue, 04 Feb 2025 06:14:47 GMT  
		Size: 212.9 MB (212923851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:8a9e5293744c28a4e7fe170652fc86cce6b75bc36b4c342e3e8e656322572690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8383420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e74eff81ede54f57110f85e062e51504e2714bc79fef0c8c9986c1814e3426`

```dockerfile
```

-	Layers:
	-	`sha256:85c49e78fe2d7b176a8f2c55a3156fbb9c61db87218d3bb28b20a83a2504893e`  
		Last Modified: Tue, 04 Feb 2025 06:14:41 GMT  
		Size: 8.4 MB (8364803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424e801614d827edc1025dd495f341b6af08f7b3db7f9a58217d59aeac27fde9`  
		Last Modified: Tue, 04 Feb 2025 06:14:40 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:33fdeb58024810f602cef043db0a890af02fded015578ec8b0660e5443acd6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349045628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da992191edfdf6ed51018ea90400ae2b53011c03034cf8b2e70c5ec1dee1f26`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 31 Jan 2025 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d49c0df93307a9bd06c9ca7b35ce6d068246a0938d0802933910b42574c173d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='ffab3ade32683a348fbb81aef96107b38545d1df7daa4e7ca81fe0f6775002ea'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d131bb45427773e6afabd46e2adb4b244b25d4dabe87133f23082bb3234e33e0`  
		Last Modified: Wed, 22 Jan 2025 02:33:12 GMT  
		Size: 15.5 MB (15526310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7a6f7e488119e361412980faf686b87fadd381cacf8e334999017c11983264`  
		Last Modified: Fri, 31 Jan 2025 22:35:22 GMT  
		Size: 210.9 MB (210876563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:da905d4fc15e2098b96e7aa210f808ccc592acb7b4e7d1b560b920a84898f53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1a4a8f47fef9a7bb7e4574ada091215cfb3c83c91f94c8faf621ad35f853f0`

```dockerfile
```

-	Layers:
	-	`sha256:4fa346edb73423b3a35fa3ca97bb08922625e836c89152535eae61e01ca498a2`  
		Last Modified: Fri, 31 Jan 2025 22:35:13 GMT  
		Size: 8.5 MB (8465747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6056d2ac0dc9ed8bcacc810acbe3f3d500a4a753922820b2948f9ada92ced3ac`  
		Last Modified: Fri, 31 Jan 2025 22:35:12 GMT  
		Size: 18.8 KB (18760 bytes)  
		MIME: application/vnd.in-toto+json
