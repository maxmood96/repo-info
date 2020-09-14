## `openjdk:16-ea-15-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:d3a67a2faff9a8e4677a579205d02fb69272e6339d9f63bb25d989f0103ed9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-15-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:0aaae979d688acfaaade5aca683c4a867d49aeb43763d4732c4b229bcce9a1d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264335540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c6ff3936c8406bf053fb62b5a22a0451a10657105e4745182a12b04b6b0e2f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 14 Sep 2020 18:33:21 GMT
ADD file:8011e31575cbf4b8ebb243821b300ba24330e02cab925024aa98f4ce27997846 in / 
# Mon, 14 Sep 2020 18:33:21 GMT
CMD ["/bin/bash"]
# Mon, 14 Sep 2020 18:50:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 14 Sep 2020 18:50:46 GMT
ENV LANG=C.UTF-8
# Mon, 14 Sep 2020 18:50:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 14 Sep 2020 18:50:47 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Sep 2020 18:50:47 GMT
ENV JAVA_VERSION=16-ea+15
# Mon, 14 Sep 2020 18:51:26 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-aarch64_bin.tar.gz; 			downloadSha256=c0fda06a69e492907fe85d1e151e34747e0fce3a2221a70e5dcffd8df048d1db; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/15/GPL/openjdk-16-ea+15_linux-x64_bin.tar.gz; 			downloadSha256=7e6eccd3ac82ce7c007b30a8cde4d849c61612be5353de130690646814f5b9f9; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Sep 2020 18:51:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79701ada7495177c292979fd69d41eee91dc93ef0feea5ff95bb453f4ab7a1c5`  
		Last Modified: Mon, 14 Sep 2020 18:35:00 GMT  
		Size: 54.2 MB (54164063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffa6cd00cf525ae203ffe0f93764b5d175c46f27a7e15bb0da88efb308e5292`  
		Last Modified: Mon, 14 Sep 2020 18:55:41 GMT  
		Size: 13.5 MB (13491747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df66d4ae3f808f3e52b901fc18e1611b78dd0bb73469727cd4bfce720377b8f`  
		Last Modified: Mon, 14 Sep 2020 18:55:56 GMT  
		Size: 196.7 MB (196679730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-15-jdk-oraclelinux8` - linux; arm64 variant v8

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
