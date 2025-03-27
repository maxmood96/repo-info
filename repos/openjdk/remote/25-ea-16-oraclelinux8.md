## `openjdk:25-ea-16-oraclelinux8`

```console
$ docker pull openjdk@sha256:23a32c63c27d38b38cb6e3088abb6fea218cff46bb13fe80e6deba11c7cc40da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-16-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b83d22ac4401d58337490f8bf8996813da1c480cc4796a8482600f85eeb5aacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278946135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc39f9d8cc60048ecb8f0da4f1edb79cabe4c4e8776e557d33c134f2bfbad2c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Mar 2025 17:20:06 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 14 Mar 2025 17:20:06 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:035e56311411a7644fa1341dfc093e1b278feac7d55c98ae09177e1755672600`  
		Last Modified: Fri, 14 Mar 2025 19:00:09 GMT  
		Size: 51.3 MB (51288940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58e47f084f8f7a7d8e6847eba92cd4a2fc915981dcb21699bf6ee11d15f00bb`  
		Last Modified: Thu, 27 Mar 2025 20:45:56 GMT  
		Size: 15.0 MB (14996342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ff0ccb088361a4dfe2e6ac5133470b261836acc14d50f1a156aac51533a775`  
		Last Modified: Thu, 27 Mar 2025 20:45:59 GMT  
		Size: 212.7 MB (212660853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-16-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:22b632ec141273a71ae8978200cd395d6e01b6e916e033330c085b5c4e9bc2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f50df861180ec921c4dd79f6736e54c13eb7d8b00958ff00267bc8c24811046`

```dockerfile
```

-	Layers:
	-	`sha256:b603bd2dd4694e01bdeb1c28748cd5aa426e819783f060423e0281293095fea9`  
		Last Modified: Thu, 27 Mar 2025 20:45:56 GMT  
		Size: 2.4 MB (2440967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f13b2daa5351d348bb5cbf6d204aa83efdbbe5c95a76a40629853b387a1cbfa`  
		Last Modified: Thu, 27 Mar 2025 20:45:56 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-16-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:42b4b76d7c689f8398ab65b4be0d0a07bc93c2b1cb1b139c5ba84911036a840d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276216564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e858f89b8aa35f7f4272e3a34f8e5a3c023d4ad1789b0c9952b4cd12bf3f0c0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Mar 2025 17:20:57 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 14 Mar 2025 17:20:57 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f8eb825c1fc22ded5eda8a11c91fd13cd2b63722a0fdbe5ed89339ba10aabad`  
		Last Modified: Fri, 14 Mar 2025 21:52:22 GMT  
		Size: 50.0 MB (49989226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d2d63d00da99812eb8285d347cd8a68c6913a3b4f406a756d3804e277dc4d6`  
		Last Modified: Fri, 21 Mar 2025 17:24:29 GMT  
		Size: 15.7 MB (15683223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c796d313a2aa05c5058d5f27bd4e2043ac38b69e7fa4a2ebd68b30cdecbb9dd3`  
		Last Modified: Thu, 27 Mar 2025 20:46:14 GMT  
		Size: 210.5 MB (210544115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-16-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:261c11b1e09b8a2216e7ad7185f502bf956097a90831f84e8742106cf3c90c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3433f5c1cfebb2993f0aadb5122d09e2379d7e65e7968f36c2b75566b802d43c`

```dockerfile
```

-	Layers:
	-	`sha256:da4aaa3779851072fe9fc982b89c51c64ee0b7d429f8b648ef77c7ddc0d02824`  
		Last Modified: Thu, 27 Mar 2025 20:46:09 GMT  
		Size: 2.4 MB (2439813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d138d2bd6e6cf711b81afb1e3eaa32a3f5b27bced42abd1985945081a70f2fed`  
		Last Modified: Thu, 27 Mar 2025 20:46:09 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
