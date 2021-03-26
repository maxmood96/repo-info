## `openjdk:17-ea-15-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:17bccba152ddeb1c69aedb5db4313fe0d35534c64d241b3b0554adf7a98de877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-15-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:048c144d882ecd7199be269294094b2cc6e4bfbda47fd66b6aed2bb9ebf92264
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240919663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9afb0c70840219aea3dc18dc1318f278b00f9f7f27242668e00c924ab6d19a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Mar 2021 20:36:33 GMT
ADD file:2ba8f9c8e1d7e464c075fdd46e81f2e15a69d9a5aefb4b991cccb352e082af2f in / 
# Tue, 09 Mar 2021 20:36:33 GMT
CMD ["/bin/bash"]
# Tue, 09 Mar 2021 20:55:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 09 Mar 2021 20:55:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 09 Mar 2021 20:55:08 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 20:55:08 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 05:42:28 GMT
ENV JAVA_VERSION=17-ea+15
# Fri, 26 Mar 2021 05:42:40 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/15/GPL/openjdk-17-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='da690c53a8d23b278b4878acf414b0d95ca40dd1533d08ce313589cf1df1c9c3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/15/GPL/openjdk-17-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93178b313750b38e1bbc811b989dcee27d988cb223b30ba829122ecdbd08f403'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Mar 2021 05:42:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63e877180dd1388e46564a2b7a72ddf3559dc506f4b6e8b435ed569643811c02`  
		Last Modified: Mon, 01 Feb 2021 20:34:13 GMT  
		Size: 42.1 MB (42069114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ff0a89ff9842ef20925cd26efa5ab427f6c745febbbe471cc0a48bcc14e60`  
		Last Modified: Tue, 09 Mar 2021 21:08:26 GMT  
		Size: 13.3 MB (13280925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e156f49304a09ad81f778f4ae88e92eb65f81fdd1f6cef1e1c8f6c0add6efbd`  
		Last Modified: Fri, 26 Mar 2021 05:48:46 GMT  
		Size: 185.6 MB (185569624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-15-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2c159596ab5eb482206fff7e6da40185c80c7eafed264c4cd5b7edb384433736
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237702601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddcdf4f7e797c061080c2a3e8b4d2f7e9e10e5d4f9c8b424dd66949b0143dd52`
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
# Fri, 26 Mar 2021 13:33:00 GMT
ENV JAVA_VERSION=17-ea+15
# Fri, 26 Mar 2021 13:33:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/15/GPL/openjdk-17-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='da690c53a8d23b278b4878acf414b0d95ca40dd1533d08ce313589cf1df1c9c3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/15/GPL/openjdk-17-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93178b313750b38e1bbc811b989dcee27d988cb223b30ba829122ecdbd08f403'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Mar 2021 13:33:29 GMT
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
	-	`sha256:6bff255d80f2a7da586bd040a8e9a44b4966707d827da38443c52c4c712f597b`  
		Last Modified: Fri, 26 Mar 2021 13:39:53 GMT  
		Size: 181.6 MB (181649290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
