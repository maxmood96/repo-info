## `openjdk:19-ea-29-oraclelinux7`

```console
$ docker pull openjdk@sha256:537cbf2b20acbf77126f32a99f0b3978578dc6ee2ef203adf1576e80140e7d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-29-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:c79fe5df511257ff9fda469219ca834e48cd58b74b2026eddfcbaa9fb91debff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259147437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a320a3f6f2f826643b206b4ef34ceb6ad10f85d7e0970bb054b708396197ef45`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:27:27 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:29:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 28 Jun 2022 00:29:46 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:29:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Jul 2022 01:29:42 GMT
ENV JAVA_VERSION=19-ea+29
# Fri, 01 Jul 2022 01:29:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/29/GPL/openjdk-19-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='04ada1133ef2771a80998706ff9168ca511e4f4e7c42b1ba4c9cdbd570d6cc31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/29/GPL/openjdk-19-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='d2d5d6b1b6f1116f93a6f934f2fb03d8a4d257f0c72ad95c61a1aa2011ceb833'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Jul 2022 01:29:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63183c9b4598e16c4cef95f706d50ff6c928de41f391cd513495b27eaa27bf89`  
		Last Modified: Thu, 16 Jun 2022 01:21:08 GMT  
		Size: 48.8 MB (48757931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27f2a0cb669162a36b2576cd36536ebb88d2e0ccedba24fe92c1b0a992569e5`  
		Last Modified: Tue, 28 Jun 2022 00:38:26 GMT  
		Size: 14.2 MB (14236080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a08a6beb724a9063272ffb0754b0a1b3c38043ed1f9dac1f1dfb6309d40bce2`  
		Last Modified: Fri, 01 Jul 2022 01:42:04 GMT  
		Size: 196.2 MB (196153426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-29-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dc935337c3b48d3ceb1da5bb46718c645fa2bc22d7c14b1d133b236c4e80b5dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259598062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c80ecf9b5f8251edd5778d12b3e154422e9e4965c2f1c32a770201a3c20f73`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:12:02 GMT
ADD file:3c802f9fbd1a9a4878df064e2b268b017930633407658a3f9d29e53eb74552fa in / 
# Thu, 16 Jun 2022 01:12:03 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:41:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:44:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 28 Jun 2022 00:44:26 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:44:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Jul 2022 01:43:21 GMT
ENV JAVA_VERSION=19-ea+29
# Fri, 01 Jul 2022 01:43:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/29/GPL/openjdk-19-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='04ada1133ef2771a80998706ff9168ca511e4f4e7c42b1ba4c9cdbd570d6cc31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/29/GPL/openjdk-19-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='d2d5d6b1b6f1116f93a6f934f2fb03d8a4d257f0c72ad95c61a1aa2011ceb833'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Jul 2022 01:43:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9071f63390163e069a5245aea05c5a92f0dd4a4a48483db57c4c3c0d557be5e7`  
		Last Modified: Thu, 16 Jun 2022 01:12:57 GMT  
		Size: 49.3 MB (49343296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e959388b0464e301c8f837d6139ee9789051dee894111f69643a0c73900dfa9`  
		Last Modified: Tue, 28 Jun 2022 00:59:49 GMT  
		Size: 15.3 MB (15265029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10e367bc9e9c8dd3b3087f2e8140197c68591cb762d5a1d16581fd7f7f41e9`  
		Last Modified: Fri, 01 Jul 2022 02:02:45 GMT  
		Size: 195.0 MB (194989737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
