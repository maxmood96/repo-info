## `openjdk:22-ea-27-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:7cd7eee03bce876dbe17de42f69b48a9077968d3deea9eacad723709aec70869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-27-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b71b2266580beda45a8f2596427a681abef538a198640a75b61a2c7bc3c11fa7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267466511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed6a0f9e23b007ea1988058cf0660aaf5a585c562de668faf8b273215d5d430`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 14 Dec 2023 23:21:44 GMT
ADD file:74b33794f8e61e810f09c38da020f9becc9f6987d22fa6f42af6b4226505e6ca in / 
# Thu, 14 Dec 2023 23:21:45 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:42:36 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 14 Dec 2023 23:43:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Thu, 14 Dec 2023 23:43:06 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Dec 2023 23:43:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Dec 2023 23:43:07 GMT
ENV JAVA_VERSION=22-ea+27
# Thu, 14 Dec 2023 23:43:18 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/27/GPL/openjdk-22-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='102a2e0fa1174ba6e67f79685a98122609d7f3106f3745f7418a5224e55e8643'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/27/GPL/openjdk-22-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='39341b5dba8789f64a9f1dd7310ede993d890a44ecde059955992c3260e82b78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 14 Dec 2023 23:43:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20e4dcae4c693910efbf28a556e2fa88ef717e15364f63da7e0a4a130b9b714e`  
		Last Modified: Thu, 14 Dec 2023 23:23:14 GMT  
		Size: 50.5 MB (50499235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291741a113838df70588f92202102813130a0a1ffc256860de0b8c13b8ec6939`  
		Last Modified: Thu, 14 Dec 2023 23:44:17 GMT  
		Size: 14.2 MB (14235978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f86afa33b49c7028f96b7768b15c16aac666587816aaf8ccb977baaeae3f40`  
		Last Modified: Thu, 14 Dec 2023 23:45:12 GMT  
		Size: 202.7 MB (202731298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-27-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0550a26e32df12cbd5436138e476a067788ecc4dcb77399711e82dc9e2d83602
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267140238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336dfe83d5aaebedeefa2ca90bfe259df83ae983758daa5814f7ff7058bf499f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Dec 2023 00:02:56 GMT
ADD file:7f9b20722f4f2c781b7814e113711ee10ee458be84fe343e7d61658ede9c4711 in / 
# Fri, 15 Dec 2023 00:02:57 GMT
CMD ["/bin/bash"]
# Fri, 15 Dec 2023 00:20:21 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 15 Dec 2023 00:21:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 15 Dec 2023 00:21:00 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 00:21:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 Dec 2023 00:21:00 GMT
ENV JAVA_VERSION=22-ea+27
# Fri, 15 Dec 2023 00:21:13 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/27/GPL/openjdk-22-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='102a2e0fa1174ba6e67f79685a98122609d7f3106f3745f7418a5224e55e8643'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/27/GPL/openjdk-22-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='39341b5dba8789f64a9f1dd7310ede993d890a44ecde059955992c3260e82b78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 15 Dec 2023 00:21:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01eab324a7fc4cacc34c78d38ce9548750df098b20899d269b500307b6765a1d`  
		Last Modified: Fri, 15 Dec 2023 00:04:16 GMT  
		Size: 51.1 MB (51110815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0c92b2a0403c99f9b8b57a84e65c115d05d0c4d6644795f60ccf2a3a122e4f`  
		Last Modified: Fri, 15 Dec 2023 00:22:13 GMT  
		Size: 15.2 MB (15245630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d0fc4b7d1f9be2744a6122f43dedccfa5e0f38561fb597191f9f615f3dd1ed`  
		Last Modified: Fri, 15 Dec 2023 00:23:05 GMT  
		Size: 200.8 MB (200783793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
