## `openjdk:26-jdk-oracle`

```console
$ docker pull openjdk@sha256:680fba302536c270447d8ae578f5df1ade3fa9fc730cccd4a7e82d1596ebf47c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:8c87d265e9b5331b8c3cf49741339d8611b6719bec31fa8216bb6a842739e296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310583489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31546fc0d41c868eee47c4200fc969ab61b4ca48b283cded0ca95c45773aa912`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 23 Aug 2025 00:48:14 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 00:48:14 GMT
ENV LANG=C.UTF-8
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_VERSION=26-ea+12
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='2d6177e017ca138d8990643910b989990751db9370cd78dfc51e5116411e7f6f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='b4e0c4bb252fe005ad3a46c54264e226c554fe95edcbdc9df81dbc268901c7cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165c69276785d440658cc7c706b1c14743d4dae8151373026e372596ff83da2a`  
		Last Modified: Mon, 25 Aug 2025 21:26:37 GMT  
		Size: 38.0 MB (38005064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daab9091392d98034b0ff1a0d0d636270de1e6044b33c31bbe54ca5b5f2e4ad4`  
		Last Modified: Mon, 25 Aug 2025 21:27:02 GMT  
		Size: 223.1 MB (223081409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:7a581a59fa9305feacf4d84b68a38afdc0fe9cf546771a5ef9b914bf19d7d5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01ed90bde53bbb3f810ec4bbe0a2849bc2194d862ab8555c13bc984def86add`

```dockerfile
```

-	Layers:
	-	`sha256:3c697954f5c32bcb3b8c7f8f85069619d92d5798e53bca30b5b118ab0e3d35ca`  
		Last Modified: Mon, 25 Aug 2025 21:23:51 GMT  
		Size: 3.6 MB (3640729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efffc3e94d1412bac89b955b6d83e3df7625d635c88d021be4307a07ea25d612`  
		Last Modified: Mon, 25 Aug 2025 21:23:52 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ad0a33d1d194ed00a465725da1f0079b30eafbb59b460a09995ca869d061159b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307360542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc603d2dddcf7cd70d7b9b4d6cb0ee76ea53dc65880c3d33fce28da264e2ac1e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Aug 2025 00:56:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f251bedb6d0a7854cec601a06650a41a8800628c25948fd9b15b8018354d6f6`  
		Last Modified: Thu, 21 Aug 2025 20:15:43 GMT  
		Size: 38.4 MB (38406411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51e28b281dcb247723ebf6d36846d9a67c6510bd10d449b943daeca793a80e4`  
		Last Modified: Fri, 22 Aug 2025 00:00:31 GMT  
		Size: 220.9 MB (220867408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:cca6cf713c262c3e8e2fdcc1069a231a2a0fca255cd89f3097c825c2491dd2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbda636cd49e2b0814e57724cfcae5eb085b2e6ae80ddb04b5986991891f373`

```dockerfile
```

-	Layers:
	-	`sha256:61cc99c6c4b0d29b8829fcf858ea1a0a4cc29696647887f0165baa70cb5ec632`  
		Last Modified: Thu, 21 Aug 2025 21:24:17 GMT  
		Size: 3.6 MB (3638491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79dc6989e1db035b62c97d207d118556a8216788b10d03e3fb738bb3a0892eb`  
		Last Modified: Thu, 21 Aug 2025 21:24:17 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
