## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:f3b8ea76d3f176652b92e28d80c155cd7034ed2542a701da585e09c09656bb3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:2946b9dbfedaa73e77e8734ebb088a9bd0a73e9763bcb2d1f573615a7918dd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292704974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35d30935234b2cac61ee9942a5ba6ee2f87a217981b817fd12231a77a1021f0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Oct 2025 17:25:39 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 31 Oct 2025 17:25:39 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 19:52:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 10 Nov 2025 19:52:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 10 Nov 2025 19:52:49 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:52:49 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:52:49 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:52:49 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:52:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fff3d29c5b5b28d342ba8d967679d9f76705eab0cf1b9c1c2a8d43102cc524c8`  
		Last Modified: Fri, 31 Oct 2025 17:26:00 GMT  
		Size: 51.4 MB (51383677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26397399be5556a8b06fbb425c783b623925fe0c0b1140a43b3e08bf2abbd803`  
		Last Modified: Mon, 10 Nov 2025 19:53:27 GMT  
		Size: 15.0 MB (14997841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eebbaf7dd6c0d81f911e14893057160cd5e66421d0a8d84221ed439c173506e`  
		Last Modified: Mon, 10 Nov 2025 22:30:28 GMT  
		Size: 226.3 MB (226323456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:678253ed74b3ef6c3cbc1715ec5c6a1d48ea46c9e9a3d8ceed3cbec6487b9cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfe1c8f4fbf31bed37a66647fd8e2c6595d6f8ab36594c7105b77ee7ec5347c`

```dockerfile
```

-	Layers:
	-	`sha256:667994e9e7fd6d3d6493a09e6e58df9b1da8f725b9526fa9c0a6343afc1e5dca`  
		Last Modified: Mon, 10 Nov 2025 22:23:59 GMT  
		Size: 2.4 MB (2448022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bc1455e0604d848b79e6d49ec9a6d7cd597239a907a6c19e32856c70a3636f`  
		Last Modified: Mon, 10 Nov 2025 22:24:00 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e543fdde29a9b523d1fe3236b8ce4d63de57298ef12479c479e64d0d9957b8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289939316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941ff1b7498d64fe68a16dace2f07bbb2be86e08ed69c6256a153b72cffa4dcb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Oct 2025 17:25:14 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 31 Oct 2025 17:25:14 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 19:53:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 10 Nov 2025 19:53:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 10 Nov 2025 19:53:27 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:53:27 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:53:27 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:53:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:53:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:913708617406390e2c3446d7f989f45259d9e8bc8c18aeb2c7030c867ecfb5d6`  
		Last Modified: Fri, 31 Oct 2025 17:25:36 GMT  
		Size: 50.1 MB (50102610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f44d53a768468dc127ed0a9d966fbe8bc953443e48676d38ba33b825742923`  
		Last Modified: Mon, 10 Nov 2025 19:54:03 GMT  
		Size: 15.7 MB (15663530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e727182e2fb5db4e833a959ba44bfc4ed2f82ac82590d756ea53b5023c334ef`  
		Last Modified: Mon, 10 Nov 2025 22:50:34 GMT  
		Size: 224.2 MB (224173176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:0d0db0c387d03abac574ff1598425cc6411986746203bac3d7f1cfb791c00819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8488130b3a923debdaf1e6e28bc3a2a51696222c80adb9b6c23965bc74f03203`

```dockerfile
```

-	Layers:
	-	`sha256:7f2d258fd8d38497011e57acaef9813123d266f981322d0286532404c61fccd1`  
		Last Modified: Mon, 10 Nov 2025 22:24:04 GMT  
		Size: 2.4 MB (2446832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b453aea28496a35a63b1210eaebbab6197559ce9ffc9d09b939a67739685fb5`  
		Last Modified: Mon, 10 Nov 2025 22:24:04 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
