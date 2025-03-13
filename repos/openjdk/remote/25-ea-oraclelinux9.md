## `openjdk:25-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:2dd05d346409a05b117d9cc0aa1b4e4e1318ecb64ef8477c3c7768837b6fdff2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-oraclelinux9` - linux; amd64

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

### `openjdk:25-ea-oraclelinux9` - unknown; unknown

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

### `openjdk:25-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ee8647db245eacfa4f261aacb8658ddd1f1f4e68f4258a18373162e881bcf6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306458229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fd76a0f948a6f6b30cb5e41c2f7887494207df736e792619d1eb37e1e0c476`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 08 Mar 2025 01:48:16 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:ce92cb0849370fbaafa6ab88c7b03cebc3063fa56835d9dbf7d0b47c679a0097`  
		Last Modified: Thu, 13 Mar 2025 18:10:14 GMT  
		Size: 47.7 MB (47668022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4526627be0e2d666f68ddd55808801d398e443da5584c4a85a1289885b0191af`  
		Last Modified: Thu, 13 Mar 2025 19:16:07 GMT  
		Size: 49.2 MB (49185276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe89e4cd49bd7d20281d24b602225a57d31e225976aa02a3f0b3cf6855c2b593`  
		Last Modified: Thu, 13 Mar 2025 19:18:43 GMT  
		Size: 209.6 MB (209604931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f63fcf30649f62a25dd33d5829a165a78f6bca220445126c8a11c6910d163c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e16a5459d0c2f0250c7b25d561498b97aeaaed4f656c6213b9d18d5aea398f`

```dockerfile
```

-	Layers:
	-	`sha256:8f3c1dc0cbb933e52919906b51a3ef10d790d962ff54eddde3230518883c40da`  
		Last Modified: Thu, 13 Mar 2025 19:18:37 GMT  
		Size: 4.9 MB (4904775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7a48fc63c325c11c7b0eb3a33d0838e14339a91228519baa98b2bf10b8dafb`  
		Last Modified: Thu, 13 Mar 2025 19:18:38 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
