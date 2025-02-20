## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:bb3eb739da42e599ed7aa43d397e5e503a12b6d605e5e8ac72e17a19bb227039
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:884d64ace7303aa35243b791375a7859548aeac5433739a5c59e2a1efe67e48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279550281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499b6cf4a596e691526a93b397d4d89c6b72c50a5cdfc4e72660bf3f898e2183`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07087e9c7fccbae68acd597cafa717397418263ef1da41fe5445a3d4776d1df8`  
		Last Modified: Thu, 20 Feb 2025 02:28:20 GMT  
		Size: 51.3 MB (51282175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf469970159cf21e46f6839e096a6a2dcd229396a5b8504cea2ee28e33c9a21`  
		Last Modified: Thu, 20 Feb 2025 04:11:31 GMT  
		Size: 15.0 MB (14976584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b32ebfdbcbe1b1353f8afc0977ded70a5f80daa05eeef86fc855f19723b1e82`  
		Last Modified: Thu, 20 Feb 2025 07:27:46 GMT  
		Size: 213.3 MB (213291522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:201f404f94ac37e1ee04423b6dc9672fce4b6644590490ece85580a2fde83566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c91344a3dd191004a47e8c3bc7cc44f36c5040c7593e952267c7c1602125adb`

```dockerfile
```

-	Layers:
	-	`sha256:858328315370f472070749217c62cd18e1a1452990f74d6a9f86b9cef0a2f9d7`  
		Last Modified: Thu, 20 Feb 2025 07:23:24 GMT  
		Size: 2.4 MB (2444671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041b4515c4aa46b55aa3d14d41d2b0b6020bf49e89bf2d2af23f7ed0a7f69f87`  
		Last Modified: Thu, 20 Feb 2025 07:23:24 GMT  
		Size: 15.4 KB (15432 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:05e55ba27c5fc457ab377646a6714ca964f996bf03e2e5f658bf3ebfb72442bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276923021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16424ce1f4aea5b841af2087371fafa46b65ecebdf2292c71cdaf6ef9ba533d1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:978d351c82d6622560a8ee00b3a217333d2e989aa95df7bcb554a799b63d5a32`  
		Last Modified: Thu, 20 Feb 2025 02:30:53 GMT  
		Size: 50.0 MB (49985763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9e541b16ff664cd5febbbec24629b72164916363b1de234600bb25a76ed4c`  
		Last Modified: Thu, 20 Feb 2025 04:12:05 GMT  
		Size: 15.7 MB (15671745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc540814392adc04f977a23e655ebe057b9d1ddb0d79317ffb32bc3daa2201cd`  
		Last Modified: Thu, 20 Feb 2025 09:36:05 GMT  
		Size: 211.3 MB (211265513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d184af401a7479b1800c5dbc4e975b10d61b645b5aa054deaf06e7fa3e873716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1b32763059a07cc08c761c6a7cf63cf5ebf6a22ec2c596cc2fc23d423f05df`

```dockerfile
```

-	Layers:
	-	`sha256:5f1c1fd871743e4569216754468d8db422cc7c819104b74881c679dc7bb13b0a`  
		Last Modified: Thu, 20 Feb 2025 07:23:26 GMT  
		Size: 2.4 MB (2443493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66cf9ffe7cc9ea359fbb7019e1fd2cac5b0dcfcc2832d44c7cc04b48833dfca4`  
		Last Modified: Thu, 20 Feb 2025 07:23:26 GMT  
		Size: 15.6 KB (15550 bytes)  
		MIME: application/vnd.in-toto+json
