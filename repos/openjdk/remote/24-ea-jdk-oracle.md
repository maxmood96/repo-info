## `openjdk:24-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:40f87b0d59dc556a1bc3e22f77ad29b1a3896a4eda88723a4dc6c2c207e6fb00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:20ecb5f184963a7ddd24e501b1734ff14e313f99f2fe472ebb81b35d66c96c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299766756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da16f755258e672f4403198e121cff48ceec2615320c2c480076dec79fc0e82`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed24f5cc22b129f6a10395430c0259a12a3f52cec000b4a668f5687e8520e3b`  
		Last Modified: Mon, 05 Aug 2024 18:57:55 GMT  
		Size: 39.0 MB (39047151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a701574b125898eedf90cbc9a6588741d8c06725b0147e11e130628ac0add6`  
		Last Modified: Mon, 05 Aug 2024 18:57:57 GMT  
		Size: 211.7 MB (211725869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:1b23024fef2606ac1babf947c5aa44e6d899ece3a06a3cb0842f2355edd52ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ab30c83f5545d9e256103b6a7153c683b61c0793ff2f4a15e759f4d994b0d6`

```dockerfile
```

-	Layers:
	-	`sha256:20e4b81ffe267add70068000a336a2a82c6322e3bae9cfa1b2c96b30d05c1547`  
		Last Modified: Mon, 05 Aug 2024 18:57:54 GMT  
		Size: 3.5 MB (3545961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1336b686fddd66b91bbef8b866ac76006669a6bc1f96844c04f0ceb0575dba`  
		Last Modified: Mon, 05 Aug 2024 18:57:54 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8ea8228f0c941be2f2ac026ec3d5de99112a57227ef4055145ca470fbf53075c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296733970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5caa9ed794e8b078e3d353f58154ccb7b839da0a79dc32da191a5ec56a9f11ae`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
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
	-	`sha256:bbed2eb45f81668975518b129f27d66e8f4b664f26ad60fde5b5960840908d69`  
		Last Modified: Mon, 05 Aug 2024 19:06:30 GMT  
		Size: 209.6 MB (209601439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:7c3edde0b1ceed4d2c4d2ca157ea3d7ce142670f376f1a2cf5e1d038ae544007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363c050bf819dde6a76b7c53576bfcea85a70ebb4161f1129b8546b695477873`

```dockerfile
```

-	Layers:
	-	`sha256:81b8e23f9fe81763bba513bcaa3a3d34ff91176b3e7b649b101bcd0948024f6b`  
		Last Modified: Mon, 05 Aug 2024 19:06:26 GMT  
		Size: 3.5 MB (3544344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c0ba2c1da3026e99e1f16f589074b172c8104b00eacdf490364d7627ff0a8f0`  
		Last Modified: Mon, 05 Aug 2024 19:06:26 GMT  
		Size: 20.0 KB (19978 bytes)  
		MIME: application/vnd.in-toto+json
