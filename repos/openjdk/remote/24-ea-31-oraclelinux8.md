## `openjdk:24-ea-31-oraclelinux8`

```console
$ docker pull openjdk@sha256:e37fc72b4c628b1ee42ff45c394fc5d968509a373ea1ac5cea1de594e558b622
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-31-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:9b4fff89f8d384ee8f8ef651ab213d427114893709e4edef12bde4c2e3fb62ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279467179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f51210bc03fa4c2b1d36dd54c0bc55d2b712bf93853c9ea3e667671a0bd21`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 13 Dec 2024 17:23:13 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e61fdb4859a26d40637db4ec936b5f92261b748fe5c9925d17930b40652f5a`  
		Last Modified: Sat, 11 Jan 2025 02:30:07 GMT  
		Size: 15.0 MB (14975433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d61c0f002b37254c08411e75eea037bea6ddc8f28b2549cdb8885b4d1e4ca`  
		Last Modified: Sat, 11 Jan 2025 02:30:10 GMT  
		Size: 213.2 MB (213216754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-31-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b9a08ddc0ce74d5a4c5e136bda836c5e5da1ce0129bdcdd3a201d76e10abe2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3705e53094cf524ccc96b435119151c2394bba8229da69b8e9951fd9cfa8013`

```dockerfile
```

-	Layers:
	-	`sha256:397c73767d74b3ab4c88d43be8ac647f7a210cc8b08193e837172959f1ec9ffe`  
		Last Modified: Sat, 11 Jan 2025 02:30:07 GMT  
		Size: 2.4 MB (2441585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:961059c8be39b798996cf3f2406535675fbb93cb8de1f3d0994a4c6137981af8`  
		Last Modified: Sat, 11 Jan 2025 02:30:07 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-31-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8ff99d45bec6f6b80bb37bf8c0da3bcbcc2984717817ea6f30af41a32db5259e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276827473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f9dce2fb23525b3dc0b1425d47617bebf4ce6c999046a3b9f9f53c042ca459`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:54 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944cd63dffddb127d99cc2a7ba13ba2ac1f47dbc72b57d4efb7ec8ed046aa53c`  
		Last Modified: Sat, 11 Jan 2025 03:21:57 GMT  
		Size: 15.7 MB (15660035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3579d777bc40e91bab7bca6500e930c8f91cf131748c574f0707d0b421255e05`  
		Last Modified: Sat, 11 Jan 2025 03:22:01 GMT  
		Size: 211.2 MB (211187163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-31-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c58c657a7e926633db78a234111aa9fced8be57c1f65151adf81c65aa21ed6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b06c04fc0f8a0f66ecda11f09c764c5c34fe4385ca373c4b0df4c95fdffdccb`

```dockerfile
```

-	Layers:
	-	`sha256:2d9733929b3f58b8a5a65711cdb90f14e86a04e8ae798beffe13924f7dfdb810`  
		Last Modified: Sat, 11 Jan 2025 03:21:56 GMT  
		Size: 2.4 MB (2440431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9280ec16b56893a501028475aac2a50d1d51e891ccfa7543ad0fe9a430e9c994`  
		Last Modified: Sat, 11 Jan 2025 03:21:56 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
