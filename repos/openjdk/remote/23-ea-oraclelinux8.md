## `openjdk:23-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:0d4ba0f83eb56c16399deeb75073165486b2347e9aa7cc12b30f6e63e4898deb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b562ec24aca0ec4f32412658ae0f81f0dbf66222c73a5fb1545984bc913fc7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269435323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acee7d59408d896ee570fccd6f1a927d566dbc6efbf87068f68adf3a985241c3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09987f4997aa8b8281df445cf1e28ddbb727dd30e2f4bb34c377bf6277bf83d8`  
		Last Modified: Fri, 26 Jan 2024 23:50:39 GMT  
		Size: 15.0 MB (14990855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89802247d78b61e88ed2a5bb32c633d022b5c81330f844445d9433b168e45e9`  
		Last Modified: Fri, 26 Jan 2024 23:50:42 GMT  
		Size: 203.1 MB (203122737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f628b38127c6c579451a7482ac07bcb9949b87e5957446a45dd61b9ecbc63297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41eb133b0013ea18994bb7c2d1bafe4f55df28a2a446ffa1b8352a05d438d622`

```dockerfile
```

-	Layers:
	-	`sha256:7efcdc5e43b52e32bc97161f71181a925ed387d616fa5e6ea61d17521f970639`  
		Last Modified: Fri, 26 Jan 2024 23:50:38 GMT  
		Size: 1.9 MB (1915843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07e8ea744e729c1e14d6ffd79a52868657c86df76e6853300b8ce6db5687c6bd`  
		Last Modified: Fri, 26 Jan 2024 23:50:37 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:faf7d7338932bc09e70435693d9bacbc2a057e1656ba83f4e2eeba952ac5cdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266793097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6b75056451ed01c93d88f490ccbf75ba40cec5b824dee95f71faefb253dd64`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 22:07:51 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Wed, 17 Jan 2024 22:07:52 GMT
CMD ["/bin/bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbecf34c8e1a9b9949041e4c9e805d7ee8c1f00ad6362349a4579d6db495c27`  
		Last Modified: Thu, 18 Jan 2024 10:42:33 GMT  
		Size: 15.7 MB (15702213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b063dde595b109bd2fdffeef4360385896a8ae35e9260c7e81825476b792a4`  
		Last Modified: Sat, 27 Jan 2024 09:23:00 GMT  
		Size: 201.0 MB (201016306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f8703804c1cc247b2bd3dc45e0d6a0900cf706a0a51258cb14c3667aa69d6bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3534e9008d112fad7cf30d4b7b335605e415ea9e06b6e74b1245368d902315f6`

```dockerfile
```

-	Layers:
	-	`sha256:6b02fc1ff04250183a71819bd4aaf1a673bc55b0409d3316e9dac5b5a8572cd5`  
		Last Modified: Sat, 27 Jan 2024 09:22:50 GMT  
		Size: 1.9 MB (1914421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46be7bb1f68444192af8b9ffbdf453d3576ff87aba8cbca01832ad3bb17f6693`  
		Last Modified: Sat, 27 Jan 2024 09:22:49 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.in-toto+json
