## `openjdk:23-ea-29-oraclelinux8`

```console
$ docker pull openjdk@sha256:c61f27f6d2820053eb1e7fb910ffb2c2cc77d361b1196a04794a29a321debae7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-29-oraclelinux8` - linux; amd64

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

### `openjdk:23-ea-29-oraclelinux8` - unknown; unknown

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
