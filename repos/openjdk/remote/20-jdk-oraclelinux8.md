## `openjdk:20-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:2c646c6304858712b1657e3620c7847db58670a0560be499322d3e1a31868d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:088aab8034380f0d9d3e042e97f9a0130fe1faeb04e8c278eccd5c73b68b7eb8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249937308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc57e4e66e694f144b16cedb3df7f6f38b7a6c8aa490a487ac06b07a1ee616e8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Oct 2022 19:20:54 GMT
ADD file:66ffe38a497f15c1941fcc4c64fda875cf27856f2ade5128546c10590c5ca84a in / 
# Fri, 21 Oct 2022 19:20:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 19:51:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 21 Oct 2022 19:51:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 21 Oct 2022 19:51:29 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 19:51:29 GMT
ENV LANG=C.UTF-8
# Fri, 21 Oct 2022 19:51:29 GMT
ENV JAVA_VERSION=20-ea+20
# Fri, 21 Oct 2022 19:51:40 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='0cb0f79bee2e61134a86049952a1e572bb3e2dad49aa200a20f18c697715a402'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4db7319dfbfb4a3561e9707c0178d0ba8d6413bc94f13d8c9ce406fd7445e000'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 21 Oct 2022 19:51:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:50cbc88660a5576a306374b5ee70e3e8aeb602409e05ffa41cd4680769ae0574`  
		Last Modified: Fri, 21 Oct 2022 19:22:39 GMT  
		Size: 40.6 MB (40588747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f15da7b20d89dec72e0bff2c38edc4d7119a8f5049343764ac32b207f7bd7b9`  
		Last Modified: Fri, 21 Oct 2022 19:55:16 GMT  
		Size: 12.2 MB (12231175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260cbb1d34a59f50f2fdfaac9c65eb84b3c19441a52f658f2063cff4c8ceccc5`  
		Last Modified: Fri, 21 Oct 2022 19:55:30 GMT  
		Size: 197.1 MB (197117386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6e2cb032efc5ee3f0d78f77186e4d30dc5fd9a5e22153bc7db98a99eddb04774
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248141888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab28b526db6b5e05a3b3b1ca6e48c52c26887053955b8841714fc5099942c4c0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Oct 2022 19:41:03 GMT
ADD file:2ccafa0c5b388d404f1100108ad9a9cb06c3e4ca4543c4b0f2aadfd9c4b97e45 in / 
# Fri, 21 Oct 2022 19:41:03 GMT
CMD ["/bin/bash"]
# Wed, 26 Oct 2022 00:43:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 26 Oct 2022 00:43:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 26 Oct 2022 00:43:35 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 00:43:35 GMT
ENV LANG=C.UTF-8
# Wed, 26 Oct 2022 00:43:35 GMT
ENV JAVA_VERSION=20-ea+20
# Wed, 26 Oct 2022 00:43:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='0cb0f79bee2e61134a86049952a1e572bb3e2dad49aa200a20f18c697715a402'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4db7319dfbfb4a3561e9707c0178d0ba8d6413bc94f13d8c9ce406fd7445e000'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Oct 2022 00:43:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba2bcb842ee086f4d448ac74f4e172e2568d56d24e6efae9b402c0e37f418943`  
		Last Modified: Fri, 21 Oct 2022 19:42:50 GMT  
		Size: 39.4 MB (39408151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e435e89e01609b5f7794b35f7cd9ecdea4fd71ca761c724e6d77a2911953776`  
		Last Modified: Wed, 26 Oct 2022 00:49:53 GMT  
		Size: 13.1 MB (13059774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad638af62ec6cec54eee74fee64ac193027481c9f355668bb827dd15e20097b`  
		Last Modified: Wed, 26 Oct 2022 00:50:04 GMT  
		Size: 195.7 MB (195673963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
