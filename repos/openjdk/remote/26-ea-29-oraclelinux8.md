## `openjdk:26-ea-29-oraclelinux8`

```console
$ docker pull openjdk@sha256:a83cfee281b6db6d3bf8cda29b61098f9117ea00006a22962031bb9302f685b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-29-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:730dfc0b41ac0847a2a3644db47d5b663deec3b752b4cc9a214194185815beab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294751385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd851349c2ace2ac7be42b97616d3e3dfcf199b840a6d8c2d411bbb2f39a32e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 21:43:04 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 09 Jan 2026 21:43:04 GMT
CMD ["/bin/bash"]
# Fri, 09 Jan 2026 22:10:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Jan 2026 22:10:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 09 Jan 2026 22:10:36 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jan 2026 22:10:36 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jan 2026 22:10:36 GMT
ENV JAVA_VERSION=26-ea+29
# Fri, 09 Jan 2026 22:10:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Jan 2026 22:10:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0ddc6852d18db715e5e4c3edd3fa8bdf8afc37b9507d95d8bc0194012c32432`  
		Last Modified: Fri, 09 Jan 2026 21:43:27 GMT  
		Size: 51.5 MB (51465737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443a4c595956fed24dda84181abe9cb07dbbe906943f80033bdad8cf5cae3aea`  
		Last Modified: Fri, 09 Jan 2026 22:11:12 GMT  
		Size: 15.0 MB (14989233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c8061032a772c77274f5b287fe651af6b620ca85d78043bee3297fdf90f77a`  
		Last Modified: Fri, 09 Jan 2026 22:11:34 GMT  
		Size: 228.3 MB (228296415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1f3fea409f56a2999eeb670e24c38995176a9782a50f09100de8ebd51efc19e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4972f60992b1436c72fda0b161b5e1557120fa48db5208feb664abc1c49218c`

```dockerfile
```

-	Layers:
	-	`sha256:863473134d0ced11df993e8c86c90bc558347888ca547b618d666c01bd8383e3`  
		Last Modified: Fri, 09 Jan 2026 22:23:55 GMT  
		Size: 2.4 MB (2448682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6919bae070bb153ef54778726c64da1f88c7333f0bea28d8ab90b26f4c623cd`  
		Last Modified: Fri, 09 Jan 2026 22:23:56 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-29-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:21bf35fd13545ce19621a8f55ecde09ed203290bc2821d003b947405e9390ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292101903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223ba6639da9ad495f8e4d3d8fee061a31a9801157b83817f261bfc69f2bca05`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:42 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:42 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:12:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:12:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 24 Dec 2025 06:12:22 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:12:22 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 06:12:22 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 06:12:22 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 06:12:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c56c47048941ddf04da7dcfda383c6b40da72e218826ef10c27b29f2fb9db04`  
		Last Modified: Wed, 24 Dec 2025 05:20:02 GMT  
		Size: 50.2 MB (50177032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2aafad89680ce7aae09a351aac5dea7d7c065b1af9b97a1a4f16b68455da7e`  
		Last Modified: Wed, 24 Dec 2025 06:13:00 GMT  
		Size: 15.7 MB (15697396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4084c0df3f48486b868595c6853a26862a186680a81419f6a19f893daaa1b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 226.2 MB (226227475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a8d0015fea7d463ff3e618fab3615abd46e285c51cb570336b6a2e3bc05f78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b964ed57f9fa4b43623fd04917867d7057b06d88d643333e3869d202e656bf07`

```dockerfile
```

-	Layers:
	-	`sha256:3df044f52c9a738907b90b95a9a52caeb4e7638d880740eb6b96c8c42c6c172c`  
		Last Modified: Wed, 24 Dec 2025 07:24:08 GMT  
		Size: 2.4 MB (2447482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeef9fd2779d56cca7dfa22bc62dd6604d3d92721f5e8a775ba743114f39b0d8`  
		Last Modified: Wed, 24 Dec 2025 07:24:09 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
