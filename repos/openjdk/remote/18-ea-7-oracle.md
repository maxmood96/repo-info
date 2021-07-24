## `openjdk:18-ea-7-oracle`

```console
$ docker pull openjdk@sha256:2d36b5af4af6bbee29d0c369723b22f67c73a3b097c57cdd6824f24724f7898f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-7-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:552edc8d54129b7aeeef93be3c45d2bab55acb5b084b033a52298a20de6bb575
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243111632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0072c1906e21ea46d68fab3423edbaee9f2bd50b93f3a94bfcdaff322f622fe9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jul 2021 01:13:10 GMT
ADD file:c047ac1784a3670f52d12ad67cf238654237149dc2c9d7b921cd005c7ec42105 in / 
# Fri, 23 Jul 2021 01:13:11 GMT
CMD ["/bin/bash"]
# Fri, 23 Jul 2021 06:40:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 23 Jul 2021 06:40:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 23 Jul 2021 06:40:32 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 06:40:32 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 21:20:33 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:20:44 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='03f895bdf47691e44e9b269eda74f407715e97385b0cfb60304bcfda29f589a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='bc3dec6f82541afbd83e9b5ba6ae70541206accd7d815dd171fd36c93a90fe3d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 21:20:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1da50e1664e1b58d93182fe5af093c642668ec93f67fcd8215b9c1979930b84d`  
		Last Modified: Fri, 23 Jul 2021 01:14:27 GMT  
		Size: 42.2 MB (42178827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8e5a84542212d0126ce88facd146befb1c731fb4faafb50a7b96ad0568cd9`  
		Last Modified: Fri, 23 Jul 2021 06:49:18 GMT  
		Size: 13.4 MB (13390485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170c51e5216c3c5f2e37bdef0e8f8f33659604066e87ede07138b73ee15398ef`  
		Last Modified: Fri, 23 Jul 2021 21:26:29 GMT  
		Size: 187.5 MB (187542320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-7-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:368f0c2ddd9f7a1a5924e62dfcd0836c249904af9da44d58e33b8ad6fbf90427
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242480722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7de1005667a721de6647195a02031f2de1141abd24afaae0cffdbb362fff382`
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
# Fri, 23 Jul 2021 21:40:29 GMT
ENV JAVA_VERSION=18-ea+7
# Fri, 23 Jul 2021 21:40:48 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='03f895bdf47691e44e9b269eda74f407715e97385b0cfb60304bcfda29f589a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/7/GPL/openjdk-18-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='bc3dec6f82541afbd83e9b5ba6ae70541206accd7d815dd171fd36c93a90fe3d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 21:40:49 GMT
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
	-	`sha256:baafd6c49ff332a8a03b7a4e83e0ddde773045f387c74cd3daef27a5f1b9b244`  
		Last Modified: Fri, 23 Jul 2021 21:52:04 GMT  
		Size: 186.3 MB (186269052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
