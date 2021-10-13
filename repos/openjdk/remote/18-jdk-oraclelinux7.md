## `openjdk:18-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:63baaa87786de43a6e6aa189755bdf3cc1c6518f033c4e35b31dd8ca47cbaa42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:919806600655c92f61f6d34d12a8cf2b7ab7ca3e3892c4079b08ed5b3b52fd9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.5 MB (251534188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492b04e5eabeef04101eb0a7965cb2660777f28e369bbfd7c45c4ffe611c55e6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Sep 2021 16:28:42 GMT
ADD file:a9e7957ff3541c254a266620f438cb7ec181b31d50f939d0e687716cefdc7cf8 in / 
# Wed, 29 Sep 2021 16:28:43 GMT
CMD ["/bin/bash"]
# Wed, 29 Sep 2021 16:54:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 29 Sep 2021 16:54:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 29 Sep 2021 16:54:15 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 16:54:16 GMT
ENV LANG=en_US.UTF-8
# Sat, 09 Oct 2021 00:50:53 GMT
ENV JAVA_VERSION=18-ea+18
# Sat, 09 Oct 2021 00:51:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='425b4f9afe439b4690593e5f78e27b6687525114a66f652c285a7dcca95b1961'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='af5b0d66cf7c4f7450066fd67dbb0d48c17bcc5ab8ddb105cf7fe66176427f87'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 09 Oct 2021 00:51:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2294629c97e56d38612a31e50aa9a544bb9ea9a60646d016dcde035fd309dfe8`  
		Last Modified: Wed, 29 Sep 2021 16:30:26 GMT  
		Size: 48.2 MB (48241319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa27d00ff441932dc4be9fc9662577510adff660e4486fa443768e0ca6d260e`  
		Last Modified: Wed, 29 Sep 2021 17:03:16 GMT  
		Size: 15.4 MB (15433173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a383685129ad6a872ebc03bb2d1626fb414d7733cd56b51e5d6cad6c8fda2912`  
		Last Modified: Sat, 09 Oct 2021 01:00:17 GMT  
		Size: 187.9 MB (187859696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:511c7d52270aabd8c2de725a2d14faa73b0bb71a4489951fac3a0e1bdff285e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (252047695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ce3a5376ce56d509713ce6e24a3f2f77e8e876e8ae69a168f253c298123cff`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Sep 2021 09:28:50 GMT
ADD file:affde62a0aaf80f490cc93e1f691166a15a32c6ef6bc21af35a6659d24c8b6ef in / 
# Wed, 29 Sep 2021 09:28:51 GMT
CMD ["/bin/bash"]
# Wed, 13 Oct 2021 05:59:43 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 13 Oct 2021 05:59:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 13 Oct 2021 05:59:44 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 05:59:45 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 Oct 2021 05:59:46 GMT
ENV JAVA_VERSION=18-ea+18
# Wed, 13 Oct 2021 06:00:08 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='425b4f9afe439b4690593e5f78e27b6687525114a66f652c285a7dcca95b1961'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='af5b0d66cf7c4f7450066fd67dbb0d48c17bcc5ab8ddb105cf7fe66176427f87'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 13 Oct 2021 06:00:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f5eee715870559160403451bcd7b891478e0df052b7f9456144f3e89e5b994f`  
		Last Modified: Wed, 29 Sep 2021 09:30:28 GMT  
		Size: 48.8 MB (48828923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d586374e21f8d72195ddee3ded7c701588c9aaf00feb9feeaf6a586f435121df`  
		Last Modified: Wed, 13 Oct 2021 06:24:14 GMT  
		Size: 16.4 MB (16438619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65f58efb12589be092310702f8cbcef49bfb4bbfa3c1ebc1c7510fa77f1b8fa`  
		Last Modified: Wed, 13 Oct 2021 06:24:28 GMT  
		Size: 186.8 MB (186780153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
