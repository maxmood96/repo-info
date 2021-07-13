## `openjdk:18-jdk-oracle`

```console
$ docker pull openjdk@sha256:2b82a99ff801c9ff96edc38bc519876dc86a9198c3ec3b639cfb2eb65c3e3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:66a49803b9232c9796871860893591b5dc37f5634079b5fc84dfebcaa0900f43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243431265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6284118bb15ba6fec340b35e825ee80acd3feaaad5dac5f503b3242086aa8d9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 30 Jun 2021 17:23:40 GMT
ADD file:d49890823c4e8287f936eec210400575f79c20f14f048017368faed0584841a6 in / 
# Wed, 30 Jun 2021 17:23:41 GMT
CMD ["/bin/bash"]
# Wed, 30 Jun 2021 17:40:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 30 Jun 2021 17:40:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 30 Jun 2021 17:40:58 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Jun 2021 17:40:58 GMT
ENV LANG=C.UTF-8
# Fri, 02 Jul 2021 19:25:22 GMT
ENV JAVA_VERSION=18-ea+4
# Fri, 02 Jul 2021 19:25:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/4/GPL/openjdk-18-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='716cfd996b255bbad0b3d17027e5637bf2cf30bf320339116c661d63e797a324'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/4/GPL/openjdk-18-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='d2c4885f81f8be83225ef11849eaaa35af6af01337b90435d9abb8b4138d2795'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 02 Jul 2021 19:25:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9660ffb7976c51eb47b4425f6bb95173c170f4fcc442a2bb2b6ba7bf154f6fc8`  
		Last Modified: Wed, 30 Jun 2021 17:25:00 GMT  
		Size: 42.2 MB (42179226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f8b4ca74ea5f238671d4c7981ca7c99e6c70d3fcd8d4d0596ccdf6b8329dbe`  
		Last Modified: Wed, 30 Jun 2021 17:50:04 GMT  
		Size: 13.4 MB (13391447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723de75bb2103323f9d145315cff6cfc7c60348e1f69e78b43d2ca48405d94ab`  
		Last Modified: Fri, 02 Jul 2021 19:32:32 GMT  
		Size: 187.9 MB (187860592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0178f6204c6284ac3d06d418cde8a81238fd3e6877eba7941865c8eb6c5fb37c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242803657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2c27e52ae279fc3d8ca460546a5c2429850cb366a8eedd6a586df9ac146b58`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jul 2021 20:40:32 GMT
ADD file:a184ed870dc7a85028f7ba3bd0cf3820d6f1b94ac4cea1ac94ca48c786901041 in / 
# Mon, 12 Jul 2021 20:40:33 GMT
CMD ["/bin/bash"]
# Mon, 12 Jul 2021 21:03:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jul 2021 21:03:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 12 Jul 2021 21:03:06 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jul 2021 21:03:06 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jul 2021 21:03:07 GMT
ENV JAVA_VERSION=18-ea+4
# Mon, 12 Jul 2021 21:03:29 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/4/GPL/openjdk-18-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='716cfd996b255bbad0b3d17027e5637bf2cf30bf320339116c661d63e797a324'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/4/GPL/openjdk-18-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='d2c4885f81f8be83225ef11849eaaa35af6af01337b90435d9abb8b4138d2795'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jul 2021 21:03:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6186b25cabd91cbdd2c6bf65b0c5ef261f52719e7c6c4d6252e7082b7a51b42e`  
		Last Modified: Mon, 12 Jul 2021 20:41:48 GMT  
		Size: 42.1 MB (42072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8304774b066b61c2ae3dc6de204cb3d384a726b9376d301afc654577b50a9c0`  
		Last Modified: Mon, 12 Jul 2021 21:15:51 GMT  
		Size: 14.2 MB (14170180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05deefb7c3e1056e2705d7d3bd025240d450baa81f3ea8731d37b6a16726f2e8`  
		Last Modified: Mon, 12 Jul 2021 21:16:06 GMT  
		Size: 186.6 MB (186560762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
