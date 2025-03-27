## `openjdk:25-ea-bullseye`

```console
$ docker pull openjdk@sha256:4a455c071191a5358baead031fda7bfe3fb09a1b779054e2cdde1d6ee514fd00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:453e774148566bb027f25ab2fd4316dc94602b5f66cf14fa01cf382018724a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350416905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c02d5c8c590c47d071ac7e9b7cf00c578c946621f2632467eaaae68e95feef`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
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
	-	`sha256:6a90d6bd9c43865149baa3ed885917269d9448ecc71a7d87eaf0bf998e355037`  
		Last Modified: Thu, 27 Mar 2025 20:45:38 GMT  
		Size: 14.1 MB (14071504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f69e0c84687076e839b0e0e182d494bcf58f010df587ae2804bc3b964e17f6`  
		Last Modified: Thu, 27 Mar 2025 20:45:41 GMT  
		Size: 212.3 MB (212293451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:7de6a55c55ba26d8c1db9d782d232a76b9e640c88a08dc87824abd48e2bb39d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8382792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937333d644b17c344ce87e41e3c86c047ea39c86a053e7b28a8d5dc8ba9822df`

```dockerfile
```

-	Layers:
	-	`sha256:6c893b13d357b36c5621549384aba5020304a3baa95919141f583dbb696fbdd3`  
		Last Modified: Thu, 27 Mar 2025 20:45:38 GMT  
		Size: 8.4 MB (8364174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daad79153d7058fe196c38b0d17f2282f4a089633cfde7153110a25c88c58fd6`  
		Last Modified: Thu, 27 Mar 2025 20:45:38 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9f59bc40d002cf7fbef94818acc7cc3099cc495a0b1a45699d62d5b0802b8e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348350281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe33636b7d04e2818641e40825b5c9ee6eb9319cd4ae19a69f171678614ac5a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
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
	-	`sha256:e1b658ea4b94c216c095b98c1eaf64a94c74a484b39c3f0e7317d2f74172b5b4`  
		Last Modified: Fri, 21 Mar 2025 17:27:33 GMT  
		Size: 15.5 MB (15526350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b320c3270e74ae2b3bb8926e05b1609f2bcb3ad94f9b0e947493d5c1ef46702a`  
		Last Modified: Thu, 27 Mar 2025 20:49:25 GMT  
		Size: 210.2 MB (210176104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:28b3a09f766c46ccbf8e1f34dd0f7f0b5fee8899e685258d5e400a72ecc20286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8483896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589afe412dfc3c6c89b79cdbd1b28a692ad927de946d0eb4c97f83e4e396a782`

```dockerfile
```

-	Layers:
	-	`sha256:d4e281660dd99925b2a42755aa83b17139451922c905cf8619de1e91a114971c`  
		Last Modified: Thu, 27 Mar 2025 20:49:19 GMT  
		Size: 8.5 MB (8465136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b21d521118d7aaedfbc569cc62e062460cc123d733d65a7f99083659beafa87`  
		Last Modified: Thu, 27 Mar 2025 20:49:19 GMT  
		Size: 18.8 KB (18760 bytes)  
		MIME: application/vnd.in-toto+json
