## `openjdk:19-ea-14-oraclelinux8`

```console
$ docker pull openjdk@sha256:193a68952637acd87d0ce5faa1f6deabddc1de9dfde1d903e8768eb22192419a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-14-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:a17744c17a2c34cee9b01bed930920ee3764625104b40c6816e0ce3f95d56778
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248715823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3c7a369a8fdb02c057613dbd2b1c10b547487be5501292721df85f686bd4d2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 05:23:28 GMT
ADD file:09b0bc8af49fa3558fb3e8d50daa682180e194cb11ca332d03ca65059e615dfd in / 
# Fri, 18 Mar 2022 05:23:29 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 10:17:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 19 Mar 2022 10:17:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Sat, 19 Mar 2022 10:17:41 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:17:41 GMT
ENV LANG=C.UTF-8
# Tue, 22 Mar 2022 01:23:40 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 01:23:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Mar 2022 01:23:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1824cb7e97fbcfc5c6ffea667f8e19cee765d015fef1b8ad70f96252d9713c95`  
		Last Modified: Fri, 18 Mar 2022 05:24:44 GMT  
		Size: 42.1 MB (42110196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db19695be7be96a8d27e754c74310c6fafa295ecdccbc10e8c5fe5b23854c2a`  
		Last Modified: Sat, 19 Mar 2022 10:34:49 GMT  
		Size: 13.5 MB (13519824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc779c18a39e785ad28edfa84ee25194f3332019134704fb5dd33e59ef575233`  
		Last Modified: Tue, 22 Mar 2022 01:31:04 GMT  
		Size: 193.1 MB (193085803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-14-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f555ebdfcee89b6271f21b6034e62403da7dbced1d60432cb563db26e9ecf1bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248429368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292f0e5a14f0519d581ed6d95bca2746a5794edc700993d9b0da7d9e18542e86`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 00:35:35 GMT
ADD file:b16af05882bd38ac02b1f1cba2cc7e80bfbe467ce57f3cf35f1f5a551cee90fa in / 
# Fri, 18 Mar 2022 00:35:36 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 07:22:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 19 Mar 2022 07:22:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Sat, 19 Mar 2022 07:22:08 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 07:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 22 Mar 2022 10:02:34 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 10:02:52 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Mar 2022 10:02:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f8e506fd7c6683f24250871efec36e3fe21cc71090a2f5c59dccdcdfeed2311`  
		Last Modified: Fri, 18 Mar 2022 00:36:38 GMT  
		Size: 42.0 MB (42017883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5fff79dab44aae745004a90eddcd68a9db24e820f0c68e482a9508464ea719`  
		Last Modified: Sat, 19 Mar 2022 07:43:39 GMT  
		Size: 14.3 MB (14291778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a47e7293c29a2389191c592de9dc220439260caa5a0d1f5c7af040e6a8e5f8`  
		Last Modified: Tue, 22 Mar 2022 10:16:13 GMT  
		Size: 192.1 MB (192119707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
