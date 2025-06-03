## `openjdk:25-ea-25-oraclelinux9`

```console
$ docker pull openjdk@sha256:3f977e6170cc37a19933845769e36f60ce4181314c648a7f56c756a39035d3cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-25-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:eb679e552ac66a00cb1a3f1550eb09e3e65e896edcd1270a75b0b9cf64b14b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310192566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2e165dd8cf6feef99a995d7eb3d4cf9c0c9c31e92e5a7a08b7d10ef1935066`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 06:48:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["/bin/bash"]
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9845df06f911da943784ccfba2249144e9c16f5ad081b3583ac643cc30b49df0`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 49.5 MB (49497893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8040d35fd09b0e17c2af73168406b7a609fb97695a378936f1125c81abdaf4`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 38.1 MB (38083417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f596540af9c091c114b58eeb3dad17bf31d855321fcb771bb6baca0ccbc34e4`  
		Last Modified: Tue, 03 Jun 2025 13:31:59 GMT  
		Size: 222.6 MB (222611256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-25-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:cc5074371f7f5daa9edb9a1c5bc7d1a213f48b9c2c76cffad1980db68d3ccd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247010c7235daea18a5eb7f3451ba9ee90afb8aa1b53294f98ce0dab0eb9f80d`

```dockerfile
```

-	Layers:
	-	`sha256:fffb7dcb6672b4c7b6cb7ee6c9fdb8fc30ea46b7d5f893133457c2ee0674dc73`  
		Last Modified: Fri, 30 May 2025 18:54:28 GMT  
		Size: 3.6 MB (3640598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6656ddbbb2f3e86124c84ac6b894dd90a0bf4eb08f91006749d66c81e5c7e8cf`  
		Last Modified: Fri, 30 May 2025 18:54:28 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-25-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:775b35bd4988b53323028d216d05d60448aa071b677649cae4f38d63339a6078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (306978241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6b6b53f14d6464cc1d9fc4eeb9185c7e61fc424cdd638db0eb50d2861c156a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 06:48:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["/bin/bash"]
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea200bdb0c47dcdadc2a348d06f2a405cfc6bd5a6663beb497489ea034193d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 48.1 MB (48090579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cfd988351345b9f04447fdf8c2c46e73b5a5a2afdfe346ff0026d0c170ac82`  
		Last Modified: Tue, 03 Jun 2025 13:49:29 GMT  
		Size: 38.5 MB (38495973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d9ae4909a15b27f8cd92d9de77a58d07f2145ff25760d9e70238264a7090b3`  
		Last Modified: Tue, 03 Jun 2025 13:50:09 GMT  
		Size: 220.4 MB (220391689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-25-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:96126d147679af58024bfee60fee8402f8155e291bafedbf100ed28019f93060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02aac6c89e9442b67d7a609e7742a2db78855cda269bc9cc284a462658b8c638`

```dockerfile
```

-	Layers:
	-	`sha256:7dd388267602f9cee662abd05207f2904ec8fc6de8a8ef5888d52bbc8e4600f1`  
		Last Modified: Fri, 30 May 2025 18:59:43 GMT  
		Size: 3.6 MB (3638360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e055815e3dc2f50253bf5b8b85f876071f1e8fe1225cb637cbaae6ee840c294`  
		Last Modified: Fri, 30 May 2025 18:59:42 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
