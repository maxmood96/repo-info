## `openjdk:25-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:77364ae2bc2562a1f770bee066485c0bb26410e3657f01853d5baaa4e56e362c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:af6d120c1d3a5f00b34c67b2aec3fa2279bb8662049142838996c3118871ef2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309683366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bfde7855064ecab55eae3fe305284e5a1828cd601647658637ec7323a28d24`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:53:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
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
	-	`sha256:1d19e87a21f588780c1e2041d7a86fa8c5b805988de43968a7ad8419eeaf76d5`  
		Last Modified: Mon, 10 Feb 2025 22:02:26 GMT  
		Size: 49.1 MB (49097200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9cdf0ddb9ab240f0157d1a2e8b7eb6b7fa629a71987f6ed4ac9d26eb3f635f`  
		Last Modified: Tue, 11 Feb 2025 05:17:07 GMT  
		Size: 48.8 MB (48767933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a4b73366af81d3d4d1d41f76adf00ac8fa7f556b7e41fdcffae76899004a03`  
		Last Modified: Tue, 11 Feb 2025 04:46:06 GMT  
		Size: 211.8 MB (211818233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9db810be921860dd46ec2ef1cee5f1daa0c543c889923c2fb13ef668b5dc14f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f152e73847cf588e4e743e8f0926e0880a4a9ef9e3dc8ca3d297227e3a17e4`

```dockerfile
```

-	Layers:
	-	`sha256:1db3ce73c51dd4ebb44db85ce4bc15f0384630f812ccf5b87b87ab25c270ad91`  
		Last Modified: Tue, 11 Feb 2025 00:28:31 GMT  
		Size: 4.9 MB (4910727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0c6c349080a43ecc6a81b03c524104245e04e7613202c2dddf709af1f902677`  
		Last Modified: Tue, 11 Feb 2025 00:28:31 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oracle` - linux; arm64 variant v8

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

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

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
		Last Modified: Tue, 11 Feb 2025 00:34:12 GMT  
		Size: 4.9 MB (4908489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8558fa689fa7a3a9d5663d3143a8799cf284c4987155c0318ccba4e8f500d6a7`  
		Last Modified: Tue, 11 Feb 2025 00:34:12 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
