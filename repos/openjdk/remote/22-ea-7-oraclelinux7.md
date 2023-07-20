## `openjdk:22-ea-7-oraclelinux7`

```console
$ docker pull openjdk@sha256:31fc4c77178e057281d6d1d95b556ac24adc4126d7ea1d546a6c3a5e7e2a7b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-7-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:c6f7607741e4441669f06c4525c95b4f1cb0acbf5a33b5d044e66018d6779357
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269563488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6823d7d5232888121e038c0e66f35e9f1a127859d47a6dc650292cfa7f3bd499`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Jun 2023 07:21:40 GMT
ADD file:733a37449d62d6e9f530185b9244e06cd8ff0ee896632576ae644437d0a1f852 in / 
# Wed, 14 Jun 2023 07:21:40 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 09:56:49 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Jun 2023 09:56:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Wed, 14 Jun 2023 09:56:49 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 09:56:49 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Jul 2023 20:22:20 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:22:40 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 20 Jul 2023 20:22:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70e9ff4420fbc58483e68c13199a06c24b14013b2548998a7e367f59ca5157bc`  
		Last Modified: Wed, 14 Jun 2023 07:22:30 GMT  
		Size: 50.5 MB (50484765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4714d29e017353e367cfbeb707bad46a96692fceb51533b3749c668baf3b5b8f`  
		Last Modified: Wed, 14 Jun 2023 09:58:27 GMT  
		Size: 14.2 MB (14242764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf38d363495539c46db020b3cecc301a7d5f666825514422ee56dfd03144a0f`  
		Last Modified: Thu, 20 Jul 2023 20:29:25 GMT  
		Size: 204.8 MB (204835959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-7-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:74d2ef58eae69dbcfaceec82fd800fd1179dc5eb972a6f55c88438903d149ea6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269438122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd32142445fcf0a48bbdf5bdf639ca664f867f763ee83434b941d3f3eea80b81`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Jun 2023 03:45:43 GMT
ADD file:a9ba9c7acb256e802c7248b56f377a6f0ea08b1b61e11e482516633a13f4d686 in / 
# Wed, 14 Jun 2023 03:45:44 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 04:08:20 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Jun 2023 04:08:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Wed, 14 Jun 2023 04:08:20 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 04:08:20 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Jul 2023 20:06:34 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:06:52 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 20 Jul 2023 20:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:52fd87ed40fcddc3fe63b876d1f94f6edae688637a5cc56983dced68a50c953e`  
		Last Modified: Wed, 14 Jun 2023 03:46:28 GMT  
		Size: 51.1 MB (51052081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aeb39f5d39e6fb51e698f8f5e6416d0689047f9392a9bd3f97f28c4d5d5596`  
		Last Modified: Wed, 14 Jun 2023 04:10:01 GMT  
		Size: 15.2 MB (15238146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f2a3d5c2f69cbc96ad2ae765a84d6a855197f0b3bd1027041495fca86d5407`  
		Last Modified: Thu, 20 Jul 2023 20:13:34 GMT  
		Size: 203.1 MB (203147895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
