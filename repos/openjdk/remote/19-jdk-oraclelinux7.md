## `openjdk:19-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:87269b33051309e17b2ae4e34e540e8ebeff44d79f3682d2db73335444b68806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:01be39a55439bc72ea93446d6c3804366fdb46bd7f782e750df969cb452d0e2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256199633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3c27925face5aceac8a99b685b3dff62da5de7615ca8967416463bd4da48a9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Tue, 29 Mar 2022 23:06:58 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 29 Mar 2022 23:06:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 29 Mar 2022 23:06:58 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:06:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Mar 2022 23:06:59 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 23:07:08 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 23:07:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80558a30268385e2f78e93d6dcd977e92f7c76354c6ca130dd3ac4cb4b90f212`  
		Last Modified: Tue, 29 Mar 2022 23:18:51 GMT  
		Size: 14.2 MB (14239096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4c6091f11318b93d8e9187c390bd28376ef225c16c7f6c7c1735eb72b63f16`  
		Last Modified: Tue, 29 Mar 2022 23:19:03 GMT  
		Size: 193.2 MB (193203054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7a5302fe80a8667ed87dd02971e31a3ff94347c6ab6bc091e253e02398ca1c62
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256676509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa6a100e909a6069a6ad57635ffb9abea7bde51c3a3262658dd8dd06d46df66`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:34 GMT
ADD file:90c167a56275b374fb1719a6f499aea26290701a7baef901065a814af0e9e7c0 in / 
# Tue, 29 Mar 2022 18:27:35 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 08:58:30 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 30 Mar 2022 08:58:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 30 Mar 2022 08:58:32 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:58:33 GMT
ENV LANG=en_US.UTF-8
# Wed, 30 Mar 2022 08:58:34 GMT
ENV JAVA_VERSION=19-ea+15
# Wed, 30 Mar 2022 08:58:53 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Mar 2022 08:58:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8909fcd1d3ed60203b3ef173f01925cfd334ae0874f19f3d19876d262428e7e`  
		Last Modified: Tue, 29 Mar 2022 18:29:06 GMT  
		Size: 49.3 MB (49339436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053940d29ef2ce62ec889516ac542e5db9ba471201782b15c2890f3f0be5b92c`  
		Last Modified: Wed, 30 Mar 2022 09:19:27 GMT  
		Size: 15.3 MB (15253020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d0b0a5fb405488add38e10cef1006708bc72a28dd4d9afe5bbd4430a693e0a`  
		Last Modified: Wed, 30 Mar 2022 09:19:42 GMT  
		Size: 192.1 MB (192084053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
