## `openjdk:25-jdk-bullseye`

```console
$ docker pull openjdk@sha256:d3460cc90b7b0b9e527f8af0ef4eca3e4109196988fc2e261a9c5fc1c8104820
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:d0aafd1ff5eab17d30568415f841c4f5cca2386060cba9420be05a36330fb01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349993473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd81a4c468a087fea69dd6809deabcb63798a6755675f908fd345b909185744`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae550f4768ad83c7dcc1ef8de6de078a33effa152d846f4604ead4cbb1f414`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 15.6 MB (15558355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322d21cc1b9c3e86a0528fd885e7483a3b2497c1448256bf87a4493be665ab0`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 54.8 MB (54752320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9856f9364c1361b6d4a3a5811305bcaa8c3fcbf6d6ac51032b124c7addf0066`  
		Last Modified: Tue, 18 Mar 2025 01:13:20 GMT  
		Size: 14.1 MB (14071420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ee58b2a5d1941651dbc1ef77e921f6e7bd67ae0ed72087302c9072643cc7a0`  
		Last Modified: Tue, 18 Mar 2025 01:13:23 GMT  
		Size: 211.9 MB (211870103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:cd313553822be08cffaca5624aacd910b42c6b9d0bd0b9b495f21b54fb9f181e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8382792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc4740cc573d1cd3e864185e9d49ad9acc38f5a9b5a72d0fd7be690bbfb4252`

```dockerfile
```

-	Layers:
	-	`sha256:8746346b751d9775c714013c186dcc9297e1f9e4b8e5e1deff6c1e44d8585f26`  
		Last Modified: Tue, 18 Mar 2025 01:13:20 GMT  
		Size: 8.4 MB (8364174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d09fbfc9dbff9d0cdfe9471bef6753c434554c1690db9d1825ce95ad63c66c4`  
		Last Modified: Tue, 18 Mar 2025 01:13:20 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f49024bc23d3a3803416e5e463af4d8ca5ce89e7b71b1c0d86fdbf69c82da2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (348004441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3a84e355d264f2989f7664abe71361baeff95703c12b64be451b28c8959a9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e51a0f3d8cbe65d5ade4dd1c5d9a5141d6e0227e40f7f7d04ca441c52729da8`  
		Last Modified: Tue, 18 Mar 2025 14:36:12 GMT  
		Size: 15.5 MB (15526089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e470eb9d9d53096fe5886d82285604defc0127e62b61e2ce06ed2b3a532eb0db`  
		Last Modified: Tue, 18 Mar 2025 14:42:44 GMT  
		Size: 209.8 MB (209830525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:0643f93329ee0580f1b466472fda7f94508958551a5c851dafb2ff45d5b66b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8483897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7cf69a65b9c8c1130fef6ff15e4ce7a5842c2addd08185617d73ce38c5f8db`

```dockerfile
```

-	Layers:
	-	`sha256:0ec66d1f3752a86bde76af6c15c97d051735aa44949246af64c1d3e4c0a033dc`  
		Last Modified: Tue, 18 Mar 2025 14:42:39 GMT  
		Size: 8.5 MB (8465136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba5c917f9b3b062a7d94e73cd600813818c655a5934dedf4a2e065c3d6fe59c`  
		Last Modified: Tue, 18 Mar 2025 14:42:38 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
