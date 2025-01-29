## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:648ce79b3f74b428b16b041b7327909422b987f8c79655b0afb9711bc1c3b416
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:21076f26dc7fcb5cc03e7b27510feef1fea18f9fdc8a5f0e56174cbd77e14e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279495710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023ce4f6dc48cc55c5463f6627f975f8d80169218705d534f7fd0b0d64bebfc7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 15 Nov 2024 23:04:32 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e3c42a0bc9e3ee9b30fb54e21599f95b05cc1edb9540ae2f9fe9ec30b7bc5a`  
		Last Modified: Tue, 28 Jan 2025 23:28:46 GMT  
		Size: 15.0 MB (14975226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd42a5acea8614d9efc13ce0fb0f22d277c7622a6ef6b9cfdacc0e01bbf6e090`  
		Last Modified: Tue, 28 Jan 2025 23:28:49 GMT  
		Size: 213.2 MB (213245492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f04e2aefe9c6b9eb11822e53ff1d687bfcd5a8847697f2cfd79c5e1b23a918b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedd2695a9f136ee39342a9904d5050350c80965fe7ff5d411ff5dbd8f8c1d2e`

```dockerfile
```

-	Layers:
	-	`sha256:9876947d3e928116b382d2e5c31f9814f527a6968b1c11ced36adcdad9f21a53`  
		Last Modified: Tue, 28 Jan 2025 23:28:45 GMT  
		Size: 2.4 MB (2441585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54501527639b6ca46da2d68d2db6f54dbb686e1227c3ffcbc7dce320f76465f`  
		Last Modified: Tue, 28 Jan 2025 23:28:45 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e6b474d7b186b0503189071e219a24e46bba71b4b48bc72ce569581886fb4704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276850691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe68b37acf9cc72a4cbb830ec7f8444c18617f3c01319cfb1622752b1c41c213`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:54 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad1cd9205a89581b21ab3876711618f2acded12b00d2b5d3a9daefffa65ac7c`  
		Last Modified: Wed, 22 Jan 2025 02:31:00 GMT  
		Size: 15.7 MB (15659984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef166be32fd25416f8676a4f45c8532619a22d121c58790d776fdf1b2ca8cbe`  
		Last Modified: Tue, 28 Jan 2025 23:38:37 GMT  
		Size: 211.2 MB (211210432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7b4d327149f9391462f4964b8ef0468230c8ae7c257b7f8fc13f54261465506a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95b030df8034aeb1d5a1a1b60c6942bbaa28e10c5cdc6f8c08d31fd1897bebf`

```dockerfile
```

-	Layers:
	-	`sha256:53ccb9a54b065e80a9c4da77d0b5de945428e2b275b6bc707f7e2814a0145a43`  
		Last Modified: Tue, 28 Jan 2025 23:38:32 GMT  
		Size: 2.4 MB (2440431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee18adf8514b6f71502b77b66215cd5db876d98312ede1f2b8c0b977469e8eb`  
		Last Modified: Tue, 28 Jan 2025 23:38:32 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
