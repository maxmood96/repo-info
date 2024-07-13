## `openjdk:23-ea-31-oraclelinux9`

```console
$ docker pull openjdk@sha256:f519e4b7ba72e14eb45b91aba8165c2f2e296b1e70a5c68466b85db71805f5b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-31-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:42402bd0c9431aadf2a000c8c9273ca12f716d7b0a0f66d860b0066a49123139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298171895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcef58001bb334b8b57224f43df6cf29e935c3dc4b1fc303aa7a87cd25f878b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c77822463f50dcf3516376e15ec30057a89604a1a2eab9873d521f343c1180b`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 37.9 MB (37872153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06af5af9eee62452221f2f29a3a817cf9ba961c46205fa9dfff4c510ecec607`  
		Last Modified: Fri, 12 Jul 2024 21:57:28 GMT  
		Size: 211.3 MB (211306006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-31-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:335a7c5df1000f04a42a61ab96a08534e38b7dd3e268668fc0b2a7e13a71137c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950dc04881855b6fe91f815af2c9b6ee2abd4165a7d037db9e5f81df41921c81`

```dockerfile
```

-	Layers:
	-	`sha256:f564b0e47abcc7cfb111098b207ac23f16d07ed4ed66924fce547cd5c35a0235`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 3.3 MB (3333244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1775e1518bc231842c0d8c1290bbc85e7bdc5ed4139ca7e6521e27a7cbc4a177`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-31-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e8c0d537fdc7c4ca0599947a5f9fa62ec54190b0e7cdcd4a81a805189fc8f6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295094478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c166b9ea98370605d7ed314484374461bcb300a15db12c6d4565d00e19ba7980`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129baf21359e4eb83f9d1391c216edfe6dce92354dbd70df14232415144a124`  
		Last Modified: Fri, 12 Jul 2024 22:04:48 GMT  
		Size: 38.3 MB (38259249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9a00d939815c50426c216f154aff6fd9aef7c065f90a37f68c3574784f5b3c`  
		Last Modified: Fri, 12 Jul 2024 22:10:35 GMT  
		Size: 209.2 MB (209182568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-31-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f9d564c63c104474b22514df2968b4077bde92d7011a962ce73e4a7f962f104c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5918d729433ebdef04e83b0ed14f7fcf18a3b37ffc2bef6bc8598f067b432cc`

```dockerfile
```

-	Layers:
	-	`sha256:cfed7b8049daed2ced7b8459df3d69f668013ec86610e8f6f08c0ecdeea2700e`  
		Last Modified: Fri, 12 Jul 2024 22:10:30 GMT  
		Size: 3.3 MB (3331627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf095faccb79c0798369fb4505364eef0f1d151baf152400b3f5590fb7d6d221`  
		Last Modified: Fri, 12 Jul 2024 22:10:30 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json
