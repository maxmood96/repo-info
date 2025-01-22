## `openjdk:25-ea-6-oraclelinux9`

```console
$ docker pull openjdk@sha256:65fa5a4eb7caceec2dc81d6737b87254439dbc91e8c85b98658c685bbc7a0e12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-6-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:b447fd351daa3e8bb890062946722de1c97e7dad9942bb02d5b7b3a735ffa1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309555462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06cf882c494720c338ec81a5dfaa71aef3f3e2649385766d7c503b08313632ff`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0568608aee291abba0f6e2e1a336cf612599f23a633494beb0d0b7c98264859c`  
		Last Modified: Wed, 22 Jan 2025 02:29:09 GMT  
		Size: 48.8 MB (48773941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465a6de24f6a349a82adfc49f628f8c943ab9971ef3085d0825caea690f83c58`  
		Last Modified: Wed, 22 Jan 2025 02:29:13 GMT  
		Size: 211.7 MB (211682819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-6-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:541422b274befe97d8b0961280c70a1f24876bbf72b6d6e0264fbbf8934ee413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4aa3554e561cee2ff3bac8483824e0b65ac7af86ca0893433cccc146938fdc`

```dockerfile
```

-	Layers:
	-	`sha256:37db238d5fee0dd8443853dce30bc8e71a19f6bc236cb50055cf6135fdcfd962`  
		Last Modified: Wed, 22 Jan 2025 02:29:08 GMT  
		Size: 4.9 MB (4906931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f20b0868584da0d834c8dec6267d9fca6bc411515e1ac7f11238c839f834ef`  
		Last Modified: Wed, 22 Jan 2025 02:29:07 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:965f353c9c057acd13a8052339f8f89558f074fb05b0a72dab60309525d69573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306504535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce785a1c2a5770e3807b95af96f4344d473744505014f332c399ba3cc7049be`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9527a70a5df0c50a0919b2bbc807b6789f8d6833d49f997079d3ab5dd2e735`  
		Last Modified: Wed, 22 Jan 2025 02:29:30 GMT  
		Size: 49.2 MB (49203729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d54504677ed6cc05b49093e10a007184bc27b9c9b79a85883b017b10a76da8e`  
		Last Modified: Wed, 22 Jan 2025 02:29:33 GMT  
		Size: 209.6 MB (209633414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-6-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:0d1d80eb9a02c3b92e9189ccc97fc83c680cdfd7e5c1d2b76a0271d549187a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4acca107fcb8b23cec13696972f2b291f5fb60c1a52e845219b28de1ebbca0`

```dockerfile
```

-	Layers:
	-	`sha256:d5ba560c5c1aace059e6200aaf45a21264c3ea926697f6b31100daa4eb4192cc`  
		Last Modified: Wed, 22 Jan 2025 02:29:29 GMT  
		Size: 4.9 MB (4904693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2a7b013d323639ddb5df82a8c9cba620f19aef87be2ecc97267f4ce4df6f67`  
		Last Modified: Wed, 22 Jan 2025 02:29:28 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
