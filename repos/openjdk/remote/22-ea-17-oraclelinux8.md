## `openjdk:22-ea-17-oraclelinux8`

```console
$ docker pull openjdk@sha256:fb8dd9b4594fb3d627620e4109c2ee95919ee20ac7cb26e315317722f30695be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-17-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3c74b9066c34f3f2682e9a4ed517603abd2ed4064e3457639f04fb15a63b78de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265066978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d4d5729d13a46212b6c4bb426ac704eda6688457d649203eac5aca871dcf9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Sep 2023 23:24:01 GMT
ADD file:909c07f3bad92a80d3917d583769a01bf62c2cbf3dd24f450fb303b1db92a83e in / 
# Thu, 21 Sep 2023 23:24:02 GMT
CMD ["/bin/bash"]
# Thu, 21 Sep 2023 23:55:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 21 Sep 2023 23:55:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Thu, 21 Sep 2023 23:55:47 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Sep 2023 23:55:47 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 01:28:22 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:28:34 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='2e079b8de8557b2bfdf2c548f69cf0c8ed9a94e7a0460dfebbebb4bf936dea8b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5b70d1b43017fc00355d38e8f5c5f96d161033968968f76777189ffff3b5ff0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 03 Oct 2023 01:28:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5262579e8e45cb87fdc8fb6182d30da3c9e4f1036e02223508f287899ea434c0`  
		Last Modified: Thu, 21 Sep 2023 23:25:18 GMT  
		Size: 45.0 MB (44959147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eab4e2287a59db00ae2d401e107a120e21ac3a291b097faffb1af38a1bc773c`  
		Last Modified: Thu, 21 Sep 2023 23:57:32 GMT  
		Size: 15.0 MB (15031479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e4994e1d4b81a4a34fc9b26ddf652e560c70d4777a60bc1853d4e4e011869`  
		Last Modified: Tue, 03 Oct 2023 01:31:08 GMT  
		Size: 205.1 MB (205076352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-17-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c1e403293e083c17074b1bd6285aaf08a7527ddd175ac1ef88b3e55f688034bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262738923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a8390fa097a94d71f37f44b2bbee4ddb84ad1e7df82fb01b08c4bee05db0f6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Sep 2023 23:40:46 GMT
ADD file:c630310324edbc0dd09d0912b8e7074d17ac71b1be8a14af9663872c081c4632 in / 
# Thu, 21 Sep 2023 23:40:46 GMT
CMD ["/bin/bash"]
# Fri, 22 Sep 2023 00:02:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 22 Sep 2023 00:02:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 22 Sep 2023 00:02:00 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Sep 2023 00:02:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 01:32:45 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:32:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='2e079b8de8557b2bfdf2c548f69cf0c8ed9a94e7a0460dfebbebb4bf936dea8b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5b70d1b43017fc00355d38e8f5c5f96d161033968968f76777189ffff3b5ff0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 03 Oct 2023 01:33:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:286c1c922769d7608c32cf62931e95d7d169a0306164d24ce7d7a8a065959315`  
		Last Modified: Thu, 21 Sep 2023 23:41:39 GMT  
		Size: 43.7 MB (43657726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5f8d4b6eb464428f46a11bf9639aada6dca4156bdef2cbe73cb3f2d805f96c`  
		Last Modified: Fri, 22 Sep 2023 00:04:18 GMT  
		Size: 15.7 MB (15692651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d345319f6887e24146618b7509916cbf21808ff05179fb00604e9c1ca595f5`  
		Last Modified: Tue, 03 Oct 2023 01:35:15 GMT  
		Size: 203.4 MB (203388546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
