## `openjdk:21-ea-25-oracle`

```console
$ docker pull openjdk@sha256:92ec4ed387a7075b18034bc50e26abafa92fa5adeaa006eb5340232be4ddae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:21-ea-25-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:68d20f3d00a8574501f5cd525465d88d58a042fdbedc2845a56803c7344cb940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263454966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9199444387fe47c50bc23dd19fdbe3700215d9aa4879d238db361f14fcd71c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 May 2023 21:20:28 GMT
ADD file:e15c235506d8dd134e69d458a7c0afefef1522e9d0cfb28e3538760ddf032785 in / 
# Wed, 24 May 2023 21:20:29 GMT
CMD ["/bin/bash"]
# Wed, 24 May 2023 21:44:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 24 May 2023 21:44:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 24 May 2023 21:44:56 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 21:44:56 GMT
ENV LANG=C.UTF-8
# Thu, 01 Jun 2023 23:25:50 GMT
ENV JAVA_VERSION=21-ea+25
# Thu, 01 Jun 2023 23:26:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/25/GPL/openjdk-21-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='26d0ae26838de257ddb7dc06e11eee28038678adf85c494686c6592ff027a0b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/25/GPL/openjdk-21-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='44d36b86be342723ab29831812a4ccd8dfe9b964ef1b12b0fee053b76f97438e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 01 Jun 2023 23:26:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90e2fb2facff1c5093f0ebfa9d08fde487930822d9ac278bb2df0195610f1d13`  
		Last Modified: Wed, 24 May 2023 21:21:24 GMT  
		Size: 44.9 MB (44873648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0845850e9baa985b97efc76bed4795ff90eb1249ecf4531667da84d4be1fcdf`  
		Last Modified: Wed, 24 May 2023 21:45:40 GMT  
		Size: 15.0 MB (15010668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901ecda32e2bc8a45e0031f3327824ca53bf48505b4831b5386e2de9d1aa155b`  
		Last Modified: Thu, 01 Jun 2023 23:28:05 GMT  
		Size: 203.6 MB (203570650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
