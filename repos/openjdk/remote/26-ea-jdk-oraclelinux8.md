## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:34ae059ffa1760091becabf47ce64a3a4356cbd116a52e6b2abad5340fb3f226
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
$ docker pull openjdk@sha256:d709c2c5601cc14bbc52ba242b3be8fcaa96b0feda8315a74d3f60d4d6490cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287021208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba48e459968a026af6f7ef7ec4ebac21bc72e2a1de6d6a14e8e7e9efdc45b7f5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 03 Jun 2025 19:33:50 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 03 Jun 2025 19:33:50 GMT
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
	-	`sha256:44b8a99d3aa3536846330d8b29cdcd8db5a0cb5f437d15e0651b4265acba376d`  
		Last Modified: Tue, 03 Jun 2025 22:02:54 GMT  
		Size: 50.0 MB (50031883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b00391e55b48ca359f7e73a227e9716652430842522c8307dea78a7e6106ece`  
		Last Modified: Wed, 04 Jun 2025 02:15:38 GMT  
		Size: 15.7 MB (15667780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f535cbc9a2ec5b29c76dab9d62b41571f35dfb0b49485fef36827a1be81413`  
		Last Modified: Tue, 10 Jun 2025 00:42:39 GMT  
		Size: 221.3 MB (221321545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6b5d07de824be608669039c1ced7b89a62a34552c2fac68eae0f13f016a35d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9eb43754af55920cc87a06cc93fd4ca4314cf4574e6a2c7f766c66dc980605`

```dockerfile
```

-	Layers:
	-	`sha256:6d074ec414f0683c56b017f7c75eab9a8f929798fc1417af215712100e49ab93`  
		Last Modified: Tue, 10 Jun 2025 00:26:18 GMT  
		Size: 2.5 MB (2450520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4be98c69862356071e2757dff2a70e98df99d0896a920b4b3335c09518c0e2b`  
		Last Modified: Tue, 10 Jun 2025 00:26:18 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
