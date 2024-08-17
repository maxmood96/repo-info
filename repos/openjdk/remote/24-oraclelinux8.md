## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:79011889678293745b93e8ed74d5bc16035a28dcbd238549b03e38f93cd1d7fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:9a4a420c2f6edc0c7901fd863eb74361092e5375ed343335859acc9f6df8d799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278482101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b04f95b01c491c18cf16fb1d6c253cb06c4ee910d2e0a9b2bf5f23c1ecf0fd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:50 GMT
ADD file:f88a328d16b39a012900e14f6463799b448cd9796472d5fb3c58c2cc5ebdee21 in / 
# Thu, 15 Aug 2024 00:20:50 GMT
CMD ["/bin/bash"]
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 16 Aug 2024 18:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='c8cc4f7709c86eca1eb249323b8502416afffc54ddffc85278182dc222b1dcd8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd79e2e9877e5f8efa2324bc78851af99fbd9dc936c41c7c07ba928efd889c21'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:964443381b57e80f40937734e7dfea9e93836abe517bd3e9e9c0fc9f21af4ee5`  
		Last Modified: Thu, 15 Aug 2024 00:21:56 GMT  
		Size: 51.2 MB (51221701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e06d02e0827282431e78f77c137c0e8ed7449a03e32f18c3a3d75a3655638e0`  
		Last Modified: Fri, 16 Aug 2024 21:58:31 GMT  
		Size: 15.0 MB (15036152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d069f5a45e4d27d7e1676aff2e69a36bde6f23d60089d33c48211c08c0b2c1b`  
		Last Modified: Fri, 16 Aug 2024 21:58:34 GMT  
		Size: 212.2 MB (212224248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:466851f0e4e5b7f8c961517cc8dcfd820d5526a9b17f5bce7d0be1266ea99984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24823c996f2deb957f43c13ef3c88107aeb0e3f4e2976e655ff088cecb315a4`

```dockerfile
```

-	Layers:
	-	`sha256:06c818da187f9d36462ec49041f966d7a78f2d8f4344e1b5e32760e8909ace2d`  
		Last Modified: Fri, 16 Aug 2024 21:58:31 GMT  
		Size: 2.3 MB (2287841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80cc9e453cea437006a9f708455098000c7fc397d661764f07779c6d4d07fa5`  
		Last Modified: Fri, 16 Aug 2024 21:58:31 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6e0f6ad74856300bb149d632a8b822f40638467509000d30e9b4bb8f0b7db681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275673056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b8e24446c4ad5d1adff3e154c28d9b96e86383175289aa51ece16377b7eb13`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 10 Aug 2024 00:48:15 GMT
ADD file:ddad218f4909f6f7002ab7531840c692add651f86b77e1e847d3d9b2bfc8c8b6 in / 
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["/bin/bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
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
	-	`sha256:6c616c126182ebbd4c60ad434ed7c0c221c43f91120ac41ae0b662c43b76dd41`  
		Last Modified: Thu, 15 Aug 2024 01:50:12 GMT  
		Size: 210.1 MB (210061779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:539784d906aa5decb93f3473841d06e961811eee74b5adfcdf932ce3fd27e52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af0657ebdfcb7a6239a7826c8f383b5bc26c300bc06c29c5dd178ecc6449c35`

```dockerfile
```

-	Layers:
	-	`sha256:31bf4ca8b01b7e6ab04f4d082bca5458f53d31e8d4b91e166448e54b3ee750fa`  
		Last Modified: Thu, 15 Aug 2024 01:50:06 GMT  
		Size: 2.3 MB (2287310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c03eeacdadebc85dd7bf68c337d1e06ffdaad47dd992a1ca3f18a4b205b21a5`  
		Last Modified: Thu, 15 Aug 2024 01:50:06 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
