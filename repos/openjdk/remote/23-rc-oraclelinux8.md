## `openjdk:23-rc-oraclelinux8`

```console
$ docker pull openjdk@sha256:44aa0cfcbcd9cd9a39e8c4289157834a0098bb801fc0b10cda002713ccc4552f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-rc-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:bb139777ac073bde8f4f827c03985e050d20a561634376c05cc421d0dc9c7fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278029882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40e02b850ae46d5e97c856a8f925cb85891e13e58e332a44483e5caf0ef14d5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Aug 2024 18:48:11 GMT
ADD file:f88a328d16b39a012900e14f6463799b448cd9796472d5fb3c58c2cc5ebdee21 in / 
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:964443381b57e80f40937734e7dfea9e93836abe517bd3e9e9c0fc9f21af4ee5`  
		Last Modified: Thu, 15 Aug 2024 00:21:56 GMT  
		Size: 51.2 MB (51221701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76975107b15b778492f6289b0fe45b25f39292a1e57fb1bda38b011e823807b`  
		Last Modified: Thu, 15 Aug 2024 00:58:08 GMT  
		Size: 15.0 MB (15036008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387f56de1453f4cd4d6277e7a95fef9c449114aee8624d8d1414f8a3149db41a`  
		Last Modified: Thu, 15 Aug 2024 00:58:14 GMT  
		Size: 211.8 MB (211772173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:071d18e6e996f496b57e43b57666a115e89528dabfcfe276b23c94f28ef9d04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8778206215451ae9417fa51bd43244243eef2134892ce7b3046131bb39efcf9`

```dockerfile
```

-	Layers:
	-	`sha256:f7d14c006830f9c11c16cc6d068eeaf4d3018a54546e732fb06a50c5f81c97c9`  
		Last Modified: Thu, 15 Aug 2024 00:58:08 GMT  
		Size: 2.3 MB (2287161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4494519721ca064dad62b00523ca161e598f86702cb15c226537713aacaf287c`  
		Last Modified: Thu, 15 Aug 2024 00:58:07 GMT  
		Size: 15.2 KB (15216 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-rc-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:67da6ff672b3e8867ffee11d4ae07b2dd1caabce1433dc19fe44c928e2f5555d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275251096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46533fedfb526754b1129f5a3d9608ca6d24c6282b3d1e433ec9c3a8f89a429e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 22:40:38 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Wed, 03 Jul 2024 22:40:39 GMT
CMD ["/bin/bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6708363575e82894d4714b00358e6cfc904f5e8213ff218080d18d8c0a3aea8`  
		Last Modified: Wed, 03 Jul 2024 22:41:29 GMT  
		Size: 49.9 MB (49925030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca345db69d5fd49f13cb0fd444dd21dc5576cd6587605dd8acb1793f7ebac2b`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 15.7 MB (15686119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ea4e0858bab8fb8c470d76a9a4874e0e4ef96fdd528d2c50a8daea399f583b`  
		Last Modified: Mon, 12 Aug 2024 18:36:08 GMT  
		Size: 209.6 MB (209639947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2c78d3bcdc14967d207639d2fb554f2ce4c941dcff5f1f870c636fce2a7e129f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7ca3fda4e5ab21d3c29207eb1c10fe976192c1bff9f55f3c8c56c9a8ad85b0`

```dockerfile
```

-	Layers:
	-	`sha256:ab5ee38302431708b40c70ded87ae32aca6ea458131e8455cdf2a615484d2fad`  
		Last Modified: Mon, 12 Aug 2024 18:36:01 GMT  
		Size: 2.3 MB (2286590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a0bfde6ffcd08970b35424efea689612183e12071d5d90e47d6223810666e48`  
		Last Modified: Mon, 12 Aug 2024 18:36:01 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json
