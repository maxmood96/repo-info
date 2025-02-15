## `openjdk:25-oracle`

```console
$ docker pull openjdk@sha256:48249000d2a84730a838ad9c01aad122c90920753ec2b936cbd2f078c97fd742
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:74f648c28ce36fb952ef3a936c9ed7dfc86ba4753904e9b6e803eafa86b55ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309712532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f482a65db2b4a43874c3dc1f1b12edac455eccf45f65e43d0c4449e78139014a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 17:38:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 17:38:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606554b6fcdbcef8cf40173c823928d54e16f95896087ca83ec5ebcad5b4663c`  
		Last Modified: Sat, 15 Feb 2025 01:28:59 GMT  
		Size: 48.8 MB (48765811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e7c29008cd9892a2ac7710a8ac072317e4552b267d784387c0bdae5a568a0f`  
		Last Modified: Sat, 15 Feb 2025 01:29:09 GMT  
		Size: 211.9 MB (211855830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:94602a874fbce21bdf28e1d84fa87154b120fd0e6f6ed3bd9a138138a322b741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cdefe6286a7d9c1a52f7ea6a45a02b1b26cd474387f13971e037811079baa3`

```dockerfile
```

-	Layers:
	-	`sha256:0301b83a151739accb1babd1e1942527a4269e1afa10a7a0660a3ffaab18a029`  
		Last Modified: Sat, 15 Feb 2025 01:23:57 GMT  
		Size: 4.9 MB (4910767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b608568c986af149a48b9b4dff21614f01c7d697a1d444c45fc4a3ee5172084f`  
		Last Modified: Sat, 15 Feb 2025 01:23:58 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e62e28f1621d2f3dd776da6536eda5e46558582df425c4c6c9478a11f1d4536b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306648253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4e286e722f923f1530f408ee4334ef35ad6ba57184c401593e0eef30684378`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:53:06 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63067de277ccb20d99a5e9991dc66234bee83ce4c0d53f55d9f51995ad436f8b`  
		Last Modified: Mon, 10 Feb 2025 21:15:36 GMT  
		Size: 47.7 MB (47669546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e55e0b8b34ea5b3ba919ce4a6401eeba17103634f66be3d05c3f942cc693f8`  
		Last Modified: Mon, 10 Feb 2025 23:18:51 GMT  
		Size: 49.2 MB (49194060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1af2e4923ec73802217aa39c7fbdd0e8953953eae0f77bb63bb97912593b1d`  
		Last Modified: Tue, 11 Feb 2025 10:07:23 GMT  
		Size: 209.8 MB (209784647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:58404b32a2c779c041bb18489aef8303be412be1b2425b588428f4ba7e36712b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fcd622deca720dd58f5801fdd603956ce80f74f8f171436077730cd4aa9794`

```dockerfile
```

-	Layers:
	-	`sha256:908d52556b7bfd2fc088a950d3ec9f4d9add49791bed555931fbc37b7ee2e96a`  
		Last Modified: Thu, 13 Feb 2025 01:24:05 GMT  
		Size: 4.9 MB (4908489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8558fa689fa7a3a9d5663d3143a8799cf284c4987155c0318ccba4e8f500d6a7`  
		Last Modified: Thu, 13 Feb 2025 01:24:05 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
