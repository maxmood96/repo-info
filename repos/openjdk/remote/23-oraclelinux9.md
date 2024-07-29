## `openjdk:23-oraclelinux9`

```console
$ docker pull openjdk@sha256:d0afb0d72d93978e593347aa744346535052768f5d50b911350e44a92301c640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:a89af88e63394d7103bfcf918cf7bad9aec6e23e4a2ca6ada0062ae8f7d7a35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299357126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9ab835bd6477f378495e5ebd245ab8ac7c0c46d92a8a3a2271784eb5d8a422`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1946b917ce1759d91dae8c3a1445eadf31a076fffdc1e75d0f12dd90b6530d17`  
		Last Modified: Mon, 29 Jul 2024 16:56:37 GMT  
		Size: 39.0 MB (39047238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d444a01720114848e44e881a23f150b908ab1f7eec6fd04c643d5bc2677673f9`  
		Last Modified: Mon, 29 Jul 2024 16:56:40 GMT  
		Size: 211.3 MB (211316152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:6ee8111676acf611620acbf99b5166f1acdc4b5f2593520e7bca3277f5a15375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb1478ae0b900b781c786b605ffcbfc9f583be1a60b6691faf419468a5bf70d`

```dockerfile
```

-	Layers:
	-	`sha256:5b1fb126b0bb79ffa0303c64bf1661aa2da332b165f11941b744e8756f032a72`  
		Last Modified: Mon, 29 Jul 2024 16:56:37 GMT  
		Size: 3.5 MB (3545977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa3a78b6f534b469c4cea35d04423d56f15b0d7a6f02011205b48d131c86480`  
		Last Modified: Mon, 29 Jul 2024 16:56:36 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:453ad9aa6fc512ef35286135786af0e5f6e77c28354725e7c9aa6033f2321e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296310458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a025590d4860eca07f08256a4896291f17bf36dfbdb903513afa9b0e9b3abd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
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
	-	`sha256:db6681d2b00248b3d03ee31363579914b74731b8219fddc3c95bc41ff083a4fb`  
		Last Modified: Mon, 29 Jul 2024 17:02:58 GMT  
		Size: 209.2 MB (209177927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:bbe27ae075a9ab2c962f2dcbb9b3d799a90d8307da60535fe118133783b45155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ec814e446e817b80543a832954bcf213e4f6c6e846557db89e34407a9bf83b`

```dockerfile
```

-	Layers:
	-	`sha256:ddafb50e9253626bba815785fbb662b1077ada9c603d5b8ed85c00a54810913c`  
		Last Modified: Mon, 29 Jul 2024 17:02:54 GMT  
		Size: 3.5 MB (3544360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238c61b242fca426d212765363c46a2afd4a6ffdaae1f8a84a5814a8ed5b3c27`  
		Last Modified: Mon, 29 Jul 2024 17:02:53 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json
