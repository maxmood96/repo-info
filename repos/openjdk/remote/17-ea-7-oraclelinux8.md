## `openjdk:17-ea-7-oraclelinux8`

```console
$ docker pull openjdk@sha256:8607ee7d37c52bc0cf0e87467d2442638aeba7e59e39e4564e0b7ed98710e352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-7-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:476c4e09b999ca9eacb30916eee592c60b76722defd7c1c593f39b8586cd08e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240997330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b047dac6bad526bcce5bcd37d86e6d9dfba85ec0a6309b9f5428f022436cce`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 20:32:17 GMT
ADD file:2ba8f9c8e1d7e464c075fdd46e81f2e15a69d9a5aefb4b991cccb352e082af2f in / 
# Mon, 01 Feb 2021 20:32:17 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 23:54:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 23:54:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 01 Feb 2021 23:54:30 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:54:30 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 23:54:30 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 23:55:14 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='0e340613945c78b2eb714ba0850604a1a80a9678ba0e8d81f66629c0ca2c36b1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='f3f80fc9b41cfddd89d263ae66c0f514aaeb3db2eadd6c9bf3c31e1b2cdcf44e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 23:55:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63e877180dd1388e46564a2b7a72ddf3559dc506f4b6e8b435ed569643811c02`  
		Last Modified: Mon, 01 Feb 2021 20:34:13 GMT  
		Size: 42.1 MB (42069114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cce05db0e2c91e801a9a4024eedc06badf46bad72a11ee564bbacdbc4cbfb40`  
		Last Modified: Tue, 02 Feb 2021 00:04:16 GMT  
		Size: 13.3 MB (13277751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9608cdf547a7c2a79e6cb7fdacefcf4bc03ca5b49aba92afff7ccf5ff29d71c8`  
		Last Modified: Tue, 02 Feb 2021 00:04:31 GMT  
		Size: 185.7 MB (185650465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-7-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fdacd7dda5ebd7559e6b2ea519fa4bdba5c740d914ececbb19da0d3898166196
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236073037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616c2ce0c15b456e772be8cbe42dda4887a9ff8eea30a8387cf48f4c932d8d31`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 21:00:54 GMT
ADD file:40a46ad11c4530459867a348c980e7ed1ba9fe6bdf74da38208ee8bf7be1f81d in / 
# Mon, 01 Feb 2021 21:00:56 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:05:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 21:05:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 01 Feb 2021 21:05:58 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:05:59 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 21:06:00 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 21:06:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='0e340613945c78b2eb714ba0850604a1a80a9678ba0e8d81f66629c0ca2c36b1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='f3f80fc9b41cfddd89d263ae66c0f514aaeb3db2eadd6c9bf3c31e1b2cdcf44e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 21:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:17e75779b55909cd6075d706cc3fc9f838f287de73b35be3d551231217cbd32c`  
		Last Modified: Mon, 01 Feb 2021 21:02:50 GMT  
		Size: 42.0 MB (41996203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fad58a53edbb48f3027bc56f941db82a77fd6d28a6fc25d4bf2462f3bc62bc`  
		Last Modified: Mon, 01 Feb 2021 21:15:35 GMT  
		Size: 14.1 MB (14057108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c971450934d010ca9f87449f240d84945f55545ced545d92e76f8aaec1563cd1`  
		Last Modified: Mon, 01 Feb 2021 21:16:01 GMT  
		Size: 180.0 MB (180019726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
