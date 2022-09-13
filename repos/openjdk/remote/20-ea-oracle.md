## `openjdk:20-ea-oracle`

```console
$ docker pull openjdk@sha256:0a36ec4510ec405bcbee9665ff16e59bbd56ff75a6b86546ab44321122d18ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:584cebf24b3e47addbc7333c8670b4555bee4fb9906adc18e242e12748e829f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248607984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b61da94a9f6fce0ae7687623b9c5bdc7fca74f932b473e888f1a748fc50c35a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 30 Aug 2022 21:20:34 GMT
ADD file:94f0ad5f0805806df710f02659592b7a0ee14643d54d40f0dca144e16c2c69ec in / 
# Tue, 30 Aug 2022 21:20:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:47:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:47:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 30 Aug 2022 21:47:35 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Aug 2022 21:47:35 GMT
ENV LANG=C.UTF-8
# Mon, 12 Sep 2022 22:35:27 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 22:35:54 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='ce9c99a0d70bf7c6548b68a33770a50d1273d5d5ea72522a1fe91ae6d3f22c1d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='4935236eb4e51be13ddfcc1ce717191128feb8ff9329676971ea54775261d9ff'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Sep 2022 22:35:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:492d84e496ea03370b8fb5b989ff003b89c51a2f037216835b8b3f93dcc4d405`  
		Last Modified: Tue, 30 Aug 2022 21:21:33 GMT  
		Size: 39.5 MB (39521774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d74542bd1abb51e0ea04904a65559d263d7f85b016fcbd81a65768553957ae`  
		Last Modified: Tue, 30 Aug 2022 21:51:36 GMT  
		Size: 12.2 MB (12240649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5da156feef7424bd330906d8a0700b10312feb3480d40f20d2ec72dd4671583`  
		Last Modified: Mon, 12 Sep 2022 22:40:38 GMT  
		Size: 196.8 MB (196845561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e27425b88dfb8ad627e2243b7206e8f708804a633ac353ee069d63bbe6617af9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246723207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3331e1c1be2a396250e083fe277be57354033549d78bfd139695a47256efcbce`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 30 Aug 2022 20:47:49 GMT
ADD file:4f53d93ae4bccd786d6beda6f0ec4a450fd23a8fff2786d9e5b024a64aad6bb1 in / 
# Tue, 30 Aug 2022 20:47:50 GMT
CMD ["/bin/bash"]
# Tue, 30 Aug 2022 21:08:02 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 30 Aug 2022 21:08:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 30 Aug 2022 21:08:04 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Aug 2022 21:08:05 GMT
ENV LANG=C.UTF-8
# Mon, 12 Sep 2022 23:03:57 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 23:04:09 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='ce9c99a0d70bf7c6548b68a33770a50d1273d5d5ea72522a1fe91ae6d3f22c1d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='4935236eb4e51be13ddfcc1ce717191128feb8ff9329676971ea54775261d9ff'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Sep 2022 23:04:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fe1dbcd3b09e2c1e850118728988d6907b2f43969fe81443f422984829c640ce`  
		Last Modified: Tue, 30 Aug 2022 20:48:58 GMT  
		Size: 38.3 MB (38321155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43dbff7ac899e8f3413a3849ac2dcb6c61d52e9763a3cf5bc4c38d1e823fa3a`  
		Last Modified: Tue, 30 Aug 2022 21:16:28 GMT  
		Size: 13.0 MB (13042009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62b6efc23e3629b0619d5c4a278bd58a3a31b4f59265bf361a5fe763a01d37b`  
		Last Modified: Mon, 12 Sep 2022 23:12:57 GMT  
		Size: 195.4 MB (195360043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
