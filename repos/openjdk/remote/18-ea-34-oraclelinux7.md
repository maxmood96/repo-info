## `openjdk:18-ea-34-oraclelinux7`

```console
$ docker pull openjdk@sha256:3b788cce6a59ac81011dc8bc62d8a4151241d72fa3882dc42d40c70e23b78a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-34-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:a6af5b47312e797994d861834d5feb5118b2b864e95a8754de4db1b6dacca55b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252373509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edd63e6cfc0d46fd0228629f35abbd53095afaebd9b4659473d536414e89718`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Jan 2022 22:34:30 GMT
ADD file:18acb1f3ef1ffe1aeaff1aa22861026180d22104f6f14dd8bc4656777800fd9f in / 
# Wed, 12 Jan 2022 22:34:30 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 22:51:37 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 12 Jan 2022 22:52:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 12 Jan 2022 22:52:20 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jan 2022 22:52:20 GMT
ENV LANG=en_US.UTF-8
# Tue, 08 Feb 2022 03:45:20 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 03:45:31 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 03:45:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e1d49338f200e5dab7ef55f9d3a37259af48812603e07ae59e43615f9038b27`  
		Last Modified: Wed, 12 Jan 2022 22:35:18 GMT  
		Size: 48.3 MB (48330956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c20bdba8622bf1a49d6c3edad81bd7ef39ec5a507eb70d2e536a70e60263ba4`  
		Last Modified: Wed, 12 Jan 2022 23:00:42 GMT  
		Size: 15.4 MB (15388577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad7cadba5743c036a5b5179e361ce1d65979729982fe28b87a8c79631b6df12`  
		Last Modified: Tue, 08 Feb 2022 03:58:42 GMT  
		Size: 188.7 MB (188653976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-34-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:05bb95cdbc185d74afc3860d637ec4d0887462086670fd65e5158fee2e0e1cc5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252956333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a25df3903aecf50a49256b54ab8d61cd933f7ac4a456c8ec150ebdd07521960`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Jan 2022 21:41:07 GMT
ADD file:64aef77ed2e10e924b07f118b92f579949f920597f01ce3580c3cd17fc289b87 in / 
# Wed, 12 Jan 2022 21:41:08 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 21:58:19 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 12 Jan 2022 21:59:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 12 Jan 2022 21:59:37 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jan 2022 21:59:38 GMT
ENV LANG=en_US.UTF-8
# Tue, 08 Feb 2022 06:26:28 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 06:26:45 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 06:26:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89ad662320eff0a72aa4fc7f7af6e2a2ffe2dc642aacc7fcf25ada107b2cc3de`  
		Last Modified: Wed, 12 Jan 2022 21:42:00 GMT  
		Size: 48.9 MB (48902767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcbd5e1a30531d664d4f4f1f2c5a28be251ea96d8b492a51eabd8b7339c2f97`  
		Last Modified: Wed, 12 Jan 2022 22:12:56 GMT  
		Size: 16.5 MB (16464202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc2af267198b56e8d7a505565c9e3ceb299f0be4f0662f72ddc9fae2b5fba1b`  
		Last Modified: Tue, 08 Feb 2022 08:25:23 GMT  
		Size: 187.6 MB (187589364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
