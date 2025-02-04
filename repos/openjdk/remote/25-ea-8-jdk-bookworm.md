## `openjdk:25-ea-8-jdk-bookworm`

```console
$ docker pull openjdk@sha256:11e0a6dd4fd4ab51068c13b49ba40b467fc3a00442122d59770ba0384e1f4c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-8-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:bae08f5d19cbe7b610a426f504574f0b22d8a01a242b5c4406c768af7ed3d650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365757676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba7db5c3e91eea2055103211df015d178c078db24bacc4267cb284050ebab6b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273d2bd4aaefadec61278fa0a1d61a4fee3a5be72930abfdaebe539c9166ea5d`  
		Last Modified: Tue, 04 Feb 2025 06:14:20 GMT  
		Size: 16.9 MB (16943041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8325f8e1ab2d5c31014945a769cca0eff527a1be375a5320f0090b0c6aaa9bb2`  
		Last Modified: Tue, 04 Feb 2025 06:14:23 GMT  
		Size: 211.9 MB (211882301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:597722efb56e02612a054386a9bd2a0e66286b0535213a42856afc3a7099f1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8454216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdfba0f3d34485e8a2a19199b39af87e7a2d6c22905ad8d0b4e09567b0af2b0`

```dockerfile
```

-	Layers:
	-	`sha256:4bc00390e2b6fd443b49e89cb9f7f63b1f5e21a0cdd16e09ff81abf308e2c00f`  
		Last Modified: Tue, 04 Feb 2025 06:14:20 GMT  
		Size: 8.4 MB (8435615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56fce370e0cf4066c299c5ed778bd8243ce440ae37efbe4f0eea8e9a10c18795`  
		Last Modified: Tue, 04 Feb 2025 06:14:20 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-8-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:31aeb4406edc676646f4f201179648bfc4849afed8321883d6f5238df7e481a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.8 MB (363842813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228ff3a8e999ebe26006f13645375d8d5e136c7c741d5ed659f8aec887088dd3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6a2555d05d59a1b517aac5c56ae999793d8ea02a417f7a16f4c8c2080cafbe`  
		Last Modified: Wed, 22 Jan 2025 02:32:06 GMT  
		Size: 17.7 MB (17726678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280f21f68511e9f9f8e71ac87e09d6058bda7e1f919b192c625cea57f764d8ed`  
		Last Modified: Fri, 31 Jan 2025 22:28:12 GMT  
		Size: 209.9 MB (209854581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c06e7c5607580ddb0678cd5f4fa6302d092b8a1ccaf560cac4609baf57022290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8591227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40afb8329948176c2a0333e1e30acbd1ced27628aa5ae8ee36926e739d61353d`

```dockerfile
```

-	Layers:
	-	`sha256:a61c9e35f0ca0b2e4960e92b9e6458b35e2f0c37eebfef349cc591b964f24b03`  
		Last Modified: Fri, 31 Jan 2025 22:28:07 GMT  
		Size: 8.6 MB (8572483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d611fc73019349de9492a9b2acf1e223b721476799c8c18a41708b1f648342`  
		Last Modified: Fri, 31 Jan 2025 22:28:07 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
