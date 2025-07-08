## `openjdk:26-ea-5-jdk-bookworm`

```console
$ docker pull openjdk@sha256:7435f0fe83450ea4de718a7521b51144d11f4343dd930890f02b1cfecda87474
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-5-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:35c4fb60a918491a2111c6f19e6acd83590e1ce316e284cf586e59168edc478f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.9 MB (376906114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889f942e793263574f33c16027c7467d7351e9f426aa79f55465b022a36ccadc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf45064f532605b539dc1dca8b6eae044c5873824666953d177604e04c703aa`  
		Last Modified: Mon, 07 Jul 2025 20:59:45 GMT  
		Size: 16.9 MB (16943376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da45b31552d896ea57a81987be31f8454447b24629b067ffb5eee39bb5f65ae`  
		Last Modified: Mon, 07 Jul 2025 21:41:46 GMT  
		Size: 223.0 MB (223047883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-5-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ed19eb3a339c2d6c8ab8d5e77ab01494c6f0a45e90c6394abca59e76cb78c51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8683789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92fd68b8fb3b4217f364110e40da6a2c2691cd2b71fe05f7294fdcf1f0a03d0`

```dockerfile
```

-	Layers:
	-	`sha256:1927e4d316fb72f16669a3e2577bd9faccf647bacbd3b44cbed11181e8f8c68d`  
		Last Modified: Mon, 07 Jul 2025 21:25:07 GMT  
		Size: 8.7 MB (8665188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b343c3de509f935c9a2c2db4ecf25b65c64b0e56e98bbf334427923abdc557`  
		Last Modified: Mon, 07 Jul 2025 21:25:08 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-5-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4874154c9723e713dd43e8e0c9a0a19409aa4840d490856aa766475d6897d2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.8 MB (374790433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1d44b88fa00ba143e589b2f2ddfece65cf7dd0f244b01ca9a96c1f40b93e73`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddef9d4cb07a09ed54474f6b74e77fc575efdb560e26070de54313e299ec5238`  
		Last Modified: Tue, 08 Jul 2025 02:06:28 GMT  
		Size: 17.7 MB (17727180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bceed4210508e1de588ead110047713c6eb91085bdc8662bad545e000fb4576`  
		Last Modified: Tue, 08 Jul 2025 14:14:50 GMT  
		Size: 220.8 MB (220803166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-5-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c40a0b0dc1b5793e52a20f5e616f31d4fe2027e36ded9b996df6989f5e07b795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8820801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6baefef2685ffd3b3bfcb4316882709de9e291d0c794c94457182bd3233b1e0`

```dockerfile
```

-	Layers:
	-	`sha256:07e4d81c6ecc95895d9052bab97caecf2c878626a47e6ae6206352f0e9dc87de`  
		Last Modified: Tue, 08 Jul 2025 03:24:49 GMT  
		Size: 8.8 MB (8802057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cec7b7d8abd475a028d953a0a72d6978a29a55e6f3fd584f28a91a72f2dd435`  
		Last Modified: Tue, 08 Jul 2025 03:24:50 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
