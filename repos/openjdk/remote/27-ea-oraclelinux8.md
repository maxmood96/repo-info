## `openjdk:27-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:0a442261e63f251cea94aa90e6787633a7eae1ff545a8072761feb6563637ecb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7d30f1259f9b4f44e479e2fc105c94486fb7a3701c33da2fe39658b3e3d284f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294834968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e052387dd76fb4f000ea305cf2f5c759dc4fe43ee78aa5091235e896642f2442`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:45:16 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:45:16 GMT
CMD ["/bin/bash"]
# Sat, 17 Jan 2026 00:24:45 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 17 Jan 2026 00:24:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 17 Jan 2026 00:24:54 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Jan 2026 00:24:54 GMT
ENV LANG=C.UTF-8
# Sat, 17 Jan 2026 00:24:54 GMT
ENV JAVA_VERSION=27-ea+4
# Sat, 17 Jan 2026 00:24:54 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 17 Jan 2026 00:24:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9c709a374865394632aa738429a90691dd8d7699af8be91820b62e8c54881b2`  
		Last Modified: Fri, 16 Jan 2026 23:45:26 GMT  
		Size: 51.5 MB (51468262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c6a89f49c5ca874e3240d5fc8b7e371ed0c003f79f864dc36f8c3b7980b2de`  
		Last Modified: Sat, 17 Jan 2026 00:25:13 GMT  
		Size: 15.0 MB (14993907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355f0ba03a5b50ef93a2e0cf54a7a8f262614aa299b05dbd9a44e758e198c76b`  
		Last Modified: Sat, 17 Jan 2026 00:25:40 GMT  
		Size: 228.4 MB (228372799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:77c962d0b1435396e8390f124d4d5ffd0c801c2a9dfe5c53f217b296d00c25cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35d847cb165b2cffafde8c90fef341b048db203070304eca4cddde50254ef73`

```dockerfile
```

-	Layers:
	-	`sha256:43e74c4113b1e41e91a4e0d1c7fd525212e596155e7be8b72087f64d2b567976`  
		Last Modified: Sat, 17 Jan 2026 00:25:12 GMT  
		Size: 2.4 MB (2448676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c75298526a38b6b1b6eba2b30f485e343d61f9a0dc7a2cb0dd6a7bf728db4a0`  
		Last Modified: Sat, 17 Jan 2026 01:24:38 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:450e405f11c48700b58caa6cdd7b7d7142c511e936c8c1f3742f165954b3705d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292209017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce5d2fdf0317e648b93b12c553ef354489ea4d5c9c03295012d355f37bbfd62`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:45:22 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:45:22 GMT
CMD ["/bin/bash"]
# Sat, 17 Jan 2026 00:16:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 17 Jan 2026 00:16:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Sat, 17 Jan 2026 00:16:29 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Jan 2026 00:16:29 GMT
ENV LANG=C.UTF-8
# Sat, 17 Jan 2026 00:16:29 GMT
ENV JAVA_VERSION=27-ea+4
# Sat, 17 Jan 2026 00:16:29 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 17 Jan 2026 00:16:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d32cf4966caecd91a10183493338f37f77a209057fd98d8c3aff049ad44e3619`  
		Last Modified: Fri, 16 Jan 2026 23:45:34 GMT  
		Size: 50.2 MB (50200257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a2f0659ba93c31316a3ddffac389bc2036efd838d0a57afa2f67f9b860afe5`  
		Last Modified: Sat, 17 Jan 2026 00:17:01 GMT  
		Size: 15.7 MB (15692755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16853f91a8891ebe44544d2e0c4d963020a8175e2e715c68b2e69c0f6e876cef`  
		Last Modified: Sat, 17 Jan 2026 00:17:09 GMT  
		Size: 226.3 MB (226316005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ac5593a922f630eaa6a0b63537169c420e427f00b927191739c2310c574cce6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a80e3de8c56331d1eeb61216484f46aba4b3fedc860c5827c6f5d7ed5d9c0b`

```dockerfile
```

-	Layers:
	-	`sha256:6c978f7c0977889046ef67a9fcda2f79416378b349ac792247ee20d4e3d9fda4`  
		Last Modified: Sat, 17 Jan 2026 00:16:49 GMT  
		Size: 2.4 MB (2447486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8819b54481bacde75a11eb9f54556a5ca06a7d231cdb3380ae2ff49ce32970ac`  
		Last Modified: Sat, 17 Jan 2026 01:24:43 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
