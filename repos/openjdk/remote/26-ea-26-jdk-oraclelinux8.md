## `openjdk:26-ea-26-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:d43cded64e03e067a2d75f4e83553c6a8ca9bb453e01ca391ed15f6f13c2716b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-26-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f63d2fe5034bbb46cc99f324e72dc54ce51043682799252f7e4ce656260f2f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294456739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afe50b7c7e5e116faa6935d84e7ed1469bf1df010032607764459710acb82f9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:50:37 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:50:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 01:08:32 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 01:08:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 02 Dec 2025 01:08:40 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:08:40 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 01:08:40 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 01:08:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 01:08:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b436d89f13c92f9703618820d992b4e1f2b38ba243024b251c81a610f04c67b1`  
		Last Modified: Tue, 25 Nov 2025 23:51:01 GMT  
		Size: 51.4 MB (51378078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89cd857e680f8767fe7edaa9fb984609214e2b974b26c47cda44aff8d7ccd01`  
		Last Modified: Tue, 02 Dec 2025 01:09:27 GMT  
		Size: 15.0 MB (14999282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6427d04b14a82c50c465c4e8d6e047a26a72af7f5ffd8c824ac40750b13dbcce`  
		Last Modified: Tue, 02 Dec 2025 01:09:05 GMT  
		Size: 228.1 MB (228079379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9008c3a1bc95c0b94d3a6148eb6ba72ad7735feafd449aa5875ffab2f8cd42bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67e33fc3a12aa8c39c863b5d7c9314b3e0fbfc7badae4fcde5a70848e9d766b`

```dockerfile
```

-	Layers:
	-	`sha256:50afba1ca2da341acb2f01e9be1b82629b903cce74d78aaa909dc7cf0099c013`  
		Last Modified: Tue, 02 Dec 2025 04:24:00 GMT  
		Size: 2.4 MB (2448013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccfadd64774decb4c0c3d4a320494ce2f191885cbc6cef2bb07c44814c3c3be`  
		Last Modified: Tue, 02 Dec 2025 04:24:01 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-26-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:582b0d358fc9d596aa331822427cf8a8b8f6e5eb1602b139bb833c1982cd9823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291808701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727d0d834ab38efddff427a46188a2bf1790e7e3c66cbb13a415c4d32b32f802`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:37:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:37:54 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 02:32:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 02:32:59 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 02 Dec 2025 02:32:59 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:32:59 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 02:32:59 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 02:32:59 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 02:32:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:674388ef21c06396c4d40407ba2af1c3a42c30a5cb162fd4355950be7600edf7`  
		Last Modified: Tue, 25 Nov 2025 23:38:20 GMT  
		Size: 50.1 MB (50103076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb7e96fcaa0d0ca90b3b069efba760660742cf8a061a7542e5957a07bddbc8f`  
		Last Modified: Tue, 02 Dec 2025 02:33:33 GMT  
		Size: 15.7 MB (15691573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd5b547e53e70426cc9f31d6283e258e1fc7843b9c1a20b33e261d1babe3fa0`  
		Last Modified: Tue, 02 Dec 2025 02:33:26 GMT  
		Size: 226.0 MB (226014052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:258670f797b92e97b1735c96041cfd57ac79d12798d6d97930d6bf2a020f2120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3a4a51e9d9f6c5330a15e1dc35c736efe5e0b3fd8919ac55b6c9f7c0e90803`

```dockerfile
```

-	Layers:
	-	`sha256:7b4b3da63287642bea96626ac088fa12353076a28fa9093d2e559407639b89ad`  
		Last Modified: Tue, 02 Dec 2025 04:24:05 GMT  
		Size: 2.4 MB (2446823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8825533bc0b39fb433cf460f118ca53e38b460d268f4762fe352bad3cf0c203d`  
		Last Modified: Tue, 02 Dec 2025 04:24:06 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
