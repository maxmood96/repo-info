## `openjdk:19-rc-oracle`

```console
$ docker pull openjdk@sha256:e5c9e6037284a2aa467e3562b0abbefc8fc750d035da9d18f4b5d498006fe6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-rc-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:e9cc208f2fb9ac1de7d607423d5c409bd46068a3a8daabb721a23f6a17fd596a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247929170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbefe9a1900dfe91a84feb1e48acbd70a12fa994f18cfe0fc6faa8e0d4c4af3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:17 GMT
ADD file:e76040b70aaa15ee2b85f92df1b68036afd42973f25268e4771380f7126cb38a in / 
# Wed, 24 Aug 2022 19:35:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 22:43:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 24 Aug 2022 22:45:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 24 Aug 2022 22:45:00 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:45:00 GMT
ENV LANG=C.UTF-8
# Wed, 24 Aug 2022 22:45:00 GMT
ENV JAVA_VERSION=19
# Wed, 24 Aug 2022 22:45:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-x64_bin.tar.gz'; 			downloadSha256='f47aba585cfc9ecff1ed8e023524e8309f4315ed8b80100b40c7dcc232c12f96'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-aarch64_bin.tar.gz'; 			downloadSha256='682bfb48158ca198393c4b7fd38f873e8d6316b0bc6511a07e917f7f0f3afb03'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 24 Aug 2022 22:45:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:918cd2ecf4de32b8bf40b176c816dc0d290beeabe9444526617cc8e6556c48b7`  
		Last Modified: Wed, 24 Aug 2022 19:37:03 GMT  
		Size: 39.5 MB (39515798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e128e3eff73d46e38372efa57d197de929f5bf8c0675c9e6fbcb3992894fc0f`  
		Last Modified: Wed, 24 Aug 2022 22:48:57 GMT  
		Size: 12.2 MB (12229965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56d05b8cb0306bdaf0de6ffe1eb563d5da612187ce2807a94ef9c83af314caa`  
		Last Modified: Wed, 24 Aug 2022 22:50:44 GMT  
		Size: 196.2 MB (196183407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-rc-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:189dad694f113dd04884524d69841a97452ac19edb9d4650f0ab81691b4cdd7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247326469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016472510a9db6fb77f5b8b072e611eac465df7eb2e9740a3ea32447b30c42ba`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Aug 2022 00:40:43 GMT
ADD file:a68d82fa032efe6adc2926f7e745508f0541bba3f906e2702d34252353100747 in / 
# Thu, 04 Aug 2022 00:40:44 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 01:01:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 04 Aug 2022 01:02:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 04 Aug 2022 01:02:12 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Aug 2022 01:02:13 GMT
ENV LANG=C.UTF-8
# Sat, 20 Aug 2022 01:52:54 GMT
ENV JAVA_VERSION=19
# Sat, 20 Aug 2022 01:53:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-x64_bin.tar.gz'; 			downloadSha256='f47aba585cfc9ecff1ed8e023524e8309f4315ed8b80100b40c7dcc232c12f96'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-aarch64_bin.tar.gz'; 			downloadSha256='682bfb48158ca198393c4b7fd38f873e8d6316b0bc6511a07e917f7f0f3afb03'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 20 Aug 2022 01:53:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecf56004177eb6ca162c88de29e84bc4ba3d2e7efd3703df9ecae51b89003d52`  
		Last Modified: Thu, 04 Aug 2022 00:41:51 GMT  
		Size: 38.0 MB (38023046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e225b6ab834ff85ee0d347a2859ecb14fc169f362360408133589ab8a37d8333`  
		Last Modified: Thu, 04 Aug 2022 01:14:59 GMT  
		Size: 14.3 MB (14278746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a89f5d78db565f47da576d71535b34117efb1d2df4d6a570286c3e2177eac78`  
		Last Modified: Sat, 20 Aug 2022 02:07:35 GMT  
		Size: 195.0 MB (195024677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
