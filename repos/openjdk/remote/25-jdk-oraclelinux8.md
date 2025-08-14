## `openjdk:25-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:4593d8913db993890d48c12ea4cd1c3a0a1313087f23bf2c61ce32aec1e4d3bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:33d7f164c8410035384ec641259066a7bfc41079aec51ea275de77c169d397ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289823078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c25a066e226a64e5ac81118ad6fd5e29f4b2964e50a0856a0656ba32c4e7eec`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:58:59 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:58:59 GMT
CMD ["/bin/bash"]
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 09 Aug 2025 00:48:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_VERSION=25
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:816eb39a0552da23131629c02b98cdeccbfcda79ce23b4283b51ea7845bdb4e5`  
		Last Modified: Thu, 07 Aug 2025 23:49:07 GMT  
		Size: 51.3 MB (51323465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ad73e48dd97f4ed18b5b6890969fb28698afb8b1bdcd8d361e4e3d34cf1ed8`  
		Last Modified: Tue, 12 Aug 2025 18:02:54 GMT  
		Size: 15.0 MB (14977108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a007e01b761718ddcc1ed6e2aa1852836c3675f7d8a01903757560fede94b6c`  
		Last Modified: Tue, 12 Aug 2025 21:52:37 GMT  
		Size: 223.5 MB (223522505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e65c481d1ad831cce9cd815af568f2ccee9af081eb90024b242678e49a94c7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a51f7eeba658aa3a8eaab3e44c57983e2efd814a630ef420753454fc0f67c0`

```dockerfile
```

-	Layers:
	-	`sha256:b82fb868996688de33b05656860507eb5bf9a58ab61446127ba6961e0fe1b975`  
		Last Modified: Tue, 12 Aug 2025 21:23:54 GMT  
		Size: 2.5 MB (2451042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4144eed4374690482bf034dd08fea8bbab5c228a942f62abfc74d128448fa3d5`  
		Last Modified: Tue, 12 Aug 2025 21:23:55 GMT  
		Size: 15.4 KB (15434 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:73cc7d4fe38023952e0651d739f8339766526bdb94f37c2765553bf8940b2e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287049953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebabfbc7d44ba6e1654a34cfb4d7ff2d33893bc8a888657aaf124e60cf0ab464`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:59:57 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:59:57 GMT
CMD ["/bin/bash"]
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 09 Aug 2025 00:48:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_VERSION=25
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00aea10d937a1f6a212468c9a6eb06043ca5276b560643f3c75b3b2d11325b17`  
		Last Modified: Fri, 08 Aug 2025 01:31:37 GMT  
		Size: 50.0 MB (50035024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f29ae74ed40c5064856c8ed83a5fe610bc44cb75f0852e1026a8313f040ebfb`  
		Last Modified: Fri, 08 Aug 2025 17:01:46 GMT  
		Size: 15.7 MB (15672333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013ed23b2372217ca33966e314b496e540d632ed540cd17c26930e934d75b16c`  
		Last Modified: Wed, 13 Aug 2025 16:17:11 GMT  
		Size: 221.3 MB (221342596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f607c43d8e3b860e7018df3c14a7b75cf112712670cf18c1b904fbc8dcf1419b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f0ef8663357e4b62578854666e80b424075696ccaf987c9757fed2ff020f0b`

```dockerfile
```

-	Layers:
	-	`sha256:c7f123bac07a5a70e67b03f1220c88720d053f8c9976eb08d12201567b0de186`  
		Last Modified: Wed, 13 Aug 2025 00:23:37 GMT  
		Size: 2.4 MB (2449852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b172ca2c89b4a989a0a023e8d176ff606e6a6e5dab768ae8c17bfc432f85f39a`  
		Last Modified: Wed, 13 Aug 2025 00:23:38 GMT  
		Size: 15.6 KB (15553 bytes)  
		MIME: application/vnd.in-toto+json
