## `openjdk:23-oraclelinux8`

```console
$ docker pull openjdk@sha256:6f6424714d6c5128a542162faba081bbd282e4a5415e330520fb7b4e02bd03fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:67347bfd2d3e96a91588548a74f40108c8cea87f7c981e58525eb9d01045b10b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269455222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c634add2511a39e72e291993df264aee43a3ca18eda5504ee0063d899a460ef5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:16 GMT
ADD file:cbc540158e77b85113e3a0e0ed1e202046cf293cdb8d7cd890b04883493dbf35 in / 
# Wed, 14 Feb 2024 01:47:16 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 29 Feb 2024 19:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 19:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='892346bd29f50e248ab5980903e5759f73d8ac2b6ee0cd918e3acdb132eb8776'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e927b03ed3af88337e11918d05955c72b71c1664dc5791ba4a6590329004657'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81badc5f380f1ca21f6c430303f4107b9b5e0af27c59e3725bf731915b457fc8`  
		Last Modified: Wed, 14 Feb 2024 01:49:17 GMT  
		Size: 51.3 MB (51325575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d412247016a06df4691385ff5b5e61c5404a239d090e03be5878607fa7ffe01`  
		Last Modified: Thu, 29 Feb 2024 22:50:48 GMT  
		Size: 15.0 MB (15005957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6138a72db5e02a4f96564d5a14334e85a38f1469a84c4ab8dabd2dd59b1cf1`  
		Last Modified: Thu, 29 Feb 2024 22:50:52 GMT  
		Size: 203.1 MB (203123690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:dd0e764ca105d4078622327c8ac1bd9d654d19474de6b5b640aa77524ac9b14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab205468071e56b584605f81fe45c6f61bffe1f4bd7ca96443de2bb990972386`

```dockerfile
```

-	Layers:
	-	`sha256:cda598b137f9f3143adc51a1d0948fb6f380c71df647c5cb5d556b64a1fd80a8`  
		Last Modified: Thu, 29 Feb 2024 22:50:48 GMT  
		Size: 2.3 MB (2271204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45127a093744c7f47a2e980049c9e06c1c40dfa49f03f26afff8f49867ca6b2b`  
		Last Modified: Thu, 29 Feb 2024 22:50:48 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c0a4915b1d12d912626856e7382f27bb14691a02939201f0518a483a7dcb3cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266778545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ab5438ee75257912158a9e6442d84eaab3e62f9c55e52e3e9bc960da9996c3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 29 Feb 2024 19:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 19:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='892346bd29f50e248ab5980903e5759f73d8ac2b6ee0cd918e3acdb132eb8776'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e927b03ed3af88337e11918d05955c72b71c1664dc5791ba4a6590329004657'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b1d3eb6a012567065354e86eb0bac67a32e425e65bc6fe8b5cd84b95a0643`  
		Last Modified: Wed, 14 Feb 2024 11:04:46 GMT  
		Size: 15.7 MB (15691290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f210b4faf5e3ed18fc7cd05b43683bc9b9c838c30c274ecf0dfd0e67d027d79`  
		Last Modified: Thu, 29 Feb 2024 22:52:56 GMT  
		Size: 201.0 MB (201014341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:fcf5dbddda8e25a2efbe7966d67daf8c8332d2bdac1cf5cc126e5f4f68f274c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8132e61c1f0d3336aed381fa6955ebf1c5d00aaea2ff369508477312a26e3a`

```dockerfile
```

-	Layers:
	-	`sha256:af2d4a854bb2da1ff376b01070c9e5157777dbeab156a94076c711596ff9822a`  
		Last Modified: Thu, 29 Feb 2024 22:52:52 GMT  
		Size: 2.3 MB (2269674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2ecbf7b5e52dc63e7fd057a64e06a5088beda06301c603bffc2885e30909a6`  
		Last Modified: Thu, 29 Feb 2024 22:52:52 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json
