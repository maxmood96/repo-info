## `openjdk:27-ea-27-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:a8f4546f1ae076fd367855d15aa71039729d611e207086a08b64f67a4feefd5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-27-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:05b94e7606182c52dbf1a804374fb60af679521ed03956e893d41379b08ed18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313171070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f7a01d025dd6bf1bacdcc785acacf8524896580696e90cd7c7aa2c4afa0d8f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 23 Jun 2026 23:33:02 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 23:33:02 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jun 2026 23:33:02 GMT
ENV JAVA_VERSION=27-ea+27
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6b21eb7a1e3e8c85b9f7c55e523b7309abb9be51ed5d639b708a756b2568459d`  
		Last Modified: Tue, 23 Jun 2026 23:31:18 GMT  
		Size: 47.9 MB (47923466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055ebff846737512a06bf510ee1b659e5cb8435ece8d3cb8f90b2a541cae2ca5`  
		Last Modified: Tue, 23 Jun 2026 23:33:23 GMT  
		Size: 38.3 MB (38299720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944883fe3293f8d26d8c81ba0a9c0c9603fd93fe941048b71a09da7b0416f143`  
		Last Modified: Tue, 23 Jun 2026 23:33:27 GMT  
		Size: 226.9 MB (226947884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:2c654f0bae08088246d097b28974a774f9d3189c60a21f814f32ac91ce5851a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573aace0ff9002f22932f94f75a469f8ffbec50b6c554de2bac458c19616123`

```dockerfile
```

-	Layers:
	-	`sha256:1080b40d679463c5ed8e06a4597cffe02812109aa40fc88e5a939c7646f8e910`  
		Last Modified: Tue, 23 Jun 2026 23:33:22 GMT  
		Size: 3.7 MB (3652151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3399cf1c5d626f4821684a3124a2f348db472656ecc1b90d9fc3ac5ed676ad2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:21 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-27-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bff83aab08eef0a11d6e45c3668c36cbc482c54d4add875b313b2b8ee2323110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310095251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05421a9ea252f5f8b8ced61b54e92365dd1b76c847c4fdf34f6bde9f3513004f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:02 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 23:33:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 23 Jun 2026 23:33:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 23 Jun 2026 23:33:42 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 23:33:42 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jun 2026 23:33:42 GMT
ENV JAVA_VERSION=27-ea+27
# Tue, 23 Jun 2026 23:33:42 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jun 2026 23:33:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14f0bac426a67d312501b30c0b419c0d5c2265f32077f348593b94dd76f064ac`  
		Last Modified: Tue, 23 Jun 2026 23:31:13 GMT  
		Size: 46.5 MB (46470688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02551c076ecc4693a80b368bffde5b6c2875932f2bc08300522778836e1968`  
		Last Modified: Tue, 23 Jun 2026 23:34:05 GMT  
		Size: 38.7 MB (38690394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d027d640dafa05499dcc9fe5bf6869445e209466d529faa71f025b7bba3aac95`  
		Last Modified: Tue, 23 Jun 2026 23:34:08 GMT  
		Size: 224.9 MB (224934169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:c8b3616e8008f50e622650413ecc2c6fca9e2311135f46438aa4f4e117d1ec7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9feae824cd456f4b0c803057f409ad4353264890374a9cda43230fee85920eb`

```dockerfile
```

-	Layers:
	-	`sha256:984e1456163799d44b2ba4c51e9d327dd0c608e8c2d7e3e965797a0a6175d01a`  
		Last Modified: Tue, 23 Jun 2026 23:34:03 GMT  
		Size: 3.6 MB (3649761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15e1821a0fac59f41414529ba40c2abe0e08024adf5fa02363d0fe9a7e0cd00b`  
		Last Modified: Tue, 23 Jun 2026 23:34:03 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
