## `openjdk:24-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:797af97745e139177277dba4332dff3a286452a4e5c672971428f1a4a53426ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:025721e1821fb93ab36d6efe7af737188f81d3553b7f6c24b53a3c2093905595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278476307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204392c3772443a4946a57bc786d2b87ef0f68fc767e290bad877f25c78ecde6`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 10 Aug 2024 00:48:15 GMT
ADD file:f88a328d16b39a012900e14f6463799b448cd9796472d5fb3c58c2cc5ebdee21 in / 
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
	-	`sha256:964443381b57e80f40937734e7dfea9e93836abe517bd3e9e9c0fc9f21af4ee5`  
		Last Modified: Thu, 15 Aug 2024 00:21:56 GMT  
		Size: 51.2 MB (51221701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb0ab8ae74a8dd35af88e89e3ca98f4b75421ed858c95b1b299067b9904186`  
		Last Modified: Thu, 15 Aug 2024 00:58:11 GMT  
		Size: 15.0 MB (15035971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e6fb5f20eebacb1d816de856edaebf4061daff2cfb214ccb78bc2275e44a66`  
		Last Modified: Thu, 15 Aug 2024 00:58:16 GMT  
		Size: 212.2 MB (212218635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8fc5fa60f83da55cef3a6469243b81169f5ddcbe996b35b9a1af83cea3086839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a263893ed427a7eacf00c97ecb920e1838ffefea6ef92ea37f4c9c3235b097`

```dockerfile
```

-	Layers:
	-	`sha256:21676684e3573d8cb73cc89a6a78b8718d6f94c5adb7bcf524202a98584625f2`  
		Last Modified: Thu, 15 Aug 2024 00:58:11 GMT  
		Size: 2.3 MB (2287841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20108576001c086e73c0e325192a26ae20d9a9ca7dee599f9ad99080ad8dd33d`  
		Last Modified: Thu, 15 Aug 2024 00:58:10 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-oraclelinux8` - linux; arm64 variant v8

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

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

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
