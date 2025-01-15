## `openjdk:25-ea-5-oraclelinux9`

```console
$ docker pull openjdk@sha256:3b1d4d4d0201c82cec8d75026b3b3b7f492465a61edcd7d1dda441747180b9aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-5-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:6036079ab07cc7dac754118938092f689ad3d43cdb4441df090bec921190f831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310782491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf15e440f8ed7e862db74cb2ef97be83a8ff030a4853125c46c68a13b895f34`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e33d745e071984a69061d65388e866f2f3b8cee5dfeef6fa3dccaabc1c4ee03`  
		Last Modified: Sat, 11 Jan 2025 02:30:13 GMT  
		Size: 48.8 MB (48773951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6006bce948b8d061e9eab72df5c1ea5ab9769591856aa23324edb5459508f21c`  
		Last Modified: Sat, 11 Jan 2025 02:30:15 GMT  
		Size: 212.9 MB (212909838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-5-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:605407cf6ddc842d0f2af92a0964ee33df272a1998e644ac158a0979a8c22c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dadddd470633e132e973c99160bf2c4965b1ae9f1f02afd7a98da733cd5ff5d`

```dockerfile
```

-	Layers:
	-	`sha256:3d7396d1ac62f151df593c527a05ec479b888fb2df1863870c308bd001166438`  
		Last Modified: Sat, 11 Jan 2025 02:30:13 GMT  
		Size: 4.9 MB (4907559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7034c4becfb096ed36a5c0b6a28bb97aa1997717653e0c9e4ba9a59f2325b4c6`  
		Last Modified: Sat, 11 Jan 2025 02:30:13 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:615a44378a1a090338105d2a489b0fd70d0005a4d78db0524f9e81a9f4b200c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307749495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866f1b702841781d8a8641d7780ae77df03bb7aaddf75c6e1e7c5d81bc9672b3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039f9164d8ed0ced238957a9b29aa70115c4afbcbd9ba369b97802a864b2d615`  
		Last Modified: Sat, 11 Jan 2025 03:15:55 GMT  
		Size: 49.2 MB (49203678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca3755d13ca96024ec8086d785b5d4f85ee5392fe5ae6977b3c05697b3ab3b4`  
		Last Modified: Sat, 11 Jan 2025 03:15:58 GMT  
		Size: 210.9 MB (210878425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-5-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:e15d3bc2ffd990a1b7dbd460b7a554afce03398357c7f072bb6e5376d17aae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f00085e1576c8825029a7ddaf566da681ec32b875676906ce46965d79b116c5`

```dockerfile
```

-	Layers:
	-	`sha256:4e3ff5b1d03945bb56961d0edf92306012d147a7eaa99ae4319a724d33e313f1`  
		Last Modified: Sat, 11 Jan 2025 03:15:54 GMT  
		Size: 4.9 MB (4905321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1574df0a3f80275013872d6cac31f9ee3799543b6673a6178b6ec5bd075f92e5`  
		Last Modified: Sat, 11 Jan 2025 03:15:54 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
