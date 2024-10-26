## `openjdk:24-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:504da412686a2ebaf80606541af1a3e96565ca0a72b0b836c5ba83c61f5764de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:6caea6f844db4a6822760b18bd62c6546c1a6a5c334a55070503719b54a6d264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300740740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2148aff4d2314014230e14e305a1a07dce93f56ec10614f95f20f1829179db06`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 25 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c67029681a2f1c745c3a73366080881b2d349b4ffb9ce6a4e1e4b2c423555c5c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='3850e8de3f5cc9a22fabc0963a04d6205a9f242cf2cfc0d67a4399a54deb725e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e5a6e09b05fe8c12aaa0ac0462acb6fabb55cb0eecfe0a234e805c264a1734`  
		Last Modified: Fri, 25 Oct 2024 22:57:21 GMT  
		Size: 39.1 MB (39059606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844decee220dea4540cf3a1400fe2297a0c650ce9f9d0cb738f1e2a4cea2d72b`  
		Last Modified: Fri, 25 Oct 2024 22:57:24 GMT  
		Size: 212.4 MB (212434192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:6c2525b46f54f9f3f6af7611a7b75a685cb474b1dce40e1cd6d75e2cde282377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f54eb9ad3a4e62128e15a4b963ec136c8f740f72cc796a9229495ef6f0eb0c`

```dockerfile
```

-	Layers:
	-	`sha256:e4bee69b67eacc58514e620a835e4786f6677a65083168c407b126fd781491de`  
		Last Modified: Fri, 25 Oct 2024 22:57:20 GMT  
		Size: 3.8 MB (3782205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9a4fd612173cfd2025ab8af1231fe86ca4e9ab4357562021a234952d044385`  
		Last Modified: Fri, 25 Oct 2024 22:57:20 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9927b06d333f71e5a096113e8bc2ab8c852a01ebe6549dad7ff67c0d7ae228df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297719771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1c5157d84587cec195c544830b5e282f3820fc2d2e6ac9474e0fdc77abf979`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 25 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c67029681a2f1c745c3a73366080881b2d349b4ffb9ce6a4e1e4b2c423555c5c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='3850e8de3f5cc9a22fabc0963a04d6205a9f242cf2cfc0d67a4399a54deb725e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5187f7dd7781df5062b2bba7d82cb17d632e10163993162b9a27e2dc6d310`  
		Last Modified: Fri, 25 Oct 2024 22:58:22 GMT  
		Size: 39.5 MB (39491106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f6972361acb5dc096171d7eaeb6b7067a870716c17b52d1eb22b53b754110d`  
		Last Modified: Fri, 25 Oct 2024 22:58:26 GMT  
		Size: 210.3 MB (210314082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:89fe1d5f07eaa588814e3dc8a4f7a01519bcdbb777059e6e48c7b4f68d8e3a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00de8427d680d0ceaeaa5c0b3a40dbc4f883e35accd273612e9a6e45944aad8f`

```dockerfile
```

-	Layers:
	-	`sha256:36fa0f411137de8096c3245ee2aa3b5b164fec77cabd2690cb75fdfb7ec074e9`  
		Last Modified: Fri, 25 Oct 2024 22:58:22 GMT  
		Size: 3.8 MB (3779341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5b027dab3a8f68ee631f2fc6eab9724a4d4de423cc54c3d629fdb4cc6b5aab`  
		Last Modified: Fri, 25 Oct 2024 22:58:21 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
