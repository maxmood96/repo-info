## `openjdk:24-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:4071082b97eb3b0250a6b1404cdb582c8ca9b9ae76150e7cbb9d6733a713f8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7bd3a09cdc891617a336b97c8b6ed57829dea3e53db34d53d3449aa2b98f5241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279448550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f76728325e7c28168dd2d33191d2eca71385f0c5a8781292718fdb211dc0992`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 15 Nov 2024 23:04:32 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1616c1dbc5fc602a09f8dfc677e27bc069079f7ad8c65cc4c08d1befb3e8bf`  
		Last Modified: Mon, 09 Dec 2024 23:30:48 GMT  
		Size: 15.0 MB (14974964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad619ee2353c9cda174014564bd421442fbb352086e463046e067e69304ef1a`  
		Last Modified: Mon, 09 Dec 2024 23:30:51 GMT  
		Size: 213.2 MB (213198594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:537671bd2dd903cfd475618278238c12a42f65f39a1a134eec79e5a16ffda63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50502a8bdbd23c92a4f9e01c0281f4dc891f10c852f0ecfe7ac62cc106bd75e7`

```dockerfile
```

-	Layers:
	-	`sha256:9545efd53962246191a285738c52b6376bab5baab1dd0df96b0682dad1bda23f`  
		Last Modified: Mon, 09 Dec 2024 23:30:48 GMT  
		Size: 2.4 MB (2447760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874ab3da73c730e16cfc24ec8238a6122470583580dab521923b410b0f73e401`  
		Last Modified: Mon, 09 Dec 2024 23:30:48 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:13c61af1c0a435e8e8234eb197ba1de7eb99f9b2e7b64b4efe8d5a19bd14c319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276802569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142ef33f62c97f65da374e233b4fda3bb141612699d20bb9841821664f76ddc2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:54 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69acd795388d1f1fedcb65b1fe1cb71800f56a9beccbb0acf86fbdad421cc605`  
		Last Modified: Tue, 10 Dec 2024 01:27:38 GMT  
		Size: 15.7 MB (15659937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d65c0e8011defaf8a1fc9aa0c8e867801621afeb7c688dde8cd794dbcb9fa89`  
		Last Modified: Tue, 10 Dec 2024 01:33:15 GMT  
		Size: 211.2 MB (211162357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5acbb95bfcad547e86753a3ab87c018f26bf061eb566553c048cc7f6d646b10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08f6537b79174f11bdb8d0225d71f6407c909965f4fae9781cf7cfeb211ca89`

```dockerfile
```

-	Layers:
	-	`sha256:b79eb0773ef334488ab80231b7814a72882f173ccb5bc07f74bcb9e791e4a893`  
		Last Modified: Tue, 10 Dec 2024 01:33:09 GMT  
		Size: 2.4 MB (2446604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce9e5f1531c0c9ff1d8a415ab94aaec37bcbd47bc1c5d1688ec538b0e6649ad9`  
		Last Modified: Tue, 10 Dec 2024 01:33:08 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
