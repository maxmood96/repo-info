## `openjdk:23-jdk-oracle`

```console
$ docker pull openjdk@sha256:aab6c1cd9e48cf15f5675b33a5de8d7179e57e06434eec9d994f3714c6cc94b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:be680feaf8903ce63a7cc4c696bec8b5f31b8f4b97495d0690f0b65fb5b3a57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289430499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016259b562187773a9e1c51ada4bb0c38e4b62ee5819b94e51b3d8100b6f9c33`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:04 GMT
ADD file:9bcef05fa351e2fb72a4b6052a0252eeaa2cff794ed089a482670c67961d2e90 in / 
# Fri, 08 Mar 2024 19:21:04 GMT
CMD ["/bin/bash"]
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 22 Mar 2024 18:48:16 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Mar 2024 18:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_VERSION=23-ea+15
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='c17995b5c67b845af47704e2a664f5b6ab540f968cfae06972a7562144b7634a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='804a15db8c406a0d70ad5a2da125339de3ff66759107fdd75bc6323d6d0cc5d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:972029ff9873af36c6c0fcee05b14acbc57a61ecd0b8bf86b167bdf46f973823`  
		Last Modified: Fri, 08 Mar 2024 19:22:31 GMT  
		Size: 49.0 MB (48978454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d243b6fd58699ad9550ea314bf9c0f39da2e9e93cbb722dd6ee86ec946d8f4fb`  
		Last Modified: Mon, 25 Mar 2024 19:12:40 GMT  
		Size: 37.7 MB (37733879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab0eaec1dc023b0785b50d01391e0c5fe47f2a794b5f1c5cf12e0007ac9383f`  
		Last Modified: Mon, 25 Mar 2024 19:12:42 GMT  
		Size: 202.7 MB (202718166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef8d4bf859a08ec2602f1db9d796708d7bd0a5d2d8b8ab5d69b68bd7b13d288d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3349353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17a49052ed1d50ca97d879d4889665011ac4f7b6d900747264dd6aed2b5d688`

```dockerfile
```

-	Layers:
	-	`sha256:88093cd5d6d2f2f6ae9b126d26b9fd1fb1650a7f980bda3a5b512e3d9c87000e`  
		Last Modified: Mon, 25 Mar 2024 19:12:39 GMT  
		Size: 3.3 MB (3329466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07081e0e80e3c2a4b52b16203594de19caeb28a144a6cf55173ae41f5ff28d9b`  
		Last Modified: Mon, 25 Mar 2024 19:12:39 GMT  
		Size: 19.9 KB (19887 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:176aa1de0d471970f1e06c0e36a8481f2c925029744ab0116e373b078e5b4df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286418858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af58495e3e189f97d637f4280a0bb778cca291e502952b0f0199fe4676db2f0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:48:53 GMT
ADD file:71724b501850c3e6cd72efc58b3430394f691a428c2c62755eac0b93c5579f35 in / 
# Fri, 08 Mar 2024 19:48:53 GMT
CMD ["/bin/bash"]
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 22 Mar 2024 18:48:16 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Mar 2024 18:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_VERSION=23-ea+15
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='c17995b5c67b845af47704e2a664f5b6ab540f968cfae06972a7562144b7634a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='804a15db8c406a0d70ad5a2da125339de3ff66759107fdd75bc6323d6d0cc5d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c53b3bc8702e4b172b3fdde99731082a493b5f5fdd7e9632b3cf7dea02a52b4`  
		Last Modified: Fri, 08 Mar 2024 19:49:57 GMT  
		Size: 47.7 MB (47664888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71597242e3bc84850918d978b72bcf84c5867bfb6441051c67b805dca13e66a`  
		Last Modified: Sat, 16 Mar 2024 15:50:44 GMT  
		Size: 38.1 MB (38140694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6920a87e6f6d6b8393555bb2f2590510d7ae41123b1946aec3b3651cce62443`  
		Last Modified: Mon, 25 Mar 2024 19:54:49 GMT  
		Size: 200.6 MB (200613276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f4a60e50a582d2f2b909ffd3f04454cea2a7be28124f1401914c0d072239985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2064cc24b75d4bd502928f2f44384bf207545d057b6f68239f5bb54b59ac06`

```dockerfile
```

-	Layers:
	-	`sha256:fd49ab7cc147e3ab0bc8dc7ddfc1e7d887332dea437c813948d36c4ab10b6ac7`  
		Last Modified: Mon, 25 Mar 2024 19:54:43 GMT  
		Size: 3.3 MB (3326704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82a203ba04c07a7cf866779261589b363795591eb5dc16ff72e89d8a00ec8d89`  
		Last Modified: Mon, 25 Mar 2024 19:54:42 GMT  
		Size: 19.8 KB (19758 bytes)  
		MIME: application/vnd.in-toto+json
