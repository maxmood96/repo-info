## `openjdk:21-oraclelinux7`

```console
$ docker pull openjdk@sha256:bd17d66ce7e96522cb470846d97390bbe6084fef7c158667f3834ae44f98f02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:2f4e17b35dd272809be212091ba4fe9e88f3d3b12f72a0991a24ba5256035b30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266304341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6358ed5445810bc538b0928dad4925fd2031a603e6fd22948d99a79ff5d82c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:55 GMT
ADD file:10911d9c2c204daa6723e5b0ad36e645e6ea8c550c0ca101d05b5a7c933d07c8 in / 
# Wed, 29 Mar 2023 00:21:55 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:39:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 29 Mar 2023 00:39:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 29 Mar 2023 00:39:54 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 00:39:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 29 Mar 2023 00:39:54 GMT
ENV JAVA_VERSION=21-ea+15
# Wed, 29 Mar 2023 00:40:03 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='0fec1002b8c8975b181bd6966a817028d6b373cbc759254231f9b96db1fe6edd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93cc1eb6202093a127f1f9ed2e866a51dff29321f878085c18f317cefb113ffc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Mar 2023 00:40:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb4d5d9bb16e42b089bf97c219441b69e513f2bfe178197f1847ef7c30c98ad7`  
		Last Modified: Wed, 29 Mar 2023 00:23:34 GMT  
		Size: 50.5 MB (50492696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d3c5429efa096f173a7bbc8a5a3f3d3431ed130f2c586ec465f2b56f9ba2fa`  
		Last Modified: Wed, 29 Mar 2023 00:41:15 GMT  
		Size: 14.2 MB (14240909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf5fb7df7b308131640de294eb6488d2ef80ecb3f42ba7d891ac5b837198343`  
		Last Modified: Wed, 29 Mar 2023 00:41:27 GMT  
		Size: 201.6 MB (201570736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cafbb4214fa2e07e304d2c03e0601ec2112b35e53a634671fe5d02d9d5e8b5ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266396090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e53ca03a5c7ea9b21291fa56a71d719ca57c3708ca09c1b9a9da80ba410b3b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:25 GMT
ADD file:6e29a6d8ad154fd5e4fe7fe5f789af049d2921601982fb0e927266c3c8d9cadd in / 
# Wed, 29 Mar 2023 00:40:26 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 01:00:25 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 29 Mar 2023 01:00:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 29 Mar 2023 01:00:25 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 01:00:25 GMT
ENV LANG=en_US.UTF-8
# Wed, 29 Mar 2023 01:00:25 GMT
ENV JAVA_VERSION=21-ea+15
# Wed, 29 Mar 2023 01:00:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='0fec1002b8c8975b181bd6966a817028d6b373cbc759254231f9b96db1fe6edd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93cc1eb6202093a127f1f9ed2e866a51dff29321f878085c18f317cefb113ffc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Mar 2023 01:00:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c3cc2a3a663480e56e9b240b07f2bbd68783ecb9f3b865bb0b0513246def5b88`  
		Last Modified: Wed, 29 Mar 2023 00:41:55 GMT  
		Size: 51.1 MB (51082220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b63337a2b7a45e88c9c684956177de7c4970f1035eb5abe90810079e9bf573e`  
		Last Modified: Wed, 29 Mar 2023 01:01:44 GMT  
		Size: 15.3 MB (15279691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6b689cd031cc6557e1b6f38b2ae325d876d867618aa4fb5c2066de4e9d66c0`  
		Last Modified: Wed, 29 Mar 2023 01:01:54 GMT  
		Size: 200.0 MB (200034179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
