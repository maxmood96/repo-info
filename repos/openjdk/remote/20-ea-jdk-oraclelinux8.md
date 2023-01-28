## `openjdk:20-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:2201e97dd1b0880e0be7cea5a7db82ed22b59fdfc159241868c561239d38eba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b92a23e139bb602ed331d2c45cbabb0580c357063a10791108c82c182bae37c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254931236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d314285061a477b3117a0dcd8de600e26d84297e497d159cc2253e0395ba2b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:12 GMT
ADD file:f2aead35bfc542632b7274d3b1132eb2bb3752d6cb61414febbffb746120622c in / 
# Fri, 27 Jan 2023 23:36:13 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 23:54:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 27 Jan 2023 23:55:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 27 Jan 2023 23:55:14 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 23:55:14 GMT
ENV LANG=C.UTF-8
# Fri, 27 Jan 2023 23:55:15 GMT
ENV JAVA_VERSION=20-ea+32
# Fri, 27 Jan 2023 23:55:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/32/GPL/openjdk-20-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='d512d0c5bfbde4b2346f3621c14aaac435c37802278da117f3f2c886c6d6cfbd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/32/GPL/openjdk-20-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b2eed07f28c6044c249ddf660781540983a90c269d8c1dce073881b5d0a75da'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 27 Jan 2023 23:55:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:39fbafb6c7ef40878b859fd0e4475c5ebd2ddfa8ed785a588594e8731b7cd0e8`  
		Last Modified: Fri, 27 Jan 2023 23:37:50 GMT  
		Size: 44.6 MB (44561081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70086a6ca030344addd4b8e51d50d209385d29d8e70c28a102f5d9668e8535b9`  
		Last Modified: Fri, 27 Jan 2023 23:59:16 GMT  
		Size: 12.3 MB (12251614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e370bada0eaee5ce4c6c174ef22d20c9f0f681e3d02303f977c33c357df88d29`  
		Last Modified: Sat, 28 Jan 2023 00:01:11 GMT  
		Size: 198.1 MB (198118541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fbc2a5b8364625692ee9bfd8f4255ab4baa581b24482e3d4669e104dae011c79
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253149030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366c9450f07ad63de799fa18ba3a9669d85d3288d5757ccae20e3f3cf6fc878a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 22:41:06 GMT
ADD file:63b5b4161762e1845c1eb2bb2c967a07179819b4a1f12ab7596d9c6bd15c9cbd in / 
# Fri, 27 Jan 2023 22:41:06 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 22:58:45 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 27 Jan 2023 23:00:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 27 Jan 2023 23:00:03 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 23:00:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Jan 2023 23:00:03 GMT
ENV JAVA_VERSION=20-ea+32
# Fri, 27 Jan 2023 23:00:17 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/32/GPL/openjdk-20-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='d512d0c5bfbde4b2346f3621c14aaac435c37802278da117f3f2c886c6d6cfbd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/32/GPL/openjdk-20-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b2eed07f28c6044c249ddf660781540983a90c269d8c1dce073881b5d0a75da'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 27 Jan 2023 23:00:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d26cdabfc8c6a31055d655a58d8a8f9757f43e1ce58451b8b6b02c5dd6e6d482`  
		Last Modified: Fri, 27 Jan 2023 22:42:28 GMT  
		Size: 43.5 MB (43456742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175fa1491e9fc183c9d73f4393db52b943e03e50258cf81fd2c6970905be7318`  
		Last Modified: Fri, 27 Jan 2023 23:04:19 GMT  
		Size: 13.1 MB (13068665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e67959b28d820987c18251ac9a9df5bdad0dd5a3ac7686c4f454e9c26c0554a`  
		Last Modified: Fri, 27 Jan 2023 23:05:51 GMT  
		Size: 196.6 MB (196623623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
