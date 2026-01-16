## `openjdk:27-ea-4-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:5f802baa0955da8935ca62b30b6b5f10eaf2170d8af7c8377ddae974aa67be4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-4-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:0df533fa1982d7e059b7fe3b69414417f8a071929067bc65132b3f8f10aa98cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294823544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd903b3a04032e8c20e17a3679a6bf27cfa52ce78e96d954109561cfd397d10`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 21:43:04 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 09 Jan 2026 21:43:04 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:08:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:09:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 12 Jan 2026 20:09:00 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:09:00 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:09:00 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:09:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:09:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0ddc6852d18db715e5e4c3edd3fa8bdf8afc37b9507d95d8bc0194012c32432`  
		Last Modified: Fri, 09 Jan 2026 21:43:27 GMT  
		Size: 51.5 MB (51465737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061067420857e91535b458d492ca985dc579713d6ef94c8214ccee904a54988c`  
		Last Modified: Mon, 12 Jan 2026 20:09:34 GMT  
		Size: 15.0 MB (14989314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ecb5465198cebe3452d823adfbef1d9de0041bc1218f56a11f760da91f675d`  
		Last Modified: Mon, 12 Jan 2026 20:12:53 GMT  
		Size: 228.4 MB (228368493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:074c44f18e11a898c67e63c728c69cd45c6d7a2c53ef42cf0d8831e60d6250b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679cf4fa58339f63b5913accff71f1b02981b6d11173c42e2c08d124f85fc93c`

```dockerfile
```

-	Layers:
	-	`sha256:777279a48da0f6c235d13cfed4978e5aab6a407c0e1710773720085e9c5f1492`  
		Last Modified: Mon, 12 Jan 2026 22:26:39 GMT  
		Size: 2.4 MB (2448674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bdd3378ca57c86a94bc092396b359eca5371fa5bc5ab1524f9a359ac78b9746`  
		Last Modified: Mon, 12 Jan 2026 22:26:40 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-4-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a9d186c6b0670c2a819340d039b842b033045255dfbacec621bddfba1c1f70aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292196826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e266e50c28034a0893e2af0dbd5bfe36dcc9aec527d1f70238227bfc0c5bd6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 21:42:51 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 09 Jan 2026 21:42:51 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:09:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:09:59 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 12 Jan 2026 20:09:59 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:09:59 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:09:59 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:09:59 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:09:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5daa2797aa97d66d1615bd1c3686dd694a6f5fa7082128bee108f37838f634ba`  
		Last Modified: Fri, 09 Jan 2026 21:43:15 GMT  
		Size: 50.2 MB (50181216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332a38531011d35beda3c670e2be4635b17e5723b8bb32e6c9cc2187fdc14ed5`  
		Last Modified: Mon, 12 Jan 2026 20:10:32 GMT  
		Size: 15.7 MB (15700548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6878f6c264df22f1e6e1b69663a72e379991f7ec1b972b618e8b305b7ae63`  
		Last Modified: Mon, 12 Jan 2026 20:10:41 GMT  
		Size: 226.3 MB (226315062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:4e10b0a37470221e44a37ebf8efcb30f66beb06e6eefb0c6bebef54a8eab10b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617ff0d616dacc2ee4a541df420cc564d429a3c54a63f7e5de7853d591699e83`

```dockerfile
```

-	Layers:
	-	`sha256:11ba499cf8f8a494270ff5f43e08256b0ebbc27e61e347f0bb99aaddb43175dd`  
		Last Modified: Mon, 12 Jan 2026 20:10:20 GMT  
		Size: 2.4 MB (2447484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2131096c420d2c413a29678451b5046e10accf88b1cb2cbae32f7d7d6cfc3f83`  
		Last Modified: Mon, 12 Jan 2026 22:26:45 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
