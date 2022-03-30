## `openjdk:19-oraclelinux8`

```console
$ docker pull openjdk@sha256:35898519f4d7d7ec7158efc56e363d676a35a4f4278338a19e2889ff592ca387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ecb362d8f148b961349bef2d5472d4d07952a44577a5fbd9c3e5af6d60d99c0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248837332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814c1d3e609dd1f04155a3bb7502830cabd67aaa839d570d59a61e1fa464c650`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:47 GMT
ADD file:eaa532cad071c531a759e73fd0fd381f440f180ab45b05a74314f10b0374df67 in / 
# Tue, 29 Mar 2022 18:35:47 GMT
CMD ["/bin/bash"]
# Tue, 29 Mar 2022 23:06:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 29 Mar 2022 23:06:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 29 Mar 2022 23:06:26 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:06:26 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 23:06:26 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 23:06:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 23:06:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4430e06691f65e516df7d62db0ee5393acea9ade644cc6bc620efef0956dd17`  
		Last Modified: Tue, 29 Mar 2022 18:36:53 GMT  
		Size: 42.1 MB (42113609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ce5342b806de618f4fa582eca53ecee5a73ef976daa060d249227e1927d814`  
		Last Modified: Tue, 29 Mar 2022 23:18:03 GMT  
		Size: 13.5 MB (13524329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7446b29560b0ed17c617465f99ded7015717d0de03c9320996facda3873d86a`  
		Last Modified: Tue, 29 Mar 2022 23:18:15 GMT  
		Size: 193.2 MB (193199394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dd228d77cf95207f66285ab17193f1b7f3648a58a1797ccca7157651d1e3ddd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248396948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea611c0a4982c831dfc60c4fff47d593d4cb946089876592ca83c75c5b922494`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 08:57:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 30 Mar 2022 08:57:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 30 Mar 2022 08:57:30 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:57:31 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:57:32 GMT
ENV JAVA_VERSION=19-ea+15
# Wed, 30 Mar 2022 08:57:46 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Mar 2022 08:57:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200eb5167ed838a74239544d81e10c3d37a59ea571f23c1d6ed6e0c207cf997`  
		Last Modified: Wed, 30 Mar 2022 09:18:31 GMT  
		Size: 14.3 MB (14293802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a278a18350dc35328c5632dbd00c979a68e9feb2b19a3c119b20f48e7febe419`  
		Last Modified: Wed, 30 Mar 2022 09:18:45 GMT  
		Size: 192.1 MB (192084048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
