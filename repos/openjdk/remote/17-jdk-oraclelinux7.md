## `openjdk:17-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:2307078bf821b783cd99c1ea23960c84d53bc2ef8a1cf67f7e6b7a111ca557bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:41096f959aadb6c75959fc1fcdc937f20a23188b95e4407843c717ece663bfcb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249921083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e05d0bbeb1e4dcb71ccfbdce059b8d2583bef4d1990e0dde50096340efe1d8a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jun 2021 15:21:43 GMT
ADD file:6853efe982f87a3475099ab9aaa2ec9797afac58ee8dfc54d912b966bc3405ea in / 
# Tue, 01 Jun 2021 15:21:44 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 15:38:40 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 01 Jun 2021 15:38:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 01 Jun 2021 15:38:40 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jun 2021 15:38:41 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Jun 2021 15:38:41 GMT
ENV JAVA_VERSION=17-ea+24
# Tue, 01 Jun 2021 15:38:52 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='30b8cc8945c42ab310bca47ecfe2acdf2a0285d26dfeb6bfba46ebc5947aef6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='61d192356099180ee3beec3a22cb9e97cb810c7f55f2c870a73841c3ac61abcb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Jun 2021 15:38:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cbf629395cd4d267c366a2b3ac4cfbe6a6c5cfd5bdd8e89a7157e0901e898cf4`  
		Last Modified: Tue, 01 Jun 2021 15:22:47 GMT  
		Size: 48.3 MB (48260748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf25dc842172d49c0f45cec26c8fe86f7a083e2e5ce7a5e6d84d2b4cd2d46ba`  
		Last Modified: Tue, 01 Jun 2021 15:43:59 GMT  
		Size: 15.4 MB (15425936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed43fdc04cf1988ec7b3b16425b7caeba39aaf98dcb27422535c191ca93beac`  
		Last Modified: Tue, 01 Jun 2021 15:44:11 GMT  
		Size: 186.2 MB (186234399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7465c0108899d52514fd118dfd978b3a0a2722ad144eae7d231ee218d1c869cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247570656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc03c3c49ecc23afe260f88d85f2e832da86888dc75d779f6f44a5401d94ad34`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jun 2021 14:41:12 GMT
ADD file:3f30763d6f4fa6cd26708a9eda4872cc48b0c874b7837e0682ea4b4ed7ac5fb2 in / 
# Tue, 01 Jun 2021 14:41:12 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 14:58:49 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 01 Jun 2021 14:58:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 01 Jun 2021 14:58:50 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jun 2021 14:58:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Jun 2021 14:58:50 GMT
ENV JAVA_VERSION=17-ea+24
# Tue, 01 Jun 2021 14:59:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='30b8cc8945c42ab310bca47ecfe2acdf2a0285d26dfeb6bfba46ebc5947aef6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='61d192356099180ee3beec3a22cb9e97cb810c7f55f2c870a73841c3ac61abcb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Jun 2021 14:59:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5216e6356b12c39a03d420e358911905653d063185ac40b7250d625cfcd46024`  
		Last Modified: Tue, 01 Jun 2021 14:42:13 GMT  
		Size: 48.9 MB (48857508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0104ba284443f9b2819e0f98ad5efb21b57c2cf4d49bd3d3cbd1af4ad0ac2c85`  
		Last Modified: Tue, 01 Jun 2021 15:09:33 GMT  
		Size: 16.4 MB (16419323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32dee282fd06f40660ccd58a40f14630fb3b536f9e66b55d52fac8fd860d983`  
		Last Modified: Tue, 01 Jun 2021 15:09:48 GMT  
		Size: 182.3 MB (182293825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
