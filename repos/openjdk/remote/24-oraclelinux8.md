## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:2e49006d385976d98fd936a7de8a27640ee9c2cd0d91f4c6e47fce22ec84a489
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:2fd7e5bc86a5c55e8a3e28826471af220b31787d52784317b765a63f5f38ca11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278036911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96681471cb78700f0fcaa86cbb3ae3fde06f9704ea1804d7298ad1bf57333446`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:53 GMT
ADD file:6f8c3cf297caf3b2a501a32c94a4fc0d2c7024f63d5e4b2215730b56faa6cdfb in / 
# Fri, 07 Jun 2024 03:48:53 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 29 Jun 2024 00:52:17 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_VERSION=24-ea+4
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='64aa493b28493a2d223626bdad774640cb148b0d52f392b081b2776532a980a0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d0b65f191528ab241b4e238568e52fa7199975b4f4b7badcf58a279b1fac426'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:427bba466fea4df7396a02ec368c5aa24d07ac80d02aa94eb57ba7af7b84b5a3`  
		Last Modified: Fri, 07 Jun 2024 03:50:01 GMT  
		Size: 51.2 MB (51219315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a34eba211693c65c9d6470ed7cb853b61081d4b9db9186a73dfb2266609be8`  
		Last Modified: Tue, 02 Jul 2024 00:57:49 GMT  
		Size: 15.0 MB (15035418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4216d2be74ae752b5ef84b4b2be8d685d5588651165b9096624326ba0c6d109c`  
		Last Modified: Tue, 02 Jul 2024 00:57:51 GMT  
		Size: 211.8 MB (211782178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9948dadfb94e268c88862bd9a84565c5193630f2fbbeab61f6ce9b4a32c84ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdbd0519770fd0a70a5d01f6339a05cbacc98b6e1fac1931d7fe059685de368`

```dockerfile
```

-	Layers:
	-	`sha256:96187f1830bf962fa22f6b37122f058edd1a4b3cb583731146414482718f24bc`  
		Last Modified: Tue, 02 Jul 2024 00:57:48 GMT  
		Size: 2.3 MB (2267551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5f83efc1bcb2a5c8fbcf6c0bc8bebad20d47c944303b8497560a9ca5b96a69`  
		Last Modified: Tue, 02 Jul 2024 00:57:48 GMT  
		Size: 15.8 KB (15803 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cf0d55242920fb07dd8de36553a2c6a55a801e1a17065f9167de881acb6388e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275288014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc98086971317f4962109c1c339d7896c53af7dcd8db8d47b7fb1f50c14e3d9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:11:59 GMT
ADD file:28329ccaf9d0f8718e6c37965272b9ac3d23fdb6d109ca304f4cdc12c515a2eb in / 
# Fri, 07 Jun 2024 03:11:59 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 21 Jun 2024 18:52:10 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:52:10 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_VERSION=24-ea+3
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='dad750c864049dba95a01fa89ad1c52c3b702ba87c3c865e5e64fa624f9e3de0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='4a5515c226db56008676461bef7443163ccfe369415342136b8d9691ecd5130b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5522c693c44935bd999ae97ef2649e6707ffdfcf11d7d226a3b78066d03f8ac1`  
		Last Modified: Fri, 07 Jun 2024 03:12:59 GMT  
		Size: 49.9 MB (49926502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224c310d8d2c96f49a742c5059029d51003313d8a587e51fed9a9aedb25695b`  
		Last Modified: Fri, 07 Jun 2024 07:39:04 GMT  
		Size: 15.7 MB (15689949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d59c090afba4336d3b534d0b7d8e2927a6a61d48261e3e666e7969c2fbe04`  
		Last Modified: Sat, 22 Jun 2024 06:16:59 GMT  
		Size: 209.7 MB (209671563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:72a507cd2880b3a277b011279bbffa7a23383a0fcc488f6c45ad51944a393d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5619526804d92395847d612412fe778447a8e69c154af248b030fd74a443ecb2`

```dockerfile
```

-	Layers:
	-	`sha256:436be0f14e3d7109b55bcab9edeee3de515bb5d9a95ebac00ca421c1f30ab44c`  
		Last Modified: Sat, 22 Jun 2024 06:16:55 GMT  
		Size: 2.3 MB (2267020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ac66e317a92ed7af63711f699c2ce03d53f8417de47da64405b627a173cca6`  
		Last Modified: Sat, 22 Jun 2024 06:16:54 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json
