## `openjdk:19-oracle`

```console
$ docker pull openjdk@sha256:aae53c06c344a5cdc7fa12c17abad652d4267a376baa3e7aa678dccf7930665b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:a6ac8d51737acc785bdc5402145e4231c82d7b9ad36a837bf90dfda011e02c1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248851180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e129611dd9940131469f7a5203d13d888f3e3c5715c7151649c607e4d7af7543`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:26 GMT
ADD file:837f6c6e7e20067b92edb72e78a8399e6cbbd72dab23db7b5b5a301c58d2a0de in / 
# Tue, 14 Jun 2022 18:23:26 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:42:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:42:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 14 Jun 2022 18:42:55 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jun 2022 18:42:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 01:21:34 GMT
ENV JAVA_VERSION=19-ea+27
# Wed, 22 Jun 2022 01:21:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/27/GPL/openjdk-19-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='d88a9e824ce2c65fd634463856a6af2e8aad09a3b005a6ae9f3529b972d184c4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/27/GPL/openjdk-19-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7e93f0cde43b50161e5817e8a12907f5a2e74dbd63a4fa99d059ba4afdab02ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 22 Jun 2022 01:22:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f160c0f6cac587a73883b48a8857f5cce0930112792cef25c62510e256e93dc`  
		Last Modified: Tue, 14 Jun 2022 18:24:18 GMT  
		Size: 39.2 MB (39219730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb499df0377a2bd9163e9a611ce46b5379196826787392defef98dbf215a8aa4`  
		Last Modified: Tue, 14 Jun 2022 18:49:29 GMT  
		Size: 13.5 MB (13502563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db5c2cf3ed98a4f2edad869b3695e0bbfd88406d94c911a407d295634987d6d`  
		Last Modified: Wed, 22 Jun 2022 01:33:31 GMT  
		Size: 196.1 MB (196128887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d522472d12b768ecec0586bfd8c7fffd5a89dd396971886d90bb91a0fc0e5456
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247258647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1361b7314af96ed0ecf5797a89b333efc08c96a5002a31dcc5743644cfe351b0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Jun 2022 18:41:36 GMT
ADD file:4a6ee90ad73353bfb87b2f121e06bddaed6104536e485baa83fadbe7facc774c in / 
# Tue, 14 Jun 2022 18:41:37 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:58:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:58:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 14 Jun 2022 18:58:49 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jun 2022 18:58:50 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jun 2022 18:58:51 GMT
ENV JAVA_VERSION=19-ea+26
# Tue, 14 Jun 2022 18:59:03 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/26/GPL/openjdk-19-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='130143ba9c969760aa4aecba9cd2296887facde306841d69404dd1d1235b3d90'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/26/GPL/openjdk-19-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='cedaf6ebfab9a1a716acf5a65e0bfe298e0c965c70100bc91cc414a9fcf0b4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 14 Jun 2022 18:59:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2bbc1bf883bd601c0da5735b538963308bcc17f90d36525ecc93456ffad79064`  
		Last Modified: Tue, 14 Jun 2022 18:42:39 GMT  
		Size: 38.0 MB (38012371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bde7855ef536fce06527372a019087e1972db9d092b2ec88091b6017cfc5a16`  
		Last Modified: Tue, 14 Jun 2022 19:10:59 GMT  
		Size: 14.3 MB (14260872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc666805d6647b8626d8a172a04fc2f75d663ff6c019cc0cd2bf9800b6f6ed1`  
		Last Modified: Tue, 14 Jun 2022 19:11:14 GMT  
		Size: 195.0 MB (194985404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
