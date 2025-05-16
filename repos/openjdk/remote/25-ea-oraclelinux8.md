## `openjdk:25-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:7f7c1a1b12d484d7ae844ad39a6db6b186bf4f01d9ad84371ab04c0e4d92f702
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:228d47539c732a0fc32dc2bc2fed7c58647c2d19bf8387e58de71a2ec6477c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280223534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca473352df4555527ef19fe627d4926ead2c2c511dcc2cb9523a57219ec63af`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 21:48:19 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 21:48:19 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ee6d2b4bc3292763eeab29f03adacbfcd179273f648dc332abeb3f2f9cf99a3`  
		Last Modified: Thu, 08 May 2025 17:07:21 GMT  
		Size: 51.3 MB (51312878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3542659cd31ec51899b70cbd81e8d3be3ec10be6e469d8dccab8fb66278da1`  
		Last Modified: Fri, 16 May 2025 21:27:19 GMT  
		Size: 15.0 MB (14998001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641a8eec99c711eb9d9e125afa4c013ee7960366f19af5f992db7469d3085c29`  
		Last Modified: Fri, 16 May 2025 21:27:29 GMT  
		Size: 213.9 MB (213912655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b8cffaa22c7a9b176b2bbdec50e76504efd807ece43d8620d0ab2238772d9407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca56615660eb067a9716935855562c4bf66956cdb64e43a84d03c068989d210`

```dockerfile
```

-	Layers:
	-	`sha256:035d6c1840901d6ab40cdc879f78270da20ffe23383eb308c4c29cf3a2bc13c5`  
		Last Modified: Fri, 16 May 2025 21:23:57 GMT  
		Size: 2.4 MB (2449776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4efab0bfc7bff60f9c6ef7ce39ee1d5b80cb93f1ca1fcc638712ebd88e1f0889`  
		Last Modified: Fri, 16 May 2025 21:23:57 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:30b0f2fab23780bfc17b49753bed07c7f1ea031fc67d09fb024249a278dbad89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277373853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67620d7ad7add6f615f47207c0b0ce50e02f0d98c4ac865af0a0b95f2a46f3cf`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 21:48:43 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 21:48:43 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f9f09355eb5a75f94b3d65a17269700229fb600c0fa7b446c5cabbd22d410e6`  
		Last Modified: Thu, 08 May 2025 18:18:20 GMT  
		Size: 50.0 MB (50027777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e46de3b8fc0f00590b038000379cb18fb91e553260d144fcf9129a0edb74f0`  
		Last Modified: Fri, 09 May 2025 10:01:13 GMT  
		Size: 15.7 MB (15667699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f1c5aa495bf330ccdbdd51fb8f3fb3efa69220c9e68fe36030d4f8a8b35f13`  
		Last Modified: Fri, 16 May 2025 21:27:45 GMT  
		Size: 211.7 MB (211678377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:375b192190888dfdcfa730c9cbfeac8094deaa52cb1be5575f31dfce8cad8135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fe2b05a6102e133ead50bc9e8e5637c09a95b2345abe835d92f3a3a5bd3275`

```dockerfile
```

-	Layers:
	-	`sha256:c2d6a31bded1285d828a69c5bf91e3638b8ccc318032dc5fc8046c283b07a589`  
		Last Modified: Fri, 16 May 2025 21:24:00 GMT  
		Size: 2.4 MB (2448622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff6a3049cad4795d0a7d21070a78b51140b93766d5db20f8522c1e85f86da14`  
		Last Modified: Fri, 16 May 2025 21:24:01 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
