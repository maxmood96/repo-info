## `openjdk:24-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:facb79da15e2a7853f8d6419791f06187910b158f1c5620312fe5731d5339a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f41af16b748f2de733580723e91a050dc1590c499e079e5fd93077da3d9cc49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279501855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f064e972bc716982cbc7568acca5b73c492133371fcc58b6103f38f17edccb`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 25 Jan 2025 01:48:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b976166ae00f0fda8e12b934d92a7265904c082bbb675e0cb9bd4bbe93bedb30`  
		Last Modified: Thu, 30 Jan 2025 23:27:50 GMT  
		Size: 51.3 MB (51277963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290d39bf633160a2897c4ad2188ecc883e9973056bafa1e7bb6ab855aea4aa67`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 15.0 MB (14975247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0def97f931d1d23b2893b037e17c8974bf40d09b926e8551328e46ad32edb41`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 213.2 MB (213248645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6e147b938518e0dd3077a844bfecb744274dbb9b857a1fb93cfd16f7269d0242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0024f806d7d9b1d2ce11a44035fde63a0b9a89a5977cbbffaa6b9d1c013e337`

```dockerfile
```

-	Layers:
	-	`sha256:590b168c18468c1ac3494156e0c6ebb027b41d511a00543050ccd24bb862529c`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 2.4 MB (2441597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4615af6533c58d364268fc2eb346b2ad5f4d0d0c60cccdf269a129996adba0f`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6a1e9b4991bdd4a1975e0cf908d9ab6063a9ddc689c4179e6a65f66299b8f3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276848251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b933220aeb58e685df184649b1af50278f9399cc3931a13d0d1aaab6e9836d3b`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 25 Jan 2025 01:48:18 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bce860c27508f058f4bac6fca02fb3ef33ecf5c8331d2635b7c34a8b0af94e0`  
		Last Modified: Thu, 30 Jan 2025 23:30:11 GMT  
		Size: 50.0 MB (49984693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20da80e2bd804d65a47238fa85705492fc406b2b8cbad4cb1a153d9b26b0720f`  
		Last Modified: Fri, 31 Jan 2025 00:27:46 GMT  
		Size: 15.7 MB (15659413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed45ced462cfa5d9e6011d377e11d9cbd96b67b3ac944ea6dbe55fdd56833f6`  
		Last Modified: Fri, 31 Jan 2025 00:28:43 GMT  
		Size: 211.2 MB (211204145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:af7517e7e1c4857694ab39a74dd47564416f255d73e7e328d962f7c83dc4b794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa72718f8b457f928441512da2e916c3d345d5c02f534e76829368ea6027c2a7`

```dockerfile
```

-	Layers:
	-	`sha256:6368639218d5d474e8c1d0048c47a7b15a7d9eab4174f5a801422ceca517cc1a`  
		Last Modified: Fri, 31 Jan 2025 00:28:38 GMT  
		Size: 2.4 MB (2440443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187d322d9cb6c016b445acc60ef20cd8829bff7a3b22544d35814d7e69c55439`  
		Last Modified: Fri, 31 Jan 2025 00:28:37 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
