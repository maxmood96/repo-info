## `openjdk:20-ea-4-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:b3868aab27fd632c639f615fad10668a26d9f288701f0b16b7f44ce69a3a3287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-4-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:f1e7a6ae043c7f93207171a325f7f22ec7ff389ef21ba2c2596f170d134a3deb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259725778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa44885bdcdb50d24ecb8f6f386834d4ef05187e180a715694aa04d5bf46fa1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:27:27 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:27:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 28 Jun 2022 00:27:28 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:27:28 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Jul 2022 01:28:11 GMT
ENV JAVA_VERSION=20-ea+4
# Fri, 01 Jul 2022 01:28:20 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/4/GPL/openjdk-20-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='74243a1b83dde07c3645cd0c7c3b00135fb9ca38c357e284560bf5be45a864d6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/4/GPL/openjdk-20-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='ce9dd88462c6fb6c6e8be53151164b95a738e03d28788f3fd64e0339dee96de1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Jul 2022 01:28:21 GMT
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
	-	`sha256:95670a532d550e41ceff789d7d6f29a39a4ef9925a752b7e859a7d714b52a650`  
		Last Modified: Fri, 01 Jul 2022 01:37:44 GMT  
		Size: 196.7 MB (196731767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-4-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:12eb984095895397184f7a9d3eefa0f689fed59363730c8be224f1c74a2151b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260192876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758616e3b83476919320bdf51f3f49881872631e1ec99261d261ab4f8013888d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:12:02 GMT
ADD file:3c802f9fbd1a9a4878df064e2b268b017930633407658a3f9d29e53eb74552fa in / 
# Thu, 16 Jun 2022 01:12:03 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:41:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:41:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 28 Jun 2022 00:41:53 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:41:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 01 Jul 2022 01:41:03 GMT
ENV JAVA_VERSION=20-ea+4
# Fri, 01 Jul 2022 01:41:21 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/4/GPL/openjdk-20-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='74243a1b83dde07c3645cd0c7c3b00135fb9ca38c357e284560bf5be45a864d6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/4/GPL/openjdk-20-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='ce9dd88462c6fb6c6e8be53151164b95a738e03d28788f3fd64e0339dee96de1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Jul 2022 01:41:22 GMT
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
	-	`sha256:0737a18d529267a98f6ba071a6017dd940688fa96fd715f4b902361cb6270fda`  
		Last Modified: Fri, 01 Jul 2022 01:57:53 GMT  
		Size: 195.6 MB (195584551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
