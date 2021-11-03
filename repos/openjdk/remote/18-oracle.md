## `openjdk:18-oracle`

```console
$ docker pull openjdk@sha256:1c02742c92ace09d9cdd367c21489e376b0d8b8b4d8aa4a3b66906f76d574cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:817b9de5fd1ed622c9080f216dd6b3040f3545be2c6026fe5d413628eb87edca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243585087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55f011574655a28ccd27287ab45d17065ae9bbc0c4101281ffa665c385c2315`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Nov 2021 22:20:09 GMT
ADD file:ee2c184d933cfe1848f54f94d92f5c14d073160b62ec403259b18392d4ec6e1b in / 
# Wed, 03 Nov 2021 22:20:10 GMT
CMD ["/bin/bash"]
# Wed, 03 Nov 2021 22:37:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 03 Nov 2021 22:37:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 03 Nov 2021 22:37:07 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Nov 2021 22:37:07 GMT
ENV LANG=C.UTF-8
# Wed, 03 Nov 2021 22:37:07 GMT
ENV JAVA_VERSION=18-ea+21
# Wed, 03 Nov 2021 22:37:18 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c0a1fcdd389abdc8101892215f73413b10975f735f31e6d0484c9653fc9ba5e9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ed86d5c7f9433360bc81b5b283d6b5fc345309d16c77125c8ceff32ed5c9a8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 03 Nov 2021 22:37:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a6167eaa66c8f2dc1c8dbed1a335f3d4052409454c9f7fbcd8fc35d8576a7e2`  
		Last Modified: Wed, 03 Nov 2021 22:21:16 GMT  
		Size: 42.0 MB (41968115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88dabbf57eeb24f57debafeba0a2f7b2f4e4e76d1aa9a3bd27edf0682e0f15`  
		Last Modified: Wed, 03 Nov 2021 22:43:12 GMT  
		Size: 13.5 MB (13491241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9881991c1db3ee3e0c6ae7c15b8a4429c433a7655ffe01202511ebf51b6a2ec2`  
		Last Modified: Wed, 03 Nov 2021 22:43:24 GMT  
		Size: 188.1 MB (188125731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e41febc414a593852f052bb5105ff5588fc3dd8e943af786f4700a3902ff4cef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243202573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38d052f8e13039e074186ee1d53bcbfa2834efe0994e29d064a422fce55906`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 28 Oct 2021 01:43:49 GMT
ADD file:accebe81069e9a5a2fa2b5311f1fd53f84fc7cc12b93d70f150e3ee0c4d1853c in / 
# Thu, 28 Oct 2021 01:43:50 GMT
CMD ["/bin/bash"]
# Thu, 28 Oct 2021 02:15:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 28 Oct 2021 02:15:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 28 Oct 2021 02:15:06 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Oct 2021 02:15:07 GMT
ENV LANG=C.UTF-8
# Mon, 01 Nov 2021 19:17:29 GMT
ENV JAVA_VERSION=18-ea+21
# Mon, 01 Nov 2021 19:17:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c0a1fcdd389abdc8101892215f73413b10975f735f31e6d0484c9653fc9ba5e9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ed86d5c7f9433360bc81b5b283d6b5fc345309d16c77125c8ceff32ed5c9a8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Nov 2021 19:17:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:42445708416d90c524044613ca219573cb3b87e3c236ae8642b0e17b341389fb`  
		Last Modified: Thu, 28 Oct 2021 01:45:02 GMT  
		Size: 41.9 MB (41879582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4f9f60b42882cee2f44d430dab6e4bd76aacf43d9e203013dc45e48cfc38eb`  
		Last Modified: Thu, 28 Oct 2021 02:28:51 GMT  
		Size: 14.3 MB (14273910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aee561567e29f987c7774a500c45d8755428afd4b7fd95aacbc07a9cf202e0f`  
		Last Modified: Mon, 01 Nov 2021 19:29:31 GMT  
		Size: 187.0 MB (187049081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
