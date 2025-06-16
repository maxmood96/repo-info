## `openjdk:26-jdk-bullseye`

```console
$ docker pull openjdk@sha256:ba749dea2d1ef7e93dc9ca3f7f13d91d7b59a05437817b8325b2bdb213392e13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:d6ecd7b83e5ad18de64a6f3159ec8b225a5e75437f89049d33a7ad500b94dbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361234494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2321c5fb4fc86bdac543bcb0f4a7e1a9c7f848dd575c186e8cf018a0b303670`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
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
	-	`sha256:ad58f072431bea3114716e56be8a1fbfe6f895fcf53675b444ca7b8b3677e4ed`  
		Last Modified: Mon, 16 Jun 2025 17:51:17 GMT  
		Size: 14.1 MB (14073100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d1872b8bbcfc4c3dd943e1bda8322b30b15665c8ec4ad9733ca17d41172a26`  
		Last Modified: Mon, 16 Jun 2025 19:09:31 GMT  
		Size: 222.9 MB (222884110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:522dda3364577f859de1474e8c1745f2b3037856ffe31ef35d615c9a300006fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c50507bae34bd7173a9646d2b3ced64e5267bc1eb3483ebf6774975b53e66b3`

```dockerfile
```

-	Layers:
	-	`sha256:72f69ba48a50e8ae18abbb5c99d6c3a243fc4dda466f7118d347db07f1204346`  
		Last Modified: Mon, 16 Jun 2025 18:25:28 GMT  
		Size: 8.6 MB (8590822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6458661a00ef5a8405daecf2df7c831def84459734c72a7229d7c453105e2944`  
		Last Modified: Mon, 16 Jun 2025 18:25:29 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:543d297d6c4cd52f44d4664b6df04de8226cd21aab4e3815dddfc2d748ada91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359066300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd144b8d766e463fa549e4598043acfac9abb43b1936d630d8cea6311ca8520f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
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
	-	`sha256:8d896647166ddcbae0d1c9ee0e09d453debcf93725205925db1bd1af7653253a`  
		Last Modified: Mon, 16 Jun 2025 17:54:13 GMT  
		Size: 15.5 MB (15527713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d67d9a31440b62c3b6236b9ffc7f1b4caefbcd9fa6b1ee258cd1133924624`  
		Last Modified: Mon, 16 Jun 2025 19:09:20 GMT  
		Size: 220.7 MB (220682638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:77fa813db036f9449d82af0331c89b21f343618ac2293687e22fb28b9f7a03ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8710529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0526244088fe1033e53bb7e0f65625f28fa884f08a3ae987a467044095fbc110`

```dockerfile
```

-	Layers:
	-	`sha256:d733b595bf94a9fa1a420e963949f3138845c773c7505caa5a51d186133fbb82`  
		Last Modified: Mon, 16 Jun 2025 18:25:38 GMT  
		Size: 8.7 MB (8691785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ceaeefaa16f736300aba0bd84d26ab9199d8d74702e1e920fda199155cfc67`  
		Last Modified: Mon, 16 Jun 2025 18:25:39 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
