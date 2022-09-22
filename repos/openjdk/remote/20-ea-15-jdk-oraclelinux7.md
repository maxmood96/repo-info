## `openjdk:20-ea-15-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:9e1dc9bc79cb64416354d8a0467af3a11c2a30b2403335e69ad986f49d0db848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-15-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:a350cda25c1b2624771c7ac27a2b68a7c83821e56ca0942184bf754cde2479bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260881338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7625e83b9ae757c8f981435d3af712bddeef5eaa4fa5c81dbd75c98a0148c5d1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Sep 2022 18:21:00 GMT
ADD file:bc2c7ba728e9e4bfc9aa5e6072db4cbab3cadbd76aff485b6afd233dcdfbdb1e in / 
# Thu, 22 Sep 2022 18:21:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 18:37:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 22 Sep 2022 18:37:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 22 Sep 2022 18:37:37 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Sep 2022 18:37:37 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Sep 2022 18:37:37 GMT
ENV JAVA_VERSION=20-ea+15
# Thu, 22 Sep 2022 18:37:48 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/15/GPL/openjdk-20-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='2ee417bc5d9f36c634a5e004c201967b70b6b3a5382147d74406cc9b015eac97'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/15/GPL/openjdk-20-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ec219647905af892891d6fd018538043bf19cfae2a40df439b9fde070476681'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 22 Sep 2022 18:37:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a2a00260331c858dbb0d8dae185769162dbb3e7cb3342d52798d837e7a156c45`  
		Last Modified: Thu, 22 Sep 2022 18:21:50 GMT  
		Size: 49.8 MB (49796793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00f9fe80a003e345fd0fbed09df87921267e2893a69170bde00961786a40f31`  
		Last Modified: Thu, 22 Sep 2022 18:40:40 GMT  
		Size: 14.2 MB (14223074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0cd0602271639e2f76a0a3776bb4e476b93ecfba5494ba92e555aaf9fc9cba`  
		Last Modified: Thu, 22 Sep 2022 18:40:53 GMT  
		Size: 196.9 MB (196861471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-15-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:791cb03a50d831497114250c67062d810c852b7f7ed4db82a32d4909c9cdadc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261030466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6293297b74b6adbcf6b6f9e73f6de780654bb06e5b8c3948d6954c9225b6054a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Sep 2022 18:41:04 GMT
ADD file:fd12a0d7821d135c61925e186ce7d33634745a38f1db7d39d2f06a27585fbeab in / 
# Thu, 22 Sep 2022 18:41:05 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:00:03 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 22 Sep 2022 19:00:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 22 Sep 2022 19:00:04 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Sep 2022 19:00:05 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Sep 2022 19:00:06 GMT
ENV JAVA_VERSION=20-ea+15
# Thu, 22 Sep 2022 19:00:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/15/GPL/openjdk-20-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='2ee417bc5d9f36c634a5e004c201967b70b6b3a5382147d74406cc9b015eac97'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/15/GPL/openjdk-20-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ec219647905af892891d6fd018538043bf19cfae2a40df439b9fde070476681'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 22 Sep 2022 19:00:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63b915e1b20e56956b453bc1d5b77fa94f0901ef3367114af0ce6baff9e507a3`  
		Last Modified: Thu, 22 Sep 2022 18:42:03 GMT  
		Size: 50.4 MB (50377925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c29288401cec214da58d603f66600fe99310ca836e0f5a37863ecb4d0cc448`  
		Last Modified: Thu, 22 Sep 2022 19:06:21 GMT  
		Size: 15.3 MB (15263714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bb40b5bda16de0941886a62793d99ae1767293fee66356f1556c2b6fdd00c0`  
		Last Modified: Thu, 22 Sep 2022 19:06:35 GMT  
		Size: 195.4 MB (195388827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
