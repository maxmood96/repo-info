## `openjdk:26-ea-26-oraclelinux9`

```console
$ docker pull openjdk@sha256:5f49b7a298049a5f53f5b2f37e8d8cc72736ac680ab4d7365fbda054c507b14c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-26-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:0cecf0b958c316696a90c0b33467db32b0625a46f4828897040d2ce154ae371a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313226909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2395ffc43b55ea072a15cd615219ec0cb86a7130e69e872f180b6c9bd863dd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:30:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 02 Dec 2025 21:30:17 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 21:30:17 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 21:30:17 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 21:30:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0fdb55d75527af0af90967c586ec5502184028e3af9b29734a75e4225a35c3`  
		Last Modified: Tue, 02 Dec 2025 21:30:59 GMT  
		Size: 38.3 MB (38294666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b8d089a69220faa694bfb599b86918e2b0c56c36333f819facff2798da69e`  
		Last Modified: Tue, 02 Dec 2025 22:25:26 GMT  
		Size: 227.6 MB (227617495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-26-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:51b52f8a19c36a7f2677d7576d13c27bdcbdeb0957b8ac251fbbba12336f29b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab4d5601ad688604c12b818f323cd59bad9223f1965d427d799568ad9a2051b`

```dockerfile
```

-	Layers:
	-	`sha256:e8b58ad06d813dc74dce906e1397998b2a4edd6691386dcbda0835d1728fd24b`  
		Last Modified: Tue, 02 Dec 2025 22:23:19 GMT  
		Size: 3.7 MB (3655331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef86509f8a0f44ae64a322c1790f33c31012d02a0e8dcf30a1f63af634ecb102`  
		Last Modified: Tue, 02 Dec 2025 22:23:20 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-26-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a27c1d5a3a2f01a133fb72fc5bdab2cda55f0a70fec88c9836f01aedfb65aee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310131987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876c22e6113607297ccc396222921ad1e9e65e66e12cac27b5ab7c00cade2271`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 21:30:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 21:30:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 02 Dec 2025 21:30:31 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 21:30:31 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 21:30:31 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 21:30:31 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 21:30:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60867dd906580f857eda83c06f1c6cfb69f8fd1c731187cb053588cfab5684b4`  
		Last Modified: Tue, 02 Dec 2025 21:31:10 GMT  
		Size: 38.7 MB (38697663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9fdaf98d533880ef27c36338437c10918cef37f67eb19c1d65b5e92bf8129a`  
		Last Modified: Tue, 02 Dec 2025 21:35:19 GMT  
		Size: 225.5 MB (225537292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-26-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f133aadf3a2ce176ba77784a20f85461441f0676d285c01d7a79ab068b1dc0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80b6253f042a38713df5de9606077928ea98cfa88edd52c15b78a173b3d72f2`

```dockerfile
```

-	Layers:
	-	`sha256:0d28d271959349a4c56624190e5b7818c3e17f3f54c951572f3b8ee3b8169fc5`  
		Last Modified: Tue, 02 Dec 2025 22:23:26 GMT  
		Size: 3.7 MB (3653021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a31e3ccdbf418a3c6933b210fa5f1078d8481cbe205018779bea3a0ebe0583b`  
		Last Modified: Tue, 02 Dec 2025 22:23:26 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
