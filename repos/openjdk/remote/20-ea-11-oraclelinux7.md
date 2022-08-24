## `openjdk:20-ea-11-oraclelinux7`

```console
$ docker pull openjdk@sha256:4da29fbca129583a6672f50a6e7f962834557bedb0e7c4bd4b7f289098f7b0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-11-oraclelinux7` - linux; amd64

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

### `openjdk:20-ea-11-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:71e1b6c7cef7c5dd13447580470014f3e366a248486f0b0da077fd1faed790bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260320011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806470af3ea3a7def9c93a57da34edf3cd7a2da673f261f92d2b49012af1e2b0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:37 GMT
ADD file:6d5eeb6c0921661dff8e0b6a89c3272aa52f72b5926d62ae482a85c8ef6458a3 in / 
# Tue, 05 Jul 2022 22:43:38 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:05:04 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 05 Jul 2022 23:05:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 05 Jul 2022 23:05:05 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 23:05:06 GMT
ENV LANG=en_US.UTF-8
# Sat, 20 Aug 2022 01:51:01 GMT
ENV JAVA_VERSION=20-ea+11
# Sat, 20 Aug 2022 01:51:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='9a0afe9f1c3ef50968060fe8d70d7b27d93b5515479846193de809127f0d427f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/11/GPL/openjdk-20-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='d7e80f5000f66440c34073bdb0e443b941ef11209ca30f0e698f07a3fce08118'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 20 Aug 2022 01:51:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:456ca0cbf3e695c518e5d5c4cb5ff9f99bb999a28b5ec7da3b4ca48d3cf80e6b`  
		Last Modified: Tue, 05 Jul 2022 22:45:10 GMT  
		Size: 49.3 MB (49342729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7981fd8b8b8e53f7977497096fa392e1d14f1e3dd10684ac47d3fa4688b887e7`  
		Last Modified: Tue, 05 Jul 2022 23:21:54 GMT  
		Size: 15.3 MB (15264543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea755fd37f9d58876a55182a914a8817fe0f555526904e4ced68c1cf2e923ada`  
		Last Modified: Sat, 20 Aug 2022 02:03:52 GMT  
		Size: 195.7 MB (195712739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
