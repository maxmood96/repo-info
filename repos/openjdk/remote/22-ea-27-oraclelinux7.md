## `openjdk:22-ea-27-oraclelinux7`

```console
$ docker pull openjdk@sha256:2357e381facee0ade1f5c657f8f662c321ddad7f5e8e2d7b476258f1d3526ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-27-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:f414bbae5d824207475bfd8d652c25199d4f8572f0e77e6cf7591f25a7d3b3f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267482859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2424181876b19e543c0d2b7c6fb1e96c611e086d024d0893039c1c4f961c6328`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Nov 2023 18:20:58 GMT
ADD file:3e0277519395faaec643f0d6752812c14478974d1a914a763327a3cf30bbd28c in / 
# Tue, 14 Nov 2023 18:20:58 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 18:46:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 14 Nov 2023 18:46:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 14 Nov 2023 18:46:41 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 18:46:41 GMT
ENV LANG=en_US.UTF-8
# Sat, 09 Dec 2023 05:51:43 GMT
ENV JAVA_VERSION=22-ea+27
# Sat, 09 Dec 2023 05:51:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/27/GPL/openjdk-22-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='102a2e0fa1174ba6e67f79685a98122609d7f3106f3745f7418a5224e55e8643'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/27/GPL/openjdk-22-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='39341b5dba8789f64a9f1dd7310ede993d890a44ecde059955992c3260e82b78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 09 Dec 2023 05:51:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11a38aebcb7ae84df8b4fdcc1c7540389829a1f599b7a9986df89df733b69cea`  
		Last Modified: Tue, 14 Nov 2023 18:22:00 GMT  
		Size: 50.5 MB (50499111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d855689795ad008f2a59d12fd4c1661d113041ec2efd3339b326986f9ee7f96f`  
		Last Modified: Tue, 14 Nov 2023 18:47:56 GMT  
		Size: 14.3 MB (14252430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40649fa382e34b3623319ea91258bab032c9d94359d88eab42a3b72fdfbd5d5`  
		Last Modified: Sat, 09 Dec 2023 05:54:48 GMT  
		Size: 202.7 MB (202731318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-27-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8bbe2277c354ee67223f60accdf4617f627ede0d5e24f6fd13c9b87bdee93538
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267139265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63924d0be7305052103f77eb3b6d3dbe707187532d1671f66db0cac0e2551a26`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Nov 2023 18:47:13 GMT
ADD file:0429c6e46360abe0bf4baedbcca5a063b60eb02c2b38c8642fd5e6d6431f2216 in / 
# Tue, 14 Nov 2023 18:47:14 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 19:11:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 14 Nov 2023 19:11:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 14 Nov 2023 19:11:54 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Dec 2023 23:23:53 GMT
ENV JAVA_VERSION=22-ea+27
# Fri, 08 Dec 2023 23:24:05 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/27/GPL/openjdk-22-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='102a2e0fa1174ba6e67f79685a98122609d7f3106f3745f7418a5224e55e8643'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/27/GPL/openjdk-22-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='39341b5dba8789f64a9f1dd7310ede993d890a44ecde059955992c3260e82b78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 08 Dec 2023 23:24:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:234b67cef5b9c7021cf94a462ae8c27e19f05d8ab6020a2c08b47a355a51757e`  
		Last Modified: Tue, 14 Nov 2023 18:48:16 GMT  
		Size: 51.1 MB (51110162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3db892ec75a05fe3c6e1f29c7ee60b17e26e42c96c7901605d8be961e62e5a`  
		Last Modified: Tue, 14 Nov 2023 19:12:57 GMT  
		Size: 15.2 MB (15245362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3041faf5a36be4b700c4d7d37c84a730537479288df08910b4e9e97a6852a66`  
		Last Modified: Fri, 08 Dec 2023 23:26:35 GMT  
		Size: 200.8 MB (200783741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
