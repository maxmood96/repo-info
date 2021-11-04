## `openjdk:18-oraclelinux8`

```console
$ docker pull openjdk@sha256:6454022f8656aaa0fc08cbfcc617134fbb65e9bf91d0a8cb3a5fa9f45c43172e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-oraclelinux8` - linux; amd64

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

### `openjdk:18-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:69f8c25e377ba8ec010ce8caa460146f220662c291280ed9af9229d07256e972
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243202184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c288c27730dd8709627c4220fa83c9513cb0d2bfd26b73d92da997676a3f3d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Nov 2021 22:44:10 GMT
ADD file:42d3c96053f453ca6f7155adc565cd822cd2663bd2a3862ccaabb9886c191116 in / 
# Wed, 03 Nov 2021 22:44:11 GMT
CMD ["/bin/bash"]
# Wed, 03 Nov 2021 23:01:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 03 Nov 2021 23:01:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 03 Nov 2021 23:01:21 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Nov 2021 23:01:22 GMT
ENV LANG=C.UTF-8
# Wed, 03 Nov 2021 23:01:23 GMT
ENV JAVA_VERSION=18-ea+21
# Wed, 03 Nov 2021 23:01:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c0a1fcdd389abdc8101892215f73413b10975f735f31e6d0484c9653fc9ba5e9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ed86d5c7f9433360bc81b5b283d6b5fc345309d16c77125c8ceff32ed5c9a8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 03 Nov 2021 23:01:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6fe8bd1b591af20f7f1bf6cabe92846a2b5f1ba33ca5fd165cf03624558cd5c`  
		Last Modified: Wed, 03 Nov 2021 22:45:11 GMT  
		Size: 41.9 MB (41879080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f82d768d0f333fffcb86fe10bab796e393363d92953d26c9435077acb1598e`  
		Last Modified: Wed, 03 Nov 2021 23:12:36 GMT  
		Size: 14.3 MB (14274012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12dafb56a01afc697264735df1f9eee940086c846bc9b2d88981f202d362920`  
		Last Modified: Wed, 03 Nov 2021 23:12:50 GMT  
		Size: 187.0 MB (187049092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
