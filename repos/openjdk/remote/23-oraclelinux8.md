## `openjdk:23-oraclelinux8`

```console
$ docker pull openjdk@sha256:2ee74ccb4d6586a85326e0ef4c248d636171ec7eb6f11b4c30817871938577ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux8` - linux; amd64

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

### `openjdk:23-oraclelinux8` - unknown; unknown

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

### `openjdk:23-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5f0a875ab4dacdd7f926c9134bb3e8ec05b7abb6b6ae782cd4f501809be04165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275234947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5660cb404f9ffbccd51824904cfefe44d7e0a78ea54ff90e3dd52cde82e04e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:11:59 GMT
ADD file:28329ccaf9d0f8718e6c37965272b9ac3d23fdb6d109ca304f4cdc12c515a2eb in / 
# Fri, 07 Jun 2024 03:11:59 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 21 Jun 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+28
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='55c6ef3457ea9e056119ae7ab55e4691742458d74fbe1a1a7cdb7d08527bee1f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='9844e3616fd6e16a94212badb2aee65f0a5805b43c587d80e9ae85174f18b984'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5522c693c44935bd999ae97ef2649e6707ffdfcf11d7d226a3b78066d03f8ac1`  
		Last Modified: Fri, 07 Jun 2024 03:12:59 GMT  
		Size: 49.9 MB (49926502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224c310d8d2c96f49a742c5059029d51003313d8a587e51fed9a9aedb25695b`  
		Last Modified: Fri, 07 Jun 2024 07:39:04 GMT  
		Size: 15.7 MB (15689949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c85d5758b8b56c9a3acc80b3c4adfb53aed52f33aa1b9e7cab0e25454aae8a`  
		Last Modified: Sat, 22 Jun 2024 06:22:13 GMT  
		Size: 209.6 MB (209618496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:273cff24d07a0713a78affb9083fc9e85fdeda870c9191b4ab51b8b221d9f176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f847ad940da877edce545a6eb592599e0891ae3ce3c18e0e979ef1c68553e256`

```dockerfile
```

-	Layers:
	-	`sha256:ade63be6b98fcc99970df1000a4d54878c58707df853a940bbd81c61191eee02`  
		Last Modified: Sat, 22 Jun 2024 06:22:08 GMT  
		Size: 2.3 MB (2267028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44b39fc26ca18d7baf78e3c54a4ab122d5ffd09ee4744ca5eb0bf5e360cd96e`  
		Last Modified: Sat, 22 Jun 2024 06:22:08 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
