## `openjdk:26-oraclelinux9`

```console
$ docker pull openjdk@sha256:609200cd0a8bdc83594d8c08e442eb243fef60b046536129a14114ee54e14bd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:a6775e064fb3f3f9a0214b9f4015fed719c9fca019fd2f658fd2c13c55254950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310791393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cadb7b50c9a81b157e67c49f5a317027f1dc9f3fa4034f6c852af0a38e85a1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Sep 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Sep 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+14
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='14787165312e455276975549713f2f8699344989dee23e7099bafa7121b78b61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c0b7fc80b5a73fb433db4049bb05b46ed43827c082c5bfd0b6f8883400c4d91c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1b74a60e0abcb871fd5434f539541d0f3b626ce734094d202e74090106f5e`  
		Last Modified: Tue, 09 Sep 2025 00:25:05 GMT  
		Size: 38.0 MB (38007252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe8c4a2ee227258220131d1e110ee6edc891c76c1f636a0e9b17cd9cc43e1db`  
		Last Modified: Tue, 09 Sep 2025 00:26:25 GMT  
		Size: 223.3 MB (223287125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:dc496b6738b123fce0a8ba6186ae2aa9cf68000a8d78d4eeff94bbb0c1755ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2def5bd003424bb8c71b879d00a5fc8883570f198152a9818bdfb82593d3afbd`

```dockerfile
```

-	Layers:
	-	`sha256:3108e8dc0ccb84869e4df89976ae15c832697ed9d0ef25571bda594abcea995e`  
		Last Modified: Tue, 09 Sep 2025 00:24:40 GMT  
		Size: 3.6 MB (3640729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db851c2b395008d8e485320522fea8eab318fd8abdc9d13d11290b986febae1`  
		Last Modified: Tue, 09 Sep 2025 00:24:41 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c7f2f80c56a485a936fcd2b84fc5807711ae1674bf76b7041b3b80f63ebb57c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307628970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3e6241bd0182a72c7998d8c85bd40fc5ce1a425bc520bccede4af9662d8f60`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Sep 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Sep 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+14
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='14787165312e455276975549713f2f8699344989dee23e7099bafa7121b78b61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c0b7fc80b5a73fb433db4049bb05b46ed43827c082c5bfd0b6f8883400c4d91c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0f06fe365088b13c3e85d9d82bb0bfa20bd800107bbd4f847969b839eee731`  
		Last Modified: Tue, 09 Sep 2025 07:54:07 GMT  
		Size: 38.4 MB (38410789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854224966d2e4c929e49f507b0fc8eabbdc2bd4fa1be348d9e9cc3b04b851d45`  
		Last Modified: Tue, 09 Sep 2025 07:54:21 GMT  
		Size: 221.1 MB (221131458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:763a282623c2eea7f95543a02c0fefacd201813dbe9330f9f7ce3b3db99d496f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f136f09a092fbc9895c6ff8870d5f44422fc012234dc81e1e768f240dffbbd2c`

```dockerfile
```

-	Layers:
	-	`sha256:4d4726d808ef2569faecd5d3c6c000af57992a5ab4aa812fbe8d3def4b87e5b9`  
		Last Modified: Tue, 09 Sep 2025 03:24:02 GMT  
		Size: 3.6 MB (3638491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10578d2f7e704ed92514277cde235522fad1839eb62442734e389d9da3dacf19`  
		Last Modified: Tue, 09 Sep 2025 03:24:04 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.in-toto+json
