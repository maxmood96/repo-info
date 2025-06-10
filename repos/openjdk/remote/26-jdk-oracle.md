## `openjdk:26-jdk-oracle`

```console
$ docker pull openjdk@sha256:39bf8a3d97ff61a0c3a04f51dc24b6d670b9197f3dc8ec5f18852c23063490f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:cd34a34f7462d6754f80bf6056e43b3fdbc586a40bd52b84c300dabeff88a523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310639434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe059760ab73363a456c16a0707ce705a9571f7918126b73497053572901cb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:24:46 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 16:24:46 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 09 Jun 2025 19:07:09 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 19:07:09 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='9d95d3e025035bfe649be52a1a5f94e28f66af98693db6b4e879fa3be4dc4e69'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b80805bd34f0513f09b4cbf9928fb8c73a883c6979ba1df56e71f1b7c12e434'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9845df06f911da943784ccfba2249144e9c16f5ad081b3583ac643cc30b49df0`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 49.5 MB (49497893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693cc2b74e2f2b4e601650edad3c8e4dbd9389481aa7b579effedcab2c751577`  
		Last Modified: Mon, 09 Jun 2025 22:07:16 GMT  
		Size: 38.1 MB (38083760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc653e6197e03b98c9a8d8e17fd156db3925f6347e294ca00b3349e39cff536`  
		Last Modified: Tue, 10 Jun 2025 00:37:48 GMT  
		Size: 223.1 MB (223057781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:2996c4576c5de0569d6faac484ddb4256d9569e07100350dca50e4848e3c1baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91be5ed85b206727d1ecdb969b61c7b626b42d0ef03879c268e3def6a7c5b5b8`

```dockerfile
```

-	Layers:
	-	`sha256:a9f0a8b89403ecf93bc4d2fbcf1f9cf6edfe6fee2285e2534eca5baecf9a0afe`  
		Last Modified: Tue, 10 Jun 2025 00:25:25 GMT  
		Size: 3.6 MB (3641216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b9ad662409ba66424668fb94ec60fa756da35d7b10b6d15c622f8222998793`  
		Last Modified: Tue, 10 Jun 2025 00:25:26 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5760bf8fdcc3b05f37c8f6906261dcc911df1ac5a2774f4551934235455998ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307433551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbf3e432382d2e0c80f309fc3ca9001649d568b11a5067450393b0f7d6ea332`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:25:38 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 16:25:38 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 09 Jun 2025 19:07:09 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 19:07:09 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='9d95d3e025035bfe649be52a1a5f94e28f66af98693db6b4e879fa3be4dc4e69'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b80805bd34f0513f09b4cbf9928fb8c73a883c6979ba1df56e71f1b7c12e434'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
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
	-	`sha256:96ada76353dd947ffc4a3791830a9a30e89867723ebc77920ac21bc584878859`  
		Last Modified: Tue, 10 Jun 2025 00:38:19 GMT  
		Size: 220.8 MB (220846999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d5c2fd0253786f659067e7c8213db7a6717d6443219eea55a422b060754e7a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c024e7884b9f87a7861670b080c2c39c5cb28a151d14954c5e42f6e5ba07f46`

```dockerfile
```

-	Layers:
	-	`sha256:73c6853673aa37f36c80201e16e23a8d2269869f73ff808249289dcfb069b7cf`  
		Last Modified: Tue, 10 Jun 2025 00:25:32 GMT  
		Size: 3.6 MB (3638978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247b5b4117094de2504170aea4e38afad68b6cff4b1019a578f37486ed19a082`  
		Last Modified: Tue, 10 Jun 2025 00:25:32 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
