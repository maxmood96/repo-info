## `openjdk:18-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:c40029c03b840798dd9f17ab8df36661427d2314ce5211aa5b2601cba007f3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:f93ba76d09d9af1f45c49f64ba24a9774730df0ff5e2f1dba33e037ebc215b10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242978287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393b44d30d32a63b9ce158ee595ba4e8daab792eeaac952fe79b7cb32ee081c7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Aug 2021 19:20:55 GMT
ADD file:ab982d6f37710c434f7ef9650c722d3c6333906cbb9344bf91e79068088bcc69 in / 
# Thu, 12 Aug 2021 19:20:56 GMT
CMD ["/bin/bash"]
# Thu, 12 Aug 2021 19:37:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 12 Aug 2021 19:37:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 12 Aug 2021 19:37:56 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Aug 2021 19:37:57 GMT
ENV LANG=C.UTF-8
# Tue, 14 Sep 2021 01:31:40 GMT
ENV JAVA_VERSION=18-ea+14
# Tue, 14 Sep 2021 01:31:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/14/GPL/openjdk-18-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='6aee5779ac7488dbd6988658662ca683704ac98cee6b8dde8df3ddffac76142e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/14/GPL/openjdk-18-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='88a106afe903b8f5d552ceae108294d8b36cbc0656a744f84525ccae542c5029'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 14 Sep 2021 01:31:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c67289558ae5eb060942db5bf46d182448587a87e21c680a0486b147d4b9a0b4`  
		Last Modified: Thu, 12 Aug 2021 19:22:09 GMT  
		Size: 42.2 MB (42158041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12787f1f3888c64bfc9e779a9705ecc45ae1a60b3757074b6f16cf1d8553cac8`  
		Last Modified: Thu, 12 Aug 2021 19:43:29 GMT  
		Size: 13.4 MB (13373335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be395cd464c39a1f0010e5c9283e5e41aa3628c3da79e75e247dd6e9fee5834`  
		Last Modified: Tue, 14 Sep 2021 01:38:58 GMT  
		Size: 187.4 MB (187446911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8c4d52a61e4438932cc60bc7617c3e3c67a7dd2f5afc66f78a663a08acdd1664
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242356682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10827a6e963efeadb163a99365d9a343befd8d053967714b659232c8983136cf`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Aug 2021 02:58:07 GMT
ADD file:3a5bc6124c8d78438880a95007baec403400e29f09317331e09ba7d65a0aaff0 in / 
# Fri, 13 Aug 2021 02:58:08 GMT
CMD ["/bin/bash"]
# Fri, 13 Aug 2021 05:39:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 13 Aug 2021 05:39:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 13 Aug 2021 05:39:59 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Aug 2021 05:39:59 GMT
ENV LANG=C.UTF-8
# Sat, 04 Sep 2021 01:46:46 GMT
ENV JAVA_VERSION=18-ea+13
# Sat, 04 Sep 2021 01:47:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/13/GPL/openjdk-18-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='396584ea555ad439176473f4e22c146817290a8eeaad02e3072dfb398ba786e0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/13/GPL/openjdk-18-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='4601ee9811daa3bf282753e1fa6b8caffd869d0e56c9acfe95e1670bc580ed34'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Sep 2021 01:47:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:757bb77daa0e625f3aaa9e22fcc2dda31fa9d6e50f482403ab7be9f030a1a19f`  
		Last Modified: Fri, 13 Aug 2021 02:59:14 GMT  
		Size: 42.1 MB (42054178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d701f3bd7e43b3fb331b6b15362e9dbd4abd27a5c29f2301d998cc782a0ba1`  
		Last Modified: Fri, 13 Aug 2021 05:50:47 GMT  
		Size: 14.2 MB (14163676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfd2d8d2056af20a227dc8ba7ac6aaa39a29bad3bbb2e0dbdba0cad5ad6c833`  
		Last Modified: Sat, 04 Sep 2021 02:01:16 GMT  
		Size: 186.1 MB (186138828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
