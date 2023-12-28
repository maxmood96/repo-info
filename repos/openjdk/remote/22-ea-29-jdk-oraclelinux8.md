## `openjdk:22-ea-29-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:a53c800a9f56329d02b39a36cae0fdc36ba2d70a8e7bdbba99260f7a7351e3aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-29-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d913b718c6946ab2b70e9f505b1d97e76522b4fe0bd072b25d3502ff241ec996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269065297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a23a90e3ff3b5a55a71f36bedc105850e8c45e67225a96487af1d53d1cc89a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:50 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
# Wed, 20 Dec 2023 22:40:51 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389fb4b832d27607a7383e0960802239a63b583d8c29daa293fab73421ab3ba`  
		Last Modified: Wed, 27 Dec 2023 21:54:05 GMT  
		Size: 15.0 MB (14995331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664716af15e8070b43e686190dacf8e1adf1ba7be18db9cac2322a993aac3164`  
		Last Modified: Wed, 27 Dec 2023 21:55:58 GMT  
		Size: 202.7 MB (202746498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-29-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7fee356af6bfa6cec1cd273696e248ace31234404b7597388a159500f608d7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2001dd969c8a06769414c7dcc4b0d28a806009b39dc52619ec261d15ed951601`

```dockerfile
```

-	Layers:
	-	`sha256:8d1c7f297b32118920ab34858f620646371dae58c884da24ac5039b87c105716`  
		Last Modified: Wed, 27 Dec 2023 21:54:04 GMT  
		Size: 1.9 MB (1915851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd82a861e21c3adc1a01818e4047acfcb1f1addc8fcdd9c6546bb0dc752f436`  
		Last Modified: Wed, 27 Dec 2023 21:54:04 GMT  
		Size: 19.9 KB (19888 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-29-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:feff842fbefc974fcda104f6c0561fc57d483547780dda0922e720722f5d57aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266560512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139d2d28eacc7bc24feabe68a162f3c124f14e7d86fc9c2d1dea5acac87ffa43`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:53:14 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
# Wed, 20 Dec 2023 22:53:15 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 22 Dec 2023 01:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:48:11 GMT
ENV JAVA_VERSION=22-ea+29
# Fri, 22 Dec 2023 01:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='711a8d0580fa87221146b3c7d3bf1e8fce37b921a71a72989b8396a3fffdb71a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb3edae2765a15fce07581139c8833540021c383cb07492afcd4b130a1eb4810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f352f0f1de3c800e109fad5b2dae0cb9097249a14ca89d420642f858cc188`  
		Last Modified: Thu, 21 Dec 2023 07:07:40 GMT  
		Size: 15.7 MB (15690041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a21130bc7fa0f0b5ed7e5d41422bfe5af1c331e8cecb4d264993df794985a`  
		Last Modified: Thu, 28 Dec 2023 05:05:04 GMT  
		Size: 200.8 MB (200790757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-29-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f596027c21e4a00423662e52121bda61dc58a30d87e428dbfbbad3753c48880b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bc0980301bb12010e417828157e4543fb61e77cce59c15752f2a05f97f7bed`

```dockerfile
```

-	Layers:
	-	`sha256:8fc727417b9c5e9dea7b03293b8225bc750802e75b4ef99174336a4ae4c2dada`  
		Last Modified: Thu, 28 Dec 2023 05:04:58 GMT  
		Size: 1.9 MB (1914425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b23e23f7bf42dbd94c16de460705fd0891a044ded5adeae34639d9c37e348f`  
		Last Modified: Thu, 28 Dec 2023 05:04:58 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json
