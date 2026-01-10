## `openjdk:26-ea-29-oraclelinux8`

```console
$ docker pull openjdk@sha256:9fe917ba69310dfdc581a500618221cfe7f5da45cacb69635cd42c71e79b305f
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
$ docker pull openjdk@sha256:762e8347f2b9a7accf6a4647e7244bc4ab8ea1c14d16d7fbba22f14af2582c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292108787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3327707b9e49e22ec517db06dc1c6c2508879e2bb03f93d1a96ec6e03aad950`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 21:42:51 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 09 Jan 2026 21:42:51 GMT
CMD ["/bin/bash"]
# Fri, 09 Jan 2026 22:10:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Jan 2026 22:10:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 09 Jan 2026 22:10:54 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jan 2026 22:10:54 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jan 2026 22:10:54 GMT
ENV JAVA_VERSION=26-ea+29
# Fri, 09 Jan 2026 22:10:54 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Jan 2026 22:10:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5daa2797aa97d66d1615bd1c3686dd694a6f5fa7082128bee108f37838f634ba`  
		Last Modified: Fri, 09 Jan 2026 21:43:15 GMT  
		Size: 50.2 MB (50181216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4912b15c7728d937d8ef718136da93d85c37539367b31eb0004fb030f9fc7038`  
		Last Modified: Fri, 09 Jan 2026 22:11:32 GMT  
		Size: 15.7 MB (15700518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363f24b7425e4ee4143f0ae789fb4c8bd1c04779f7d30ed04aea96b07500d4e6`  
		Last Modified: Fri, 09 Jan 2026 22:11:43 GMT  
		Size: 226.2 MB (226227053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ff484f591bd29da95428ee2c07fd1c3ef21a8a430bec64c097f3f941c277b899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a943a4db97c0bd3d8e5365344cb78cad6c67d26943225f1a2d88030fa298a755`

```dockerfile
```

-	Layers:
	-	`sha256:10a09314fd68ebbb4de61edd2bf7eb2519bbc28126a9d1b0e844918f28f29dcd`  
		Last Modified: Sat, 10 Jan 2026 01:23:48 GMT  
		Size: 2.4 MB (2447492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a82005f01ebe3daa66106c0bce72eb707878ae9f2ec8c186e3f118ca2d9e956`  
		Last Modified: Sat, 10 Jan 2026 01:23:49 GMT  
		Size: 15.5 KB (15461 bytes)  
		MIME: application/vnd.in-toto+json
