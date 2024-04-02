## `openjdk:23-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:abeea1b3c2d08d4c5c36a44fde22856d34935a98c147409b2eba4bb73f5f3a4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:2b2237a95f0f18d786f7186d322da908a39be85c0ecbb1070822ee6aa9ff591a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277187114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaffc3761c1db92c9ef9ed3e15fc539bf0257d0157a5863beb8f880ac05e44be`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 29 Mar 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+16
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='9a5d2039ec965c15d80dbc5106c9e2f1c4a80975e18d308b55f0a3d892f24358'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d654c940f0c5b9ed7549f29066599b2caedbaf2ec45f3745ac35e265c288e2d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59d1cfd97757d15b1e28b34717feabd5f55c5f52d10a5ab6c4507303b3fd9e8`  
		Last Modified: Mon, 01 Apr 2024 23:50:32 GMT  
		Size: 15.0 MB (15024005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597c62fb615b7c97a111479fbe207013548d6b234e7b3e362d239a6a2620d6fb`  
		Last Modified: Mon, 01 Apr 2024 23:50:35 GMT  
		Size: 210.8 MB (210835689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e26524428a02ba5b0273869296c8e05932593ca084ff1e9bf24a48b155875a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eadfc3a9d40011fdffe2148105cb4b600bd68c8436f099f8e274424cfab84e4`

```dockerfile
```

-	Layers:
	-	`sha256:b800aae85080d1e02f960563586aa864299430f6ab7788723514cb671e8dc45b`  
		Last Modified: Mon, 01 Apr 2024 23:50:31 GMT  
		Size: 2.3 MB (2267498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173afb7d9318d23888cec5fd2c28142316f6ab2121de9bc91ea50c19d469d1c6`  
		Last Modified: Mon, 01 Apr 2024 23:50:31 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1717133ae164a23119606d246cbcbd49d5e71258dcf99ca742e40ea000883177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266375464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c02dd472bdc5f5dfd753444ca7acac2a373bbfea27120350535c33eaaa8879`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 22 Mar 2024 18:48:16 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Mar 2024 18:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_VERSION=23-ea+15
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='c17995b5c67b845af47704e2a664f5b6ab540f968cfae06972a7562144b7634a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='804a15db8c406a0d70ad5a2da125339de3ff66759107fdd75bc6323d6d0cc5d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d68f32ba337d0cf2080b7122389f26b960df4be750efce6ce2c697e964cb10`  
		Last Modified: Sat, 16 Mar 2024 15:52:13 GMT  
		Size: 15.7 MB (15689247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1960df209637b4caf792450f0fb94da3f5114b453b4f7ba54c740e17e5c8a2f6`  
		Last Modified: Mon, 25 Mar 2024 19:55:42 GMT  
		Size: 200.6 MB (200613303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:81c96504eabff37adaa487d7f257bbc78fca8f19c28589dd76692dfcacabe6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7819b446e55fcef462c9b587f96ee3f0e41de572919ff84e2f74c67b83c1dae`

```dockerfile
```

-	Layers:
	-	`sha256:9446faa3085bf8bce1e0b5bfcd3ddb90071c8c8bbfbfd4597bde443e1508d364`  
		Last Modified: Mon, 25 Mar 2024 19:55:38 GMT  
		Size: 2.3 MB (2265910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee7a55abcacc498925d1488122626014724b19e4d35eea0fe31b30277da17ead`  
		Last Modified: Mon, 25 Mar 2024 19:55:38 GMT  
		Size: 16.0 KB (16027 bytes)  
		MIME: application/vnd.in-toto+json
