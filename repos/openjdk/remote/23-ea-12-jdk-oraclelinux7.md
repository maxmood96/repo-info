## `openjdk:23-ea-12-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:32bf8e016b52dd18c28a8154bdea0fda83ece10914cfcce9d377a12dc3a7f42d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-12-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:3fb2601f73e748b040f0243354e4f4594a729624292a42a9053ba9d9e3646ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267745095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceeb8d28f3cb15eed59cb36deccf65e638836880a4776a339ab43d38f400e98a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:52 GMT
ADD file:6c43f1bc1b598f7b1a5fc6f5c7951e8525eee01704f8f5e5caec8a944a4ecb4d in / 
# Wed, 14 Feb 2024 01:47:52 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 29 Feb 2024 19:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 19:48:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='892346bd29f50e248ab5980903e5759f73d8ac2b6ee0cd918e3acdb132eb8776'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e927b03ed3af88337e11918d05955c72b71c1664dc5791ba4a6590329004657'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ff90099b5a4df32952d1822d472a72c931c53a68c05a3ba7431ea0f85d54135`  
		Last Modified: Wed, 14 Feb 2024 01:50:04 GMT  
		Size: 50.4 MB (50389833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21acbc331b157c0a6041a427b0cf6544d5762ec1c4f6befc8e2c603e89b053`  
		Last Modified: Thu, 29 Feb 2024 22:50:36 GMT  
		Size: 14.2 MB (14231638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e483fcabb2db18afff94279e51572e2e69ce48111245208d0e51a0b289f9b250`  
		Last Modified: Thu, 29 Feb 2024 22:50:39 GMT  
		Size: 203.1 MB (203123624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-12-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:54ab1b8d26f620970aa92f73d64885bc29230c71cee08b374e483747f5a7139b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301ddfa514d667b11c1fa952662ac6246e3be636feaa267c84fecf30f2b5dce1`

```dockerfile
```

-	Layers:
	-	`sha256:eb24c46cf782822bc8dfbd0b211196bcf4e7a13d54b6489354fafdcf1e2157ad`  
		Last Modified: Thu, 29 Feb 2024 22:50:36 GMT  
		Size: 4.4 MB (4429923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db061cda2e456ddf69fbb78d6ac107b8578f384d408f0c4edb5dc7aaa0c968c`  
		Last Modified: Thu, 29 Feb 2024 22:50:36 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-12-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1d9cfa5cb1a5b35feaeb43ca8aadf167b5a901f2d3b31a9d8a5d08dfd303ccac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648980df3fc827d1c9cc60cf3edd7b4ba75bf8d8929e9831222156e3f0edc256`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:45:11 GMT
ADD file:8a1de5e2eb0c974503a07ee47335076f6fd201d377d647cbc5454453b71f05dc in / 
# Wed, 14 Feb 2024 01:45:12 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 29 Feb 2024 19:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 19:48:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='892346bd29f50e248ab5980903e5759f73d8ac2b6ee0cd918e3acdb132eb8776'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e927b03ed3af88337e11918d05955c72b71c1664dc5791ba4a6590329004657'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f12fd75c9aeabed692ef7b5d8a691db1e8f77911ac84bdaba43458300ab36fb9`  
		Last Modified: Wed, 14 Feb 2024 01:47:06 GMT  
		Size: 51.0 MB (50996218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f5782b608cb55c41f80fe5c4e8c6606f42add68733d4172117af3cbf2d90aa`  
		Last Modified: Wed, 14 Feb 2024 11:17:14 GMT  
		Size: 15.2 MB (15244449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318e3609db00b16ef4ff476b4e46ccb9c902bd3d1e0c46b4ff9731cc2203843a`  
		Last Modified: Thu, 29 Feb 2024 22:53:48 GMT  
		Size: 201.0 MB (201014390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-12-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:33e31fac6acc178ed9b7f059064a2d57f740d1983c6432da97dddc728ccf677f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4441830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a4b04acb6ba02ea64c015bb9fa68d61ceaadf292703c752d013cfbfcecc1f9`

```dockerfile
```

-	Layers:
	-	`sha256:e1f5058ad9d7fcd7dd99b6ac6d6c3e8109a85618bc0fe3e8a9ffbd25b2edcea3`  
		Last Modified: Thu, 29 Feb 2024 22:53:43 GMT  
		Size: 4.4 MB (4425580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb253ef08624b6e6182a8141cda050d61defe1aa1e1d2eb28ec0bc119ebd6ae3`  
		Last Modified: Thu, 29 Feb 2024 22:53:43 GMT  
		Size: 16.2 KB (16250 bytes)  
		MIME: application/vnd.in-toto+json
