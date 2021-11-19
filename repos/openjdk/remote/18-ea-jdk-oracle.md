## `openjdk:18-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:fad171726fe0dce2576195f041d2560167d9062b020bda179ce5175c7c40cbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:4bb73c25d5c1b643d96548f49189789c8dce599aceae9a9dab0b63748f684c44
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243806926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157c4e76f36104f701713c2f9fabac3290c0a35c8ac634afd535cfff61006c03`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Nov 2021 16:05:57 GMT
ADD file:977d9a2c7a8ab07ec719edd585faf23ef08768a09abf97a80d62d2091936b052 in / 
# Thu, 18 Nov 2021 16:05:58 GMT
CMD ["/bin/bash"]
# Thu, 18 Nov 2021 17:33:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 18 Nov 2021 17:33:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 18 Nov 2021 17:33:39 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 17:33:39 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 17:33:39 GMT
ENV JAVA_VERSION=18-ea+23
# Thu, 18 Nov 2021 17:33:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='e9f310e519b12280fc023ab4b734e533377e212ae77da8981f462c2849851316'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b235ab4e5dc79031e5c08593080c58ec66b96b530e023e5c789b040d0095a3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Nov 2021 17:34:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a39cfde620ea7949c12d65ef5a24d4b6f737bb5a2f57d9a4a16013c060c9c67`  
		Last Modified: Thu, 18 Nov 2021 16:07:11 GMT  
		Size: 42.1 MB (42098006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a90c9cadc5331c54e5f53b906e967fe1942c54666e8da9bf055c378d02b2ad`  
		Last Modified: Thu, 18 Nov 2021 17:43:13 GMT  
		Size: 13.5 MB (13511675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6da1fe6812ea2ec39f0250dc78349d20476a44d1a7aa035090a48755ce177e7`  
		Last Modified: Thu, 18 Nov 2021 17:43:29 GMT  
		Size: 188.2 MB (188197245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:627467d99437e3ffa790f62cdf37e040379b7e162fd55647da9fc4ee6acf4f93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243438164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32861ed6d98395b5128faed46cba7ce86aca17b19bae731e782372b8e0d9544f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 19 Nov 2021 02:35:27 GMT
ADD file:31ec2bba02fab51f683553c78815a422089e6227bd4a65d33f35bc15588da3f7 in / 
# Fri, 19 Nov 2021 02:35:27 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 02:52:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 19 Nov 2021 02:52:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 19 Nov 2021 02:52:31 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 02:52:32 GMT
ENV LANG=C.UTF-8
# Fri, 19 Nov 2021 02:52:33 GMT
ENV JAVA_VERSION=18-ea+23
# Fri, 19 Nov 2021 02:52:48 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='e9f310e519b12280fc023ab4b734e533377e212ae77da8981f462c2849851316'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b235ab4e5dc79031e5c08593080c58ec66b96b530e023e5c789b040d0095a3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 Nov 2021 02:52:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c621c1ca8ceb7b3c3055633f5e537023039566ffcde238e41463f74eb6396051`  
		Last Modified: Fri, 19 Nov 2021 02:36:28 GMT  
		Size: 42.0 MB (42011387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d87024ee2f6936bf9ad81953e5ec643cddc67e7055ec11cf737242c60e2c9b`  
		Last Modified: Fri, 19 Nov 2021 03:04:14 GMT  
		Size: 14.3 MB (14300939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d2b468f6ba40357d0e98384b80aa1e832d2ff003a4d5dcc938320c9d2a6473`  
		Last Modified: Fri, 19 Nov 2021 03:04:30 GMT  
		Size: 187.1 MB (187125838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
