## `openjdk:19-ea-33-jdk`

```console
$ docker pull openjdk@sha256:f87be5327cf5bd58adb8a636dde241f4e094fd289fc9dce150feac0e21de2357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-33-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:43b2ba4532fddcd78f0335113f6c6e0959ebd583c396ab57ead86209f322c5c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248904023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9616e9959323572145e38dcf4e38935e7192cfe086e8c253c9fde23eab4fa458`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:49:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:50:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 05 Jul 2022 22:50:40 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 22:50:40 GMT
ENV LANG=C.UTF-8
# Fri, 29 Jul 2022 02:04:27 GMT
ENV JAVA_VERSION=19-ea+33
# Fri, 29 Jul 2022 02:04:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/33/GPL/openjdk-19-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='31aa1cf0a266dfc90d9e85d688379a2b2b9b1888bb7df326a4434dc92fdc105f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/33/GPL/openjdk-19-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='8e758bdc4cd496f29c85a53ce1eb155b7ee8f945c11517cc4a766492349c52e2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 29 Jul 2022 02:04:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e62647f09f0ab1a3ac2d84823777bead33aa8e201c13b86c063296e8268023`  
		Last Modified: Tue, 05 Jul 2022 22:58:01 GMT  
		Size: 13.5 MB (13505357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8d410d7ec7b2575f28cff89f6c4dc0b5ef15313985b7dddc9cebca466e27eb`  
		Last Modified: Fri, 29 Jul 2022 02:15:47 GMT  
		Size: 196.2 MB (196176545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
