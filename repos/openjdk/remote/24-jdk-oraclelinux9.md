## `openjdk:24-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:2b6a2f1f9944d09e2a3cd217a979013c4be4f5777bd5683faf8071398e0082a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:c523c191d7e471170f6a4184da41f07b579869f531865823e931c43f7c1db1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310696539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deea31ac117607ba80134d346eb1dc2f0d8b4ab32eb292d8ed6591fd5154da0c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758b5cdc0820cd282118aa6035c71428802b729afa056fccb151397acccf0a`  
		Last Modified: Sat, 15 Feb 2025 02:10:02 GMT  
		Size: 48.8 MB (48768601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d04b07e7673fe63f27989699cac217c32fca630b277edca3b6b2e6a9186373`  
		Last Modified: Sat, 15 Feb 2025 02:10:06 GMT  
		Size: 212.8 MB (212837047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:73346847fd2bb9a7b8f07f733b2a3d03f9cfb9be048cfc1bb3c2bb567ce73fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7564c366311efb7099bb044c07cfc7977fb68702d0ba2cf04c527a34f93e7208`

```dockerfile
```

-	Layers:
	-	`sha256:d4a2100e9eb7b770519cfde2d824374c6061ab932bca9c5d7c1f81a23071f5cd`  
		Last Modified: Sat, 15 Feb 2025 01:23:16 GMT  
		Size: 4.9 MB (4909455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eda9eb3385d5fa1b05c68bc5d519801cdcfff2f99dd428c3fc59977266e7e06`  
		Last Modified: Sat, 15 Feb 2025 01:23:16 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:47a960decf116da8bac771d2e04c85835fc8872e4b01d8fc083f16e7e4032af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307645021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7b045d4d2bfa4b54ebd1d8e9c4ab4a249522e726eae949f138a79c9245772a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca163d5e019bf3d8fffa833ce86f630b0f296399ec45fe5da979a5e604b2e20`  
		Last Modified: Sat, 15 Feb 2025 13:36:07 GMT  
		Size: 49.2 MB (49187884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac2acf1aef584af944f1f1193da211778df744f6616cfaa8a1ac094ac65b1a0`  
		Last Modified: Sat, 15 Feb 2025 14:43:26 GMT  
		Size: 210.8 MB (210787922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:b3d706d4ba2548dfef5fb14dcad2a5caac4b4e935850c18608ff10f628194f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888a504c83af21708e3117c7d2d2e31faeb1a27f2d035ac5da9de3fd610447e1`

```dockerfile
```

-	Layers:
	-	`sha256:7ebf9352bb9ea5e912f3544068d35e75d720e7639aad456febe11ba294a277a3`  
		Last Modified: Sat, 15 Feb 2025 13:23:18 GMT  
		Size: 4.9 MB (4907145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a84664090ba131788a1a4b054b8379c23387e1e472319098c6e6b212ef7a665`  
		Last Modified: Sat, 15 Feb 2025 13:23:19 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json
