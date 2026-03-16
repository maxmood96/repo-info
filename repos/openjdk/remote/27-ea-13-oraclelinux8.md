## `openjdk:27-ea-13-oraclelinux8`

```console
$ docker pull openjdk@sha256:1af161b82f1a2658e3c32df4ca1685bf0e0e0961deb8c34a547546b383a7d9e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-13-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:6540a263211216b197215f73188989fd6d659938545d0d67cec8114cc578b8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295336434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0045baf1e655b6ff502a3068f9a5b49d452de9915793e1b28cb5a8d92533a347`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:12:15 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:12:15 GMT
CMD ["/bin/bash"]
# Mon, 16 Mar 2026 17:03:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 16 Mar 2026 17:03:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 16 Mar 2026 17:03:11 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 17:03:11 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 17:03:11 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:03:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 17:03:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:910e0c7025a94af1bf4f9980abe31c6c0541dbb5c579f5a09497c1a5d667c578`  
		Last Modified: Tue, 24 Feb 2026 21:12:26 GMT  
		Size: 51.5 MB (51462874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7b2452b5413899d2aa66237f129f76be8a3892d373ee87514a8fa5640afc9b`  
		Last Modified: Mon, 16 Mar 2026 17:03:33 GMT  
		Size: 15.0 MB (14986723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a326e42acf072a0d6b9e9fdce83c9b9a30185c3715e96feb6ef53db04fd25ac2`  
		Last Modified: Mon, 16 Mar 2026 17:03:36 GMT  
		Size: 228.9 MB (228886837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a422a8774c21ef21be3d5259a2a0dce19234c8d1dd125bc371a2f3bcbb935aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8463284f812cc824a1f1d87996ca3b037052f4597ed4a01070ac3fed2b95b6e7`

```dockerfile
```

-	Layers:
	-	`sha256:0a7eed967ba0e08362d15abe7ae3dc854292570463992a8181752818a0c04c78`  
		Last Modified: Mon, 16 Mar 2026 17:03:31 GMT  
		Size: 2.4 MB (2448698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8658099581203d007a2b106556bd8b24186e10c1b9e4dc190965c149150c1c6b`  
		Last Modified: Mon, 16 Mar 2026 17:03:31 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-13-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a5cdcb4c6ac5d2e7fd48ebdf99b90b178f58bd07fceaee3457614a253d44e6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292789989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86736dc166151358fd1bc8d62d562fac4796a145017c457f4a1d836ed527e669`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:25:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:25:54 GMT
CMD ["/bin/bash"]
# Mon, 16 Mar 2026 17:04:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 16 Mar 2026 17:04:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 16 Mar 2026 17:04:53 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 17:04:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 17:04:53 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:04:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 17:04:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:308b2ffa0912bdff2bf3b77a5f2634a00c2761e38a51260adbdfe882bc668185`  
		Last Modified: Tue, 24 Feb 2026 21:26:05 GMT  
		Size: 50.2 MB (50199180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aad8bfda547d570c0b4d72db20629124b5ca7b562e56217a0f3d146c172f1de`  
		Last Modified: Mon, 16 Mar 2026 17:05:15 GMT  
		Size: 15.7 MB (15700081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60334b3f2c203e9218a80866db2cc83573282046d4e510306332d8283a37df4`  
		Last Modified: Mon, 16 Mar 2026 17:05:19 GMT  
		Size: 226.9 MB (226890728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7d80756075598140eb57a3cb31a2cd16e086318492681bed8bffc38d38cd1176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535875cc25eaaa71a311e64c46c696ce480a7e803b22796a30d266b53a8a72a0`

```dockerfile
```

-	Layers:
	-	`sha256:ded5cb2f078a510a03666dbf7c8b87cedddf57235b4a18dc53f38fbf111e9a6a`  
		Last Modified: Mon, 16 Mar 2026 17:05:14 GMT  
		Size: 2.4 MB (2447508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d5a9b5aa94e502378084b1a767d71192724c3ce348a4974285805d0d4363b2`  
		Last Modified: Mon, 16 Mar 2026 17:05:14 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
