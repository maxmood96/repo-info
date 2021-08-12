## `openjdk:17-oraclelinux8`

```console
$ docker pull openjdk@sha256:ac5be8d46dcb942b14ce1b0ccd6a2a319dd2e12f32928c05ef89d76910d3cf4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:9f507a555448a8bdaa3c85f63c4e693e13e74a93a034803af7498f1d992dd3f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242678037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff693b5bd1bb25516b3b8df5d9140031551bdc9215b52b0f404313b5fb1824b1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Aug 2021 19:20:55 GMT
ADD file:ab982d6f37710c434f7ef9650c722d3c6333906cbb9344bf91e79068088bcc69 in / 
# Thu, 12 Aug 2021 19:20:56 GMT
CMD ["/bin/bash"]
# Thu, 12 Aug 2021 19:37:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 12 Aug 2021 19:38:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 12 Aug 2021 19:38:25 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Aug 2021 19:38:25 GMT
ENV LANG=C.UTF-8
# Thu, 12 Aug 2021 19:38:25 GMT
ENV JAVA_VERSION=17
# Thu, 12 Aug 2021 19:38:37 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 12 Aug 2021 19:38:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c67289558ae5eb060942db5bf46d182448587a87e21c680a0486b147d4b9a0b4`  
		Last Modified: Thu, 12 Aug 2021 19:22:09 GMT  
		Size: 42.2 MB (42158041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12787f1f3888c64bfc9e779a9705ecc45ae1a60b3757074b6f16cf1d8553cac8`  
		Last Modified: Thu, 12 Aug 2021 19:43:29 GMT  
		Size: 13.4 MB (13373335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b68cfe81aec89c9ea5d63332c1b03b8ceff1475a26ea818f01a9f09e15ed95`  
		Last Modified: Thu, 12 Aug 2021 19:44:41 GMT  
		Size: 187.1 MB (187146661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7635e2fe97a9b02ec11a610a02c314318b146f7155b5af39355479def02fa2b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242163876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711d6712d7f7e4ece96ef26a61ab66b859486d219b6bf0e88fdda3fd9bd03561`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jul 2021 00:50:01 GMT
ADD file:2b2b9653730f3bb9d3a6327d4b9a6b425279decd90b84755c033b95536ebe027 in / 
# Fri, 23 Jul 2021 00:50:02 GMT
CMD ["/bin/bash"]
# Fri, 23 Jul 2021 04:34:01 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 23 Jul 2021 04:34:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 23 Jul 2021 04:34:49 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 04:34:49 GMT
ENV LANG=C.UTF-8
# Sat, 07 Aug 2021 01:24:35 GMT
ENV JAVA_VERSION=17
# Sat, 07 Aug 2021 01:24:58 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 07 Aug 2021 01:24:59 GMT
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
	-	`sha256:50cb23492547b15e41b0b4837aac0f9984ee30531114cbb44c6ac161a4ffeea6`  
		Last Modified: Sat, 07 Aug 2021 01:38:11 GMT  
		Size: 186.0 MB (185952206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
