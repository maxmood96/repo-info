## `openjdk:23-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:6133bb8feb4dd3f18515d815db22c3e9c8a519ce263bbef6cca65d72b7207acd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:88702690cce729700ffc56e50bfd56e43b6fdcafb8c2a07c91bea346346eb12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278022529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2f639d304b3b9a15de90f8fd89b4554f884908d8061c552842c8f572fbb496`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:53 GMT
ADD file:6f8c3cf297caf3b2a501a32c94a4fc0d2c7024f63d5e4b2215730b56faa6cdfb in / 
# Fri, 07 Jun 2024 03:48:53 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:427bba466fea4df7396a02ec368c5aa24d07ac80d02aa94eb57ba7af7b84b5a3`  
		Last Modified: Fri, 07 Jun 2024 03:50:01 GMT  
		Size: 51.2 MB (51219315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af118198e86ce5de690f112e5b9b759c933ddfc2cfd50fe350c0480199fac707`  
		Last Modified: Tue, 02 Jul 2024 00:57:55 GMT  
		Size: 15.0 MB (15035394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8eb0116d7ef39841c7979e83b90b317f14cce46737ebf3440856a4f4316c41`  
		Last Modified: Tue, 02 Jul 2024 00:57:58 GMT  
		Size: 211.8 MB (211767820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1904f1472b5936d2adb77d59bf1c69af79bedbb5a43dc90470be617c7eea508b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d0b2b339e54b329031155414919faa0f58b8961fbd85fc78ce2b5ef17af73a`

```dockerfile
```

-	Layers:
	-	`sha256:0c14f853cb94cc7d0f4b1063f953bf002e496c8d2e3963af0bec196842e48eac`  
		Last Modified: Tue, 02 Jul 2024 00:57:55 GMT  
		Size: 2.3 MB (2267559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a34e7e8c69064f5b32bb6ba39bcbedc323653d4bab6f099a978a883b8ca1c4`  
		Last Modified: Tue, 02 Jul 2024 00:57:55 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:324bdd75a34e3b564ac7ec12476f92e6b8470be802742d5a3734310eef854264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275244435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec72fdd0f02ead9f585df2163bd22e8149dc6adcdcf4cd84c9718ef135dd5e4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:11:59 GMT
ADD file:28329ccaf9d0f8718e6c37965272b9ac3d23fdb6d109ca304f4cdc12c515a2eb in / 
# Fri, 07 Jun 2024 03:11:59 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5522c693c44935bd999ae97ef2649e6707ffdfcf11d7d226a3b78066d03f8ac1`  
		Last Modified: Fri, 07 Jun 2024 03:12:59 GMT  
		Size: 49.9 MB (49926502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14fe16d50c54f92acd8a9f01692345e9731fbc9f75eea9480e538505c430d2a`  
		Last Modified: Tue, 02 Jul 2024 08:46:46 GMT  
		Size: 15.7 MB (15689994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b0e62becb0532bd2a2f4c639a2565c377eda4109527071e2e0dd500968638`  
		Last Modified: Tue, 02 Jul 2024 08:48:59 GMT  
		Size: 209.6 MB (209627939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:31a486335e68ad79c263eafdc6558a3939b8658b8b43c55af21791a1a6e9a63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6695dad3a8e441cf237914ed7e7be2a1b4a032c399e91cae8de117dde6d0843`

```dockerfile
```

-	Layers:
	-	`sha256:3fad7b22999bcc1845bd9d0ae289f870a919eece8a6d6105d67795e95f01f187`  
		Last Modified: Tue, 02 Jul 2024 08:48:55 GMT  
		Size: 2.3 MB (2267028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:578123296881cb1e6e8b0fff3327d488ea81168cae8dd3c68e51c8f74ab2c964`  
		Last Modified: Tue, 02 Jul 2024 08:48:54 GMT  
		Size: 16.1 KB (16150 bytes)  
		MIME: application/vnd.in-toto+json
