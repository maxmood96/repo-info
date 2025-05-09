## `openjdk:25-ea-21-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:7f699c2acc97dadb6073375795a38f3b00ffd49c18829c81fdf24eefe96f16ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-21-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:cf31887db638230e488da537128b9b85a27f8ab634c10b4c9c3a1dce13639b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280077874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b1952c0000a2ed5df2337c598e7d3ba28701c6d7db41cc13401eff0865e630`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 21:48:19 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 21:48:19 GMT
CMD ["/bin/bash"]
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 03 May 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 May 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_VERSION=25-ea+21
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='9215df470d2d44c8ea731dcde9e170b6951e29f6e96e90625be983f0f9cfd1ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='23b6cbdac4dedcb1e7d290e7f5e9da01be8c4dcc35b4d296054aae3588d4465a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 03 May 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ee6d2b4bc3292763eeab29f03adacbfcd179273f648dc332abeb3f2f9cf99a3`  
		Last Modified: Fri, 25 Apr 2025 22:19:54 GMT  
		Size: 51.3 MB (51312878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218eb0a34daa41fb3015241231840e3f7bf25cf462cfb7f8d70e6873ee36a558`  
		Last Modified: Mon, 05 May 2025 17:30:38 GMT  
		Size: 15.0 MB (14998163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd29c5c2a44a5ddd1ff5ad53310f3ea1784cac82bd5cf43ec8eae16b5593909`  
		Last Modified: Mon, 05 May 2025 17:30:44 GMT  
		Size: 213.8 MB (213766833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-21-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:726b5a0b7e8e6936102b22c12e71712a83106063b14540756b1e2f8be334f4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4124ed8b37a982ebfa9ca0f7f035c1b9bc14e6e00b24641e2e406875547862`

```dockerfile
```

-	Layers:
	-	`sha256:4a3aaf910f6afc2413dd7c3f4b15dd13a8a1619725651632e9025c9789704b34`  
		Last Modified: Mon, 05 May 2025 17:30:37 GMT  
		Size: 2.4 MB (2442873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec37e2e9d3063c5a2c5848303b815d52c8bbea63a4b1e6b85a49e3cf755e170`  
		Last Modified: Mon, 05 May 2025 17:30:37 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-21-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f6f5bc039044451ffc2941dcf2754f4289f78392cb4c4cf4652d9605171e82d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277255300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc8a51ee7fcdeb1be7be81168197ce7a5c957c6fdaa3ebaff6624727029dd91`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 21:48:43 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 21:48:43 GMT
CMD ["/bin/bash"]
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 03 May 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 May 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_VERSION=25-ea+21
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='9215df470d2d44c8ea731dcde9e170b6951e29f6e96e90625be983f0f9cfd1ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='23b6cbdac4dedcb1e7d290e7f5e9da01be8c4dcc35b4d296054aae3588d4465a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 03 May 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f9f09355eb5a75f94b3d65a17269700229fb600c0fa7b446c5cabbd22d410e6`  
		Last Modified: Fri, 25 Apr 2025 22:20:08 GMT  
		Size: 50.0 MB (50027777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e46de3b8fc0f00590b038000379cb18fb91e553260d144fcf9129a0edb74f0`  
		Last Modified: Mon, 05 May 2025 22:37:44 GMT  
		Size: 15.7 MB (15667699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a3510f2d384bf6ad013d0f7cf0461aae3a98d9fce3a326d27d0d4d8cc66b0`  
		Last Modified: Mon, 05 May 2025 22:37:49 GMT  
		Size: 211.6 MB (211559824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-21-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e46bb4ea44e885a73a04782e9e6634b0cb3509e97c11907c9dbcf08d1f195b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977ed1aa33153dcceab0566d033da8001053ec304d23d0e93be3ec07cdde76fe`

```dockerfile
```

-	Layers:
	-	`sha256:e2a3ac5db69cad921e9b637986619730e311f1b895befc701287f9920808e57e`  
		Last Modified: Mon, 05 May 2025 22:37:44 GMT  
		Size: 2.4 MB (2441719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ec283cbe180deb7ad0541bff64bcea115cd01bcd6ba7a42b685c4f115772ea`  
		Last Modified: Mon, 05 May 2025 22:37:44 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
