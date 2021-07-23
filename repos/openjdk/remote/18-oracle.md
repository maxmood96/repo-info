## `openjdk:18-oracle`

```console
$ docker pull openjdk@sha256:f3f29427e5e0cebf4870495b5e6171bdfd72fad47c728a8f8142af5afef8e90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:b9e42f281115a8ccf82b912d2f88b631c82c9261b0f37f79f6b7f8be207def43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243148226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb1cc4e7f7f2317cc7499a9375225a0205f957a09bbcf3267af2688d098acbf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jul 2021 20:20:57 GMT
ADD file:c830de449b9ecd90e02f56d99e8326701da17970fa314bd7b060fd9a7cf7ac77 in / 
# Mon, 12 Jul 2021 20:20:58 GMT
CMD ["/bin/bash"]
# Mon, 12 Jul 2021 23:33:03 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jul 2021 23:33:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 12 Jul 2021 23:33:04 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jul 2021 23:33:04 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jul 2021 22:20:30 GMT
ENV JAVA_VERSION=18-ea+6
# Thu, 15 Jul 2021 22:20:52 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='13bb69d5907c906e8b9347e531919e17c54f6505cbb4c5fcde71f358b8afac15'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='821ae9c92e8ef55f8cc0671cff324e7e866ee1acbb2d0a86f90b009b35d11925'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 15 Jul 2021 22:20:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c828c776e142cb23ad61c84403bb42deaa97efeda5e2b600df46f7dbd38ec681`  
		Last Modified: Mon, 12 Jul 2021 20:22:25 GMT  
		Size: 42.2 MB (42179737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8846dac42cae4499c0917b5bd5e81c0e6d6fcc5326d50972b3faed7ccdf688b8`  
		Last Modified: Mon, 12 Jul 2021 23:41:34 GMT  
		Size: 13.4 MB (13392657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687cc0badf0d77dbb8657d953b38fbb85f37e5df3e1973fa29702d55a7cc7f40`  
		Last Modified: Thu, 15 Jul 2021 22:27:57 GMT  
		Size: 187.6 MB (187575832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b6b66fa6adf822be51a001b7e198893e6633d21264bdda0598443d3d8ecb671e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242520925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a042648613cc637f5f4f10efc6c576caceab35d24a5eacef5d4c4d575525d6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jul 2021 00:50:01 GMT
ADD file:2b2b9653730f3bb9d3a6327d4b9a6b425279decd90b84755c033b95536ebe027 in / 
# Fri, 23 Jul 2021 00:50:02 GMT
CMD ["/bin/bash"]
# Fri, 23 Jul 2021 04:34:01 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 23 Jul 2021 04:34:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 23 Jul 2021 04:34:02 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 04:34:02 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 04:34:02 GMT
ENV JAVA_VERSION=18-ea+6
# Fri, 23 Jul 2021 04:34:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='13bb69d5907c906e8b9347e531919e17c54f6505cbb4c5fcde71f358b8afac15'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='821ae9c92e8ef55f8cc0671cff324e7e866ee1acbb2d0a86f90b009b35d11925'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 04:34:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a21bf021f71862240d392ffdd7f376294fa46f2729f1771f269c1a888d0aab25`  
		Last Modified: Fri, 23 Jul 2021 00:51:19 GMT  
		Size: 42.0 MB (42040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20d17a0583d5448fece8a45dc16fcd83266885f5eabbeaa44c9bcc8738ed0fa`  
		Last Modified: Fri, 23 Jul 2021 04:45:32 GMT  
		Size: 14.2 MB (14170914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ffdc7493af2e1c669d3adb29d302c72d15ac20d093928025215f2026866c06`  
		Last Modified: Fri, 23 Jul 2021 04:45:47 GMT  
		Size: 186.3 MB (186309255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
