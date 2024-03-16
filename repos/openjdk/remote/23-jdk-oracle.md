## `openjdk:23-jdk-oracle`

```console
$ docker pull openjdk@sha256:1025e9263b51fe4e677896a85fb9624e49c256f1bd7bfca58a5683197e9c7865
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:79163db329c780a8c8f37f84c6235dda02f3356825fd08dc88d91544f96898cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289476999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5369da73efdcc05eb015464f6c53e592e71088f3c9333b163729284251b1b837`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:04 GMT
ADD file:9bcef05fa351e2fb72a4b6052a0252eeaa2cff794ed089a482670c67961d2e90 in / 
# Fri, 08 Mar 2024 19:21:04 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Mar 2024 16:08:04 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 16:08:04 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:972029ff9873af36c6c0fcee05b14acbc57a61ecd0b8bf86b167bdf46f973823`  
		Last Modified: Fri, 08 Mar 2024 19:22:31 GMT  
		Size: 49.0 MB (48978454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bf66d4984a0af52297b870b1bec7972ac9dae49ffaafb2d48cc862e4b18948`  
		Last Modified: Fri, 15 Mar 2024 23:55:57 GMT  
		Size: 37.7 MB (37733350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25254ac94875805b7f08940e29ec52c17cc60b668e0879ed43a8074f7ea2ea79`  
		Last Modified: Fri, 15 Mar 2024 23:56:00 GMT  
		Size: 202.8 MB (202765195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e0db65ea6d1e1330440dbb4b6919ec7619bbb16a182eb130ae7cf6ed055e0f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3349411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b26e47c9e59021bec6683da8898b2e150dfbab19580a5b75e136c6a8c12af63`

```dockerfile
```

-	Layers:
	-	`sha256:2e7be5e179b99f955cce7a918f7f5bbe16736986a1e44da4b76915e1023f560f`  
		Last Modified: Fri, 15 Mar 2024 23:55:56 GMT  
		Size: 3.3 MB (3329522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1979087ab30f36a5923628862c40b996607e6faaef54e3dc84146d930fb2dc19`  
		Last Modified: Fri, 15 Mar 2024 23:55:56 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3463083d7a54bb57200a2d16c15eb87c4f729c8e09cde2942273b88530905643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286428309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffeddc4e5000f8ad0298c5bc019f9b9f23edbdb241783db7adffc76a215dce3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:48:53 GMT
ADD file:71724b501850c3e6cd72efc58b3430394f691a428c2c62755eac0b93c5579f35 in / 
# Fri, 08 Mar 2024 19:48:53 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Mar 2024 16:08:04 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 16:08:04 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c53b3bc8702e4b172b3fdde99731082a493b5f5fdd7e9632b3cf7dea02a52b4`  
		Last Modified: Fri, 08 Mar 2024 19:49:57 GMT  
		Size: 47.7 MB (47664888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71597242e3bc84850918d978b72bcf84c5867bfb6441051c67b805dca13e66a`  
		Last Modified: Sat, 16 Mar 2024 15:50:44 GMT  
		Size: 38.1 MB (38140694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0647b5a01cfcf58d84174f7b6488e248162cd2e4d60fe0994ec193a89ba2c`  
		Last Modified: Sat, 16 Mar 2024 15:50:48 GMT  
		Size: 200.6 MB (200622727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:ab705c5bd9ecb2128dcd68ed46c6db9f02f654a8b24792dee17ec6ab0b461cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb20d6ac7a4e8ee685070a716f3f6632285b07344bec5a357cc19aec40317bf7`

```dockerfile
```

-	Layers:
	-	`sha256:2069872da5b4d1f97d55f9316c39cc372a87ad96d863333a624583e128008ab1`  
		Last Modified: Sat, 16 Mar 2024 15:50:43 GMT  
		Size: 3.3 MB (3326760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d300e28e93fdeffcca2d0b1ecc74c0036328ebaef94f5edef7de193162f37d`  
		Last Modified: Sat, 16 Mar 2024 15:50:42 GMT  
		Size: 19.9 KB (19927 bytes)  
		MIME: application/vnd.in-toto+json
