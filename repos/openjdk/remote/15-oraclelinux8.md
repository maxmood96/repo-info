## `openjdk:15-oraclelinux8`

```console
$ docker pull openjdk@sha256:87bd5c417e644acf4bfdaabbb42f7e8bebbe06641646f0537af004213b7b8443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:15-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:aaa62154b94d1ff55252dcc629225698247fa231402c28b04767341b74326a9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251145588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7666c92f41b0e66c9446eab5661f8eec9481a57c7440eff65dd4af00ed7e6908`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 20:32:17 GMT
ADD file:2ba8f9c8e1d7e464c075fdd46e81f2e15a69d9a5aefb4b991cccb352e082af2f in / 
# Mon, 01 Feb 2021 20:32:17 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 23:54:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 23:58:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 01 Feb 2021 23:58:24 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:58:24 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 23:58:24 GMT
ENV JAVA_VERSION=15.0.2
# Mon, 01 Feb 2021 23:59:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='91ac6fc353b6bf39d995572b700e37a20e119a87034eeb939a6f24356fbcd207'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='3958f01858f9290c48c23e7804a0af3624e8eca6749b085c425df4c4f2f7dcbc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 23:59:10 GMT
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
	-	`sha256:58ee7ac9a7c36de0dbd0eee4c01c5ff312b82f7ea245374a0d1d84c4f5a5b81c`  
		Last Modified: Tue, 02 Feb 2021 00:06:44 GMT  
		Size: 195.8 MB (195798723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b3c087e0aee891b4e087cdc76ce50338cc4acb509353110a2a163055e1eb9ee9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230935054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319d538cd70748e681b399b617486ed6b16bb461f01e64f94f0e121376f915e4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 21:00:54 GMT
ADD file:40a46ad11c4530459867a348c980e7ed1ba9fe6bdf74da38208ee8bf7be1f81d in / 
# Mon, 01 Feb 2021 21:00:56 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:05:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 21:10:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 01 Feb 2021 21:10:28 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:10:28 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 21:10:29 GMT
ENV JAVA_VERSION=15.0.2
# Mon, 01 Feb 2021 21:11:09 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='91ac6fc353b6bf39d995572b700e37a20e119a87034eeb939a6f24356fbcd207'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='3958f01858f9290c48c23e7804a0af3624e8eca6749b085c425df4c4f2f7dcbc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 21:11:11 GMT
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
	-	`sha256:2a7a6a574bcdcf0c9439189be4b3d61df8466e2ed2c5f5d23c1e26d1cda2b4cb`  
		Last Modified: Mon, 01 Feb 2021 21:18:51 GMT  
		Size: 174.9 MB (174881743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
