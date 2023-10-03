## `openjdk:22-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:49d8109f8d45f50e41acc094ba03a45fbb0aed39dac6179eef134c8aaa98d2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:3082833ad5757efbaa0ba4bfcc31e400c2608f08ae85c496b4e45dd9119d5584
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269805377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63483e23a56c98e835acf23ac6f3367744b59a136066bcb8383ad1ac0ef4e3d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Jun 2023 07:21:40 GMT
ADD file:733a37449d62d6e9f530185b9244e06cd8ff0ee896632576ae644437d0a1f852 in / 
# Wed, 14 Jun 2023 07:21:40 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 09:56:49 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Jun 2023 09:56:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Wed, 14 Jun 2023 09:56:49 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 09:56:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 03 Oct 2023 01:28:39 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:28:49 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='2e079b8de8557b2bfdf2c548f69cf0c8ed9a94e7a0460dfebbebb4bf936dea8b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5b70d1b43017fc00355d38e8f5c5f96d161033968968f76777189ffff3b5ff0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 03 Oct 2023 01:28:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70e9ff4420fbc58483e68c13199a06c24b14013b2548998a7e367f59ca5157bc`  
		Last Modified: Wed, 14 Jun 2023 07:22:30 GMT  
		Size: 50.5 MB (50484765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4714d29e017353e367cfbeb707bad46a96692fceb51533b3749c668baf3b5b8f`  
		Last Modified: Wed, 14 Jun 2023 09:58:27 GMT  
		Size: 14.2 MB (14242764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b054c20b45d3f5ab4c83367db53d30f66163c786489499523975c8fd79d8067`  
		Last Modified: Tue, 03 Oct 2023 01:31:51 GMT  
		Size: 205.1 MB (205077848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3437a8913cf754b20e1252f572f6e3b09012015247eb3e1d357f90050d9f8105
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269680428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d6bd7cfb2fbf8fec0d31195d564a2563dcceb5f5028eafbb34e34432cb863c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Jun 2023 03:45:43 GMT
ADD file:a9ba9c7acb256e802c7248b56f377a6f0ea08b1b61e11e482516633a13f4d686 in / 
# Wed, 14 Jun 2023 03:45:44 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 04:08:20 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Jun 2023 04:08:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Wed, 14 Jun 2023 04:08:20 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 04:08:20 GMT
ENV LANG=en_US.UTF-8
# Tue, 03 Oct 2023 01:33:04 GMT
ENV JAVA_VERSION=22-ea+17
# Tue, 03 Oct 2023 01:33:17 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='2e079b8de8557b2bfdf2c548f69cf0c8ed9a94e7a0460dfebbebb4bf936dea8b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/17/GPL/openjdk-22-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5b70d1b43017fc00355d38e8f5c5f96d161033968968f76777189ffff3b5ff0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 03 Oct 2023 01:33:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:52fd87ed40fcddc3fe63b876d1f94f6edae688637a5cc56983dced68a50c953e`  
		Last Modified: Wed, 14 Jun 2023 03:46:28 GMT  
		Size: 51.1 MB (51052081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aeb39f5d39e6fb51e698f8f5e6416d0689047f9392a9bd3f97f28c4d5d5596`  
		Last Modified: Wed, 14 Jun 2023 04:10:01 GMT  
		Size: 15.2 MB (15238146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36e9c72a2824c0ef1a65f1b5be7464ff1ae099f65868f3a512fa83d60f5ab69`  
		Last Modified: Tue, 03 Oct 2023 01:35:56 GMT  
		Size: 203.4 MB (203390201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
