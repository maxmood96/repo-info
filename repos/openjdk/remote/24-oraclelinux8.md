## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:548d9a85448beb9f077dc062ad1547d98ad9565428c2360d1b1f2c58bf447f30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:02573fb5e6b4e6727d0856d1f3c473353f07b27373e1a3adcfc43c8c1a623886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279226410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68b5524c9a087efb58cc2f445d3084c171b3e07eb4baffa09ee5863b70f8b45`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 10 Oct 2024 22:15:38 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 10 Oct 2024 22:15:38 GMT
CMD ["/bin/bash"]
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 18 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+20
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='b7a84616949bac4a00a9a96d771f6595e7fed371c0a5a54139285311e4c0b367'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4fe26b4900462d35fcaa9c7b551fd23791906f05eab3a609de8d771cc15ad9d0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ccec4de1d50efaab175e979c24b513dacdec266a6a00f442167c614564b83ef0`  
		Last Modified: Fri, 11 Oct 2024 00:11:24 GMT  
		Size: 51.3 MB (51295624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17897e212457cbef879558d948b3334e40c26008fc8529a56f7d48afb48b1d13`  
		Last Modified: Sat, 19 Oct 2024 01:01:52 GMT  
		Size: 15.0 MB (15036796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e9040fcc454269add36d467f3d715234417f3d978d7a6b82f326fb4408f310`  
		Last Modified: Sat, 19 Oct 2024 01:01:57 GMT  
		Size: 212.9 MB (212893990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e97d65f4c7921793b12d1478ee71d609c1eb6f5c03bbe2d4f78175270d557245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2441837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9473d4525429ac4184486b5462fcf9710293b5c7f3150d15c34c9239adf1e3d3`

```dockerfile
```

-	Layers:
	-	`sha256:30e1ebc13766416135f1bdead8aafac2ac1eee2444fc0b8aa07aabf2287c2105`  
		Last Modified: Sat, 19 Oct 2024 01:01:51 GMT  
		Size: 2.4 MB (2425799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9912b9a3ea242b0cfe12b160b68bacfb7939ace1eb1815cda46cbbcd0e31de8`  
		Last Modified: Sat, 19 Oct 2024 01:01:51 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6c6c4d662cba4d89afdc9d8cc1c27c5b839ec5d7c3380da78b160cf2a6e4b27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.5 MB (276492079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3667bd9d9fae3d07cb935cbaa132ba10ff7c0b3ac58a61d437d4f43bfd3189c5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 10 Oct 2024 22:16:27 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 10 Oct 2024 22:16:27 GMT
CMD ["/bin/bash"]
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 18 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+20
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='b7a84616949bac4a00a9a96d771f6595e7fed371c0a5a54139285311e4c0b367'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4fe26b4900462d35fcaa9c7b551fd23791906f05eab3a609de8d771cc15ad9d0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5aa1f5d85d147a7c16d0057c3fc21b1ae3d482ca5ede955163a95cc540b4244e`  
		Last Modified: Fri, 11 Oct 2024 00:11:55 GMT  
		Size: 50.0 MB (50004038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096a2c0e68dd1c814c85ae00b2652f096632e44095b6ac5ff4756a756a3ef3bb`  
		Last Modified: Fri, 11 Oct 2024 00:50:19 GMT  
		Size: 15.7 MB (15706108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f21a352f7959a8dc284658587d32d65509cf20d5aa85f96e41b052702aa5c9`  
		Last Modified: Sat, 19 Oct 2024 01:24:46 GMT  
		Size: 210.8 MB (210781933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d975c5a1b2c9f8a425dd60bf7d5e1d0c54293be0cdb7eb7ed6ea1baf3bc960b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1580eed253fe2cc35385bc717d09313d9c271faa79d97da7977dc6abcea34b27`

```dockerfile
```

-	Layers:
	-	`sha256:24849af50f64932ac495ff664dca94935b82e901fc597600c58e306cc4eba89d`  
		Last Modified: Sat, 19 Oct 2024 01:24:41 GMT  
		Size: 2.4 MB (2424021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57abf8c9886de138c639b5bf0c697b9877fa57fc6da1e9a09ee728c0a13121f`  
		Last Modified: Sat, 19 Oct 2024 01:24:41 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
