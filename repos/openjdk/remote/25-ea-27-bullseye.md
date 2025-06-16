## `openjdk:25-ea-27-bullseye`

```console
$ docker pull openjdk@sha256:01239651fed370f20f7efc85131bb9eac0d625077a81e9b0f4b39eedf8e28e3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-27-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:96f29fffc52284c11c724c48d373e7203e7e0070ac40576c418490478ce7b671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361432687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f1e3f73d2b45046bc5579c1af1a0969d4e6d02217cef1231231b3c1066e4fe`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e62d57731aac5ac8f4de4a69eaada3404bd8fb49a4eec6bdda22e5051064a206`  
		Last Modified: Mon, 16 Jun 2025 17:51:14 GMT  
		Size: 14.1 MB (14073178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53680ef832e8d4e781bf30fa4c4c9a046835bcc80c8b0ce2175881f2cd27e0fd`  
		Last Modified: Mon, 16 Jun 2025 19:27:56 GMT  
		Size: 223.1 MB (223082225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-27-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bb210c6265326233d11bf47b1f3effd61cb54c673ddc8ef7005c27646c31c814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c020c1160d7397a30e9e7b5d41a13e3a9a322e34d0268f843a126b96e64286`

```dockerfile
```

-	Layers:
	-	`sha256:4790ce797206beabd5e87a312b86bfb1f5a3547e9d5135efbf9219a6393696e6`  
		Last Modified: Mon, 16 Jun 2025 18:23:42 GMT  
		Size: 8.6 MB (8590832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ba0c99eaec3c2dac241263be3d1b8cd062bb43562da6913688995b8b38b0e17`  
		Last Modified: Mon, 16 Jun 2025 18:23:43 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-27-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6e53bcaa055c196dbec75013be9738553a4e7cf08f46db04b34fd1d39ce2e5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.3 MB (359268061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737d3a6bec735d6e3033c69ae791129795ef32baaeef6b4a0545d61c4b3e3cbf`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:f2fe81b4fa1d2df487b86a9ecf7a3171a53c5fb9a4b75ec5724a92684968a799`  
		Last Modified: Mon, 16 Jun 2025 19:28:10 GMT  
		Size: 220.9 MB (220884399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-27-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:691e4fddd80a633d82365abde9cbab9089b958a5522e927f252776cde7c93af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8710556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6db363e5b1817b990ef59f4876191041e661848781a2a43f6edc259ebf9fb7`

```dockerfile
```

-	Layers:
	-	`sha256:a8b125f0f628189292c11bf688b1c4a7111d826705d21e96a387a4d9a5d11a57`  
		Last Modified: Mon, 16 Jun 2025 18:23:49 GMT  
		Size: 8.7 MB (8691795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432ab7440bb2f3812b3274d14320aa244e6aa6637c07c58b046d24c79e82f18a`  
		Last Modified: Mon, 16 Jun 2025 18:23:50 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
