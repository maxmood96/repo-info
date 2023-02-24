## `openjdk:21-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:468d8b185a4e53e83326d5d03b4fc390d62dfd4ff817530470c04d39140c2683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:0cdff385bb2ee77031815328e9812f2230f461ca628d954726f2d7db4aa6140f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258898748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e4864e5404aad23a4cad00d9ff32e0e9935af4fd54b2f98693106777c3c492`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 24 Feb 2023 00:20:27 GMT
ADD file:9c8b13ccecebc19a9105d94b9b8060d87741d158a6de27ec96b14028de164443 in / 
# Fri, 24 Feb 2023 00:20:28 GMT
CMD ["/bin/bash"]
# Fri, 24 Feb 2023 00:40:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 24 Feb 2023 00:40:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 24 Feb 2023 00:40:14 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Feb 2023 00:40:15 GMT
ENV LANG=C.UTF-8
# Fri, 24 Feb 2023 00:40:15 GMT
ENV JAVA_VERSION=21-ea+10
# Fri, 24 Feb 2023 00:40:25 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e60198534add038869d333ae9564ff8be298d712c5518b865952d66d07638b7b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='eb5e840f2f81330fa3080312da34ce1daabb27138bbebdbb5ea409d79a970e6c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 24 Feb 2023 00:40:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b4ddc423e0463a3d58b6c40ac1d97a950af62e9db703bb4c9d55afad67394149`  
		Last Modified: Fri, 24 Feb 2023 00:21:21 GMT  
		Size: 44.6 MB (44556861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f918ee7b32337dedda10e8566b1e5d96678ad53c0527e878e3866a6f713189e`  
		Last Modified: Fri, 24 Feb 2023 00:42:24 GMT  
		Size: 15.0 MB (15015003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10eb6e59d815f3fa7e277c72fe1822dfdc92d5b4cba30664944cba50bfd8a31c`  
		Last Modified: Fri, 24 Feb 2023 00:42:35 GMT  
		Size: 199.3 MB (199326884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-oraclelinux8` - linux; arm64 variant v8

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
