## `openjdk:24-ea-6-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:8ed82e5e900fc816f89f459193686484d82c99f9cdbd3175273e2d1352b94f4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-6-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:773d4eb57c7e6b938614b9eae135a5fbf61b0656e9f9adf55935d0cedaeed375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 MB (278229331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933e3902d2ce0d8588d5ebd864c13a429d78c6f9e8827f51bc36e43ac5a65e01`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 23:20:38 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Wed, 03 Jul 2024 23:20:38 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 12 Jul 2024 06:52:24 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='85969884f11f2863595c13dff1cb6f6d94149bbe5188c34f0a7aaa284a545a27'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c719648382b7e5d564dc1d39d4408890d92ce5484fd46a5ef338da7380684ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc2f4070a6bf60cc7e75626775184317712160370fd1172d7a46acdca5ed49f`  
		Last Modified: Fri, 12 Jul 2024 21:57:30 GMT  
		Size: 15.0 MB (15036037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1f92ddf05b1c7d837aa659513eaf0593313d7af41824536622c37343605ba5`  
		Last Modified: Fri, 12 Jul 2024 21:57:32 GMT  
		Size: 212.0 MB (211973670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-6-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5bbae24b2611427f1d0f2e693d12726628fde061f1f868e9a0baf74f50fdb8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90320c839b5f1c651e5374ee8ced9b43f76a939237bea9d42df127cd40d90606`

```dockerfile
```

-	Layers:
	-	`sha256:1a937f133f13a07e5ec6b9cb8e1c1ef04ca601c96d7462e6b63377ba0d5d02b0`  
		Last Modified: Fri, 12 Jul 2024 21:57:29 GMT  
		Size: 2.3 MB (2267569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22532553853164f3b5f3df2443b46dad85d62c5eb174972baff554614d7a2e0a`  
		Last Modified: Fri, 12 Jul 2024 21:57:29 GMT  
		Size: 15.8 KB (15803 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-6-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:09d26f26a35506d51bcc28488c9228a5a62d5f8b7cce90fb9e69099136266a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275458085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba91109d82efc9f41c4df510504497ae154bc992e4ce346adcd40d5c9c0a03fc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 22:40:38 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Wed, 03 Jul 2024 22:40:39 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 12 Jul 2024 06:52:24 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='85969884f11f2863595c13dff1cb6f6d94149bbe5188c34f0a7aaa284a545a27'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c719648382b7e5d564dc1d39d4408890d92ce5484fd46a5ef338da7380684ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6708363575e82894d4714b00358e6cfc904f5e8213ff218080d18d8c0a3aea8`  
		Last Modified: Wed, 03 Jul 2024 22:41:29 GMT  
		Size: 49.9 MB (49925030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53325ebdf5962703e657719964570a5baf1824ea843ea45441c78f115b80fb18`  
		Last Modified: Wed, 03 Jul 2024 23:56:52 GMT  
		Size: 15.7 MB (15686023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284f7a18171b90552e4eaea4df016def9c05fb7de2ed10851c7423badf8732df`  
		Last Modified: Fri, 12 Jul 2024 22:05:40 GMT  
		Size: 209.8 MB (209847032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-6-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d8ac8e483f63fc4a1195105b7296e9ea37c9111b37a6518e27f98e67b7f4d0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd1926311686b00412bbcf6feac0aa5e310d667c6c08674c084ffe578cc1b26`

```dockerfile
```

-	Layers:
	-	`sha256:015a2e511157a59bd7b2d6ffaae7a8d36e6bf4593d85de68fc46afc050c628bd`  
		Last Modified: Fri, 12 Jul 2024 22:05:35 GMT  
		Size: 2.3 MB (2267038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5f7dea2c6634270c9e8d07ee7c78323b90d10128e5c52b49c41c5cea9f5bae`  
		Last Modified: Fri, 12 Jul 2024 22:05:34 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json
