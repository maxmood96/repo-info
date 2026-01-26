## `openjdk:26-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:50e18ec188cb4b4602fb9f499a76c581b7b167f15483f1575a91e05170a25db0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:624a96bdd3a9b4e4e7543c343e5a04fe85a3dec23a81f8bab3a176045a60a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386711517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0d3985cf2ec88b48166bdd2a5ef7dde0c1710a4f5239d4b033686bf5738db9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 20 Jan 2026 18:47:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:47:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 20 Jan 2026 18:47:41 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:41 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:41 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:47:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc41e52022006ad1d8e8ddce9a5f4966b0397434a3c739c43b8fa3291fbcdcf`  
		Last Modified: Tue, 20 Jan 2026 18:48:06 GMT  
		Size: 16.1 MB (16062856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9749f1797f52cb0ebd7e594ef42094c1d66855329ce758b75156671a9ed7b0b`  
		Last Modified: Tue, 20 Jan 2026 18:48:10 GMT  
		Size: 228.0 MB (227962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:10b67c013983e858c3bbd29b357fa4f269ec561fcc309ab4940e25153e041936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306106e54b2a75d6102162d9bd1664969c61fc893c58840202047d1cd9eecb2e`

```dockerfile
```

-	Layers:
	-	`sha256:e5a20673f50108b596c3b4fbf3a4e2dac1f6acd96ac701220ef2cfcd9f7ba3dc`  
		Last Modified: Tue, 20 Jan 2026 18:48:05 GMT  
		Size: 8.5 MB (8511018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c493f92c6cb22e0341721109cfdaaf660ed61e84b8c498e7fc2d6b4134d27d7`  
		Last Modified: Tue, 20 Jan 2026 18:48:05 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:37d35a3383bad8ee6753dce3a3848ead700917f3300868ae3c56de32d292b472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384245976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ede6497c2bce5de60f60cbe52f5e98a196bd6b5847ae3900788850c2a10e1a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:09:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:10:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 26 Jan 2026 22:10:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:10:10 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:10:10 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:10:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:10:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:39 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9b61504e95f4e780984631244a34ed7a91a4196dccb8eac3dc6c8e7366b5b0`  
		Last Modified: Mon, 26 Jan 2026 22:10:36 GMT  
		Size: 16.1 MB (16071533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62125dab563d15a24bb05118e9c2d6ab108987dc1fe27ddf177b1b008abf6fb`  
		Last Modified: Mon, 26 Jan 2026 22:10:40 GMT  
		Size: 225.9 MB (225912211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0a7c2bfcaa1408c23963b0a1d2f75863fd236dd8d4c394ecef67e42532041cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39e0ca2e45f640fcc642e1f87dfb01def5499accd0cd64e018f36d73c7effc6`

```dockerfile
```

-	Layers:
	-	`sha256:28c31c87287bdcdcdf6fa66e7bdbe8728e6308c0837938db24c8fe4bc1a7f7b6`  
		Last Modified: Mon, 26 Jan 2026 22:10:36 GMT  
		Size: 8.7 MB (8705808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5098f8cdbdc24a2ab5d0e54f2c36b0824ccad729f2ef0a3f9130424b18539ffb`  
		Last Modified: Mon, 26 Jan 2026 22:10:35 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
