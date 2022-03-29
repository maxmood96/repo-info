## `openjdk:19-ea-15-oraclelinux7`

```console
$ docker pull openjdk@sha256:a26ce17fa2ebc34160f26c9ac3689eb5622cb439d9aaf1fba2300a6577c240e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-15-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:36d61121a03c6629fddc81d3478cb3ed35d87e1e67cd256c711dfd375a9a6241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256181876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2025f417c8b4fa3638040344e141ec9a1e743ab5aa436b35ea5591b58dfa74cb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 24 Mar 2022 22:26:41 GMT
ADD file:c54c465abf0c60dc924ca0809a1a862121214379efe90dacb9c9947c81054213 in / 
# Thu, 24 Mar 2022 22:26:42 GMT
CMD ["/bin/bash"]
# Fri, 25 Mar 2022 01:17:16 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 25 Mar 2022 01:17:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Mar 2022 01:17:17 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Mar 2022 01:17:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Mar 2022 00:51:40 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:51:49 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:51:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fda5369ef22868b2225eb458f776aabaf140371e2f8d709c4de99b69a02ae748`  
		Last Modified: Thu, 24 Mar 2022 22:28:00 GMT  
		Size: 48.7 MB (48749451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175ebd0783e9e11a5749d6a07553e79af5cce82b84020eca354389f2e772070e`  
		Last Modified: Fri, 25 Mar 2022 01:25:40 GMT  
		Size: 14.2 MB (14229382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd46fbfbe52a04e9c1d17b36a0748721c552a56dce512d07086e803bebbf9966`  
		Last Modified: Tue, 29 Mar 2022 01:03:37 GMT  
		Size: 193.2 MB (193203043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-15-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dfa1f6a36e2cced21032d90109ee8094fd8916852511630bd9487cd026803e16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256694394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbbe641e290083a55896d3eb8ac7d996ea60830da2a337648e333b339ee7226`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 24 Mar 2022 22:21:33 GMT
ADD file:458f691e62c6797d5a132b3af3e3d34358f4563c2f767879ff5a5edaac9c76ee in / 
# Thu, 24 Mar 2022 22:21:34 GMT
CMD ["/bin/bash"]
# Thu, 24 Mar 2022 22:46:20 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 24 Mar 2022 22:46:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 24 Mar 2022 22:46:21 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 22:46:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Mar 2022 01:17:05 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 01:17:22 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:17:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a4f104bbb26007de614fa29a9ed91e9210287087323d3de394a39f0d9f1139c`  
		Last Modified: Thu, 24 Mar 2022 22:23:06 GMT  
		Size: 49.3 MB (49340038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a5491893ff1eefd4a92b9f85621f8ee58a84cb7d0fa6edf8ca55ed7dad5724`  
		Last Modified: Thu, 24 Mar 2022 23:02:13 GMT  
		Size: 15.3 MB (15270343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8074c23f43a211dc5c22edce8741a6cf0816b80df98ff6f372e6737a5ed725`  
		Last Modified: Tue, 29 Mar 2022 01:36:50 GMT  
		Size: 192.1 MB (192084013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
