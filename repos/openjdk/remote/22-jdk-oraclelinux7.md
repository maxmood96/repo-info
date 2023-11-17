## `openjdk:22-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:258012894360fcfaba12b05ad4685094d58c7161d639f94fdf8915183ce8fe34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:3a41eaa311af647498194c9477397030ea53dc205a3a2b48daf4363d6dc14fac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269005475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd45864d71cf182e004f08152b1bc7fa73e8e1941aa810e5a22ede7cb7cdd7b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Nov 2023 18:20:58 GMT
ADD file:3e0277519395faaec643f0d6752812c14478974d1a914a763327a3cf30bbd28c in / 
# Tue, 14 Nov 2023 18:20:58 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 18:46:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 14 Nov 2023 18:46:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 14 Nov 2023 18:46:41 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 18:46:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Nov 2023 04:29:00 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 04:29:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='f2b3d5371bc7ab762205f286fc5b5da9dabbdd0477965fc87d02076faf69ab3a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='909c2841030baff026a45248785f3dc50906ce921620913a28b8d6cca0075838'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Nov 2023 04:29:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11a38aebcb7ae84df8b4fdcc1c7540389829a1f599b7a9986df89df733b69cea`  
		Last Modified: Tue, 14 Nov 2023 18:22:00 GMT  
		Size: 50.5 MB (50499111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d855689795ad008f2a59d12fd4c1661d113041ec2efd3339b326986f9ee7f96f`  
		Last Modified: Tue, 14 Nov 2023 18:47:56 GMT  
		Size: 14.3 MB (14252430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8eddb538558fffc6380da677aa9f5ca09064059547d4995138163958d5dc1`  
		Last Modified: Fri, 17 Nov 2023 04:32:35 GMT  
		Size: 204.3 MB (204253934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:32a9796d81dd1f940844881431be96006667717cac5d1aa75a97176ca50c2eeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268670490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26131616511160d265324b6c0e8d8da0a67b80ee98b9fa881a6e91ccb776a35f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Nov 2023 18:47:13 GMT
ADD file:0429c6e46360abe0bf4baedbcca5a063b60eb02c2b38c8642fd5e6d6431f2216 in / 
# Tue, 14 Nov 2023 18:47:14 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 19:11:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 14 Nov 2023 19:11:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 14 Nov 2023 19:11:54 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Nov 2023 02:05:12 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 02:05:34 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='f2b3d5371bc7ab762205f286fc5b5da9dabbdd0477965fc87d02076faf69ab3a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='909c2841030baff026a45248785f3dc50906ce921620913a28b8d6cca0075838'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Nov 2023 02:05:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:234b67cef5b9c7021cf94a462ae8c27e19f05d8ab6020a2c08b47a355a51757e`  
		Last Modified: Tue, 14 Nov 2023 18:48:16 GMT  
		Size: 51.1 MB (51110162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3db892ec75a05fe3c6e1f29c7ee60b17e26e42c96c7901605d8be961e62e5a`  
		Last Modified: Tue, 14 Nov 2023 19:12:57 GMT  
		Size: 15.2 MB (15245362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373326c4a992ddb27ef829c9aa7b8b78fd9ca3f50625bf04a826f8eb724c6f24`  
		Last Modified: Fri, 17 Nov 2023 02:09:01 GMT  
		Size: 202.3 MB (202314966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
