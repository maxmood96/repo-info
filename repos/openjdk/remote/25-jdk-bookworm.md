## `openjdk:25-jdk-bookworm`

```console
$ docker pull openjdk@sha256:b97c92c570c898ea4554297ae40a67207708d5230646325a6d5270b7dca44600
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:49bbeead8ea54f0156de54627de6216d83e4a2cf7bd4238ad8155e4509dd8b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365823242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f199a643467b445404c8238460f2ba4d7b524d3d5748b3b08f1e052562517e2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0fe164662cb8810c03658f8b0d2764a494cfe786b5e012cb4fdb311fb34de1`  
		Last Modified: Mon, 14 Apr 2025 22:58:56 GMT  
		Size: 16.9 MB (16943294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382aaaff89820fb2428efd2d8250e6f98e168e1704146d09a42f9edbdb7fd11c`  
		Last Modified: Mon, 14 Apr 2025 22:59:00 GMT  
		Size: 212.0 MB (211981849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:592124e2b4aead35157aa7ea4633aee4a75f50e70e98f384ab286523517c5413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8451952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f7f2a7301609223398751dfe9e13ff8adfaa66eb028a827ef51e2fb65d9d48`

```dockerfile
```

-	Layers:
	-	`sha256:e2f0cb5c66d58f418726098665f9742a355f38f94569dc15bb87cdfc34c46314`  
		Last Modified: Mon, 14 Apr 2025 22:58:55 GMT  
		Size: 8.4 MB (8433335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:805d430d962ccb6d2412690b148fe4b780b5a001744e2d7c6cfbd13cada492a0`  
		Last Modified: Mon, 14 Apr 2025 22:58:55 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4fa8649921dae061c2e0dd9b6cd1511533b89957e3bea8217e0aca8cc337b8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.8 MB (363751466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52632a69eaa4b7499c47c2518ae93d30157b9222307037a7f993e263af5277a8`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c6f8c583e350c4c0560ef0654dff7fbc9a5e71b683b62b9d74ac05195f4329`  
		Last Modified: Mon, 14 Apr 2025 23:01:05 GMT  
		Size: 17.7 MB (17727052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106c49ac8d80ef8aacd39eba673d281ed220c415289caef3fa4fe53375948dcf`  
		Last Modified: Mon, 14 Apr 2025 23:01:10 GMT  
		Size: 209.8 MB (209796826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:86c5aff83c0d63474b94e3eaec6b98b08fbd6bb19613dc1466c4f53b8c8d7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8588964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28442d13eb898ee611647776bb717b481681e5e173393bb7630c2b1d92515edf`

```dockerfile
```

-	Layers:
	-	`sha256:caa04f937706eb591e450cff16176930ad29898438c8c00b549ea17adebcabd5`  
		Last Modified: Mon, 14 Apr 2025 23:01:05 GMT  
		Size: 8.6 MB (8570203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21c57810a80976ee07f9ea031c2280644966b3b4417c07f49b4cc6a291e8b1b`  
		Last Modified: Mon, 14 Apr 2025 23:01:04 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
