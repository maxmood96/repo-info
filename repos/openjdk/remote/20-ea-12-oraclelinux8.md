## `openjdk:20-ea-12-oraclelinux8`

```console
$ docker pull openjdk@sha256:6c782b56e0cfc1132ab1cedfab6e96922d2b8778a9beaf06468edba1de00e088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-12-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:230a0cc902d5f815f4f17792fd11dc0d33d3ef61af3d249eedd6cb5043f9b34f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (249005670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ccf8d57ddca645604e148c25afa587b02c98c0eae27a677a25480b929c93d0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Aug 2022 21:25:57 GMT
ADD file:923c2af16ef366fe4e85b8ba8979b8a31da0cdbc606c08148463849bf66c395b in / 
# Fri, 26 Aug 2022 21:25:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 21:43:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 26 Aug 2022 21:43:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 26 Aug 2022 21:43:53 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 21:43:53 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 21:43:53 GMT
ENV JAVA_VERSION=20-ea+12
# Fri, 26 Aug 2022 21:44:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='c15feea1a5fa60e2d919fe6f1d30f0c1ae790c975e58e9e5e3681523bef0fbb7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='30ddc30c2c4a6058212c829ca65f18bf21f7b97a88d08eb084840a355372c865'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Aug 2022 21:44:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee4ca39e1b6ea333d785f1cbc6b64b874a4f16f1200dad9e17d2015c925d1d57`  
		Last Modified: Fri, 26 Aug 2022 21:27:39 GMT  
		Size: 39.5 MB (39520501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f806f92441177162c8149eb36189b0eae2287007a7837b949d24fb72102008`  
		Last Modified: Fri, 26 Aug 2022 21:49:14 GMT  
		Size: 12.2 MB (12237733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b96762c18264db36ed95260f9dce2307afffa258c39ffd529d369081012094c`  
		Last Modified: Fri, 26 Aug 2022 21:49:27 GMT  
		Size: 197.2 MB (197247436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-12-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0987317e654a0197c1013724c7cb8455906a943d0c92d1bc63099ca9d94d59d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247163792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b04aa202476f86dbe63cc5ca7bbe8a6d9c3a759e286c1d2997790073115c05`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Aug 2022 22:19:36 GMT
ADD file:e1881d48dc095ac87c2423fc55d6becc2c53c4acd328b61ff6977a76c99c63d5 in / 
# Fri, 26 Aug 2022 22:19:36 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 22:43:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 26 Aug 2022 22:43:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 26 Aug 2022 22:43:37 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 22:43:38 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 22:43:39 GMT
ENV JAVA_VERSION=20-ea+12
# Fri, 26 Aug 2022 22:43:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='c15feea1a5fa60e2d919fe6f1d30f0c1ae790c975e58e9e5e3681523bef0fbb7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/12/GPL/openjdk-20-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='30ddc30c2c4a6058212c829ca65f18bf21f7b97a88d08eb084840a355372c865'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Aug 2022 22:43:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:603d7d3fec0e313f107fe00bade46982a9180dc340b6b25cd3d0f202b702c09f`  
		Last Modified: Fri, 26 Aug 2022 22:21:24 GMT  
		Size: 38.3 MB (38321055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03886fdd651d5bc2cd1f8174b66f8cb3a2d3d8ae936a84afc5d75e863afbb50c`  
		Last Modified: Fri, 26 Aug 2022 22:51:45 GMT  
		Size: 13.0 MB (13042043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df05f078a1844564d434699364cd0a5b67bf886f9bcf4573925c397469994ff9`  
		Last Modified: Fri, 26 Aug 2022 22:52:00 GMT  
		Size: 195.8 MB (195800694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
