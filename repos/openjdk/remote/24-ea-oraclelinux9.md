## `openjdk:24-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:e972c77e92c22700d7b7c2010abf075373994a1e5aa828c4de8f73821f65e273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:7a5a1d2afa3a9a94b07c0f8dd674cca6a5d71248bdcec1f44449cbc8423831fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299792375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd2be6ae4495d46d1bf9a037e6235a6e60c399fe6272293bc565ce8f2019ba7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf79bae0630d45787fedb5fa953cc436dfc12274f55a4f452528c4b1ef7ab5e0`  
		Last Modified: Mon, 12 Aug 2024 17:59:25 GMT  
		Size: 39.0 MB (39047374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3725799aed99a347a32658dba672a4a23ef876e1e847c9ff71fc13c12a0851ef`  
		Last Modified: Mon, 12 Aug 2024 17:59:29 GMT  
		Size: 211.8 MB (211751265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f0d76ab4ccef6b262be79532509dcc5960501f3159aaa0eeabb82c60867ea94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4812f20e22dde0716831844048072798e46204267203326d81985ec3479e0bf0`

```dockerfile
```

-	Layers:
	-	`sha256:f6f4bddd91a09398ed5f92fe019a04b7206d988bd8ceb92761e6e11a7fce1195`  
		Last Modified: Mon, 12 Aug 2024 17:59:24 GMT  
		Size: 3.5 MB (3545977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:613d14a3d1edb71f7edff845d1a45a52f7da3fcd4984325f2ba72f6ea1cab775`  
		Last Modified: Mon, 12 Aug 2024 17:59:24 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c15c998838b3edb32de918bf31ac7f0da26c476a9a1cd02fbaf2602c23b7d995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296732116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dddc7a8d94ca4ecb80da85b22b98ca653e1ed4bbfa6d40de870a60b674a598`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12335bb1126bd80cd31b34b4fde93f2ccb7bb979403e778624cb60c3ece28c`  
		Last Modified: Mon, 29 Jul 2024 16:56:31 GMT  
		Size: 39.5 MB (39479870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a0a3983fbeb53dc3831ff1c0b6de018a7d416830f60d292b33cb0d580f0e37`  
		Last Modified: Mon, 12 Aug 2024 18:29:06 GMT  
		Size: 209.6 MB (209599585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:89ba66d189308793ed7fed583c49db2305794310ccbb07a55e6a073f251583ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e8882b9edb11850dc3777dc43ab2fce961afca9bcd0a7db0e4a29980e132b`

```dockerfile
```

-	Layers:
	-	`sha256:c32c7ce1e8379d45944da4f095d1ba1982ec6bf5492c00d5c55413034d33080d`  
		Last Modified: Mon, 12 Aug 2024 18:29:02 GMT  
		Size: 3.5 MB (3544360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba08e1d1442cdffbe04bfb5bc5d76f96b8a340f7521b75b361c2f4bd2ecf5172`  
		Last Modified: Mon, 12 Aug 2024 18:29:02 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json
