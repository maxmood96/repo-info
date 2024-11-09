## `openjdk:24-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:cc044924be703f16255eb85c3fc4c141531a39f81ce550db84c94994945e3d03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:068bcec5059782307a0ca5e98f14eecf686d215d5ce2e0620f462922674253ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280137703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9af895d1a94b4449fe64fcb32ba65a62cabb510663db788dea815ac1af58b1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Nov 2024 18:59:19 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 18:59:19 GMT
CMD ["/bin/bash"]
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 07 Nov 2024 19:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_VERSION=24-ea+23
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='4a83df6c5ba87f963cb8f7830f1ddef7dbe387b6884749411cdd4db6f3be6ee4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='76fba0034d8bd3edd8983162ebe459dfcdeb8d19e0202eb42803716fedf61a32'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8df6f63f2e2929475f749cf187aea26bf8fb9ab4d9a3bd0bab1fa00562e234f3`  
		Last Modified: Thu, 07 Nov 2024 20:58:25 GMT  
		Size: 51.3 MB (51274428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39be3859ca6eb7f858c8a693c56f5c6d74b53791a9a2564d3dc75656372be52`  
		Last Modified: Sat, 09 Nov 2024 02:06:55 GMT  
		Size: 15.0 MB (15029479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e880109e88da4a285f630d3b02cebe5dcca0d770392ecfe35e885d22c16ef45`  
		Last Modified: Sat, 09 Nov 2024 02:06:58 GMT  
		Size: 213.8 MB (213833796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2f8a95e126e47b6a71ee2b89f5d8090599fc74a553643546b34e63009425b32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2441849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84db895684b9a4b67f68fa600cab3fa09dcaa413c742e4e43f0105c63f30a88`

```dockerfile
```

-	Layers:
	-	`sha256:942102bda4523d67a5163b8c26cdc4d0d28e90c1826cf5cc80a0ea7637bad369`  
		Last Modified: Sat, 09 Nov 2024 02:06:55 GMT  
		Size: 2.4 MB (2425811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f17ab8ed2091ed66af32ae7242e8677ed31686a586ca8e805a07a7daff39702f`  
		Last Modified: Sat, 09 Nov 2024 02:06:55 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:08138c6b26274b2a45b1e33e8de4553c83b765b3eb92b44523ce79644d6227e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276038892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad277fc5e718c0ba51f4bfc806775e5ec967b48dfe5c67f3cc90d0f8caff6ca0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Nov 2024 00:48:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1eb947feb489743470a528a50fbdbbe5f33202c89f643437b01546e583abf260`  
		Last Modified: Thu, 07 Nov 2024 21:00:01 GMT  
		Size: 50.0 MB (49982495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8835d30e8162a2f089f49e425d12f0ddd1e5275c283a756d2c38fc17519577`  
		Last Modified: Thu, 07 Nov 2024 22:10:09 GMT  
		Size: 15.7 MB (15710467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae1aaa00946910f5c91d005e4e6bc180fa9e50aca5430cb4c623078fe075e2`  
		Last Modified: Thu, 07 Nov 2024 22:10:15 GMT  
		Size: 210.3 MB (210345930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:406b5d9ddd02ed9dbedf584de27766e068d4af7c295c2715a6048903f70887e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7e1951f83a585e85d2f24e5bddecfaeca5df1e2f0b8c512fb6c8412400f68b`

```dockerfile
```

-	Layers:
	-	`sha256:781ee01bd53dc000981d3b00a4d85da120c5bd0ea39c33c4c82d0681e306395e`  
		Last Modified: Thu, 07 Nov 2024 22:10:08 GMT  
		Size: 2.4 MB (2424033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009897079055819a45e382cb2bdb934ddaa79c2a8ef847ab505323f82036f5e0`  
		Last Modified: Thu, 07 Nov 2024 22:10:08 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
