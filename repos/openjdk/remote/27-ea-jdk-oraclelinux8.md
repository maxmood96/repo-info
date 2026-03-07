## `openjdk:27-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:34939e44e23df557ad41c715b930739df94451673b2b0b15db37dd3c1c7fcfe4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b3abb8fa87401f6125b2933904318163195b514b0e34e83d96f049053b89cf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295317425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b62a3ff17e765c6279bcb9d5625cf1b37336f9873e779e034bf3260fd2598c6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:12:15 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:12:15 GMT
CMD ["/bin/bash"]
# Sat, 07 Mar 2026 00:40:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Mar 2026 00:40:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 07 Mar 2026 00:40:34 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:40:34 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:40:34 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:40:34 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:40:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:910e0c7025a94af1bf4f9980abe31c6c0541dbb5c579f5a09497c1a5d667c578`  
		Last Modified: Tue, 24 Feb 2026 21:12:26 GMT  
		Size: 51.5 MB (51462874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949e01789e3d19b2b6b582b2240081f05ab9ca24ac636bf004c9aa727c952087`  
		Last Modified: Sat, 07 Mar 2026 00:40:54 GMT  
		Size: 15.0 MB (14986795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b44cfd957b7840bfac8f32beb5f41d8181688e03e0f0be522f9f9564bcbf39`  
		Last Modified: Sat, 07 Mar 2026 00:40:58 GMT  
		Size: 228.9 MB (228867756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:eb5db67661309317a945a4f2609a89480e41cbb97862eff335bd26752d279041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ee156e37a8f208d8a7d1e75b0133d77a93df4e932ae921913d1ccc72642a10`

```dockerfile
```

-	Layers:
	-	`sha256:6039bebee7ebee33697d1590dc80ecd7fd2ba6813e0dfc5604800f6cc10ceaca`  
		Last Modified: Sat, 07 Mar 2026 00:40:54 GMT  
		Size: 2.4 MB (2448698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09a19b4139d2ef14945785102e6a0ca2d9304585b5ceca4007e595b85bc1896`  
		Last Modified: Sat, 07 Mar 2026 00:40:53 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dee1d73e3e61e88db7eaaaf02ed46382e1447cf2c1ca96723736f6c846338d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292747604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b39bcadfc7c5251cd50094d77a9aa029604f96b6bd80e1b93ecad04d398d885`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:25:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:25:54 GMT
CMD ["/bin/bash"]
# Sat, 07 Mar 2026 00:41:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Mar 2026 00:41:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 07 Mar 2026 00:41:39 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:41:39 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:41:39 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:41:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:41:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:308b2ffa0912bdff2bf3b77a5f2634a00c2761e38a51260adbdfe882bc668185`  
		Last Modified: Tue, 24 Feb 2026 21:26:05 GMT  
		Size: 50.2 MB (50199180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec98407f645d849917513e7a1f729aefa64131ee42c62f05826981fd9d36455`  
		Last Modified: Sat, 07 Mar 2026 00:42:01 GMT  
		Size: 15.7 MB (15700133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63119a4d86fa680efd1693b190e00e0bde133c5bf6e16b317e0329d6448c5837`  
		Last Modified: Sat, 07 Mar 2026 00:42:05 GMT  
		Size: 226.8 MB (226848291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:20d7e20a33c36825804e55e1da00e0538bea270b6c3b5beae199af5a08156e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1789be031e841c397c68efb868bac1123a9b7c3bcdb76fe59edd1e2ade03fb`

```dockerfile
```

-	Layers:
	-	`sha256:d89414f72858214be1f1f691fd389a10d26877b6609c018671a85458149b9182`  
		Last Modified: Sat, 07 Mar 2026 00:42:01 GMT  
		Size: 2.4 MB (2447508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27fc2ddda61c6e2ecbe6a8bfd49b855bef2bdec8384e307d438384c80e313819`  
		Last Modified: Sat, 07 Mar 2026 00:42:00 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
