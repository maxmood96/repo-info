## `openjdk:21-ea-15-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:0ca5f54b353a014c7372e26f58e1e3591c73cc802da1262b0815cdb76b497dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-15-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:1e765dd1a8f6fa157fa6d33f42f7e2afd816a907f517fb90211775966d05328c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261139952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c451870e361cf7f6dc5c0c57a64b1acb82c67c89864da9030edd65bca9c266a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:39:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:39:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 29 Mar 2023 00:39:18 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 00:39:18 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 00:39:18 GMT
ENV JAVA_VERSION=21-ea+15
# Wed, 29 Mar 2023 00:39:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='0fec1002b8c8975b181bd6966a817028d6b373cbc759254231f9b96db1fe6edd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93cc1eb6202093a127f1f9ed2e866a51dff29321f878085c18f317cefb113ffc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Mar 2023 00:39:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76522ebbbebe1d33d391848d9f7910bda3808bb7ca0ec5f2a7f84db25521768`  
		Last Modified: Wed, 29 Mar 2023 00:40:36 GMT  
		Size: 15.0 MB (15006652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e21df7acaee6af113a84facd0a98a4333a3b99a721e8a086a1d8ec388cf026c`  
		Last Modified: Wed, 29 Mar 2023 00:40:48 GMT  
		Size: 201.6 MB (201571124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-15-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b63242539e333f181a05f7d40f16ae18da4cc71d8aa4a309e806c5562330ea5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259356063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6073ac1fc33d44fe0bb06ed99a4173f83bb2d54449dedbb7d2d26e08c11d3fb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:59:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:59:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 29 Mar 2023 00:59:46 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 00:59:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 00:59:46 GMT
ENV JAVA_VERSION=21-ea+15
# Wed, 29 Mar 2023 00:59:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='0fec1002b8c8975b181bd6966a817028d6b373cbc759254231f9b96db1fe6edd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93cc1eb6202093a127f1f9ed2e866a51dff29321f878085c18f317cefb113ffc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Mar 2023 00:59:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015334e79538f75edd26ca4da7bffb8eb69d94d9292d602053b1fd07f37c8cee`  
		Last Modified: Wed, 29 Mar 2023 01:01:08 GMT  
		Size: 15.8 MB (15844650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34f8291c956e0648177e2c357ab96eda4c15cc9c5eca0d7f80a495e120a34ba`  
		Last Modified: Wed, 29 Mar 2023 01:01:18 GMT  
		Size: 200.0 MB (200034425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
