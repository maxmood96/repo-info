## `openjdk:19-ea-11-oraclelinux7`

```console
$ docker pull openjdk@sha256:cc4b5a6cff54ab76eafa55bee86669727d324ab817fb657a7933a45081d6ec19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-11-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:6efa63ff447a7170bb8753598fad8d903d74df5e54fba632352626fcc22c57a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256732419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a449e84477e325dff09908783a3a26ebefb7ef1985a05ba93c8a246fa29caa5f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:38:09 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 25 Feb 2022 03:38:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 03:38:10 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 03:38:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 02 Mar 2022 19:57:07 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 19:57:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='df51ead7190d118175654b6d0688649e67ffe6f23e84d30584145ce3908281e1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4edb9b2995bb4727d03834c22b36adc9d90b3e75a173420474bad629853756d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Mar 2022 19:57:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a747076cd653f857a43ad06edf375d2d7f9d70470d618d826d9fd2239d9431e4`  
		Last Modified: Fri, 25 Feb 2022 05:32:07 GMT  
		Size: 15.4 MB (15402277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8e8a63ad1b9e2622d78a7ffff6c9275d134aa73e69cfb2f19b42ab8820e54f`  
		Last Modified: Wed, 02 Mar 2022 20:07:49 GMT  
		Size: 193.0 MB (192999280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-11-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8a5a485a927ff4eec2e46919007fa06ef2c1acc2edd87f44f4a675fa51ac57d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257378370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4520cb0e5385f3deba686af2552771b6ad69d7fccf5464095ac87a3e380f262e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:933bf8bd076f0c42499df14ceb4b409753b2ce9f8b0bd81331ac2630b6dab149 in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:27:32 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 25 Feb 2022 02:27:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 02:27:33 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 02:27:34 GMT
ENV LANG=en_US.UTF-8
# Wed, 02 Mar 2022 08:04:49 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 08:05:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='df51ead7190d118175654b6d0688649e67ffe6f23e84d30584145ce3908281e1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4edb9b2995bb4727d03834c22b36adc9d90b3e75a173420474bad629853756d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Mar 2022 08:05:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5148c102f8614047b0330785165cb7096428df640af91104fbe61a7ebb5b8713`  
		Last Modified: Fri, 25 Feb 2022 02:09:24 GMT  
		Size: 48.9 MB (48901247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5afd0c7f5b0b7ae1e56ff4afb456806881a77fe14b8769883e0684cbcb9ac76`  
		Last Modified: Fri, 25 Feb 2022 02:48:54 GMT  
		Size: 16.4 MB (16445028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba73715701d177b39d37bd6ebfee3d2f307d09439a3c57c8c52ce58cd8313ae`  
		Last Modified: Wed, 02 Mar 2022 08:19:07 GMT  
		Size: 192.0 MB (192032095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
