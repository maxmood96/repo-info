## `openjdk:27-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:b9d63fae7ef3024fa2dc40d60c4dd9bf2a8db95a9635a09f5b56dddf51f09470
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:ed641bb98317b4dd756979ea9db3397fd02ae7b74fd64c2738f7feefc38130cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 MB (386874983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4a215c46919cdf2d8ac7315b7fc939d1feb1ce7cd76165a7b327047da3964c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 16 Dec 2025 00:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:04:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Dec 2025 00:04:18 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:18 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf26f671821940e7147868a9aae8dd8c2fd2900796ecb476cd0b937575cda93`  
		Last Modified: Tue, 16 Dec 2025 00:04:56 GMT  
		Size: 16.1 MB (16062743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12729cc06a85cbd0b7361ab3b45c9c9a45fe50370b67bd0c96b17a360d1a7e`  
		Last Modified: Tue, 16 Dec 2025 00:05:21 GMT  
		Size: 228.1 MB (228130210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ec3fad2185fe48159310620f44be41d3f56081d74f681fd5ad394957e6b56f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586f4cc553c3f82aad8a1c93ee08130ead6804fc3e50159a6d6ac6d864497483`

```dockerfile
```

-	Layers:
	-	`sha256:1ccdac194fa4d09db349a80af847507458b03a5cd2d7c2433a28fbb53509e131`  
		Last Modified: Tue, 16 Dec 2025 01:27:10 GMT  
		Size: 8.5 MB (8509969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa586a5e74deebe4c0e900c9c7f20fd00e68bcc4f46e80ff0719fc3cf03e3d6e`  
		Last Modified: Tue, 16 Dec 2025 01:27:11 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8f28bd538f1bb479200e97c446bba38737290bb71c23eaa5004047d11f52c924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384381464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd4240d5e79a469463b2f4f175994d33eef559a391fc5231378f256ac7a51dd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 16 Dec 2025 00:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:04:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Dec 2025 00:04:05 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:05 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:05 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a75f81fa46df2ee909810df114ec4a3fe57077e99d250e3861daa688b3aa0fe`  
		Last Modified: Tue, 16 Dec 2025 00:04:43 GMT  
		Size: 16.1 MB (16071478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98238303f584076bccf56e61e1ccc5ca96d3b9d81973aed738c578773bcac45`  
		Last Modified: Tue, 16 Dec 2025 00:06:11 GMT  
		Size: 226.1 MB (226053805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:af4a8592d3d4eec0d8dc78503219200d10d68a4157ded14c549ccb1753805503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7821a9dfe8c93b1ccc1a7b64f8f92a74ed91eb1a4a24dd5b9775bce1ec05426`

```dockerfile
```

-	Layers:
	-	`sha256:6b457f1812ad307449362aacbd4a3f7020382ba83e40dc567df25f530fd4a7f6`  
		Last Modified: Tue, 16 Dec 2025 01:27:19 GMT  
		Size: 8.7 MB (8704759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9964807c9aaca3cf9adb099451096f0848451b239d93f7848d5be11b3e63df18`  
		Last Modified: Tue, 16 Dec 2025 01:27:20 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
