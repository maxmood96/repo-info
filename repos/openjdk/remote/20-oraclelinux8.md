## `openjdk:20-oraclelinux8`

```console
$ docker pull openjdk@sha256:2c4d185471cea6f68b5254f7977b97d5d117365539b076a80857d5cc568ec686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:6324ee6334ed5946c42212bc0ae2fc82165dea87b93cc1291123e0c790a2f706
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254252708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b11bc6374cd51391437ab4205181088ffe3b5ff715587af584b38431dea0b2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:27:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:27:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 07 Dec 2022 02:27:04 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:27:04 GMT
ENV LANG=C.UTF-8
# Fri, 13 Jan 2023 00:30:14 GMT
ENV JAVA_VERSION=20-ea+31
# Fri, 13 Jan 2023 00:30:30 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/31/GPL/openjdk-20-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='3269ddcaa2745f47e0610531a0c6f06671f7b85fd4c02ae4a29a6f14089748a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/31/GPL/openjdk-20-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ee53148820a0f603ef492aa7c62154c043cf38cea3259581a79010d8297c2f5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Jan 2023 00:30:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3502f40d35be69b4df858d92b5ac60d6b792eec7beabb7cbd78c816329f47b7f`  
		Last Modified: Wed, 07 Dec 2022 02:30:44 GMT  
		Size: 12.2 MB (12248357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a18f78fb0f32547fd3c73722ed3649bd46c6a334cd9ea52e4cd86f8d4266ac`  
		Last Modified: Fri, 13 Jan 2023 00:38:51 GMT  
		Size: 198.1 MB (198135613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:90eb182716fb06d86f2865cf0b96b626ad4103b6c1100eb8af1159adafcc7075
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252458083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c391bd2c17cbc57ed7f3bd03a7e1256aaf987241d1e858960ee60d273f6197`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:53:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:53:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 07 Dec 2022 02:53:06 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Jan 2023 00:49:50 GMT
ENV JAVA_VERSION=20-ea+31
# Fri, 13 Jan 2023 00:49:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/31/GPL/openjdk-20-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='3269ddcaa2745f47e0610531a0c6f06671f7b85fd4c02ae4a29a6f14089748a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/31/GPL/openjdk-20-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ee53148820a0f603ef492aa7c62154c043cf38cea3259581a79010d8297c2f5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Jan 2023 00:50:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e459b46a4edc515fedc5c9be076b28ba6b0606f3cc90d412ea3d88b15576e`  
		Last Modified: Wed, 07 Dec 2022 02:57:10 GMT  
		Size: 13.1 MB (13058882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8190e0b0c4d0f589cdcf81d0383b84dbc2aa5fbe2d915b3acf8bc7c345e62b`  
		Last Modified: Fri, 13 Jan 2023 00:58:24 GMT  
		Size: 196.6 MB (196627142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
