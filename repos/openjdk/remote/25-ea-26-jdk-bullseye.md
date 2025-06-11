## `openjdk:25-ea-26-jdk-bullseye`

```console
$ docker pull openjdk@sha256:5dfc0740ecc2c0bc7f03f7ffb4c5b5399a85bf39d1cdf30ed328a3dad38c0b93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-26-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:2c6890c8976eb20ed9d992b2586fa6217da43fee6330fcc4a16e8964950bf752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361432431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef840e73b9472fc0ccf6394de1367597d6274e8b1abfd6af7be1e0def5b15d39`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83577993e16147f4593abde205fb3dc597440e3bf425eb6dd77bd84d309ecdbd`  
		Last Modified: Wed, 11 Jun 2025 01:16:31 GMT  
		Size: 14.1 MB (14073156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b016951648ba79dd974bfa980c926ce0a4768c2c91305d974ba55d97b6356697`  
		Last Modified: Wed, 11 Jun 2025 08:12:40 GMT  
		Size: 223.1 MB (223081991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-26-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:941d0d2116c636be77787e7997f49081aed285f63eb2836e6e792932164cf8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c356badd831bdffef87aca2612da02fb73c6f7149c995245f73bbde0924e56`

```dockerfile
```

-	Layers:
	-	`sha256:8cdbc673804dfce9652194dea1debdfd9cc3c089a045d2eef638c9a444be1cc9`  
		Last Modified: Wed, 11 Jun 2025 03:23:26 GMT  
		Size: 8.6 MB (8590832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b62965b88331b8084c617a459874951fb901d6c8ec303b79c9181e91f76be8`  
		Last Modified: Wed, 11 Jun 2025 03:23:26 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-26-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e839264cf91f2f5b59ab30be5c71fe4891e744a44bb7e6dc13798288a776e507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.3 MB (359270872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933d5386c65b18ed52b878f1875a31143bfa9daecf17297d36c9ae6f2af9e372`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6cf4c8c5bed5afeb734d65b48f87d9bbef4fe159e3cd46699dc036a3de392`  
		Last Modified: Wed, 11 Jun 2025 20:03:35 GMT  
		Size: 15.5 MB (15527734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3521d16567649a287002be49f74954c262e604244ef496808281d043b7acdb2b`  
		Last Modified: Wed, 11 Jun 2025 21:22:23 GMT  
		Size: 220.9 MB (220887189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-26-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9467a56a0c977dc38fe6f5509bfde544d9dd5cfdedc69b7228596e30d4bca4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8710555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5770b4bacb8c14b37141535d08492154129adbc929eb906c50c80e6d565bb154`

```dockerfile
```

-	Layers:
	-	`sha256:bc0fa4ec0034bfe2c3b36777b9d0668a40c23c2aedbd012e853b37126cca618a`  
		Last Modified: Wed, 11 Jun 2025 18:23:32 GMT  
		Size: 8.7 MB (8691795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8baa57abdf837c6d28ac652dab51c9faccf79da6b11d5b0a423e1d98dac45a3`  
		Last Modified: Wed, 11 Jun 2025 18:23:33 GMT  
		Size: 18.8 KB (18760 bytes)  
		MIME: application/vnd.in-toto+json
