## `openjdk:23-ea-35-jdk-oracle`

```console
$ docker pull openjdk@sha256:56094926fff5409e0b248c5a797c8d5c7d8c3ff8e42112b2ad45b5269913034d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-35-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:407d847aae44738b0af6b6b43e401fa7e3a51ae56f150b4fb05be46879802127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299356481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e530f6d1145bb85ac68470a141fc52c733d5d74734e7dc27591ba82a1d9c55`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Aug 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+35
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='5387c8da8acb4261265c12bb46cea856c248d70bf9d64164019b74ed96545655'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='d5765b057a4eca4913ddd3d661e0ecd9cb182d4ad79359a645e427bdadd574d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edacfed42f286c8f364caaf7c2dc2d0328ca3fee7345bf9d85be4bed27812e92`  
		Last Modified: Mon, 05 Aug 2024 18:57:59 GMT  
		Size: 39.0 MB (39047438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0835696e71fc021aefd9fe7ba3449bd6e5773835e55026bd7367d853fb0888e7`  
		Last Modified: Mon, 05 Aug 2024 18:58:02 GMT  
		Size: 211.3 MB (211315307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-35-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a6e897dcf2d370bf524533c85f685e130bc66cde17ec92976c77a945005396f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f344d4f5fc5b071e4c05867cf481dd387662ff1713f1b9f5f1b20d4bfae68097`

```dockerfile
```

-	Layers:
	-	`sha256:48fbc5d09e6cfee5bc7877a696d3d09bd72e878c0478f30df61e6e535540bc8b`  
		Last Modified: Mon, 05 Aug 2024 18:57:59 GMT  
		Size: 3.5 MB (3545977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c460ecfe571e242c15fca2d31d3f3fe10e9f2e51aa542c4ba13e9aeca0996b`  
		Last Modified: Mon, 05 Aug 2024 18:57:59 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-35-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9568d2cbbe0895857305a8f7194ec1b856d711f769040bfe4bd17c352e700189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296310110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d97d07fa4b89d30b673d207571c764dea47b9d327431b3e566086b33318aa6d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Aug 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+35
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='5387c8da8acb4261265c12bb46cea856c248d70bf9d64164019b74ed96545655'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='d5765b057a4eca4913ddd3d661e0ecd9cb182d4ad79359a645e427bdadd574d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
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
	-	`sha256:a7521d566e0bac1bd61f00d619cb5416c948ff814f3990a5a68ff8a8c719f921`  
		Last Modified: Mon, 05 Aug 2024 19:11:55 GMT  
		Size: 209.2 MB (209177579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-35-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5a405983ac4d728ae4a0d01560f5dbb157779099c7973482eff3f433ca15e314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30cb460645cf70fdd2961f4c5dfabcac85c1955bb01855e5942835fe8af0d4b4`

```dockerfile
```

-	Layers:
	-	`sha256:2650d30cffa3d0e80444366d87e8243253365c2617b81c15b530064c874fbcc8`  
		Last Modified: Mon, 05 Aug 2024 19:11:51 GMT  
		Size: 3.5 MB (3544360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fbfb445981f164ea086f6ba8f4c87805843f956144138d03f2bedb7875f69a`  
		Last Modified: Mon, 05 Aug 2024 19:11:50 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json
