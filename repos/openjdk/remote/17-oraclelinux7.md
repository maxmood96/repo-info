## `openjdk:17-oraclelinux7`

```console
$ docker pull openjdk@sha256:db323a0e23a463900bd422e71383d8c3b2a4cdc34d36036f35c18795cbbdd906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:f9d1be36f4e06d23b57ce397a70cb79e229a6fc7dd52fb0649efd7e452d9b32b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249916548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070809a921d7b01dd7e511d94123bcf1f94c5cb5cafd6b6a842c807eb3af904a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 May 2021 00:10:37 GMT
ADD file:7532c4c6850a2e95d341f39828f60573728d50ba1fc6264ed19bb36eb4b24d1c in / 
# Thu, 06 May 2021 00:10:37 GMT
CMD ["/bin/bash"]
# Thu, 06 May 2021 00:27:43 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 06 May 2021 00:27:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 06 May 2021 00:27:43 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 00:27:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 27 May 2021 23:30:17 GMT
ENV JAVA_VERSION=17-ea+24
# Thu, 27 May 2021 23:30:27 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='30b8cc8945c42ab310bca47ecfe2acdf2a0285d26dfeb6bfba46ebc5947aef6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='61d192356099180ee3beec3a22cb9e97cb810c7f55f2c870a73841c3ac61abcb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 27 May 2021 23:30:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:22f7711cf64307564c3293688489295d9458bac2ca47cd6576382cfb75c9d2b9`  
		Last Modified: Thu, 06 May 2021 00:11:49 GMT  
		Size: 48.3 MB (48258661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87180291cc45c5c610f6909495ba989b36ef14701a331d8689e264f9d7c23796`  
		Last Modified: Thu, 06 May 2021 00:32:56 GMT  
		Size: 15.4 MB (15423518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef5144168862fa2407c34db2e97c880b314282d8628167000a3b9ee30ee62ba`  
		Last Modified: Thu, 27 May 2021 23:36:11 GMT  
		Size: 186.2 MB (186234369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9df52970da98d26de77f3949355e8a20e00e49fe18b15ec045f7fd940729e826
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247605426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdac6281660f19c29786b347edf5037f1579a3d9007b922c37a1e07044e6557`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 May 2021 00:13:32 GMT
ADD file:57303578fa11d312dcc51eb7aef116316c2b60e48b533a1471e2f2ba915ee46a in / 
# Thu, 06 May 2021 00:13:35 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 08:37:58 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 27 May 2021 08:37:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 27 May 2021 08:37:58 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 08:37:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 May 2021 05:19:23 GMT
ENV JAVA_VERSION=17-ea+24
# Fri, 28 May 2021 05:19:47 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='30b8cc8945c42ab310bca47ecfe2acdf2a0285d26dfeb6bfba46ebc5947aef6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='61d192356099180ee3beec3a22cb9e97cb810c7f55f2c870a73841c3ac61abcb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 28 May 2021 05:19:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d575bf1166e11ab792c567b7bdfab507a987976bc375994e3516987e6e1e600`  
		Last Modified: Thu, 06 May 2021 00:14:38 GMT  
		Size: 48.9 MB (48869643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7409ca04ff6a5e0e0929209eb0102acb783813b9f0319a3c76480ea957b961`  
		Last Modified: Thu, 27 May 2021 08:53:20 GMT  
		Size: 16.4 MB (16442064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fcca64aca724d5b7f69de15540bfbc39ee5f7bcc8cbefec9f1d0c85016011c`  
		Last Modified: Fri, 28 May 2021 05:31:55 GMT  
		Size: 182.3 MB (182293719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
