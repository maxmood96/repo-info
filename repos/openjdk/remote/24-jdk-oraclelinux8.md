## `openjdk:24-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:1efd87480a132e8f4a2a11bb3f42b971298bdd570e492ca1d5d9f15c063d85b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:89a231cbd934309b58d4339dcae52566b0f2ce5f22311a962f135d0b00a8bc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279231148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886a2d7dd8603efbff8c1b23a3001203e2e17bff6b1ee7b12c05bb9c2a795632`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 10 Oct 2024 22:15:38 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 10 Oct 2024 22:15:38 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 25 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c67029681a2f1c745c3a73366080881b2d349b4ffb9ce6a4e1e4b2c423555c5c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='3850e8de3f5cc9a22fabc0963a04d6205a9f242cf2cfc0d67a4399a54deb725e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ccec4de1d50efaab175e979c24b513dacdec266a6a00f442167c614564b83ef0`  
		Last Modified: Fri, 11 Oct 2024 00:11:24 GMT  
		Size: 51.3 MB (51295624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0266b942f64992e96fa24d9fc8cd61705a8404a8df4182aa76cfaaee7d455165`  
		Last Modified: Fri, 25 Oct 2024 22:57:22 GMT  
		Size: 15.0 MB (15036729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e3abdb61a6978684408fda91a055e761227850b6989baeb6164639d00cf76`  
		Last Modified: Fri, 25 Oct 2024 22:57:24 GMT  
		Size: 212.9 MB (212898795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b333c29345704cc611a9d5ccfd24bb22d418e62615a1d1457d1ea15b94905334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2441837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff39611806b8f355d9e5cb2f92e6c1d9f643b7c06dce1384d40b7952adc731e9`

```dockerfile
```

-	Layers:
	-	`sha256:648f8bd0e021721fc930d5dae5c5f219c8bbac3dd7154d8bf42fadfa150532db`  
		Last Modified: Fri, 25 Oct 2024 22:57:22 GMT  
		Size: 2.4 MB (2425799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6015d492fde7b7e754503555fbee6d57fbacf2847fe54bb9144866caf1f99909`  
		Last Modified: Fri, 25 Oct 2024 22:57:22 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:149ef1ffc8ea2e9d9fed4ee38736980cdc83f6c1edca8c15a17ded6324144147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.5 MB (276494137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d923fe0eb858164ed5444ae3e143b70cdb7c10d123f536473068e04b059033cf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 10 Oct 2024 22:16:27 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 10 Oct 2024 22:16:27 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 25 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c67029681a2f1c745c3a73366080881b2d349b4ffb9ce6a4e1e4b2c423555c5c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='3850e8de3f5cc9a22fabc0963a04d6205a9f242cf2cfc0d67a4399a54deb725e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5aa1f5d85d147a7c16d0057c3fc21b1ae3d482ca5ede955163a95cc540b4244e`  
		Last Modified: Fri, 11 Oct 2024 00:11:55 GMT  
		Size: 50.0 MB (50004038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a41cafa4139b00f914d4c1b7945d43692861a8a657666a91c7e8b3de502e15`  
		Last Modified: Fri, 25 Oct 2024 23:00:03 GMT  
		Size: 15.7 MB (15706034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da764e94b89c978c04d4b705a2252ba6b6c76ccc9c5720139c27e7877dae2e69`  
		Last Modified: Fri, 25 Oct 2024 23:00:07 GMT  
		Size: 210.8 MB (210784065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:12709c472cccaf2d38b8265c61969126b06ec666a19f29f6ce1e420daf1d54e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b391e29c9e2e30d2682a937145d0c10f0ff42cb1fd90b4b4e480c98497e0884`

```dockerfile
```

-	Layers:
	-	`sha256:a7567a05258bc2dc624c5f50bc75953b6046c43c168a228ce16a6c5adf86972e`  
		Last Modified: Fri, 25 Oct 2024 23:00:03 GMT  
		Size: 2.4 MB (2424021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26750dcc1c44b9d40375c0e73a86eb35a69e94370e14123cbff4a3b0df0a50bd`  
		Last Modified: Fri, 25 Oct 2024 23:00:02 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
