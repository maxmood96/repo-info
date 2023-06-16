## `openjdk:22-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:6301dd3a574be34f7c5c9edff7509d8092db030bf13d3df73a2b50264fc6ff39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:4d8c5b5ebbed517c5285a7fbb17720b063d5dd3a4858e6e435e1405cb3950d25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264597842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7dcdf456e88050cd77dca1aad45b3f79eebe5778727e87a02ae0accb57f1701`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 04 Jun 2023 17:54:32 GMT
ADD file:39d09c6c7c3a0f64981f5cbcb12cc8f0128979c3d4b91d74c84fe62aca5ea87e in / 
# Sun, 04 Jun 2023 17:54:32 GMT
CMD ["/bin/bash"]
# Sun, 04 Jun 2023 19:01:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jun 2023 22:26:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Mon, 12 Jun 2023 22:26:29 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 22:26:29 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 22:26:29 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 22:26:40 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jun 2023 22:26:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e0c3751e6482e67b70ffad144b2cb9aec9be672df2642a322e875e51b748aeb`  
		Last Modified: Sun, 04 Jun 2023 17:55:32 GMT  
		Size: 44.9 MB (44872720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5b8981d150f5706ec1b30f459a99b1c25abb86225512911608e4175546c8d9`  
		Last Modified: Sun, 04 Jun 2023 19:02:11 GMT  
		Size: 15.0 MB (15004426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede12e8bc9615c77ffdc13709569c7eea1c5e9f139b87d298d66056e999aebbd`  
		Last Modified: Mon, 12 Jun 2023 22:29:14 GMT  
		Size: 204.7 MB (204720696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:aa3067068e4bcdeb8e0aa4b8b2943161f9eece64002a3811ead93dc8fa41f63a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262324141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0fa74fc42d5366ae4633b71515e0a780dfa1b4c3e6961d7fb43b5b140ac65f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Jun 2023 23:40:30 GMT
ADD file:37cef5fcd08f57d005adb8f14f69ecc78a9c669280f45f7d81b1c899489e93ba in / 
# Thu, 15 Jun 2023 23:40:31 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 23:59:49 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 15 Jun 2023 23:59:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Thu, 15 Jun 2023 23:59:49 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 23:59:49 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 23:59:49 GMT
ENV JAVA_VERSION=22-ea+1
# Thu, 15 Jun 2023 23:59:57 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 15 Jun 2023 23:59:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:029ab4a5f8e75aadbbba1505624cf10a4c35a0fd897cc85b9e7536785b8ba37c`  
		Last Modified: Thu, 15 Jun 2023 23:41:45 GMT  
		Size: 43.6 MB (43601336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cca9ab147b9b93cf01a583c33e8ade844f6d31bfb69334e1614ef5dd4d6a973`  
		Last Modified: Fri, 16 Jun 2023 00:01:25 GMT  
		Size: 15.7 MB (15673775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcbbe4f5220c3c0786ed24c23f9c9c01e3e4d5aa06b4d49e7defe92c7578b59`  
		Last Modified: Fri, 16 Jun 2023 00:01:35 GMT  
		Size: 203.0 MB (203049030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
