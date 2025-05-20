## `openjdk:25-ea-23-bullseye`

```console
$ docker pull openjdk@sha256:35213493beebcc33cd273ff331d073494c8ac4a1815b439e8bed16ab66ff12bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-23-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:6dc74bc15dfc5dac5ae9ec939e095e68d0492e0a18d71d63651e7752c12dc65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351868763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80eeb6f434ff793a4017dc79609087e4409f41efaab0da6a20a4650c44e755c4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e598af895df2929ac09e18cabbf0116ce24146bc39a64b3bf95828ea946d23`  
		Last Modified: Fri, 16 May 2025 20:54:04 GMT  
		Size: 14.1 MB (14071389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6e2bdf65d06e103d8245cc22958dd1d221f0ed6fe59433b471e63f65a9e02d`  
		Last Modified: Fri, 16 May 2025 20:54:07 GMT  
		Size: 213.5 MB (213530084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5b26bc197fd999fab5b9fccd562bed7dc06df116c75e242f43f22702181ef3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c74d6c6aa3db069f2876f39977852861d3c36258be99fcf884945e7efd7dcb8`

```dockerfile
```

-	Layers:
	-	`sha256:cf94802da494d459d22f8e14ad28c8c5267a3503c2eab6dabaaed68c6cb63151`  
		Last Modified: Fri, 16 May 2025 20:54:03 GMT  
		Size: 8.4 MB (8402311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20aa8499c988e40867e068d460ab9a4eef67e8a6a94730c6a13463e8fa72fe08`  
		Last Modified: Fri, 16 May 2025 20:54:03 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-23-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7781056aa739a5b5427d416bdd75657e94f97c5cecb7cdb9145301c8a7631cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349675900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7ae4483165e871b5f35ab9205ef9dbcfe81022fe3256d09c3be3d5f6f5741b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e083c302b4f5ef95e7f103ab22b947c3e67397db7ff914707f08c59f2ec6b5`  
		Last Modified: Wed, 30 Apr 2025 03:54:13 GMT  
		Size: 15.5 MB (15526614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded81d2274d5224229e7e46a4f82bbf92d209a1669edd072c119cde2e005887f`  
		Last Modified: Fri, 16 May 2025 20:56:54 GMT  
		Size: 211.3 MB (211304198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a100fc39a8fc871c2a9e18f159c09d3c34db2820bae6ffa7d17c727040d03f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8522034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f317f2a96f4513b7d1a075a3af3da4f36c57165c8dcf38f51b09a2e89337ea2a`

```dockerfile
```

-	Layers:
	-	`sha256:eb50a0bf0b757676821f62bc08dab1752a3b32762ec3202951583713eccf4134`  
		Last Modified: Fri, 16 May 2025 20:56:48 GMT  
		Size: 8.5 MB (8503273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ff80fa248ac3f5453bcda0531063ac0228e6926b1ebafcc42445f040d11af0`  
		Last Modified: Fri, 16 May 2025 20:56:47 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
