## `openjdk:25-rc-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:f85391ead0dd98140c41cf7a0fbd52f5eec0c795f72dd799c4d0f14fc5d4e56e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-rc-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:183d1e494d0e3faaad4f875fb68555b5bc00af171fd23d4bd97043f3d72e336e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289831318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbd3a770b2738aee94ea8ef6b73ae94bd02be763fbf19851990b9e77631c986`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:58:59 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:58:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:816eb39a0552da23131629c02b98cdeccbfcda79ce23b4283b51ea7845bdb4e5`  
		Last Modified: Thu, 07 Aug 2025 23:49:07 GMT  
		Size: 51.3 MB (51323465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5baa83123fad45dea398e581e53c23f01d6123cd7fd8a0f67227854d5ff2d02`  
		Last Modified: Mon, 18 Aug 2025 18:18:50 GMT  
		Size: 15.0 MB (14976974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fdd5a2ec8f540315579cbc51691844a98669900c065632a64b222148c0acb7`  
		Last Modified: Mon, 18 Aug 2025 19:08:56 GMT  
		Size: 223.5 MB (223530879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:72d757145724cfd22a69e9a4346551318ce0ca64d25f230fa6dda3afbfce57c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3e15f8d4afd0fd01ec6677977826584173c26d1c5cfd4927d299ddf46e6b99`

```dockerfile
```

-	Layers:
	-	`sha256:f13a3a42bd806ff363aa1a32bb4996162cd9b9fba0e9366ae3d28275f2d2fdbc`  
		Last Modified: Mon, 18 Aug 2025 21:23:42 GMT  
		Size: 2.5 MB (2451042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cab46408a93543358f19bc2c5dee73db75168b18c7f9f22ccd1f59fa8a757cd`  
		Last Modified: Mon, 18 Aug 2025 21:23:43 GMT  
		Size: 15.4 KB (15434 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b3e92bde7b77125422a1853c35aba7fd8eca2069d0362f08a85b2f784cde6770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287049703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae68299d5151da58ab9c922d06764c1f86236c85bacb5f1e7299b8c873c2bb36`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:59:57 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:59:57 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00aea10d937a1f6a212468c9a6eb06043ca5276b560643f3c75b3b2d11325b17`  
		Last Modified: Fri, 08 Aug 2025 01:31:37 GMT  
		Size: 50.0 MB (50035024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c37ff1ab922b373a81603dbefbd345e8daf8902d5e960727d0807504e32e43`  
		Last Modified: Mon, 18 Aug 2025 22:41:23 GMT  
		Size: 15.7 MB (15672355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09508472cb2c44c2628fa599c650db7ed4aec046c970dbb7ecd247eb3aa5a1a5`  
		Last Modified: Mon, 18 Aug 2025 22:41:32 GMT  
		Size: 221.3 MB (221342324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:3fd55eab5931f1000284f9c607894f854ba780319316d106c6d77221839e569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e28076763f0cab7fd3f80f51f962fb811df82a8826175b9adffc91cca95b2`

```dockerfile
```

-	Layers:
	-	`sha256:e0faae7803474edf46d432d8b62b2a6aceee9b0e6a7e4fefe8cadb039eb45409`  
		Last Modified: Tue, 19 Aug 2025 00:23:37 GMT  
		Size: 2.4 MB (2449852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0847e57490659b8bc8cf45ac49c1498fd287d55960c9241c4946db49d9de893`  
		Last Modified: Tue, 19 Aug 2025 00:23:38 GMT  
		Size: 15.6 KB (15553 bytes)  
		MIME: application/vnd.in-toto+json
