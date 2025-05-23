## `openjdk:25-oraclelinux8`

```console
$ docker pull openjdk@sha256:084c8c15d8c4ce53614cb610269275b6483c92a710cee7a359125c09902ef034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ebf61bb76ee0da4c2d36ef1b64a1414855a396df639c93725f34cf05a62dc4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280668217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a03ddebc9bca6d6daf3e0ada97f88f2627878e6c9bbaa728e17d3b6a266718e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 21:48:19 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 21:48:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ee6d2b4bc3292763eeab29f03adacbfcd179273f648dc332abeb3f2f9cf99a3`  
		Last Modified: Fri, 25 Apr 2025 22:19:54 GMT  
		Size: 51.3 MB (51312878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52aea1e076e17fb537eafe9fa9c8c4128b7731331c5398d4b1e94699313a879`  
		Last Modified: Fri, 23 May 2025 19:55:49 GMT  
		Size: 15.0 MB (14997961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f19dcb685c7d61021bb22fd841a7e076d71822a1dd749c8493d2a1ae0bc709`  
		Last Modified: Fri, 23 May 2025 19:55:52 GMT  
		Size: 214.4 MB (214357378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:0fa85a855317d69db986d41900d5a0035bae9291e3c1c9aeeb3e16a76396d1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8f7996b88aa3d089b61ebcc981b9184bae9002b7eea74565687a96073c3c9c`

```dockerfile
```

-	Layers:
	-	`sha256:3e890cb6fd947bb2cd4bfb17df5a6e7976db6e10e2f13d592335739e2db55f85`  
		Last Modified: Fri, 23 May 2025 19:55:49 GMT  
		Size: 2.4 MB (2449776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b828eec957c7bf89f6327f7cf49b7bfdb4936c4206f523adaf5b301d1dd06d1`  
		Last Modified: Fri, 23 May 2025 19:55:49 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d8cb0a3cc53b8bdab80cbde4e9440f3244bf7ca86ecfb74fe2251b8afe360026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277819538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb16df4fdc40e27b0ee0c743de53b3bd892daafa8ecfa9ddbc690dfe3ccd0b9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 21:48:43 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 21:48:43 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
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
	-	`sha256:ef593a8ba4d709a298315c96b9f361e0884e3d962c21577892cb95a6b33926cd`  
		Last Modified: Fri, 23 May 2025 20:05:44 GMT  
		Size: 212.1 MB (212124062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e0794d4cce7d6bbe3019fa98de530337209f3ccdfbcc3883769135c17fa051a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7fe31be101f0dd086543c7374a1b600cbfc67d47f155cc2a394ee9ae0de104`

```dockerfile
```

-	Layers:
	-	`sha256:5387adac321b7b484bfbab11e62a26abf8056f7ec6f7721decba967088914086`  
		Last Modified: Fri, 23 May 2025 20:05:40 GMT  
		Size: 2.4 MB (2448622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aaa9841c1b361e778907d4f74474e98b3673e675294689c31d54fcd5a7fdde6`  
		Last Modified: Fri, 23 May 2025 20:05:40 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
