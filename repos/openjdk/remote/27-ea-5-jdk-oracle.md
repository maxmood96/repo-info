## `openjdk:27-ea-5-jdk-oracle`

```console
$ docker pull openjdk@sha256:ff6bde9f35f9b2ae284989bcd05d987e0a72623086aef5d40e8b788dc9cbf659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-5-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:3db54cd179fcb0bf8e6a0feea230837dfe9f2cd58f01266ac4f2098cf2eb195c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313676708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee2cf868ebae36261d7a0aca63c878e23d9db4d291a38f33de84b91754cad19`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:07:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:07:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 23 Jan 2026 01:07:29 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 01:07:29 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jan 2026 01:07:29 GMT
ENV JAVA_VERSION=27-ea+5
# Fri, 23 Jan 2026 01:07:29 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Jan 2026 01:07:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa302177a5c6a5c4dc88c1937c3c5c7de7276be4f52c4996088f50c84385ce`  
		Last Modified: Fri, 23 Jan 2026 01:07:53 GMT  
		Size: 38.3 MB (38296652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd842e7a994931dc439ba3fc0bbc8a95e49421be8273ebc3c9e7a617571ed4d2`  
		Last Modified: Fri, 23 Jan 2026 01:07:56 GMT  
		Size: 228.1 MB (228066508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:fbdc4bf55a61fea5add42e6cfdf4e6a0c6b6272c5992d822962b71d3d842c30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e7e4b9a1129a27517bface44e44b57d1ce4c5147aa184e3960fd9d5730233d`

```dockerfile
```

-	Layers:
	-	`sha256:ac4844cd89b038c90c22cac52fa0f9d2c21d15150a4350852542cf7fe6d9524d`  
		Last Modified: Fri, 23 Jan 2026 01:07:51 GMT  
		Size: 3.7 MB (3655359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e690c27bb6dd30d06bea702cc2f7f2d99fea44325180b820f10aa2538f376d08`  
		Last Modified: Fri, 23 Jan 2026 01:07:51 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-5-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:eb9e9b3614aa388d392616143983edbaf157e1c7839bd8db41709bd44d6e2e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310601155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80631cad885568c01fdd5ddba1779c52e9d9cd69fefb12532ed3e54a37d3cf17`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:39 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 23 Jan 2026 01:03:57 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 01:03:57 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jan 2026 01:03:57 GMT
ENV JAVA_VERSION=27-ea+5
# Fri, 23 Jan 2026 01:03:57 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Jan 2026 01:03:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b714d6dc4abe6f689665354c4cf44a16e94729cfc60fabd29fa1982418eb96d`  
		Last Modified: Fri, 23 Jan 2026 01:04:19 GMT  
		Size: 38.7 MB (38699722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a88aee01418c9d2646f5349ccc80b1e6b94bf8d3d6a763f99012af309b381`  
		Last Modified: Fri, 23 Jan 2026 01:04:23 GMT  
		Size: 226.0 MB (225999523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b2d65aafc757a4dc865f886aaaecac7a3c53326a908bb3b6f93b538c44a4fe43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b61cb31f7f4e2406725f2c57a0e3abf36a1557d5dd9614905a08acf08b6aef4`

```dockerfile
```

-	Layers:
	-	`sha256:dcaee0da90de3e973149623f94dbfa8d162c3656b0b10f7e604b761831ec312d`  
		Last Modified: Fri, 23 Jan 2026 01:04:18 GMT  
		Size: 3.7 MB (3653049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2ca04b5980b5bd83d52e22509aa798a3e15ae1ed580b145fc0dcf9111300bb`  
		Last Modified: Fri, 23 Jan 2026 01:04:18 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
