## `openjdk:23-ea-1-oraclelinux7`

```console
$ docker pull openjdk@sha256:26ba9bae1b0a3e81e17562f6fea2dee661be53c8834fae538a92650157ca18fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:23-ea-1-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:37d2335b3120013d251795e3b06ad3cf81b035c1047a53b42adef3b5a559357f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267546668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ee2469fcf9e4529d04aac239a0d535bc794e181a09c25dc7e97f574d4cd13d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Nov 2023 18:20:58 GMT
ADD file:3e0277519395faaec643f0d6752812c14478974d1a914a763327a3cf30bbd28c in / 
# Tue, 14 Nov 2023 18:20:58 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 18:46:40 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 12 Dec 2023 20:27:59 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Tue, 12 Dec 2023 20:27:59 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 20:27:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Dec 2023 20:27:59 GMT
ENV JAVA_VERSION=23-ea+1
# Tue, 12 Dec 2023 20:28:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/1/GPL/openjdk-23-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='740a84253d35402b9213bf187ee4f058817c614f8cc47cb3414e02760f05099f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/1/GPL/openjdk-23-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='74fe7c8e67c5b80f868ec20daecb112fc090fb91c58bf4ce5297cf77c9935fa5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 12 Dec 2023 20:28:11 GMT
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
	-	`sha256:90caf2430ba6541bfb778f0e11c1d38e7674fb96d6c414d7e0183a01d50c6c17`  
		Last Modified: Tue, 12 Dec 2023 20:31:35 GMT  
		Size: 202.8 MB (202795127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-1-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:83fa9326568700c1b4c2c21be67e14f32dd9685176aae4a4f2edf1c25e54b8a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267205929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac59223df1b3b6039ca726199677f7f5674e7916e61e84c2f76c2f828b55866`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Nov 2023 18:47:13 GMT
ADD file:0429c6e46360abe0bf4baedbcca5a063b60eb02c2b38c8642fd5e6d6431f2216 in / 
# Tue, 14 Nov 2023 18:47:14 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 19:11:54 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 12 Dec 2023 19:47:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Tue, 12 Dec 2023 19:47:49 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 19:47:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Dec 2023 19:47:49 GMT
ENV JAVA_VERSION=23-ea+1
# Tue, 12 Dec 2023 19:48:03 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/1/GPL/openjdk-23-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='740a84253d35402b9213bf187ee4f058817c614f8cc47cb3414e02760f05099f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/1/GPL/openjdk-23-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='74fe7c8e67c5b80f868ec20daecb112fc090fb91c58bf4ce5297cf77c9935fa5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 12 Dec 2023 19:48:05 GMT
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
	-	`sha256:c129881b3fda9e63cfdbc29841a5422fcc531df1c83c35b9cb0f6ed321444759`  
		Last Modified: Tue, 12 Dec 2023 19:51:09 GMT  
		Size: 200.9 MB (200850405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
