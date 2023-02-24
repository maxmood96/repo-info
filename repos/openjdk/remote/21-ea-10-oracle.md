## `openjdk:21-ea-10-oracle`

```console
$ docker pull openjdk@sha256:3a3c00c18f0fc2c8341cbff8944dfd8f21f22004098aea69eeb93cc562f7810c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-10-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:07f02c9be711e04f8ab59a4a40ab41d47abb5c2cdbd7b964540be886953c428b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256125648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7191613b0bb1eb14f9ae2f9356d1eece7daf36db5a3f526ea27ee17f4ff91223`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 19:56:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Feb 2023 19:56:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Thu, 23 Feb 2023 19:56:18 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Feb 2023 19:56:18 GMT
ENV LANG=C.UTF-8
# Thu, 23 Feb 2023 19:56:19 GMT
ENV JAVA_VERSION=21-ea+10
# Thu, 23 Feb 2023 19:56:29 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e60198534add038869d333ae9564ff8be298d712c5518b865952d66d07638b7b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='eb5e840f2f81330fa3080312da34ce1daabb27138bbebdbb5ea409d79a970e6c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 23 Feb 2023 19:56:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565fe2a72fd544bf059ba3dab17c20dd57232b65e41885f9004b841d0106f73b`  
		Last Modified: Thu, 23 Feb 2023 19:58:20 GMT  
		Size: 12.2 MB (12246468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cc176753cc1e165ecfba28a9a7c494cc15e2d19148b3529c58152e4125b66e`  
		Last Modified: Thu, 23 Feb 2023 19:58:32 GMT  
		Size: 199.3 MB (199326728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-10-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9ad6914095fa424c21552bb461541b2eb67da7b0e74af7f7b7e6e7249e97ea18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257113043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5b5cc1d0d344da569850b4859c32fe8aa7358db63a2ac8d33e5526997f6732`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Feb 2023 23:40:03 GMT
ADD file:b9db410ba951fb740a34187417442b96a27a7fd918b16023c16cb1b0777b292f in / 
# Thu, 23 Feb 2023 23:40:04 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 23:58:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Feb 2023 23:58:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Thu, 23 Feb 2023 23:58:52 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Feb 2023 23:58:52 GMT
ENV LANG=C.UTF-8
# Thu, 23 Feb 2023 23:58:52 GMT
ENV JAVA_VERSION=21-ea+10
# Thu, 23 Feb 2023 23:59:02 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e60198534add038869d333ae9564ff8be298d712c5518b865952d66d07638b7b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='eb5e840f2f81330fa3080312da34ce1daabb27138bbebdbb5ea409d79a970e6c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 23 Feb 2023 23:59:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf42ad2544e3a5379ea5e0050457e87df46409adba81dba4686a3efc595ccd2`  
		Last Modified: Thu, 23 Feb 2023 23:40:48 GMT  
		Size: 43.5 MB (43461050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2911a20ed1ec4cf4241519f3d97458f77a1eaded44c42d9ae79a999075ef4c`  
		Last Modified: Fri, 24 Feb 2023 00:01:00 GMT  
		Size: 15.8 MB (15838054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8a86db14f5eea970611f3dc7e7d3fe8468233991a556d80735dd9b4af7c626`  
		Last Modified: Fri, 24 Feb 2023 00:01:10 GMT  
		Size: 197.8 MB (197813939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
