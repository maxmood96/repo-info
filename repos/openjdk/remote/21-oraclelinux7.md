## `openjdk:21-oraclelinux7`

```console
$ docker pull openjdk@sha256:104fc118c6a0176bca8aa2cc51faade28ab8418a5e22073c268f1f198e2cf493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b79910ac6e776a50e9493b90044397bde21ad6b7d399309cbdc17370590c9b5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263154640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db69f8d51a28059e6d53e18756e9ff526b98b1bee92f49ba1d021dd90cd596`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:56 GMT
ADD file:3853624d773c4bf6fc1464ca06bd07366109fab78072fcab59075073a5da6525 in / 
# Wed, 07 Dec 2022 01:51:56 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:27:36 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Dec 2022 00:33:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 14 Dec 2022 00:33:09 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2022 00:33:09 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jan 2023 00:28:42 GMT
ENV JAVA_VERSION=21-ea+5
# Fri, 13 Jan 2023 00:28:57 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/5/GPL/openjdk-21-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2dba614859e77c261a7a30b3019b05dc1e7b5651d065de741426ea540a4ba264'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/5/GPL/openjdk-21-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='621f8196ad96481076d3730496db77ff154976c81798fc7ff3064cd1deeacdb8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Jan 2023 00:28:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d26998a7c52d2b84e7927f97651d1d703a805c8e4d3f658a03138721f5a5dd44`  
		Last Modified: Wed, 07 Dec 2022 01:53:46 GMT  
		Size: 49.8 MB (49818482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13169d9a90276a4f8190fd6edcdf29f7dd28e38d5919cd950939ffe59628af48`  
		Last Modified: Wed, 07 Dec 2022 02:31:28 GMT  
		Size: 14.2 MB (14217950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e1cf1a2e13e5af66841914b7b619512b6ab41ce676654b025e861cbae6db11`  
		Last Modified: Fri, 13 Jan 2023 00:35:54 GMT  
		Size: 199.1 MB (199118208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fe5cda3ab4dbc2fb0a26a609ac8a84a8a1bf14b4ceedd878e28da745723f9010
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263230495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e1dac598782a9b5e1b9b1b524cce91582018942bf5bda5b7033f3c6d530c1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 02:11:05 GMT
ADD file:811a8ff51774a6c04c874e49a9bf2f3ef1a447402946740d2128a81809dc1a22 in / 
# Wed, 07 Dec 2022 02:11:06 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:53:45 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Dec 2022 00:53:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 14 Dec 2022 00:53:44 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2022 00:53:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 Jan 2023 00:48:25 GMT
ENV JAVA_VERSION=21-ea+5
# Fri, 13 Jan 2023 00:48:37 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/5/GPL/openjdk-21-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2dba614859e77c261a7a30b3019b05dc1e7b5651d065de741426ea540a4ba264'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/5/GPL/openjdk-21-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='621f8196ad96481076d3730496db77ff154976c81798fc7ff3064cd1deeacdb8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Jan 2023 00:48:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81ac616e14aefb691216238b73174a9efd12a5e52bc4e297c5c1cf38561e5aca`  
		Last Modified: Wed, 07 Dec 2022 02:12:40 GMT  
		Size: 50.4 MB (50386463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804baa16591d133fbd09bac6a9223716dbf71fec46b68197f09b7ad836238810`  
		Last Modified: Wed, 07 Dec 2022 02:57:50 GMT  
		Size: 15.3 MB (15268238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad51c16f2c3f3fd06faa366f306101923adfc49a094b1b121865b2d43498567`  
		Last Modified: Fri, 13 Jan 2023 00:55:38 GMT  
		Size: 197.6 MB (197575794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
