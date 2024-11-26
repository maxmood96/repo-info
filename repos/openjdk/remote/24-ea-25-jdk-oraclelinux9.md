## `openjdk:24-ea-25-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:4ac38119ec63146e8be3b4a52c729ff5101fa8e8a717104e2a2cc16f1c5a8964
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-25-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:e6162b2ae15cf020c66152fcff7dc7f2d600cf06651a08de799d3a49d9acfe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310791101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3f81acc5b7399283abbd9bca1bf103c3d7f1233ed7a9d0546b0a36acb838c8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 22 Nov 2024 19:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_VERSION=24-ea+25
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='06d2571c8af4948ac1eaad2b912ab59f320f01744bc4152f3476a65512bb3901'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='022d2edea028f26d0aa8cc933429f305abac8f8a74451095a55b1354f0db7966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad7616db1cc4766419b9ecbbca68b24225ef7b46816e94bbf0da45d9edc059`  
		Last Modified: Mon, 25 Nov 2024 23:25:11 GMT  
		Size: 48.8 MB (48767436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c06c0dee8c4f57fe9e59a244be1a496c5256063d2ccecb023ce4930ab7bbbab`  
		Last Modified: Mon, 25 Nov 2024 23:25:14 GMT  
		Size: 212.9 MB (212924963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-25-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:afc9eac6df7fec5ee96b466d218f8d92853b377e9e403569ac52e3b5b603f34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd3f176f8d76f72998f1eeb13e1f4ab0fddd2b5887d602d54ca7021d717921e`

```dockerfile
```

-	Layers:
	-	`sha256:4799c7ae1a39e51ca4c8259445fb1532d8b1f5b227f5be27145ac695be46fc8e`  
		Last Modified: Mon, 25 Nov 2024 23:25:10 GMT  
		Size: 4.9 MB (4912583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa428769b128b239098e62fae1de54b7b31b6a573c3735feaab6e7634d38f5b`  
		Last Modified: Mon, 25 Nov 2024 23:25:09 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-25-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5a4472fdca0885a309c16490756d113d6c1994cfa1b323e887a0ddb71a78121d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307734185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6189d34ae7c7d944c5d19cb6f4b0ca3335e379b3c623697dbd2f3475321266`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 22 Nov 2024 19:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_VERSION=24-ea+25
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='06d2571c8af4948ac1eaad2b912ab59f320f01744bc4152f3476a65512bb3901'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='022d2edea028f26d0aa8cc933429f305abac8f8a74451095a55b1354f0db7966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff9f5494a427d9d8a40a0f42c60afadac361e3515d52601f7d74bf0d09b993`  
		Last Modified: Fri, 22 Nov 2024 05:14:01 GMT  
		Size: 49.2 MB (49188086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981ee1f51758540a106d4ff7d7d1c5015a848f6afcc728729d0d1a8a2267651f`  
		Last Modified: Mon, 25 Nov 2024 23:24:35 GMT  
		Size: 210.9 MB (210878707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-25-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:13f822835dad7cb22d2bc37e32865a02f613835ce8895dbf3f8015751b7c16f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cea25c644d7fdbe1ead4a0fe217ada6cc76e8110c4e0ac0b55dbcb7fd61db15`

```dockerfile
```

-	Layers:
	-	`sha256:68e9399bf9598e70aaa7728ac9f1830bcf882d81f3088dced726d43383350feb`  
		Last Modified: Mon, 25 Nov 2024 23:24:31 GMT  
		Size: 4.9 MB (4910341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2607f942e15dbc8d452db9488f584d0dea081161408a602251f95094b240bd4`  
		Last Modified: Mon, 25 Nov 2024 23:24:30 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
