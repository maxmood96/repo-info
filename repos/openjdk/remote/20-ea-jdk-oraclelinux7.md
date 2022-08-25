## `openjdk:20-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:94787ac9b9a4036a268d0a75e58826824d606e59650b54c64a0c3e1eb8fcee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:a56d53a920ddf954609b8b8b8ecf67356f456aec9484c12e5913eeda0013bd14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260147415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a8ff59eed6a00462b383b3de1b91b77a706424e1f2a1db9499cceb8098c20d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Aug 2022 19:35:42 GMT
ADD file:adf7ebc1d65494dba22f4f0a12f2f8f63128836b87646ffd6e9964f936343e6d in / 
# Wed, 24 Aug 2022 19:35:43 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 22:44:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 24 Aug 2022 22:44:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 24 Aug 2022 22:44:32 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 22:44:33 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Aug 2022 22:44:33 GMT
ENV JAVA_VERSION=20-ea+11
# Wed, 24 Aug 2022 22:44:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='9a0afe9f1c3ef50968060fe8d70d7b27d93b5515479846193de809127f0d427f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='d7e80f5000f66440c34073bdb0e443b941ef11209ca30f0e698f07a3fce08118'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 24 Aug 2022 22:44:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9815334b7810943f0c417fa41a2732d56b098252185c5749c2c2ce80f8e8e140`  
		Last Modified: Wed, 24 Aug 2022 19:37:41 GMT  
		Size: 48.7 MB (48727120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbb6577271d2ea4eb7961ad553fcac407890cd27f6514b5d071119191d585fd`  
		Last Modified: Wed, 24 Aug 2022 22:49:44 GMT  
		Size: 14.2 MB (14230815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88f4265454e9b4edeeb85aa8e48d53c8796e6c548f09f6e63c5dcb29232d9c1`  
		Last Modified: Wed, 24 Aug 2022 22:49:58 GMT  
		Size: 197.2 MB (197189480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6d7e43c1f8048846b74eb8c1b8d9bda7115f06d1856f81172a5f6836d6d894ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260289152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73f10ae0846e9bca498d4546ed73a334a847cf463f2dfc15e8e90b0319b28d6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Aug 2022 19:55:21 GMT
ADD file:58b53a780a05a9f314e6821fd85f38a0d86fed5a98ab7c3fd52b0ea2341c3d64 in / 
# Wed, 24 Aug 2022 19:55:22 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:31:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 24 Aug 2022 23:31:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 24 Aug 2022 23:31:55 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 23:31:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Aug 2022 23:31:57 GMT
ENV JAVA_VERSION=20-ea+11
# Wed, 24 Aug 2022 23:32:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='9a0afe9f1c3ef50968060fe8d70d7b27d93b5515479846193de809127f0d427f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='d7e80f5000f66440c34073bdb0e443b941ef11209ca30f0e698f07a3fce08118'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 24 Aug 2022 23:32:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d094a37c2b34cb4c876f39d579c422eba5a195ec17dff5a5fcbbbd9398dafef`  
		Last Modified: Wed, 24 Aug 2022 19:57:30 GMT  
		Size: 49.3 MB (49309770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346cd8d935004b602845ed18ab7ddf7b6bf15cfcb9eb50d1b98f6153c188f3a3`  
		Last Modified: Wed, 24 Aug 2022 23:41:46 GMT  
		Size: 15.3 MB (15266557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92acd54b5d52520ff7bcc5e514f35508ee056bd6f35950efd8a129e63bf441ed`  
		Last Modified: Wed, 24 Aug 2022 23:42:04 GMT  
		Size: 195.7 MB (195712825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
