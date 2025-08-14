## `openjdk:26-ea-10-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:58709ea1a79ece8eabebbdf1cd809ac1bcb3e9342800e86cf37c814a003e1540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-10-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:73531cd80e2f7bd80051411c6199d0b34611ce49d591b091ccdd07b146b1f7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289793212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a2f6b0a5241fce6f9ac0e166f99fa22589b351b73b804f330c832bb8d3d9dd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:58:59 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:58:59 GMT
CMD ["/bin/bash"]
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 09 Aug 2025 00:54:27 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:54:27 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_VERSION=26-ea+10
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='09044ebef2f1122e484e84df3a95605462c66caf6fb6363a6b3bb70cb6dba3db'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ffacf32c82e822c5ffb1400e05a279b08ddcc3f2c5538d01bf79f31c2af0fb2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:816eb39a0552da23131629c02b98cdeccbfcda79ce23b4283b51ea7845bdb4e5`  
		Last Modified: Thu, 07 Aug 2025 23:49:07 GMT  
		Size: 51.3 MB (51323465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ea1d1fe10915397d685b7726010ef7be231d9fd7a741b4761465e66b5eb5f5`  
		Last Modified: Tue, 12 Aug 2025 18:02:37 GMT  
		Size: 15.0 MB (14976973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7618a6672807ed44ed3cd48607b031782597749d2e52cecf3c7f0b83a2b1f0`  
		Last Modified: Tue, 12 Aug 2025 21:52:32 GMT  
		Size: 223.5 MB (223492774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-10-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a90e92adfb7d56c5730a51693bbfbbede6afb8a4f121609f53d5823c4534897b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8385062a0a86849a9da428520a786101ff92c4964223ff728ab7dff62fa0055`

```dockerfile
```

-	Layers:
	-	`sha256:0390b501f8dde75b96ff19c63f737d356c197ef3a0002786c6f9851ca01ab781`  
		Last Modified: Tue, 12 Aug 2025 21:25:23 GMT  
		Size: 2.5 MB (2451093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842e63a50eefa46804d834cd0b37ff729f6443a0d7c289f7a8f258913effa10f`  
		Last Modified: Tue, 12 Aug 2025 21:25:24 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-10-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ae21f815ab031e96880ae73c90d82a4267e67d38257ce03a3113aa71df756e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287037636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05269ae53cfb73a2cdc347a1c4965ea8cca4f1ded6589e292c8e39fe8d17e739`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:59:57 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:59:57 GMT
CMD ["/bin/bash"]
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 09 Aug 2025 00:54:27 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:54:27 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_VERSION=26-ea+10
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='09044ebef2f1122e484e84df3a95605462c66caf6fb6363a6b3bb70cb6dba3db'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ffacf32c82e822c5ffb1400e05a279b08ddcc3f2c5538d01bf79f31c2af0fb2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00aea10d937a1f6a212468c9a6eb06043ca5276b560643f3c75b3b2d11325b17`  
		Last Modified: Fri, 08 Aug 2025 01:31:37 GMT  
		Size: 50.0 MB (50035024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f29ae74ed40c5064856c8ed83a5fe610bc44cb75f0852e1026a8313f040ebfb`  
		Last Modified: Fri, 08 Aug 2025 17:01:46 GMT  
		Size: 15.7 MB (15672333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eeed7fdbea13946265f29a83dea9d2ff935c0d7d89dff6a46793897e961415e`  
		Last Modified: Wed, 13 Aug 2025 16:49:27 GMT  
		Size: 221.3 MB (221330279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-10-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d70e40463fa90c50893076b119967befb944aad81e175e55eeebff5f38bb82ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e34c39c6ceb66fdf6dcee5424bc9c674a64525f4332e17f0d7865b8e31ad72a`

```dockerfile
```

-	Layers:
	-	`sha256:34bc7da02cbef1d83c7ec546670db4619fae098f7fd729325de75a03ab928b59`  
		Last Modified: Wed, 13 Aug 2025 00:24:44 GMT  
		Size: 2.4 MB (2449927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c81f0a2f5cb5e6ce2a8ad7ff0289662272abc577950d6546c1870f05b5e9ab`  
		Last Modified: Wed, 13 Aug 2025 00:24:44 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
