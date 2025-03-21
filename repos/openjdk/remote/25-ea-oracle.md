## `openjdk:25-ea-oracle`

```console
$ docker pull openjdk@sha256:c261319631e2956ea2a6c054ebe7b922d41e511f13de86f562c590cd28867167
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:918cab14dc02a366ed2badb858787d959266b10d39dbbee345e786eb7c9b2546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 MB (298999607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e312bcd67ba30538d61eb14b34a396115f50b5ef4c77a56c330b7c2bd23d5e8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 14:53:19 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 13 Mar 2025 14:53:19 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:804bb8ae89decacdf918af27c892df04e6f2d3038e3a7d1e34475eef6be9aba3`  
		Last Modified: Thu, 13 Mar 2025 17:46:19 GMT  
		Size: 49.1 MB (49091441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0596be43617a8c9e9e79b51b3274512eaffdfcaaca45ab74362f7fd6ca88462`  
		Last Modified: Fri, 21 Mar 2025 17:13:04 GMT  
		Size: 38.1 MB (38107618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141510402d39a46be96517f5884cb5095147abc48c7edaefa77936818d2415c2`  
		Last Modified: Fri, 21 Mar 2025 17:13:05 GMT  
		Size: 211.8 MB (211800548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:58a604691d1a0c4afa251d90dc35e0052f6ed9b9c21b4b3d7bff1b6879ee94ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c6e1ac83ab3fa293b190c35575838e7d7289395e109de3823b10569816d44c`

```dockerfile
```

-	Layers:
	-	`sha256:9e17cd7754be7e88a0cac697df3c6cee45dc5d17698998a0308c00becd059477`  
		Last Modified: Fri, 21 Mar 2025 17:13:02 GMT  
		Size: 3.6 MB (3622594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14a0cbe9d317f0cbd2e9e802e8b492c58e724ab02cf77e4d315319188657647`  
		Last Modified: Fri, 21 Mar 2025 17:13:02 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c0f86995ae945d25261dc4b78d878ce2bc0d1cb9a9720c64554e9466fce2de7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295925155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f333a6c56afb98ebbc5ab0be8c1ef20c77f139b57bd46a7c567a0e809100f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 14:54:08 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 13 Mar 2025 14:54:08 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce92cb0849370fbaafa6ab88c7b03cebc3063fa56835d9dbf7d0b47c679a0097`  
		Last Modified: Thu, 13 Mar 2025 18:10:14 GMT  
		Size: 47.7 MB (47668022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f603eee483e7db27118eb6e115b494f4c84c9e0787decd993290afbae16ae0b`  
		Last Modified: Fri, 21 Mar 2025 17:23:03 GMT  
		Size: 38.5 MB (38492465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12f1e1334eb337bc2bdfeadafc2719ce0800246af5a0634d00d1dc379f7caa7`  
		Last Modified: Fri, 21 Mar 2025 17:23:08 GMT  
		Size: 209.8 MB (209764668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6efc58c7ea1262b78e0a462c8ef450cf897510fdc82f32919ddebede4c0e7f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b288fc9a988215776c740f8fe65fa0b5d672824c0a275e318e6fb33633a0a2`

```dockerfile
```

-	Layers:
	-	`sha256:95b348eee88982a3730266551a4c6124290de9160de8f1043113a38c55284058`  
		Last Modified: Fri, 21 Mar 2025 17:23:02 GMT  
		Size: 3.6 MB (3620356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbaee2117cdde8e78057920b28762431ae9d4593883c26b9d4a5e8ec9c7c8468`  
		Last Modified: Fri, 21 Mar 2025 17:23:01 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.in-toto+json
