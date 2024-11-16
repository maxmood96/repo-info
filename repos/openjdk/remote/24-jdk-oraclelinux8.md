## `openjdk:24-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:f755037d780d59e1b6aebacba6fe9090cd2ca5252b7e8c6908c0d901b0192871
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:14b4210f212bbd9cf0a36b1a180e24d9ae3f8f81cf8aa6d48c23b9e9aa4815d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288876409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6064b210eba31e00251bf6d96c532acf67d7e4e1e0346d2c90a5efc63878272`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 01:48:14 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 15 Nov 2024 23:04:32 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7865feb3c762b4fb0d8ac7582e5817117021161805db359a1a67c9f93084ed`  
		Last Modified: Sat, 16 Nov 2024 00:04:04 GMT  
		Size: 15.0 MB (15033187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448012971ff561181bf3922d5f5ced5d16a1076730bb66493b8abf2230577aa3`  
		Last Modified: Sat, 16 Nov 2024 00:04:07 GMT  
		Size: 222.6 MB (222568230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f30b5bb27942a0c0b559edc1e1ae7d0a8b44a41999c83d8c3073aead01f7cf38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ac85deba04c077c8f85575e0017bd7aface8902209d3eecf6756c87ae0c24f`

```dockerfile
```

-	Layers:
	-	`sha256:5ec9889afe3245fab9c2a29bd2adbf8738c5970493ded698e5843d5b1645da49`  
		Last Modified: Sat, 16 Nov 2024 00:04:04 GMT  
		Size: 2.4 MB (2443943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3054b7d68276d0e4f8cc61ba8ce5aec9180819160daff6f2d1e6824b312298a`  
		Last Modified: Sat, 16 Nov 2024 00:04:04 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c557edd0f75eba8e291da478ceee9923f95ec5714bfdf41a6f104475e8b9b2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286221692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c992e12490fe0d11b558f2e6a0d68a4856531b3c38c7fd04353f901850e6117`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 01:48:14 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:54 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3503b2eba1b5d814a6e5c252cef5befbc0d42d778f675f0079729eab5a133e`  
		Last Modified: Sat, 16 Nov 2024 00:05:58 GMT  
		Size: 15.7 MB (15712335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5804b5a8015225ed400089c0cfe336dd9a57c87c51f2cc4963d0d4baaf6e0d98`  
		Last Modified: Sat, 16 Nov 2024 00:06:02 GMT  
		Size: 220.5 MB (220529082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7f4418ed4e4a516a6213794887c9d53fa04761b81f585c5f541f56ba7c28a23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d96ef39307be37c5148137d4770e7ab0245f999f2d0ca1bebc8e2420ff94bb`

```dockerfile
```

-	Layers:
	-	`sha256:fc6210eca36c6715a9ba620a35204f09f91db86077210ea1b88f93c4d2188f10`  
		Last Modified: Sat, 16 Nov 2024 00:05:58 GMT  
		Size: 2.4 MB (2442787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:976f12ce496ce21705a54b8e87dc7b33b5e7e80b404229d694a3239d4d4e1f2c`  
		Last Modified: Sat, 16 Nov 2024 00:05:58 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
