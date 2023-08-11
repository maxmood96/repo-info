## `openjdk:21-ea-34-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:0aa4165eccb2bc46dd7d65fc3eccd2fc1dc737f03068b430b8c5ec704e727c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-34-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:e5f953030f7bacf7c58634b976529132302350ad1e0722d16f6b2cca6031f1a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263855990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169752ca61233f252e6cb1c9c711ca8c76c5ed07ad13db50dce5bd183e6ec066`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:32 GMT
ADD file:6d43f7bf7c8d8c056e6fcc566ccfa2c1e42be1ef095f94d6780d0ca7d9a02e6e in / 
# Sat, 22 Jul 2023 01:20:32 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:40:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 22 Jul 2023 01:41:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Sat, 22 Jul 2023 01:41:26 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 22 Jul 2023 01:41:26 GMT
ENV LANG=C.UTF-8
# Fri, 04 Aug 2023 00:29:43 GMT
ENV JAVA_VERSION=21-ea+34
# Fri, 04 Aug 2023 00:29:54 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d16356385a726320077563c6180f2eabf72ded64b5695f24f3e7a2d3980b1f11'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='cb862b1f34e15c99aacab2c9e6ed259ad056eaa3dfc547ebc6026630db64af94'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Aug 2023 00:29:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49bb46380f8cb3491e82d000b27a6eb26b2490291da814ce3363bbf2c8baeb1a`  
		Last Modified: Sat, 22 Jul 2023 01:21:47 GMT  
		Size: 44.9 MB (44915006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c78e257f8d32905a5685feaf98c164b8091b3f15fb7705c4181bd3998b783`  
		Last Modified: Sat, 22 Jul 2023 01:42:50 GMT  
		Size: 15.0 MB (15009045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2812a03d4b572a1bd76105c08f15689f45786628f00ca726def2bb7196eb2d6`  
		Last Modified: Fri, 04 Aug 2023 00:36:13 GMT  
		Size: 203.9 MB (203931939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-34-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:659b0f85de2f031b3393213c164e40143a84024d6946ac9bf360538f99b83a7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261560882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8e53658b9a973129890e482df183a703997e469b77457c8165eb8bdf2f99c1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Aug 2023 00:40:33 GMT
ADD file:24663feb951dcfae36948e6cbc8697e8bef563d86c15af3daa54a1b830965593 in / 
# Fri, 11 Aug 2023 00:40:34 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:11:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 11 Aug 2023 01:11:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 11 Aug 2023 01:11:44 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Aug 2023 01:11:44 GMT
ENV LANG=C.UTF-8
# Fri, 11 Aug 2023 01:11:44 GMT
ENV JAVA_VERSION=21-ea+34
# Fri, 11 Aug 2023 01:11:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d16356385a726320077563c6180f2eabf72ded64b5695f24f3e7a2d3980b1f11'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='cb862b1f34e15c99aacab2c9e6ed259ad056eaa3dfc547ebc6026630db64af94'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Aug 2023 01:12:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd2ec1b01835c3bcf117123886f982435cd8e445790b761779f35779d61faad3`  
		Last Modified: Fri, 11 Aug 2023 00:41:41 GMT  
		Size: 43.6 MB (43625591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7023146e285ffba3adcf0df2d0ef98b1f28c00ef46b2ffc20a5c3d01540eba`  
		Last Modified: Fri, 11 Aug 2023 01:13:09 GMT  
		Size: 15.7 MB (15666637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0f94eb1652cb21489d1a1719225ceb4b47f1694be38e244e6b95d9f32990a6`  
		Last Modified: Fri, 11 Aug 2023 01:14:14 GMT  
		Size: 202.3 MB (202268654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
