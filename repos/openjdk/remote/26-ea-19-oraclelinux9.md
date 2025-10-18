## `openjdk:26-ea-19-oraclelinux9`

```console
$ docker pull openjdk@sha256:e010c782d6b9367b6219a5c77818c9ea6ceb9cbda54c74ba33a4ac09e1a5129e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-19-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:5fb2da0a10211a297ab8b5483ebd4334e709768bd1648a513a08fb3b356b3f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313280263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89624cd3a2e9cf96aa07a2cf475c56e7661b66a498c0c79212136ba1cbaf1d0e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 11 Oct 2025 00:48:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd625a07e8742f44278506ab443c0c89b9598f006893e2f1f1b2217a3577aa7`  
		Last Modified: Sat, 18 Oct 2025 00:13:51 GMT  
		Size: 38.1 MB (38087600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5e907e844d79264a1acbe68bc3d5b496bd4ad8a028324d1cc8034a393c04e1`  
		Last Modified: Sat, 18 Oct 2025 00:57:39 GMT  
		Size: 225.7 MB (225696158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-19-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:595c34be93ac5529113c3afe26f627f1e248eb5b41fabe0ece41e7d4647c4aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783a32dc2859825e12ece333cb37d90f75eeddb083830f7c7bc1d4becff79b31`

```dockerfile
```

-	Layers:
	-	`sha256:fc66eceade7e115e441eb8b39127e7818d6d6c81cb9ca080e737d9881f0d040f`  
		Last Modified: Sat, 18 Oct 2025 00:23:21 GMT  
		Size: 3.6 MB (3640745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f349cb4e56aa889ccc258d2f90a532185ccb677ec61c07061678e6126a6593`  
		Last Modified: Sat, 18 Oct 2025 00:23:22 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-19-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8bfef00dc2b305c90305b060c4d561cf799e895003fd78a0b053882fe8b4beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310130898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58474323468fc6d992061851f1e22a4decb1eb946e786fffa0e7a8d96d40b95`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 11 Oct 2025 00:48:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["/bin/bash"]
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0245494e167b25dc8a27d614ef806cd4e1aaf7d89b506e17a18faeb609c9d43`  
		Last Modified: Sat, 18 Oct 2025 00:14:39 GMT  
		Size: 38.5 MB (38490829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ecd072449d59f4b1265bcdad051a7f4a219a11b057140ccc1943486b0cf4d5`  
		Last Modified: Sat, 18 Oct 2025 00:14:30 GMT  
		Size: 223.6 MB (223553168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-19-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:e6138c7899deb879df517b9981c0bdb8601b8e6702d462182fcc00f9adb73ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c788a7d362aba62ed46ec9fbc80f3c2fe49fafd4992cd9c626f033dbb1303`

```dockerfile
```

-	Layers:
	-	`sha256:6af1f6b1d32855a34a53a9c7feeff5b22976c412d9bc55eb582bb26e2e129a58`  
		Last Modified: Sat, 18 Oct 2025 00:23:27 GMT  
		Size: 3.6 MB (3638507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75cca1a4902a8c2bd5360e308fb835e24d9c0e8d8be9d497c3c1dd0864467df`  
		Last Modified: Sat, 18 Oct 2025 00:23:27 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
