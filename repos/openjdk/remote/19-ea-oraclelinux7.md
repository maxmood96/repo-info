## `openjdk:19-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:cbc53d5940e227b16147174326e930481a8c05d10fc661276055c4c998f000fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b11ed2c7b7bd251d021108568bc269996cecf0454233f6ad4fcc0cc320d0485a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259134631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a3c8e23296b9f0373c38960bbad2d2267c22ee49257f0d4762edbdbe8019d4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 May 2022 18:21:17 GMT
ADD file:60c2a17c0433d95caf7d6bac5520da02174f48bf0c50f6f369b00bf8f9774f82 in / 
# Thu, 19 May 2022 18:21:17 GMT
CMD ["/bin/bash"]
# Thu, 19 May 2022 18:22:53 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 19 May 2022 18:22:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 19 May 2022 18:22:54 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2022 18:22:54 GMT
ENV LANG=en_US.UTF-8
# Mon, 13 Jun 2022 19:52:39 GMT
ENV JAVA_VERSION=19-ea+26
# Mon, 13 Jun 2022 19:52:49 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/26/GPL/openjdk-19-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='130143ba9c969760aa4aecba9cd2296887facde306841d69404dd1d1235b3d90'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/26/GPL/openjdk-19-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='cedaf6ebfab9a1a716acf5a65e0bfe298e0c965c70100bc91cc414a9fcf0b4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 13 Jun 2022 19:52:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f0182e2fe516824cf8f93b207b7c4b65d05c48db476f53312b17b5cd952bfcc3`  
		Last Modified: Thu, 19 May 2022 18:22:04 GMT  
		Size: 48.8 MB (48757934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf5bd358537747774933b2ee9c613076ddeadddfb40f451054ba3989a4b2a80`  
		Last Modified: Thu, 19 May 2022 18:29:27 GMT  
		Size: 14.2 MB (14244311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44378fe4ed72cdef13acc68bbb53e590cbd02aa42bec7132770272f1460b555`  
		Last Modified: Mon, 13 Jun 2022 20:00:00 GMT  
		Size: 196.1 MB (196132386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:030393be91a4817cff287e9af372ad2189918481775426facbfeb6fb4cdce6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259592766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0095dd0bb86238e71eb1db67266860a8d70b3d30c42aecf8df35d2d9061cb7fa`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Jun 2022 17:42:45 GMT
ADD file:38edee0c3395726e7b6c49418111c57515fb5158f2d9007df25b1126becbe835 in / 
# Wed, 01 Jun 2022 17:42:45 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 18:06:10 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 01 Jun 2022 18:06:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 01 Jun 2022 18:06:11 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 18:06:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 13 Jun 2022 20:26:07 GMT
ENV JAVA_VERSION=19-ea+26
# Mon, 13 Jun 2022 20:26:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/26/GPL/openjdk-19-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='130143ba9c969760aa4aecba9cd2296887facde306841d69404dd1d1235b3d90'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/26/GPL/openjdk-19-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='cedaf6ebfab9a1a716acf5a65e0bfe298e0c965c70100bc91cc414a9fcf0b4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 13 Jun 2022 20:26:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f32f2fa821eee2ec9063a1b4319bd010b81853e0530a69451b35606e68be303b`  
		Last Modified: Wed, 01 Jun 2022 17:45:48 GMT  
		Size: 49.3 MB (49342882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7422ac4472668232f731f99e0cfcf6637faa083e23675a9b4fd3259163ebff4`  
		Last Modified: Wed, 01 Jun 2022 18:19:08 GMT  
		Size: 15.3 MB (15264563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a508954c11ffe89546718e47f140c9af112a73c46a6b05fac7729e066e9f871`  
		Last Modified: Mon, 13 Jun 2022 20:39:02 GMT  
		Size: 195.0 MB (194985321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
