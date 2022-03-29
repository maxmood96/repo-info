## `openjdk:19-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:5d1cf47d128b5ed0bf7b024cda95ab364be47899386c244a9610fc0bad0d616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c3adcf293e562de010bb63d5a42b242630490bb0a16c35fa2945a95e675b0994
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248841182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e157ef5b874585dfe38af77ada230434b0d0015606e2f0931c59fcba4cf4bf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 24 Mar 2022 22:26:17 GMT
ADD file:ebb4986af4fcca0d00738e77d2c814e70536c01a0e02eef98c71e9e3a56c0abd in / 
# Thu, 24 Mar 2022 22:26:18 GMT
CMD ["/bin/bash"]
# Fri, 25 Mar 2022 01:16:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 25 Mar 2022 01:16:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Mar 2022 01:16:47 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 01:16:47 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 00:51:23 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:51:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:51:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1de6f411eccf5041d90362d2d035abf0e59cf91dce4eacbc37ef0aa52f5b5920`  
		Last Modified: Thu, 24 Mar 2022 22:27:23 GMT  
		Size: 42.1 MB (42111629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbc239737191ccc9950c0b7c7a0aa6dac0a92906c45c8c72d511820cf4cd3b6`  
		Last Modified: Fri, 25 Mar 2022 01:24:51 GMT  
		Size: 13.5 MB (13530268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64458ab0f171b4f00c71c3d97205f7d23d50b4972f98ed2a5beb2c2fc8e13e6d`  
		Last Modified: Tue, 29 Mar 2022 01:02:48 GMT  
		Size: 193.2 MB (193199285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3ed8dc88c4683e019627226704c0c23d14018e3de59f1c35d58f0a5dc0397fe5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248396693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f6f901739d6bc4e497f2312296fd8ba01a235738270465e2ac3a9e6ac5e05a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 24 Mar 2022 22:21:09 GMT
ADD file:1eaca9dccdbe88c4fac0b484a625100443af30879cf6cba7b5615db77745b0c7 in / 
# Thu, 24 Mar 2022 22:21:10 GMT
CMD ["/bin/bash"]
# Thu, 24 Mar 2022 22:45:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 24 Mar 2022 22:45:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 24 Mar 2022 22:45:17 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 22:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 01:16:33 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 01:16:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:16:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c11319b13f376dfb3fa1ee22d0047cfb7157eba4ba2786653cb29ac6defcb93c`  
		Last Modified: Thu, 24 Mar 2022 22:22:26 GMT  
		Size: 42.0 MB (42018948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d7710250d8de942c9ab085f8642e5e854d0b85b2578079aa2a8f4aaac0bf73`  
		Last Modified: Thu, 24 Mar 2022 23:01:12 GMT  
		Size: 14.3 MB (14293656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efe9ab413014049e6eb2e57f29ee6aea9d39fba47a35abd2c01a21b9817b969`  
		Last Modified: Tue, 29 Mar 2022 01:35:52 GMT  
		Size: 192.1 MB (192084089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
