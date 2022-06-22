## `openjdk:19-ea-27-jdk`

```console
$ docker pull openjdk@sha256:5fc13e2586a03fd6da222e0cc9baa023b8c752e2fd9a39612ab08e8fb20d84a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-27-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:a6ac8d51737acc785bdc5402145e4231c82d7b9ad36a837bf90dfda011e02c1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248851180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e129611dd9940131469f7a5203d13d888f3e3c5715c7151649c607e4d7af7543`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:26 GMT
ADD file:837f6c6e7e20067b92edb72e78a8399e6cbbd72dab23db7b5b5a301c58d2a0de in / 
# Tue, 14 Jun 2022 18:23:26 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:42:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:42:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 14 Jun 2022 18:42:55 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jun 2022 18:42:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 01:21:34 GMT
ENV JAVA_VERSION=19-ea+27
# Wed, 22 Jun 2022 01:21:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/27/GPL/openjdk-19-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='d88a9e824ce2c65fd634463856a6af2e8aad09a3b005a6ae9f3529b972d184c4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/27/GPL/openjdk-19-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7e93f0cde43b50161e5817e8a12907f5a2e74dbd63a4fa99d059ba4afdab02ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 22 Jun 2022 01:22:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f160c0f6cac587a73883b48a8857f5cce0930112792cef25c62510e256e93dc`  
		Last Modified: Tue, 14 Jun 2022 18:24:18 GMT  
		Size: 39.2 MB (39219730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb499df0377a2bd9163e9a611ce46b5379196826787392defef98dbf215a8aa4`  
		Last Modified: Tue, 14 Jun 2022 18:49:29 GMT  
		Size: 13.5 MB (13502563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db5c2cf3ed98a4f2edad869b3695e0bbfd88406d94c911a407d295634987d6d`  
		Last Modified: Wed, 22 Jun 2022 01:33:31 GMT  
		Size: 196.1 MB (196128887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
