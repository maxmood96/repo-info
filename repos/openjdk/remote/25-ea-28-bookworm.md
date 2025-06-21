## `openjdk:25-ea-28-bookworm`

```console
$ docker pull openjdk@sha256:ae29282cec2945642db41809f85f8f26158b8387f2d27607d87bf05c050d151f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-28-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8a6ea3b91241340c242b26a3fa3ad877c3606a9183105fa88b046bfde09e712d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.2 MB (377249386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7891d0fec252b11137676ed70c5a44fda32b8eee10d6ae492f3b487c237b0223`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 20 Jun 2025 18:48:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_VERSION=25-ea+28
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='ddd476f5dc6e80fc93f06ba240cf3537fd8aed344823abfd64c1cfe470f441b4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfbc99aedd5015a5ab41d74f53972f7cb6616032c983216add8cf2de21a1fa5b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f0b3172c5b059e29226dc97698abb31fb23858e664d8ae45da2a7b737cc3e4`  
		Last Modified: Sat, 21 Jun 2025 03:23:49 GMT  
		Size: 17.2 MB (17227509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80e98ac5ad95040b17920558e7c0156ee51e8ec5fd5f951bfc76141376a9524`  
		Last Modified: Sat, 21 Jun 2025 03:24:03 GMT  
		Size: 223.1 MB (223112103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-28-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c4a0de14ecdc399c86f9602a8e3130df0ffaf70574227ee899e6fc782feb0e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8683814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19039672d6df0e2b79f1ba08e4c192ec7955b39cac40b48291c02568d92e5ffd`

```dockerfile
```

-	Layers:
	-	`sha256:89450476c8027bc1e616caa7cbf851ce7830cc27d7308e2531ce97a00062f05c`  
		Last Modified: Sat, 21 Jun 2025 03:23:32 GMT  
		Size: 8.7 MB (8665196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d7fa5cb8f529773f9eeaaecbbf9682a34fb2064e619154a7ec89f160911ebf`  
		Last Modified: Sat, 21 Jun 2025 03:23:33 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-28-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f20aa920d8d380b0e3e40533a0957d90e7d5a9393e6b396625d8b15b5d20cd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375163086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179348b4aac686052f650595d6dfd1a4e3d6c7ee80f9d097b4c5caf1d7614e5b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 20 Jun 2025 18:48:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_VERSION=25-ea+28
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='ddd476f5dc6e80fc93f06ba240cf3537fd8aed344823abfd64c1cfe470f441b4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfbc99aedd5015a5ab41d74f53972f7cb6616032c983216add8cf2de21a1fa5b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154371975b8325994bca32bb0a00994674b6beaa8c22ce78562c07918b7376b6`  
		Last Modified: Mon, 16 Jun 2025 17:52:18 GMT  
		Size: 18.0 MB (18014447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a7a9fc57f12c4382024916c520415bc085f8aba5fa10841cebd9f28adeccc3`  
		Last Modified: Sat, 21 Jun 2025 04:20:28 GMT  
		Size: 220.9 MB (220895378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-28-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f42ab6886c3991d189314ab3a3e97eaf4ed197fdfe9097b277bc0e195e5d835d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8820826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc753e8833d5f755a05c92bfd2bc4c2e73f129da0690ec03f28b7e61aeb020f`

```dockerfile
```

-	Layers:
	-	`sha256:116217dfcca6fb2caff24769ae9894f2316ac011af856e31c811b7654dedda8b`  
		Last Modified: Sat, 21 Jun 2025 03:23:44 GMT  
		Size: 8.8 MB (8802065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae2e0b0c425eafc9b45629cb49d2a1370366ecb43c24f3cf809f53cd4f3ea91`  
		Last Modified: Sat, 21 Jun 2025 03:23:44 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
