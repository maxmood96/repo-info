## `openjdk:20-rc-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:dc0c1f921a58da8c499d74102ddda08bba4beb015980bc9b14cfff9584c4b044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-rc-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:67787c1e11dc2ac303e95340c1a9ce6707cd1674b3b1b48f675bf008c6cde710
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257697952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb622fc92bbb51cc5c88e88f3bcaa249eb140a988866c72490eaaa294d6e1ad`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 24 Feb 2023 00:20:27 GMT
ADD file:9c8b13ccecebc19a9105d94b9b8060d87741d158a6de27ec96b14028de164443 in / 
# Fri, 24 Feb 2023 00:20:28 GMT
CMD ["/bin/bash"]
# Fri, 24 Feb 2023 00:40:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 24 Feb 2023 00:40:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 24 Feb 2023 00:40:45 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Feb 2023 00:40:45 GMT
ENV LANG=C.UTF-8
# Fri, 24 Feb 2023 00:40:46 GMT
ENV JAVA_VERSION=20
# Fri, 24 Feb 2023 00:40:57 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz'; 			downloadSha256='bb863b2d542976d1ae4b7b81af3e78b1e4247a64644350b552d298d8dc5980dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-aarch64_bin.tar.gz'; 			downloadSha256='b671dd1513e7bd4f3de6b1424a90a4998997a67593bf259936d55f5e83e31959'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 24 Feb 2023 00:40:57 GMT
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
	-	`sha256:491ff468a9965309ef7f11740e94a4b8487174329cf93196161ac71df75b42ed`  
		Last Modified: Fri, 24 Feb 2023 00:43:30 GMT  
		Size: 198.1 MB (198126088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-rc-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3b590fe684765d114188c4afc5194dd899113fd8c0883fdc4ebbb5a3a47ca5b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255926719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b68bc9c7fd15a512c4f4d7c3bba6ed31ee37837261bb89572f8ba978be80624`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Feb 2023 23:40:03 GMT
ADD file:b9db410ba951fb740a34187417442b96a27a7fd918b16023c16cb1b0777b292f in / 
# Thu, 23 Feb 2023 23:40:04 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 23:58:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Feb 2023 23:59:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 23 Feb 2023 23:59:17 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Feb 2023 23:59:17 GMT
ENV LANG=C.UTF-8
# Thu, 23 Feb 2023 23:59:17 GMT
ENV JAVA_VERSION=20
# Thu, 23 Feb 2023 23:59:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz'; 			downloadSha256='bb863b2d542976d1ae4b7b81af3e78b1e4247a64644350b552d298d8dc5980dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-aarch64_bin.tar.gz'; 			downloadSha256='b671dd1513e7bd4f3de6b1424a90a4998997a67593bf259936d55f5e83e31959'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 23 Feb 2023 23:59:26 GMT
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
	-	`sha256:0eb14c31d1bbe3445069886c7ae16975d2fd32ef20ea20ff1e88571f61ea9c91`  
		Last Modified: Fri, 24 Feb 2023 00:02:05 GMT  
		Size: 196.6 MB (196627615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
