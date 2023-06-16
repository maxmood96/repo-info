## `openjdk:21-oraclelinux8`

```console
$ docker pull openjdk@sha256:136da3364642518b55349747bfae7bbda528c7f31522f45d8265cefabaae1f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:796782223bf8cabee6a5f7d406c12262b3cc1c8fb19a5d73abc620993ac6f89e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263705937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9b7eedb1690c8a931669941dbf7c64a4cf926a75c9e719d37417ef3f49c0fc`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 04 Jun 2023 17:54:32 GMT
ADD file:39d09c6c7c3a0f64981f5cbcb12cc8f0128979c3d4b91d74c84fe62aca5ea87e in / 
# Sun, 04 Jun 2023 17:54:32 GMT
CMD ["/bin/bash"]
# Sun, 04 Jun 2023 19:01:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sun, 04 Jun 2023 19:01:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Sun, 04 Jun 2023 19:01:15 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 19:01:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Jun 2023 00:27:25 GMT
ENV JAVA_VERSION=21-ea+26
# Sat, 10 Jun 2023 00:27:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='16c6b09c742e73c9e092134517ecc36db2a5e44453c8b8b5374cfac1ee367a28'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa59bb222c548c18c21cb05a71854a46263a618a72ec6f2f408328689280380d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 10 Jun 2023 00:27:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e0c3751e6482e67b70ffad144b2cb9aec9be672df2642a322e875e51b748aeb`  
		Last Modified: Sun, 04 Jun 2023 17:55:32 GMT  
		Size: 44.9 MB (44872720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5b8981d150f5706ec1b30f459a99b1c25abb86225512911608e4175546c8d9`  
		Last Modified: Sun, 04 Jun 2023 19:02:11 GMT  
		Size: 15.0 MB (15004426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85f1a70ced789c6238073d0956e694bd24f2e7a8c37cbea80fcf528436d88cc`  
		Last Modified: Sat, 10 Jun 2023 00:29:38 GMT  
		Size: 203.8 MB (203828791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d39168aa1aa08306cc7330e03aeae238e6b90a1e181cd82819229c352634b7f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261445740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d54493c4d9e620b05d91d4ad257c4f8ee23068ce7c17ecb0a4d5e6ee14f1ab5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Jun 2023 23:40:30 GMT
ADD file:37cef5fcd08f57d005adb8f14f69ecc78a9c669280f45f7d81b1c899489e93ba in / 
# Thu, 15 Jun 2023 23:40:31 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 23:59:49 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 16 Jun 2023 00:00:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 16 Jun 2023 00:00:10 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 00:00:11 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 00:00:11 GMT
ENV JAVA_VERSION=21-ea+26
# Fri, 16 Jun 2023 00:00:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='16c6b09c742e73c9e092134517ecc36db2a5e44453c8b8b5374cfac1ee367a28'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa59bb222c548c18c21cb05a71854a46263a618a72ec6f2f408328689280380d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 16 Jun 2023 00:00:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:029ab4a5f8e75aadbbba1505624cf10a4c35a0fd897cc85b9e7536785b8ba37c`  
		Last Modified: Thu, 15 Jun 2023 23:41:45 GMT  
		Size: 43.6 MB (43601336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cca9ab147b9b93cf01a583c33e8ade844f6d31bfb69334e1614ef5dd4d6a973`  
		Last Modified: Fri, 16 Jun 2023 00:01:25 GMT  
		Size: 15.7 MB (15673775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e8ecd9a6a9f7f006a2749ab8d2e70b8093b984a849d945f467a03d574acd69`  
		Last Modified: Fri, 16 Jun 2023 00:02:28 GMT  
		Size: 202.2 MB (202170629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
