## `openjdk:27-ea-4-oraclelinux9`

```console
$ docker pull openjdk@sha256:d7803ec1ca0e59f60b6984491e3c8e6061d5e9437f01a877a1ce63b75fecb5f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-4-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:66cff965e580d106a0c859e76edd28d3318d312f2a3f5ba8d8c415d58bbd300d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313529546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c2ee565fd5c8432f8e63b7d37760d6d25b6a48c02fe8e509450ef5e460a80a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:08:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:08:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 12 Jan 2026 20:08:12 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:12 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:12 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:08:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d474d946492df41b7e7a91f3c19601cad11d4aa8558516013ba64b34a781712`  
		Last Modified: Mon, 12 Jan 2026 20:08:51 GMT  
		Size: 38.3 MB (38299942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b34947e8cb3e4a23f3db1037f3c281ab1d66ea3e4b15deab9e347d9e73d88`  
		Last Modified: Mon, 12 Jan 2026 20:08:57 GMT  
		Size: 227.9 MB (227912606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:59ec1d3bc1b89a8fcdb10858616b650ef0e71f340f62cdbf6ab91af0a3f9e804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb9edb7e9b3628024bb4b369657e88f6aff81a1dbc6a48c674eec903f986ad2`

```dockerfile
```

-	Layers:
	-	`sha256:e3c899cca72b2d7faa74d626fe107c75046f9eb17dce767bfb4525540e02bfc7`  
		Last Modified: Mon, 12 Jan 2026 22:26:06 GMT  
		Size: 3.7 MB (3655351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050f18a3eee86b339c361d5509139c140b47d08d27d3d20537253a693316e3c1`  
		Last Modified: Mon, 12 Jan 2026 22:26:07 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6bd028cb7d91ca940e92fb1cc9f957c3495c30225f8b87f1e3c5a158e956767b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310438656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7594b54857d107ed5f8795abf4c94db3973ec397b28452a60960f6a86ba4c99a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:08:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:09:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 12 Jan 2026 20:09:11 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:09:11 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:09:11 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:09:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:09:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa04a99adbceec323b63783930bd43b8598872c6606f6327ba43849b46744fe`  
		Last Modified: Mon, 12 Jan 2026 20:09:47 GMT  
		Size: 38.7 MB (38696847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756d8d562e401d3e356a0d092df909ed3601330c8f52c2518496ba73b29e86ba`  
		Last Modified: Mon, 12 Jan 2026 20:10:07 GMT  
		Size: 225.8 MB (225836269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-4-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:a35079649b126f2cc8efc7bf2268ae2caa1a9a5df384d1a89215ed6ba3b283eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc00c8bd46297151310add8312300e5d53ec6f351b69f696a01d4cfa9338f49`

```dockerfile
```

-	Layers:
	-	`sha256:ad863713a98f09184e84362665c9ef5b5052ecc0c150d3d7b944a64641f18a76`  
		Last Modified: Mon, 12 Jan 2026 22:26:12 GMT  
		Size: 3.7 MB (3653041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb06d7555f99b22544ddd13ceb41045579534895b7c300603fa9a14856aa78d6`  
		Last Modified: Mon, 12 Jan 2026 22:26:13 GMT  
		Size: 18.0 KB (18028 bytes)  
		MIME: application/vnd.in-toto+json
