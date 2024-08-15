## `openjdk:23-oraclelinux8`

```console
$ docker pull openjdk@sha256:6b6568f5878c86b98bdf2a5cc4a2832b18fb842dabd4d467b70e141eca45dc22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux8` - linux; amd64

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

### `openjdk:23-oraclelinux8` - unknown; unknown

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

### `openjdk:23-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2a1157d4435923dc3a1350efcff7e1dac1274908c49a62c062a7c78202d7aa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275254581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f8593d8d7ca30d7972e3ac399ead2970385bbd923bd390d5c626d191da64f8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Aug 2024 18:48:11 GMT
ADD file:ddad218f4909f6f7002ab7531840c692add651f86b77e1e847d3d9b2bfc8c8b6 in / 
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
	-	`sha256:ed876bde92ee249d3e0143b5e51b17dcecf0128d775998e97e0812e3218cde0e`  
		Last Modified: Thu, 15 Aug 2024 00:41:13 GMT  
		Size: 49.9 MB (49924065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ff93538bc6272378ffb755908dacde2dad43d975364d67e19f6ad1f4763010`  
		Last Modified: Thu, 15 Aug 2024 01:50:06 GMT  
		Size: 15.7 MB (15687212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45cb028ebfd33c32324946bcb46d50117bf3606f2b4c5ffe5940ecb2d4d6461`  
		Last Modified: Thu, 15 Aug 2024 01:51:02 GMT  
		Size: 209.6 MB (209643304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:047fb4d02ac265238a7e9fe3dccd0f41e8915cf9d9587cb96afdd3da0c7e863e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cccfad38ff74d4acfe92727ff03db801fcee36ebb36fa068b2c53441cffcc04`

```dockerfile
```

-	Layers:
	-	`sha256:c221372eaa6178793552083ddf21d5fbfa13e8a1e52850fb90b330dd6ebca96c`  
		Last Modified: Thu, 15 Aug 2024 01:50:57 GMT  
		Size: 2.3 MB (2286606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3da1c534e24b00effaecaee7bb052cd42bdad5fccd502a8441ad864594e1da6`  
		Last Modified: Thu, 15 Aug 2024 01:50:57 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json
