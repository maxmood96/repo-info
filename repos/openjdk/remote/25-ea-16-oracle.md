## `openjdk:25-ea-16-oracle`

```console
$ docker pull openjdk@sha256:4597b8147edad48483726d9763d1f5ebc9192277ade646854b1fc0c54eaf1c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-16-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:bd9bd3fd150000f48d9920332aec44368748987c7be88461b04db15be0702521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299380738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ff4c2966e7a409bb536798efb2b2b97e210218c6c6af58a25d9ad2ebd47dd0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 14:53:19 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 13 Mar 2025 14:53:19 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:804bb8ae89decacdf918af27c892df04e6f2d3038e3a7d1e34475eef6be9aba3`  
		Last Modified: Thu, 13 Mar 2025 17:46:19 GMT  
		Size: 49.1 MB (49091441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a7ae9329eea3c7ae283b83e09e2971faab47b6307c3b72ea402ca9ba3e57f0`  
		Last Modified: Thu, 27 Mar 2025 20:46:15 GMT  
		Size: 38.1 MB (38107756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabb2914999d0600d0ac19e2cce8496f847f38613d342b744f01b2286999fe9c`  
		Last Modified: Thu, 27 Mar 2025 20:46:19 GMT  
		Size: 212.2 MB (212181541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-16-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:306cf3bf6b711375e8e531df89136db69787214fd492a6341b9c263fac1b6e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0741e06f2a9f312c5d836cff433df3527801b38bd9264c006a3870ece8986f`

```dockerfile
```

-	Layers:
	-	`sha256:5d1fe8278a985c570b393132b0c43cbb2e05bc2f69b6de9baa5a1298165c99a0`  
		Last Modified: Thu, 27 Mar 2025 20:46:14 GMT  
		Size: 3.6 MB (3622594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:646efb0929a791b083a6209838358273e01949d30da1059f2c53b3035d55f0ad`  
		Last Modified: Thu, 27 Mar 2025 20:46:14 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-16-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:68a49f93b62ffd9060a041e1a75b14e36e53a80143b4216ab553dafb669d1e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296228936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4e87add867124e1a15f33fb6e6f01324aebbd402dbc450b4141dfa486b745e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 14:54:08 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 13 Mar 2025 14:54:08 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce92cb0849370fbaafa6ab88c7b03cebc3063fa56835d9dbf7d0b47c679a0097`  
		Last Modified: Thu, 13 Mar 2025 18:10:14 GMT  
		Size: 47.7 MB (47668022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f603eee483e7db27118eb6e115b494f4c84c9e0787decd993290afbae16ae0b`  
		Last Modified: Fri, 21 Mar 2025 17:23:03 GMT  
		Size: 38.5 MB (38492465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3c86dc30379af0ee02e43c68fb17b881b32523bfa9f62d99ecdd66735aac7b`  
		Last Modified: Thu, 27 Mar 2025 20:45:21 GMT  
		Size: 210.1 MB (210068449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-16-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:fffafd5991857410919daca434c722d4a0faff135abc6ac9c81ee2cc1615217a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f7a05a068ac762cb62853cff78dc8423822ea42b76bfb190022bbe112c04e0`

```dockerfile
```

-	Layers:
	-	`sha256:39db432db7081d99cac91e2d6585ffb037af26466c74ae27b7db37c2e21f0e38`  
		Last Modified: Thu, 27 Mar 2025 20:45:16 GMT  
		Size: 3.6 MB (3620356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c602cb8ac2757c21906b708e6fb6bcb351c4a4775bcc0c18e43ae11778f27413`  
		Last Modified: Thu, 27 Mar 2025 20:45:15 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
