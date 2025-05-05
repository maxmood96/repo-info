## `openjdk:25-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:1082237669c2a5322fd4470505fd3036e76c074300ec8e700502419a2401e38a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:0058caf455d3abf7ad0aed38e8bb9ec007287e595997f6042e443f27bef55c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300480428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87970d20762c9aeec1703ac4fb7949acf7860a1e24840c634456a287e564d4ad`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:26:20 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:26:20 GMT
CMD ["/bin/bash"]
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 03 May 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 May 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_VERSION=25-ea+21
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='9215df470d2d44c8ea731dcde9e170b6951e29f6e96e90625be983f0f9cfd1ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='23b6cbdac4dedcb1e7d290e7f5e9da01be8c4dcc35b4d296054aae3588d4465a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 03 May 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2eb5d06bfeaafd2195d3612935e86f925a4620bf5bbcea5112a1fb07138dd80`  
		Last Modified: Tue, 29 Apr 2025 18:16:07 GMT  
		Size: 49.1 MB (49093011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7be8ad57ba147f1faf66dac5dac2e9ac884e3a969758333ac746acaf4af292`  
		Last Modified: Mon, 05 May 2025 17:30:24 GMT  
		Size: 38.1 MB (38107384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e9225792a5800b9744b44cd5267b0d56b1dc94dec4411793aeac4e1e04671e`  
		Last Modified: Mon, 05 May 2025 17:30:27 GMT  
		Size: 213.3 MB (213280033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:cea1729b3cedeb5ea00979f7db7bad192e34d1542a5e2694079f2b1100ed1b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3644252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232a8f1c6575a75d3c8f3a719aa039242eb9351b67b55382786a354e0cff2d21`

```dockerfile
```

-	Layers:
	-	`sha256:f157fb8230d8b278f468ac44d2bc46aecf392ba91e81d7dfecff4b7b40a79ed3`  
		Last Modified: Mon, 05 May 2025 17:30:23 GMT  
		Size: 3.6 MB (3624506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e6ffde1f745d2e34e380ab2429deaeaf7d25945327de4297372fa29b442c87`  
		Last Modified: Mon, 05 May 2025 17:30:23 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b8d6fd0d62552fbc7473497b5a0d04002f167f1cc0b44ee7ef4c45752bcb3e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296407203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc27e884cb09f061f53a50d89a09cc41dcb195094616846490be2a8305af1b7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 18:48:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 25 Apr 2025 18:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6bc1d37add3f10b8826fef26bfc5ab51183b308c32a12f08a18ee2b6d9e28111'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='e6b42d0f5816ea1fd6c27505ddf93dc11eae12fc2cc64b4139350d7c0acdd55a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88a33dc8906274baf54eb28aeefeba84c17922e3854e6fd41883f273d87d330d`  
		Last Modified: Wed, 30 Apr 2025 01:59:51 GMT  
		Size: 47.7 MB (47672989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b5aea1d0deca854a3762f4e396dad66260211f50004210a8e73e2146af926a`  
		Last Modified: Wed, 30 Apr 2025 07:05:49 GMT  
		Size: 38.5 MB (38500810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7aadc4a87e0f25e471df03345f26917cd536e48f1626a437997621424b5e4e5`  
		Last Modified: Wed, 30 Apr 2025 07:05:53 GMT  
		Size: 210.2 MB (210233404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:ec5fd874517095f12f6a758a0d17ebe3704c760e231a0f8033e36ade19a22d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c7b8ecc4de6b69cda0fe2f93537e2283c609aced0c99b08dc0f6d0b6a7cb0c`

```dockerfile
```

-	Layers:
	-	`sha256:b3219dcfc1519a47554ee0846fed9170d5d67c26cd86a1b6b21f00bbcb4a3678`  
		Last Modified: Wed, 30 Apr 2025 07:05:47 GMT  
		Size: 3.6 MB (3622268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61832b6ee78829b5784b27ceba658bce145dabf3e0f2e64004bf3f6845a4407f`  
		Last Modified: Wed, 30 Apr 2025 07:05:47 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
