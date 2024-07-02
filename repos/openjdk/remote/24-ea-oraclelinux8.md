## `openjdk:24-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:c5cefd3739c29397169214115d3dbdef20815f1f4caa619c801d13a09923ff37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux8` - linux; amd64

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

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

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

### `openjdk:24-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:35a4c5f7658e4de08346b2290009a6c7b4f0df4249f5d38e62501a1dbcc81e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275259116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317f8d699f2060c308d59ebb59a9c2e4d9c907474bc41938b49eee1d3557a657`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:11:59 GMT
ADD file:28329ccaf9d0f8718e6c37965272b9ac3d23fdb6d109ca304f4cdc12c515a2eb in / 
# Fri, 07 Jun 2024 03:11:59 GMT
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
	-	`sha256:5522c693c44935bd999ae97ef2649e6707ffdfcf11d7d226a3b78066d03f8ac1`  
		Last Modified: Fri, 07 Jun 2024 03:12:59 GMT  
		Size: 49.9 MB (49926502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14fe16d50c54f92acd8a9f01692345e9731fbc9f75eea9480e538505c430d2a`  
		Last Modified: Tue, 02 Jul 2024 08:46:46 GMT  
		Size: 15.7 MB (15689994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82940d494fc53ad1b33664229fde9bc63b9a2bddb251416028a16ee068af74cc`  
		Last Modified: Tue, 02 Jul 2024 08:46:50 GMT  
		Size: 209.6 MB (209642620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:0affb4f1934b28c230d2a5eb1279912e270924fe2171a9f973d0f1d16f1fc483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9607c68b24742d0b0fd8a0b944acdd3d485f65f7dc9728bb7c9fe3a1f99710`

```dockerfile
```

-	Layers:
	-	`sha256:d02bad510bce4a9055261aebb3fe84563355e796263c7bff8be43e2ced73e909`  
		Last Modified: Tue, 02 Jul 2024 08:46:46 GMT  
		Size: 2.3 MB (2267020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db17a2f0980ebbe642378a2fff28463d1fca1841f59f3e6a39c49bc0defbcc48`  
		Last Modified: Tue, 02 Jul 2024 08:46:45 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json
