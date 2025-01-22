## `openjdk:25-ea-bookworm`

```console
$ docker pull openjdk@sha256:6377bc25ac8af8996adcc26bda13940a1dc041f7cf3de828b8fec6554378692d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:18635aa781a7bc32320691435df9acd090feabd04390fd9436e56abdae01bff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365680466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b257f7f28a26db1978616edfe2581b5fe681bacba92b27b8dd3f17bcaa86078f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608dcde434dab5c65a1bb3278d1167e88e01bcfedd4f10d4f3855f8e1ec371c5`  
		Last Modified: Wed, 22 Jan 2025 02:28:40 GMT  
		Size: 16.9 MB (16943045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc9a40d2a0aec0c86d606289f36965b90d81c40c83dec49dfc9390f3f5fafce`  
		Last Modified: Wed, 22 Jan 2025 02:28:44 GMT  
		Size: 211.8 MB (211800136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:706695962f55be96123c27cbc2361007ea52dafdb1fd1bbc423c0c5555ceb0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8454216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef727d24336c1be4b4467b97675cec64da045bbf6f2bbe714393723aef2904b6`

```dockerfile
```

-	Layers:
	-	`sha256:6b2d91563a7db83a98b8ccdd3029edbabe0426d58707a71a1b33a7ac334b8a44`  
		Last Modified: Wed, 22 Jan 2025 02:28:41 GMT  
		Size: 8.4 MB (8435615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b0b836e5e3253660a9c91c3b34edbca8a9c6dc2bbc5b997847e75411ebf679a`  
		Last Modified: Wed, 22 Jan 2025 02:28:40 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1c73fd48f6e7e6d713b49c97bc08e1065b001bf7c75cc4dd0a47c3694c1aa654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363742201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091418a7d188d59a674808052c0a27a5ea5f59787e5f2c7fea3f3ce9c90d4568`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
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
	-	`sha256:20b78360f432a83d510229ccd73bd8488d4987646d9ab9abad640b341b94c294`  
		Last Modified: Wed, 22 Jan 2025 02:32:11 GMT  
		Size: 209.8 MB (209753969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0f1151710659cae6dabdbfb6ee2d6f069f8b998e4505093583ced6477cfdd7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8591227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f3520b1766a0ca7522072fc0ffdb894c8b39621884f5c484bfaa95572e6d09`

```dockerfile
```

-	Layers:
	-	`sha256:5f9546b9d6879c6fe0ffe4fdf03881c1f49b16e4905b1700c210606dd0f949f7`  
		Last Modified: Wed, 22 Jan 2025 02:32:06 GMT  
		Size: 8.6 MB (8572483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22e0f1e65fdafce34b4099eeae836428a168eaa9494793bb884fa820a8eeff73`  
		Last Modified: Wed, 22 Jan 2025 02:32:05 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
