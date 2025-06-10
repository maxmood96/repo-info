## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:9b823700044ed6d9ce95b5998712b247d1124599a2b3123b819679c2e718f3a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:bebdda9a5d0b8b1377641976350bd4e023c70e258c3b2870b12241e7459487d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289848724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe684baf4fab3a1d8f3f1e47cd403ae052d4375c260f60834eb8639989b63951`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 03 Jun 2025 19:32:58 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 03 Jun 2025 19:32:58 GMT
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
	-	`sha256:b1a7000049ecfef865d125a112ed40237daf19bc27e872529fef00770b81ebc3`  
		Last Modified: Tue, 03 Jun 2025 22:07:40 GMT  
		Size: 51.3 MB (51313330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f651a3e2baa2807e73c34aff45f11ade2799d051f1aedf77877a8dfe723a56`  
		Last Modified: Mon, 09 Jun 2025 22:07:04 GMT  
		Size: 15.0 MB (14997028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1976361e50b4b9564a0e0cc40e727e413b2054040782ff5c7a25e10f8ffb5997`  
		Last Modified: Tue, 10 Jun 2025 00:42:39 GMT  
		Size: 223.5 MB (223538366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:01d379886ec2632f088aa1c8c48d9fa08cc0ae6c6ced7f5ddc04bfc2d1120d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc1447e9f73f21b84070f834e9728d4c563a6902eb6659952070e01d0da8d95`

```dockerfile
```

-	Layers:
	-	`sha256:275be573a9385b2d5c82188dc09eef50a28bbdeb9ce918143477d85aeeef0d64`  
		Last Modified: Tue, 10 Jun 2025 00:25:56 GMT  
		Size: 2.5 MB (2451674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223f45fd1e7ddacbe72988549d69d5cb71069014980b93b2dc854be9f70035b5`  
		Last Modified: Tue, 10 Jun 2025 00:25:57 GMT  
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
