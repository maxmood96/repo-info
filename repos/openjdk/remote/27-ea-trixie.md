## `openjdk:27-ea-trixie`

```console
$ docker pull openjdk@sha256:22bbb16798126619836ec5caffbc4a1e7cf1428043d5ab1b9573d7af75093291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:e101d73659462619dd79c56a9e16a8672e5b64904b259fe1a85a9bdcde0a4c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387527215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e530a2020e8f2b9a77dc7f334968561906ccb257ace8866f831429e342bc853`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:15:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 22 Apr 2026 05:15:29 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:15:29 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 05:15:29 GMT
ENV JAVA_VERSION=27-ea+18
# Wed, 22 Apr 2026 05:15:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 22 Apr 2026 05:15:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fa8a51a54ac3e15b4119d7c35ee258effe588942aa533bcfe6a7b0a99e7b31`  
		Last Modified: Wed, 22 Apr 2026 05:15:52 GMT  
		Size: 16.1 MB (16064928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771e7e3c9d6eb955f280402b2bc0533ee3c09889f375f7f872f64c750ba7adf`  
		Last Modified: Wed, 22 Apr 2026 05:15:57 GMT  
		Size: 228.7 MB (228747653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:bf53c1a788629f969d1efa920db2df2463d075d8ed2ed4b013559d922528eab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6decdf35f86ae8dbce13b6e2726aaec9c2f6108f36d263d9c524ceff26ffe989`

```dockerfile
```

-	Layers:
	-	`sha256:45e016b75a6ec88784b0210414d340b069409380ca9e9e435b2dff58310ba556`  
		Last Modified: Wed, 22 Apr 2026 05:15:52 GMT  
		Size: 8.5 MB (8509920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49c5c6839218229233e5b8a6d167d64887e8d88981dabcd8d3345061a4699f50`  
		Last Modified: Wed, 22 Apr 2026 05:15:51 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d0aac91c419d4ac48cbf6a1d0b085b5a9126a20c73abd464da3964c0ae58c8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.0 MB (385049850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae83580fb9b6482d7e8f734f7205756646e7da1543534b8f2f6f073e9d4dfe05`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:18:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 22 Apr 2026 03:18:41 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:18:41 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 03:18:41 GMT
ENV JAVA_VERSION=27-ea+18
# Wed, 22 Apr 2026 03:18:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 22 Apr 2026 03:18:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b777bf3d6a13ca1d6c0ef078da232f3c8a68ed9ad6fad8638a6aed6e2b2ef37`  
		Last Modified: Wed, 22 Apr 2026 03:19:07 GMT  
		Size: 16.1 MB (16071181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878f2c3b4c66fff389276e6586eca32f060e14f32aaadc16d757cea03ba1b36`  
		Last Modified: Wed, 22 Apr 2026 03:19:11 GMT  
		Size: 226.7 MB (226701280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:867519a52b0cbd77f2de896e8c18be188723113dd162ec73bb9a6b67105a59be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1f31cfde92c295a2fcfe95b6fdd010f11cb6bbdc50938e3d3a6dfb9f7e7d2e`

```dockerfile
```

-	Layers:
	-	`sha256:479dfb3fc38828bb36aa3b503c0a4fc4f9ddafb2eaeff83c16cf1d5c04516795`  
		Last Modified: Wed, 22 Apr 2026 03:19:06 GMT  
		Size: 8.7 MB (8704710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cea83bace62d28c74f9c27bb66eac090472ada4443aeb3fa2d78fd88a079fd9`  
		Last Modified: Wed, 22 Apr 2026 03:19:06 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
