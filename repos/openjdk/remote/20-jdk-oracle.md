## `openjdk:20-jdk-oracle`

```console
$ docker pull openjdk@sha256:0b1752256fb9a6ebecc495d1c5556df816028b3601b686f97e6d0f4a0ffbec5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:679b7488a7ebd07083fe88c8f29343ba0f420f22f210acaf29050418f408df95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248933728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460f1f8ec7b99f201eb878124cb841e05f99d09993b30f327a6498785e5173f4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:17 GMT
ADD file:e76040b70aaa15ee2b85f92df1b68036afd42973f25268e4771380f7126cb38a in / 
# Wed, 24 Aug 2022 19:35:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 22:43:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 24 Aug 2022 22:43:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 24 Aug 2022 22:43:59 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:43:59 GMT
ENV LANG=C.UTF-8
# Wed, 24 Aug 2022 22:43:59 GMT
ENV JAVA_VERSION=20-ea+11
# Wed, 24 Aug 2022 22:44:09 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='9a0afe9f1c3ef50968060fe8d70d7b27d93b5515479846193de809127f0d427f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='d7e80f5000f66440c34073bdb0e443b941ef11209ca30f0e698f07a3fce08118'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 24 Aug 2022 22:44:09 GMT
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
	-	`sha256:8e4085c01f12269f3bfe0ff8bc09c58bfdf3cbae52e145e9d18d66c7466544e2`  
		Last Modified: Wed, 24 Aug 2022 22:49:10 GMT  
		Size: 197.2 MB (197187965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f53c94953d7782e65bd238521baf9527a82d1609ca7151aae27d62a2d1e603c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247075715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200042f190ac6e17b5fd88c19a4a07e9523a6be1d88b993c5f4dfbf924ab972`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Aug 2022 19:54:55 GMT
ADD file:2016956ebf5b305d0029ca641d3175f879fb9c5f35f801b5c52927afeb8f8422 in / 
# Wed, 24 Aug 2022 19:54:56 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:30:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 24 Aug 2022 23:30:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 24 Aug 2022 23:30:53 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 23:30:54 GMT
ENV LANG=C.UTF-8
# Wed, 24 Aug 2022 23:30:55 GMT
ENV JAVA_VERSION=20-ea+11
# Wed, 24 Aug 2022 23:31:09 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='9a0afe9f1c3ef50968060fe8d70d7b27d93b5515479846193de809127f0d427f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='d7e80f5000f66440c34073bdb0e443b941ef11209ca30f0e698f07a3fce08118'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 24 Aug 2022 23:31:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4fad3655bea38b31843315fea6a076b3b13bee189d1b3d017cf9beb5feb39909`  
		Last Modified: Wed, 24 Aug 2022 19:56:49 GMT  
		Size: 38.3 MB (38320858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299639459c280cc4a1b9d1299ff192e2925aef24610273aa1288cbbecdd6e689`  
		Last Modified: Wed, 24 Aug 2022 23:40:50 GMT  
		Size: 13.0 MB (13041901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06546da9b4041ac61aacd811b33df80e61039e8801e487745cd27fe0a1976d91`  
		Last Modified: Wed, 24 Aug 2022 23:41:04 GMT  
		Size: 195.7 MB (195712956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
