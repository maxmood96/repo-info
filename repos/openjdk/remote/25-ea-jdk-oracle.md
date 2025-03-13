## `openjdk:25-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:41b145e5d775b247df8f4bc70862868bcc5b2b6dfb78a987f6eba25e921972f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:3da1551ec6ee3b1b8579018055cf0c7678d0e62a5a74dc63ebd147e70c9b70a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309504711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c32156608c49e8438a558933f5d3300f0daa45152f95d50d36aeb1e0f5bee5`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 08 Mar 2025 01:48:16 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["/bin/bash"]
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 08 Mar 2025 01:48:16 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 01:48:16 GMT
ENV LANG=C.UTF-8
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_VERSION=25-ea+13
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='456a1dced4795cf35e28459b6289a9eb1d6921f83c79cf460c5c694cb52e11ba'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='518a0d1c64c68f4563c167e052f135827c1b218933dd68a481a7973694fc64b2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:804bb8ae89decacdf918af27c892df04e6f2d3038e3a7d1e34475eef6be9aba3`  
		Last Modified: Thu, 13 Mar 2025 17:46:19 GMT  
		Size: 49.1 MB (49091441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b26f6926816e86d12e6c9ee6a4df860b8d3afda6c18fa1bc1c4dc10e4eef8`  
		Last Modified: Thu, 13 Mar 2025 17:52:59 GMT  
		Size: 48.8 MB (48759075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7afba0b90f4583b25efa2fb6524a885f9a1eddb8093108b7d6a00e9de53240`  
		Last Modified: Thu, 13 Mar 2025 17:53:01 GMT  
		Size: 211.7 MB (211654195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:22238bb67e2e602534ba124e55ac3df12edde0fad369cac510187494903ce1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19d1c88735864e9a69eee31b8b5a4a335b8e08722e7a545e57880bbe7e96672`

```dockerfile
```

-	Layers:
	-	`sha256:d54587971553d16cd16b85c7e7361f7cddc02a413841a6ea734af6c7da74fb29`  
		Last Modified: Thu, 13 Mar 2025 17:52:58 GMT  
		Size: 4.9 MB (4907013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bab8a84f4e65630f7ad593d7dd0f83e62ee09a73f2101a48e79e630e7c73a4d9`  
		Last Modified: Thu, 13 Mar 2025 17:52:58 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cd5e8f03fb5274635da5363694cc129e63c6d267a242c331217b47aa635c39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306462135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34afbbe17763157efb72d7468a6700defc8f66991c00a918a6459446eae3b2b8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 17:39:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 17:39:49 GMT
CMD ["/bin/bash"]
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 08 Mar 2025 01:48:16 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 01:48:16 GMT
ENV LANG=C.UTF-8
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_VERSION=25-ea+13
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='456a1dced4795cf35e28459b6289a9eb1d6921f83c79cf460c5c694cb52e11ba'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='518a0d1c64c68f4563c167e052f135827c1b218933dd68a481a7973694fc64b2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 06:45:29 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b0d69a874386856ef53a0253c98018d354dad7da9fb44540d22e351f1c97ae`  
		Last Modified: Tue, 04 Mar 2025 22:06:08 GMT  
		Size: 49.2 MB (49187852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1b576a3d0e8e028f14c74317feac5254c9e2b5807b7025f656da677af208c`  
		Last Modified: Mon, 10 Mar 2025 22:03:35 GMT  
		Size: 209.6 MB (209605068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:92cfdfe57ca32c28b2d41ffc7dc0857e9e70158fc3a046988c8d54fe6f421d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15501a78252234ca5498927b41dc6dfc469850eeb0a8bad720bd352aa1f501a0`

```dockerfile
```

-	Layers:
	-	`sha256:cd3f6dd36e10b8932fc359e482ed2ac7f5791322ab5ce4fe68b1fad47518956a`  
		Last Modified: Mon, 10 Mar 2025 22:03:30 GMT  
		Size: 4.9 MB (4904775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a304790d04e57bf89d70c59e5074f92a939e03db4c348361d03f22375a1ff3f`  
		Last Modified: Mon, 10 Mar 2025 22:03:29 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.in-toto+json
