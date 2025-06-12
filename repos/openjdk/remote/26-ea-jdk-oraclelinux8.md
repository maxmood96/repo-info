## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:c84467db05c8439af9754a8062d4efb3a8cf3bb4e0eff28537a29f92cdd18511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d7da763b24b54fabe039116e9de276d291eb0a08e9ab51ae8dc22764ca3cc350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289823699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e73a695bb023e832dabbfe643b8b44583cb8e382ceaf9f8822b1d26bf821744`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Jun 2025 19:07:09 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 09 Jun 2025 19:07:09 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 19:07:09 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='9d95d3e025035bfe649be52a1a5f94e28f66af98693db6b4e879fa3be4dc4e69'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b80805bd34f0513f09b4cbf9928fb8c73a883c6979ba1df56e71f1b7c12e434'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6987fb89a70d9360470c7d0a557d09b1376bb71b0da1a493ca4adfb203bedf83`  
		Last Modified: Thu, 12 Jun 2025 01:08:11 GMT  
		Size: 51.3 MB (51315459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ac4371f503544d1b4be6fd06f6bdf580277ec295fbf68ed9bbb8ac7e9a4d5f`  
		Last Modified: Thu, 12 Jun 2025 01:09:53 GMT  
		Size: 15.0 MB (14984280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7f2f4773dd8558de2eb5467d4f978ee5c548b21535cdb72096a30c5c26cee7`  
		Last Modified: Thu, 12 Jun 2025 03:26:44 GMT  
		Size: 223.5 MB (223523960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c21d204af0d8af8e532ec76fc7d3f0e82ad14d3b3d9d20bae0d848aee9af2bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669a1d943216cda6c037ecd9c06036cf736baa13a86d5b674d032693b1deb4b9`

```dockerfile
```

-	Layers:
	-	`sha256:a96cd5b9284594381e19c3bdc049ab2e2f21df7f8033dfd8aa05c57d2a88072f`  
		Last Modified: Thu, 12 Jun 2025 03:24:07 GMT  
		Size: 2.5 MB (2451686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5f2623fd8de093717d318657c838fff71e8fccb9f3bade2fd76c48370770bf`  
		Last Modified: Thu, 12 Jun 2025 03:24:08 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2e0a4155965a981dfd71dffd03d0561af3fb59ecff39a51d209a0913e97a1909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287034575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ae49755a98853803f0433454ac2eebae164085bc5b2211aedb9dcabb020e1e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Jun 2025 19:07:09 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 09 Jun 2025 19:07:09 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 19:07:09 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 19:07:09 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 19:07:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='9d95d3e025035bfe649be52a1a5f94e28f66af98693db6b4e879fa3be4dc4e69'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/1/GPL/openjdk-26-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b80805bd34f0513f09b4cbf9928fb8c73a883c6979ba1df56e71f1b7c12e434'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 19:07:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:536d3420c0ce742c95ed769186c8d4f7e7b53e438009b99d9b1f9eda4a3ec949`  
		Last Modified: Thu, 12 Jun 2025 07:48:23 GMT  
		Size: 50.0 MB (50035464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829293c0cb30761825f4640678503eabfdac0447747fbd12fdb49a2d8b55a87`  
		Last Modified: Thu, 12 Jun 2025 09:26:23 GMT  
		Size: 15.7 MB (15674396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51563fecb9143ef43e43ee3a35bdcab368669a023867a50619492b9afffe05e2`  
		Last Modified: Thu, 12 Jun 2025 09:27:12 GMT  
		Size: 221.3 MB (221324715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b47d5ab541c06ff08406b4e79ea46c0bddc105dc1f9948d2f6031417cc926d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6089b14775833810258a1ee0158144fe9bff5d9016afea110efa33b54179b55`

```dockerfile
```

-	Layers:
	-	`sha256:6a422eac1e10c99af116c4eb3f5fc6cca021236f9c91eb33f3851678d050075a`  
		Last Modified: Thu, 12 Jun 2025 09:24:13 GMT  
		Size: 2.5 MB (2450520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d551f18bdc384d8c75eabfaf2841a69b935c0bd9175104993e10febe2847fc65`  
		Last Modified: Thu, 12 Jun 2025 09:24:14 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
