## `openjdk:25-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:a841cab58d78b06dc2d0f143c8b5ec7c5c9df3e6547eb01ded314f4788cb9a91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:907ad570b116d74951eb44c1d7e1a3520767f7c0c37a448101efe83a22ed7787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279575361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0e319407c578b40b810a2fba339ed68d79079f63a1840461e3636eb91bf052`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 15 Nov 2024 23:04:32 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30cc4134598ea09f5e216d1ac20eb1be90d28033c6d6057355086560540d58c`  
		Size: 15.0 MB (14975120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9690321f82b4afc25a808614f27e06e95877c2d560e2dfe79f2b08d88be9f444`  
		Last Modified: Sat, 14 Dec 2024 00:30:23 GMT  
		Size: 213.3 MB (213325249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:34d06fc2297d2a1056cc254f55459810a05d3cf51dad965ec047c3f1eac99c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83d380513221da4a3e3675293e742f2ba021bda77daa31918440b941651213c`

```dockerfile
```

-	Layers:
	-	`sha256:c9ab38df9bee79dfe820dbe0f0dbf980e675b8c01fd300f6ead4b744add8131c`  
		Last Modified: Sat, 14 Dec 2024 00:30:20 GMT  
		Size: 2.4 MB (2447752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cca37ec63939e8407c2ff56c333f1b9fc03b1319eae5cd6843d1ac3628579f1`  
		Last Modified: Sat, 14 Dec 2024 00:30:20 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0550dc22fff16e216da5e0a6e8a5ff7586184392b30070f107f8fa09a8758423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276932159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c0c1dc4631953515a6f0854ab2fd48104a8444cd81fc9e380384208db721bb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:54 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69acd795388d1f1fedcb65b1fe1cb71800f56a9beccbb0acf86fbdad421cc605`  
		Last Modified: Tue, 10 Dec 2024 01:27:38 GMT  
		Size: 15.7 MB (15659937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d6d22ce1697e0e7cef25956c7621daffe7890ff126bf70f39ddea18efd2c77`  
		Last Modified: Sat, 14 Dec 2024 00:30:41 GMT  
		Size: 211.3 MB (211291947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8d5b98adc3a8432ac0aa608aee913d53e7ab4e3db891015b1a8bbfa6db0dac78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29584939d78cf661360998a38044510ec5a65e06ef6c0b5ea20d853da7918bb8`

```dockerfile
```

-	Layers:
	-	`sha256:49be92af61618ccda18ebb707011d810ed2ea1ca49ec055da53232968bfe9d45`  
		Last Modified: Sat, 14 Dec 2024 00:30:37 GMT  
		Size: 2.4 MB (2446596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c5b435598a6b984a9df2f4c44df3035ee3aaf80199b460643359651a11c6465`  
		Last Modified: Sat, 14 Dec 2024 00:30:36 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
