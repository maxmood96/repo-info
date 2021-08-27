## `openjdk:18-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:3942ab727b40a3634e204ed1fedaae354cdbf2e43dc356dcd737da0f832eb043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:a5956c3159522f30b2becc3ec2119e62b46405d03434929148f9950a463f2209
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243043413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f618b24f3a46efd66e964f8e3a0c78cf00ba20b63747ca29a7a19dc004fad5a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Aug 2021 19:20:55 GMT
ADD file:ab982d6f37710c434f7ef9650c722d3c6333906cbb9344bf91e79068088bcc69 in / 
# Thu, 12 Aug 2021 19:20:56 GMT
CMD ["/bin/bash"]
# Thu, 12 Aug 2021 19:37:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 12 Aug 2021 19:37:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 12 Aug 2021 19:37:56 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Aug 2021 19:37:57 GMT
ENV LANG=C.UTF-8
# Fri, 27 Aug 2021 17:30:47 GMT
ENV JAVA_VERSION=18-ea+12
# Fri, 27 Aug 2021 17:30:57 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/12/GPL/openjdk-18-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='a9bc316abb2e03378f35fc574685b8bbdd15cd6803df70c02e71ff8f19ad292b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/12/GPL/openjdk-18-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='08129b3c4ef9956a14a7112565a185ac9ea7e3b327875089114ce6fe2563f585'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 27 Aug 2021 17:30:58 GMT
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
	-	`sha256:c72e03546379f5545ea6eba2dfc4bbe7068fedaa6908bb403332b1060b92dbd8`  
		Last Modified: Fri, 27 Aug 2021 17:38:52 GMT  
		Size: 187.5 MB (187512037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b0d146450407b8b86cedb79a381a4e318e38aa3b7f7ab55b4aba593cd5606821
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242469597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fff71ac7900c35ba2ceb9eeb809e4153deda21adf3c58a5518325ec23a180fc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Aug 2021 02:58:07 GMT
ADD file:3a5bc6124c8d78438880a95007baec403400e29f09317331e09ba7d65a0aaff0 in / 
# Fri, 13 Aug 2021 02:58:08 GMT
CMD ["/bin/bash"]
# Fri, 13 Aug 2021 05:39:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 13 Aug 2021 05:39:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 13 Aug 2021 05:39:59 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Aug 2021 05:39:59 GMT
ENV LANG=C.UTF-8
# Fri, 27 Aug 2021 17:48:59 GMT
ENV JAVA_VERSION=18-ea+12
# Fri, 27 Aug 2021 17:49:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/12/GPL/openjdk-18-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='a9bc316abb2e03378f35fc574685b8bbdd15cd6803df70c02e71ff8f19ad292b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/12/GPL/openjdk-18-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='08129b3c4ef9956a14a7112565a185ac9ea7e3b327875089114ce6fe2563f585'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 27 Aug 2021 17:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:757bb77daa0e625f3aaa9e22fcc2dda31fa9d6e50f482403ab7be9f030a1a19f`  
		Last Modified: Fri, 13 Aug 2021 02:59:14 GMT  
		Size: 42.1 MB (42054178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d701f3bd7e43b3fb331b6b15362e9dbd4abd27a5c29f2301d998cc782a0ba1`  
		Last Modified: Fri, 13 Aug 2021 05:50:47 GMT  
		Size: 14.2 MB (14163676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b50ba406b7fb618ef3f2b749a08e84c43fd35c68e33585b9ccfa1aa56b6dcf6`  
		Last Modified: Fri, 27 Aug 2021 18:03:28 GMT  
		Size: 186.3 MB (186251743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
