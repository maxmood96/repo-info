## `openjdk:22-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:7a0b7518879248805036f31f876f02c6bf4345a6134b470ea723ebaa219940e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d4edd95e233b788d58eff0a2578efb16a95a4689ff7b8ea8c7a28fc52a18eef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269074742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30da4ea82668c92cc45da55ac76e0443989be669950c1298a15592c84a63af0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:50 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
# Wed, 20 Dec 2023 22:40:51 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d348d46b29638a8952a7396193aa3b4743e0bbd69a80cef3219051a20ec89e6b`  
		Last Modified: Sat, 13 Jan 2024 01:07:39 GMT  
		Size: 15.0 MB (14995315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e241452337b2344beb9425b2f7b1597a94a0adb92b0ab53cfd10a9f9506e6973`  
		Last Modified: Sat, 13 Jan 2024 01:07:42 GMT  
		Size: 202.8 MB (202755959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:3a7d93c6eb7b7e5655a677583717ac81650d2067e1b7ed8e0b78a045bebfee26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0d6c641160fce3a4e8caf293c1c8a7b07ac72b347db1d5f96017ab836d07cb`

```dockerfile
```

-	Layers:
	-	`sha256:7bda2155e17977da2dc91b4e460ff4c8a273ab4174597739dcaf148edbb2945e`  
		Last Modified: Sat, 13 Jan 2024 01:07:39 GMT  
		Size: 1.9 MB (1915851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbd24806353b6b55bff45f15d6f93755c87835972859c2f5d7ecb3a76d45e930`  
		Last Modified: Sat, 13 Jan 2024 01:07:39 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b65f494877fcad96ec34377a7ae241c033a7893ad842eba7c108889905660192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266586351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5554cb0472c9a99ae66d274eb511a972e340e7121efc48489565e71ae083343`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:53:14 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
# Wed, 20 Dec 2023 22:53:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
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
	-	`sha256:2c7063049804cf18affca14d0f85d5253f4ff50454702171190db1c661b1af73`  
		Last Modified: Sat, 13 Jan 2024 01:43:18 GMT  
		Size: 200.8 MB (200816596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f008449dba91dc444936d4509f445c6a0aff449db948cf3c17a473e5fb0c7213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96618127ca86161de983ee4491f8d39ae0c122c9f74d7c325b6401573f5ce835`

```dockerfile
```

-	Layers:
	-	`sha256:33a86303746bbfceb75d0d9fd1679a86f286d18f1cc19a290bc726e601b960d8`  
		Last Modified: Sat, 13 Jan 2024 01:43:14 GMT  
		Size: 1.9 MB (1914425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381da29c290b40545cb1cf3c22048fcebfb3337f923c57e72bf3f31aae891325`  
		Last Modified: Sat, 13 Jan 2024 01:43:14 GMT  
		Size: 19.8 KB (19759 bytes)  
		MIME: application/vnd.in-toto+json
