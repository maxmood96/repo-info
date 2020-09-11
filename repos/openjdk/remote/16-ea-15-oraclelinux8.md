## `openjdk:16-ea-15-oraclelinux8`

```console
$ docker pull openjdk@sha256:5659954e56d9e78ad6dd6d6b1fc0ae9d6245fc10195b47688c0d252972fa2d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-15-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ef8485d2763912e731a131e65a65bcdb856528d17e4075996a72ac34c43687d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263283166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9f03bcb7d7da66acdc1a6610ee0357be5acf7e179deaef389d81bed63bd05c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 11 Sep 2020 09:49:59 GMT
ADD file:50f1210cda2b0463fc72e0e56a1636cc26b6685c08c7e2cabf7fc2329b04537b in / 
# Fri, 11 Sep 2020 09:49:59 GMT
CMD ["/bin/bash"]
# Fri, 11 Sep 2020 10:23:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 11 Sep 2020 10:23:52 GMT
ENV LANG=C.UTF-8
# Fri, 11 Sep 2020 10:23:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 11 Sep 2020 10:23:52 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 22:31:27 GMT
ENV JAVA_VERSION=16-ea+15
# Fri, 11 Sep 2020 22:32:24 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-aarch64_bin.tar.gz; 			downloadSha256=c0fda06a69e492907fe85d1e151e34747e0fce3a2221a70e5dcffd8df048d1db; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-x64_bin.tar.gz; 			downloadSha256=7e6eccd3ac82ce7c007b30a8cde4d849c61612be5353de130690646814f5b9f9; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Sep 2020 22:32:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4374a5c9a09aec3eb7169ecd4f7ff91fedce7aeb23b479e5f83af47ec91c5d7c`  
		Last Modified: Fri, 11 Sep 2020 09:51:53 GMT  
		Size: 53.2 MB (53194134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628f382586998761d4d6eaf3d2f5d56829c3099ff15ff17f86c2767c85530a14`  
		Last Modified: Fri, 11 Sep 2020 10:28:24 GMT  
		Size: 13.4 MB (13409452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cf7275d491e65ed1e0a1e6b82c38cbacd94eba5f3ae6d7d9a8743652a91044`  
		Last Modified: Fri, 11 Sep 2020 22:37:12 GMT  
		Size: 196.7 MB (196679580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-15-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2e6860907d0c3412893b069551d2ae9177f4fa149a6c7cc9eb097b5c2f1c861e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242989080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a11140b62843509653c04dc7d7cc17e46cdb3533961bee17ef6287b6789bb5b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 11 Sep 2020 06:39:42 GMT
ADD file:c8745918ce90d90daefed5ea00db8b400158109f53a85988975f96ce7084c609 in / 
# Fri, 11 Sep 2020 06:39:46 GMT
CMD ["/bin/bash"]
# Fri, 11 Sep 2020 07:09:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 11 Sep 2020 07:09:38 GMT
ENV LANG=C.UTF-8
# Fri, 11 Sep 2020 07:09:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 11 Sep 2020 07:09:39 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 23:03:44 GMT
ENV JAVA_VERSION=16-ea+15
# Fri, 11 Sep 2020 23:04:28 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-aarch64_bin.tar.gz; 			downloadSha256=c0fda06a69e492907fe85d1e151e34747e0fce3a2221a70e5dcffd8df048d1db; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-x64_bin.tar.gz; 			downloadSha256=7e6eccd3ac82ce7c007b30a8cde4d849c61612be5353de130690646814f5b9f9; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Sep 2020 23:04:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b0a89fc27ec40345cd34fac22c2caa5adb9d10c730a6bd900435007be8e8ac80`  
		Last Modified: Fri, 11 Sep 2020 06:41:50 GMT  
		Size: 53.3 MB (53291835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54565c8f5569913127216a9630522b7177b23429e528cdd38041680808117936`  
		Last Modified: Fri, 11 Sep 2020 07:13:47 GMT  
		Size: 14.3 MB (14311816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1178dca9cbd0693b51fcdcab3af84b63489207e7a49e44f78291389ee407570c`  
		Last Modified: Fri, 11 Sep 2020 23:08:49 GMT  
		Size: 175.4 MB (175385429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
