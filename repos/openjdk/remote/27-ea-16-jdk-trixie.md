## `openjdk:27-ea-16-jdk-trixie`

```console
$ docker pull openjdk@sha256:9ef6fd104ad4ab3f21274beda01f8c07e69c1f3963474883438bfb9b09053613
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-16-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:57c31149e676afd230ab55c25a966983ed1c3954789cd16f676d02d8444378ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387679078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7d75a71947e123f81fa9ccc2fa63100af76be9101dbcf1cccb523e4273630e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:24:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:24:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 07 Apr 2026 03:24:59 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:24:59 GMT
ENV JAVA_VERSION=27-ea+16
# Tue, 07 Apr 2026 03:24:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 07 Apr 2026 03:24:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11536b924be5cc7f5b8479a5e860b5c35f471b1e210b9154b4d1ad737af09f11`  
		Last Modified: Tue, 07 Apr 2026 03:25:24 GMT  
		Size: 16.1 MB (16064955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f610d818ae3535d0404bdf0fc2cd78fc6c2eaba331be70f14c708f82156b50`  
		Last Modified: Tue, 07 Apr 2026 03:25:34 GMT  
		Size: 228.9 MB (228913904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:576e6f98decba1c8d32801db062a2c5befac276b148b56d82f6a98f35d8cc87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8529048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecf7e98ebe2be1fdf45df7d35588b99e3c58226b8130aff007bb69b6b3f5bcc`

```dockerfile
```

-	Layers:
	-	`sha256:2e8db6ecba9c3503f72854e51a75672f0b9cf647989cdb4567392cbcb7161337`  
		Last Modified: Tue, 07 Apr 2026 03:25:24 GMT  
		Size: 8.5 MB (8511136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86804bf8205a6d24014e671ce0ccab4a96597ef47be4a501fc56ec1f7f5e93da`  
		Last Modified: Tue, 07 Apr 2026 03:25:23 GMT  
		Size: 17.9 KB (17912 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-16-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:95f8d6dd6c4f5352021cf8b5b2acb895ba8401f03730da09abd215449b20b378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.2 MB (385230748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4248442f7f8410aef775c9aa172ad8fbe2af542ed59c97957fdeb2973803a48d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:36:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:36:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 07 Apr 2026 03:36:59 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:36:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:36:59 GMT
ENV JAVA_VERSION=27-ea+16
# Tue, 07 Apr 2026 03:36:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 07 Apr 2026 03:36:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d13d7df20aafff202e9c92b95ec36cb6bcd2384623097f0b50f546cd6967ff`  
		Last Modified: Tue, 07 Apr 2026 03:37:29 GMT  
		Size: 16.1 MB (16071233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b6c3db016644a12028928dc09936b6ecd29898f98bcd01667ec3d723707b96`  
		Last Modified: Tue, 07 Apr 2026 03:37:33 GMT  
		Size: 226.9 MB (226878690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:60e7ca7332448ee4a6aa3d50a52e48f6d1623a7b01c185ad8d99f5cfa5e8019b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74916b06134e1000dbf7fd60a064f0cdcef7b3002ac2a77d505bd1c2cd8274f8`

```dockerfile
```

-	Layers:
	-	`sha256:a7143ab97be5accf76dcc652610ac3fbe59431be4858c655e543350d09ccb3b0`  
		Last Modified: Tue, 07 Apr 2026 03:37:29 GMT  
		Size: 8.7 MB (8705926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa14d2c7492079dd477ea155183aafd732e9e7250a66f43a1ab1f0bad5ff208`  
		Last Modified: Tue, 07 Apr 2026 03:37:28 GMT  
		Size: 18.0 KB (18030 bytes)  
		MIME: application/vnd.in-toto+json
