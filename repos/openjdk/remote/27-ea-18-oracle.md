## `openjdk:27-ea-18-oracle`

```console
$ docker pull openjdk@sha256:419034e5ae76112ddc1a4f254b77f6d3bd176ed03c6544f8b46409a90c99a24a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-18-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:22c147d32bbc2b39aacd6e6dc5a96759fbe948d53c9e969a00a1f006ad9fac44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309370057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1537ecf88caef69718c06dcd92978a95e4bfc646e3cd877142efe6e58e44b5cc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:51 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:51 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 17:40:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 17:40:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 20 Apr 2026 17:40:27 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:40:27 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 17:40:27 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 17:40:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Apr 2026 17:40:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59f98efa373e352e94c44103a934ba322d4b0d08d660faa4e8642d56b03dd4fe`  
		Last Modified: Fri, 17 Apr 2026 23:39:02 GMT  
		Size: 43.1 MB (43074999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b5649a316378f3896479638cad71e20c70d00f3f4b8c772db1597d92ed878f`  
		Last Modified: Mon, 20 Apr 2026 17:40:50 GMT  
		Size: 37.7 MB (37678468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af511bffbd28249e2515a4f49a7eb97c5efb49d493affac1035c7695605564c3`  
		Last Modified: Mon, 20 Apr 2026 17:40:54 GMT  
		Size: 228.6 MB (228616590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:36e0d6a1d62c1f2ca781e82f95d58726fe0fd931d72a0b77334fe22106a1f424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50d8232d312f9e2a3f7523a178cb9bdda5941821c3fbf722da5d30c184a97cc`

```dockerfile
```

-	Layers:
	-	`sha256:1a705140ab407a262cc9da254d0b84deb59d7101d1a7356065042d8e81b44c94`  
		Last Modified: Mon, 20 Apr 2026 17:40:48 GMT  
		Size: 2.4 MB (2367767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e0c95ed2865e1dfc10173a5973f80064d561876618f0190d12635c136922d9c`  
		Last Modified: Mon, 20 Apr 2026 17:40:48 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-18-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0757e597a2a78d31a146d784af0e38b193e6258bc14121569cc40e6ac75986c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305757016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2190481b9842770970601526afb90ed856b9789a43abf58c721e4885d588e8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:18 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 17:40:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Apr 2026 17:40:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 20 Apr 2026 17:40:41 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:40:41 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 17:40:41 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 17:40:41 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Apr 2026 17:40:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b998cd5b08c06e4f5efb16eb3e3a01c0e5c56b8b33a94e55d1a919f120c4e0ab`  
		Last Modified: Fri, 17 Apr 2026 23:38:28 GMT  
		Size: 41.5 MB (41476716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786949ac4b2715c546f225d484e4aeaf2759471650f7eb32da523c3142aace26`  
		Last Modified: Mon, 20 Apr 2026 17:41:05 GMT  
		Size: 37.7 MB (37697821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f3f1cbf6d282a2301f084810e9a8963706e1795921879010583d03e9af052f`  
		Last Modified: Mon, 20 Apr 2026 17:41:11 GMT  
		Size: 226.6 MB (226582479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d001a0c62ff05b7f8cfb6bad9c04541c53237ecb44db4f611742ca11821341f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa15f88d4a41940f7307b8ccfe014134f07f251e995e53785a058447027376ad`

```dockerfile
```

-	Layers:
	-	`sha256:4dbad2858793014b456f1cb79d1290bcd16984650011e78ecdc759bf8953fc79`  
		Last Modified: Mon, 20 Apr 2026 17:41:03 GMT  
		Size: 2.4 MB (2367295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7057e04b4beac66e5d4777adf13df7ce4123e83124fb76ee8d1067f96add156`  
		Last Modified: Mon, 20 Apr 2026 17:41:03 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
