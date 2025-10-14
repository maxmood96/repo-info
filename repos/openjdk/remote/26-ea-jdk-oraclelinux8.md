## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:68db976c6380e5756495417c27bd169c59152e7fb95c967b261b2e789ed9482a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:8aefd3aa41b79a5bc8deff10da675c721b37688675ad54fe25aea0acdfd9647e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292480022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa814a96c11de898612cf37e00e88515e8a4b2c1e83d360a3c5ec85452501795`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 11 Oct 2025 00:48:11 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:80e11c6d4bce0f7cfb8f6a005414529a5d7400a97a14d49bdd14af604c319592`  
		Last Modified: Mon, 13 Oct 2025 20:59:50 GMT  
		Size: 51.3 MB (51317609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92054f01fcbc0fa9fcdb7861ecdfdfb166e479b0b16b4836df2a39c03b71479`  
		Last Modified: Mon, 13 Oct 2025 21:10:08 GMT  
		Size: 15.0 MB (14991753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5592fe384c31786c5dad4290c7e8b087896f287e1abe3b5635f77763eadde67c`  
		Last Modified: Tue, 14 Oct 2025 01:25:53 GMT  
		Size: 226.2 MB (226170660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:18f23c5bdb75b0e0355a276ecb9f49351dfb00fe5ba829c09dbc73c7b1776a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3541af78c86f4f384c1932d264341bf10f6221a90ae88bf343d80ba05fcbe965`

```dockerfile
```

-	Layers:
	-	`sha256:2cb700f873d4626da76974e4cc2dda637e5265c6873d9192664ba70e0675164e`  
		Last Modified: Tue, 14 Oct 2025 00:23:22 GMT  
		Size: 2.5 MB (2451117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac31fc11686c03f417e8834d790c30465761f933c7ec1977331b263544dfcb7`  
		Last Modified: Tue, 14 Oct 2025 00:23:23 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c6f3ec9000bee0e12767aa857dcbbadf058229f22a1d56cf9857396dec1bcc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289724974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0357256a8a9b8d186f06e38c9b44e36784d4c178b5d411884f046fa4b4e33522`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 11 Oct 2025 00:48:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e02731574931ec9bdc32dd8c8318f7852e7941a5505a71857b506b382a97f7e9`  
		Last Modified: Mon, 13 Oct 2025 18:13:14 GMT  
		Size: 50.0 MB (50041880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e752ea6dd57e0a38431dd5e3daca8753f903c06706fa3e36843d8dd2001cf81d`  
		Last Modified: Mon, 13 Oct 2025 18:20:11 GMT  
		Size: 15.7 MB (15659314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80edc187a20cec1ebb639d80bcad40a360fcab08a835d85799051b1bffb5b61`  
		Last Modified: Tue, 14 Oct 2025 01:26:23 GMT  
		Size: 224.0 MB (224023780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b09747b573cd170ad1166d36991eaacbd9fffb34866882b052fccd5026c5ca56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02f44114bf7a9208f9809f97b44599e3b6ebe34a42e77d657a40953c669113f`

```dockerfile
```

-	Layers:
	-	`sha256:72811d52399de227981aba7e783793b960909ffaac82fdb802012d09e0212da8`  
		Last Modified: Mon, 13 Oct 2025 21:24:02 GMT  
		Size: 2.4 MB (2449951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135b138cd682c80181ff90e9412e59c364eae9df8fedc9da165f2f558f5b4dd8`  
		Last Modified: Mon, 13 Oct 2025 21:24:03 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
