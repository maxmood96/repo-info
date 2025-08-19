## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:17771308fce82e8a3555cad5ca5ea05506aa2ca76a4efb0609043d782f6a85bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d8156c2ee483f744b8da33acc4a533a01b7b24d2842f3252609c99367ce744e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289788234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d89a4c226085d5ba528ab8877c44d36473e1d959a06742293443c343fd84d1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:58:59 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:58:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:816eb39a0552da23131629c02b98cdeccbfcda79ce23b4283b51ea7845bdb4e5`  
		Last Modified: Thu, 07 Aug 2025 23:49:07 GMT  
		Size: 51.3 MB (51323465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dffa126367aadd7556b2e5ac7d349534b4040e261d02de6dbb945ba334ab56c`  
		Last Modified: Mon, 18 Aug 2025 18:17:06 GMT  
		Size: 15.0 MB (14977027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8794da544e6f075b00a7799a421bf51ba94d6d8a35adac20cf0cf55e3614e89`  
		Last Modified: Mon, 18 Aug 2025 21:37:42 GMT  
		Size: 223.5 MB (223487742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:0cee77b7862360d569f50ee8ba140f1ce91820889c2f2e291bf771c2a4f0d555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3884418ae97b8bcf94c0aba7f82c4e746a891e944094cdd8319d4b23a8d1e6d7`

```dockerfile
```

-	Layers:
	-	`sha256:178e78e8b4e45422ed2ddfec270a4df69207e686da9a5bf68b8f47623bcfc657`  
		Last Modified: Mon, 18 Aug 2025 21:25:09 GMT  
		Size: 2.5 MB (2451093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4503e35d6aa0574236eeb199a845d9a4217a2c6984b7dac81ab3c700e8a5cff`  
		Last Modified: Mon, 18 Aug 2025 21:25:10 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7182ee0415f35c7a263d8d578ec0d3ef47bebbfcaddd990e21e5631d2cd2a643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287049466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fffcf2f17537395579d01ab0d611a34e7cc0ade0de295559653dd68cc83ffbe`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:59:57 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:59:57 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00aea10d937a1f6a212468c9a6eb06043ca5276b560643f3c75b3b2d11325b17`  
		Last Modified: Fri, 08 Aug 2025 01:31:37 GMT  
		Size: 50.0 MB (50035024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c37ff1ab922b373a81603dbefbd345e8daf8902d5e960727d0807504e32e43`  
		Last Modified: Mon, 18 Aug 2025 22:41:23 GMT  
		Size: 15.7 MB (15672355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfd7c2b99fe9dab3c9679ddbe3426879f5357acebef1c273ce06b35ddcbc14`  
		Last Modified: Tue, 19 Aug 2025 18:13:39 GMT  
		Size: 221.3 MB (221342087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:172e7949a02db5cb720d07c1472a986d1ab1b05c577d6505ca012b2ae9b0a77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de777eda841f8eef1facb1396e536d5ba59df100efd9790a24ca851029706d69`

```dockerfile
```

-	Layers:
	-	`sha256:5678f7632ec7bffcb993d9b04cff618d5dbb54c0cd7446cd8b0e6f4e6c260733`  
		Last Modified: Tue, 19 Aug 2025 00:24:45 GMT  
		Size: 2.4 MB (2449927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55113584bf58349c9501800030923f198946757e05375f7cb3ef1ad103bfede1`  
		Last Modified: Tue, 19 Aug 2025 00:24:45 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
