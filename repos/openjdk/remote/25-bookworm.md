## `openjdk:25-bookworm`

```console
$ docker pull openjdk@sha256:86710f2e526b986f6354023b8c53ddd9bb9e5a3c15743d6637e459c009223d37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:40d04a64030c35e75f415faf2efb6dd10d48e1dc8732fd3e6cbb2195626c9668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.2 MB (377239924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310e06a59addf7ce0ffa9b1369479583644f2f76c53a22c7dd3cb8b1201ab80`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
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
	-	`sha256:b7093ce84eeeeed5e55c80b4c2ff5753b237deace8361df70e0aacd49a7fda22`  
		Last Modified: Mon, 16 Jun 2025 17:51:31 GMT  
		Size: 17.2 MB (17227503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d342b976d4e0d8126a51bda8ce3b45c6c17b07b3625e0e29db0bff135b4bb9`  
		Last Modified: Mon, 16 Jun 2025 19:03:48 GMT  
		Size: 223.1 MB (223102647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:cf79cdc528630e50d70944f5ad5351bd34a897a700367f717a161452a3277a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8683814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c027744a5e20ee3e99bb67d7c58f423aa984680797fcbfc80751521a15105ec1`

```dockerfile
```

-	Layers:
	-	`sha256:33ca296154ceda6d627b948ca569da24995776114000aa35bdb9519441a2673e`  
		Last Modified: Mon, 16 Jun 2025 18:23:37 GMT  
		Size: 8.7 MB (8665196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f99b7a23447c35b3492649bccf6bbf5f767973dcc6fe7b2ec6cf95551033b4`  
		Last Modified: Mon, 16 Jun 2025 18:23:38 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5287420130cd9265553148067d88a5b17d667d942e55c64afa100cea1421f9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.1 MB (375148214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e627ff8a60e3db7b18cf47c7aea82f22575ff61615303af60ecec83cc134e5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
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
	-	`sha256:6233123d95a3ecec6c398f100175257c19a8a177185aa310752bb8657f6b5c83`  
		Last Modified: Mon, 16 Jun 2025 19:23:15 GMT  
		Size: 220.9 MB (220880506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8a7ea652fb267bb931c30ba827fd43ad35038f1b11b7c6a978d0294e4cceb032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8820826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58496424c8bb0e65cddca517dce7aadb7760e3ae139dfe336b3d0c388b59924`

```dockerfile
```

-	Layers:
	-	`sha256:06bf844c1e17e01af9a614c3143b97306fe11c6c08a609f5bacf01a883c0a461`  
		Last Modified: Mon, 16 Jun 2025 18:23:48 GMT  
		Size: 8.8 MB (8802065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca756ff11c553e62059b433bd86f81c3031ed0623425c9055d7a9aa23a25c5fd`  
		Last Modified: Mon, 16 Jun 2025 18:23:49 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
