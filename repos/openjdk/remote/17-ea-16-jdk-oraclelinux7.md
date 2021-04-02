## `openjdk:17-ea-16-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:0437521ffc2b5e2742da42d470e657457aae7e029f8423825a5e735e852f8309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-16-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:7450a35406addf781d0bb65f29c5d04033eb48dc3dae12f4a3e0aa543dd36321
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249398929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5165a7b4bbf6228f5461a7a0aaab13b666c874158ddb347ec9efa9b0e146c4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Mar 2021 00:21:32 GMT
ADD file:837f2bca2cab135736ad43644356710dcac6516fdfc2023d239d157d1fa4ba7c in / 
# Wed, 17 Mar 2021 00:21:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Mar 2021 00:38:33 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 17 Mar 2021 00:38:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 17 Mar 2021 00:38:34 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Mar 2021 00:38:34 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Apr 2021 18:25:57 GMT
ENV JAVA_VERSION=17-ea+16
# Fri, 02 Apr 2021 18:26:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='ee7a5b391e275d159e623b7a35008d180c0ff362e93216395412aae871a1790a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='7554740bd86ea06cfdead0b768cd15758ea76d21ba2140b9b7b9bb1e45fd0c39'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 02 Apr 2021 18:26:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:401a42e1eb4fe87d89990847d6ef97767b5ac57457c8001203ee2ea137736907`  
		Last Modified: Wed, 17 Mar 2021 00:22:34 GMT  
		Size: 48.3 MB (48263709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f752366003eed4ac964ebb4be3453e3f19d854828f4f50ff708900bb4c42924`  
		Last Modified: Wed, 17 Mar 2021 00:45:21 GMT  
		Size: 15.4 MB (15429957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf0d8dd89c86301fe328e700664ccc045c95f0e52158e0d8c622a4577cf176`  
		Last Modified: Fri, 02 Apr 2021 18:32:18 GMT  
		Size: 185.7 MB (185705263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-16-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fa85d344fbbdfd387fe5d16781a964b8f0cc7eaf06e8dde50b828b3d4408e090
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247090576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5a7b0cfab0f2ebce4d0dec6238dc3b89e9e99ebb74dbae0ad15583672c5a07`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Mar 2021 03:42:09 GMT
ADD file:035a776cfbed0261290447a1f521123f230f599d8a9ede7feb4616146e47fe10 in / 
# Wed, 17 Mar 2021 03:42:13 GMT
CMD ["/bin/bash"]
# Wed, 17 Mar 2021 04:00:37 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 17 Mar 2021 04:00:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 17 Mar 2021 04:00:39 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Mar 2021 04:00:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Apr 2021 19:12:07 GMT
ENV JAVA_VERSION=17-ea+16
# Fri, 02 Apr 2021 19:12:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='ee7a5b391e275d159e623b7a35008d180c0ff362e93216395412aae871a1790a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/16/GPL/openjdk-17-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='7554740bd86ea06cfdead0b768cd15758ea76d21ba2140b9b7b9bb1e45fd0c39'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 02 Apr 2021 19:13:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d8ef6a6bcc7f4a961a86d5d1f004e51937aa0e6caf0086b892501d0f909ac044`  
		Last Modified: Wed, 17 Mar 2021 03:43:17 GMT  
		Size: 48.9 MB (48853748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aee6eb11d4d9526fe0e54fda7fb88ac928a854d7984a42bda3cb37c97b5bf0`  
		Last Modified: Wed, 17 Mar 2021 04:07:44 GMT  
		Size: 16.5 MB (16465148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df86454e90adb21821b7cddd370c663d6c80b9eaa3edcd63fdc9c0ce9e67da71`  
		Last Modified: Fri, 02 Apr 2021 19:22:07 GMT  
		Size: 181.8 MB (181771680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
