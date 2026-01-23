## `openjdk:27-ea-oracle`

```console
$ docker pull openjdk@sha256:7955174926cd70031712e944b8646550f0f6d4b7d605766b5e307be9e8ef7dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:044e00e7d725c97bf09d62ac0be5c5715383bd92e521feadece148a1a19bd964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313677188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2879c4a8eabe2359074e4a0478fe01f8b476105fc51f084c687013e0a000782e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:46:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:46:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 20 Jan 2026 18:46:46 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:46:46 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:46:46 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:46:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:46:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5c65ef8298a36f2091528dbc70ce16fb2b685fe9e234aa80bca9294ddb27f1`  
		Last Modified: Tue, 20 Jan 2026 18:47:10 GMT  
		Size: 38.3 MB (38296097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb17f06827a1bc4df9d04cbc37bef169d7852266770da1be1a3dcdcd75c818`  
		Last Modified: Tue, 20 Jan 2026 18:47:13 GMT  
		Size: 228.1 MB (228066553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:bba8ae143115ea33ee3e0aa829a696ed4c083c04f4a8f45760aa98d02308d059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6340f8a01a0d70bf344d12e1d82a809915665d818a9b7c9f72270c06aa3b077d`

```dockerfile
```

-	Layers:
	-	`sha256:03fccd02d5aeb1dfcb45673e60e8e17350aa807c422318e6504f9d92dcbc1a00`  
		Last Modified: Tue, 20 Jan 2026 18:47:08 GMT  
		Size: 3.7 MB (3655355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3eb66a3e293b7bdd85bd5ad8ca2b5c2448cae9c4cc4507f9d48d9dbaf84726`  
		Last Modified: Tue, 20 Jan 2026 18:47:08 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oracle` - linux; arm64 variant v8

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

### `openjdk:27-ea-oracle` - unknown; unknown

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
