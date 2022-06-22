## `openjdk:20-ea-2-oraclelinux7`

```console
$ docker pull openjdk@sha256:d97f4f686e1c4559edca5566ae45d9e1bacf99a12c471fb0a0273f368a8ce08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:20-ea-2-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:9c8576320de4f3af6a93c7de7d0d9a78f329067fb64dfc5886719bd1ce96d0ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260146434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9186289864dcb23607745a395939862e69d4660d61cbb8f292f25d90036bcac5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Jun 2022 01:22:07 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 16 Jun 2022 01:22:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 16 Jun 2022 01:22:07 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jun 2022 01:22:08 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 Jun 2022 01:20:17 GMT
ENV JAVA_VERSION=20-ea+2
# Wed, 22 Jun 2022 01:20:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/2/GPL/openjdk-20-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='21ff68a0fba20bd62c33f66b6215e4dbb6a4ccc40ee4c63aefd5a69ded443812'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/2/GPL/openjdk-20-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='23ec06e04606ac8ccd9f304bc06527f78c6a196b796b8b7581de2153a3097bff'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 22 Jun 2022 01:20:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63183c9b4598e16c4cef95f706d50ff6c928de41f391cd513495b27eaa27bf89`  
		Last Modified: Thu, 16 Jun 2022 01:21:08 GMT  
		Size: 48.8 MB (48757931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb5aec2fa88dbfc29b4af04e13302acbb1298cf96be28433c81b5293be618be`  
		Last Modified: Thu, 16 Jun 2022 01:31:20 GMT  
		Size: 14.2 MB (14236378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850ef979bd7af977664f80b3fd5ee38779ae066116ef3cd48e7cd96a1f20e094`  
		Last Modified: Wed, 22 Jun 2022 01:30:23 GMT  
		Size: 197.2 MB (197152125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
