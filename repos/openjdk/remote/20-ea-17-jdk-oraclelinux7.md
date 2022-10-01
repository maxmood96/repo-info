## `openjdk:20-ea-17-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:779f5d83b6309b885e08272b9e6ad13f8782a7c1ffcee54b0a13ae8a7342ff46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-17-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:4432cc2466d5ad06f698b4c210aa4eb6687594a3aa33cc6840c2b8ad306b0530
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260918055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a4def3c9279a111784fa206c4e7b150171f9038b844aca28f74683d4be07c4`
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
# Fri, 30 Sep 2022 23:30:20 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:30:30 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9d46acb0892a134f62ab21fca33fdef1da5d579f61ddbd0ae3ff0b4d33c5eca2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='31245b15195bf9f12a6db08474bfcbd1ddbccc76436372bf4db538c6ede8f976'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 30 Sep 2022 23:30:31 GMT
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
	-	`sha256:14ac60cd056b1ab39f42052e9ff954bce32f0f38b7706c58cbf5d32fa13137cf`  
		Last Modified: Fri, 30 Sep 2022 23:35:02 GMT  
		Size: 196.9 MB (196898188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-17-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:66ffbcc0d6f9fab24347c618a05797776edd01a02e5293b93a5a5b9de482d57a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261100863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7a1675007a0dde1fe041fdaabdc3078c80efa231ca09168e3ff6214e50b33a`
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
# Fri, 30 Sep 2022 23:27:27 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:27:46 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9d46acb0892a134f62ab21fca33fdef1da5d579f61ddbd0ae3ff0b4d33c5eca2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='31245b15195bf9f12a6db08474bfcbd1ddbccc76436372bf4db538c6ede8f976'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 30 Sep 2022 23:27:47 GMT
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
	-	`sha256:cd1b47a22af06aec051709b6f0bb5ad660891921e87974f3e11f58b80fe3563b`  
		Last Modified: Fri, 30 Sep 2022 23:35:18 GMT  
		Size: 195.5 MB (195459224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
