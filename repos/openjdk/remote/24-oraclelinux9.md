## `openjdk:24-oraclelinux9`

```console
$ docker pull openjdk@sha256:83853afd72355d065b3d8276f13e629d9dcc736c81d15cdec70d9a1a291564aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:bb1376086038d04fbdda7f7ee833765501e80d06a1fdc624fcff779d0d50b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299759672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b4dbf7a2e90124fae983c14e1e1659671c4a1c5543d2390fecb488a810ef8f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993d255fdae2cb850f5151c6c8c2da7a256cf222aed45dd557fc8a0109b37f89`  
		Last Modified: Mon, 29 Jul 2024 16:56:36 GMT  
		Size: 39.0 MB (39046948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0bc2a74a0816fb6e9c74789244567d1b3bbb945aea325aeac3000626608eeb`  
		Last Modified: Mon, 29 Jul 2024 16:56:39 GMT  
		Size: 211.7 MB (211718988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:ae2a6c4a8b9230a254bf590a93ccc2b20130467ca9863a1b73bae17fd30175d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235a8611bb63917851a37ff9ebeb243f6df90de493a6b98fd1803703a1c7d3ed`

```dockerfile
```

-	Layers:
	-	`sha256:5bfc8d4dd365eac042ad82df61d8663bf9769c4a33462668047565073d7616b3`  
		Last Modified: Mon, 29 Jul 2024 16:56:36 GMT  
		Size: 3.5 MB (3545961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f23ca0014a0435a6c1f76e0cc88981a654c6cddd7422e9c08662870397e9523`  
		Last Modified: Mon, 29 Jul 2024 16:56:36 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7c1bbc4c72c1d1793c3368cfbd6a37f09b832d46515fe4926da6fa7601b9fdf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296735088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51ff13caa519baea93142dbf88b015542e041efed14e2227a59fdeb356fa606`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 26 Jul 2024 18:52:50 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:52:50 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:52:50 GMT
ENV JAVA_VERSION=24-ea+8
# Fri, 26 Jul 2024 18:52:50 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ad921fcf79177162d3309d2311a35239dadd06ba0bfc2a43f424a280d671f59e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc05a41f1fc4e5287b22b98e9bf4c07f19955459a38a72c518e89eaffbbbcd74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12335bb1126bd80cd31b34b4fde93f2ccb7bb979403e778624cb60c3ece28c`  
		Last Modified: Mon, 29 Jul 2024 16:56:31 GMT  
		Size: 39.5 MB (39479870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb217d4ddc8935e348b181b316606f8dd090000ef04e9b7d755e27cd3d6e8faf`  
		Last Modified: Mon, 29 Jul 2024 16:56:35 GMT  
		Size: 209.6 MB (209602557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:4c5cd2042d2771104c00b13a6ae363125a9bc16cfcdbaaac3c0c482fbfd9441e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c700adadba873f3115f9925141430909ced5bbba0f4d8161db89e6efa8c28d`

```dockerfile
```

-	Layers:
	-	`sha256:f033e67f0bc3718c285a91b016b3c2fb25a58ddb245a53548b2de609ff234390`  
		Last Modified: Mon, 29 Jul 2024 16:56:30 GMT  
		Size: 3.5 MB (3544344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94bc19622bf4e5836155e4669dfdc56bc0df7adaa358091d97308327be6bca1`  
		Last Modified: Mon, 29 Jul 2024 16:56:30 GMT  
		Size: 20.0 KB (19978 bytes)  
		MIME: application/vnd.in-toto+json
