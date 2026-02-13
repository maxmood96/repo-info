## `openjdk:27-ea-8-trixie`

```console
$ docker pull openjdk@sha256:c7f3ad4a9347d5039c78d2517f5a2bd275895e1ff86b0c57977404c991cebff9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-8-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:2108bc459920c9de0279519474b1053ee6bfbe90a3f996635c1d3bb14fc0f167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.2 MB (387199611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4106fd606879fc165487b9a8816c069a6ab4b27e69b846a915a65240e64c3ae9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 00:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:11:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 13 Feb 2026 00:11:07 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:11:07 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:11:07 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:11:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:11:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e2021c4c8bd1a46b34d9608a9381afdc333600ee1ef3c94306ecf7373e1956`  
		Last Modified: Tue, 03 Feb 2026 03:29:16 GMT  
		Size: 67.8 MB (67787365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa2e44b700bbae72ffea1b2d9059db6fe582c400cde123727e7b7dd82aee983`  
		Last Modified: Fri, 13 Feb 2026 00:11:32 GMT  
		Size: 16.1 MB (16062921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b0a40823bf0cd34c6330d0c7bd5cf2f871e28d726885a749aa972f96fe6321`  
		Last Modified: Fri, 13 Feb 2026 00:11:36 GMT  
		Size: 228.4 MB (228442363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-8-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a6cf639f18d565e2a17a0b7999348a093385e6678505309651d38f4a5d3b34c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1f05af481a1f7ef27a33c91f7f54ed26c3b924554f982be2bb46f50a60c1c9`

```dockerfile
```

-	Layers:
	-	`sha256:0cb7d49c74cee280a797e51c31be7bf47542b8a627df0bdbe891a310ede403a1`  
		Last Modified: Fri, 13 Feb 2026 00:11:32 GMT  
		Size: 8.5 MB (8510389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba0fc0dac358235866c7ca3b2f9942832ab7d8f3694af06b9a9fcae592e16b1`  
		Last Modified: Fri, 13 Feb 2026 00:11:31 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-8-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8310d03061f3264b1b48dd4c9f8f912014bce141388d25337f46c3a4ee61bdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384718423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f126add41743681ee36128cf4603a3903a2bc52304e7e49026d677f9dbfaa15`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 00:02:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 13 Feb 2026 00:02:52 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:02:52 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:02:52 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:02:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:02:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8128ce97ccffb1094b6eafc78b5827499d0496944f3d357e222bfc29f01968`  
		Last Modified: Tue, 03 Feb 2026 03:47:30 GMT  
		Size: 67.6 MB (67593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d854728ce137c07e57c4cbceb3c6ca4ef7852b116a6bafc2d84c00defdcd4108`  
		Last Modified: Fri, 13 Feb 2026 00:03:18 GMT  
		Size: 16.1 MB (16071606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee45b6899400bd5df7d1766136fa6331461f526b6c63ddb46ca5717a847d400`  
		Last Modified: Fri, 13 Feb 2026 00:03:22 GMT  
		Size: 226.4 MB (226379107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-8-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:110427d31d42ca5fd6e65ec86929f9696c7b9385c5a7142af3ec5149f1e31259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ecdd736a02c09b321904da62ff2c25fd6123b5ad49fb289d61058b87b0df14`

```dockerfile
```

-	Layers:
	-	`sha256:12b88aebb92491cc0c13e3a72cd0bf06aab24824e170e341c8086290041d56c1`  
		Last Modified: Fri, 13 Feb 2026 00:03:18 GMT  
		Size: 8.7 MB (8705179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24f3041b412fa6fcda36831f421ceac548e00fb988c7449cfbc1c663ecb3dc0b`  
		Last Modified: Fri, 13 Feb 2026 00:03:17 GMT  
		Size: 18.0 KB (18014 bytes)  
		MIME: application/vnd.in-toto+json
