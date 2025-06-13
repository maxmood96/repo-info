## `openjdk:25-ea-26-oraclelinux8`

```console
$ docker pull openjdk@sha256:d904e90f7fdb56edbc9940383c4a1e7fc9563ff1401d5f21a2576c3ed0a941fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-26-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:9ec897a13ff43fa10b6f10b7d170150a550769ed88577eef61627305ae3a0074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286973791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c07dd5bb2b07629e4598541044299a81acaef0980d389682c3ccdc374eee699`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Jun 2025 06:48:11 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0915556054e5fcd1f04e454b0deedf305bb209616c5a72a8b2d83db9191e5115`  
		Last Modified: Thu, 12 Jun 2025 21:07:27 GMT  
		Size: 51.3 MB (51311558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b57b9dac735bf8086f01188476d48851004f64f3e3608a0c9640124ece40e6`  
		Last Modified: Thu, 12 Jun 2025 21:09:13 GMT  
		Size: 12.2 MB (12217912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfed9b3b8b2634daf24f6d5b51e9451375604d1e391191daab7276b8eb86353a`  
		Last Modified: Thu, 12 Jun 2025 21:08:39 GMT  
		Size: 223.4 MB (223444321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:084bb57ac3df8aa1fb9ee33f8fcf2acb17b0a5a3c788ffdc02176e49dee28035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4062d9af875b7cff1f29ac0e33a265054b4811503033210b96e9a72a53c17514`

```dockerfile
```

-	Layers:
	-	`sha256:6b7816b84785f86fd4d9c58e95ef9fde31188582b0979368910bec17c71e54a4`  
		Last Modified: Fri, 13 Jun 2025 00:23:26 GMT  
		Size: 2.4 MB (2438161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d1bcd146ac004f4b063de98c985cde06e34d9f1b7947ce1c49213faa16baf3`  
		Last Modified: Fri, 13 Jun 2025 00:23:27 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-26-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:476c2e6ecb9a01c7da5d2b2ec6473d07abe1cf260a2cedbd4d28bfbb7a72ef05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286955688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10c00657f9e7953df7336b6dfc9bfbf5e768069a3636ee097ab5a237bb0e34c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Jun 2025 06:48:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
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
	-	`sha256:d8f7d36d2233ff5d3f30c4b8a4afc76383de5c7212a4c721974e54357430d5c4`  
		Last Modified: Thu, 12 Jun 2025 22:57:47 GMT  
		Size: 221.2 MB (221245828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9971ec6d976154490b1d1cb3c3eca8a0ff396da4346b0624564eb89879cda048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0831d9568ba1b1e926d4be5e3820023cdc9494f9fbb03388fb75f1e1f27ce4f8`

```dockerfile
```

-	Layers:
	-	`sha256:c4e76ddf439f4f3d1ccf796c81e3a831e650f97ced8145bd61be964b11a74f6b`  
		Last Modified: Thu, 12 Jun 2025 09:23:28 GMT  
		Size: 2.5 MB (2450532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77396dc99dfbf500e3c453d3e5afcacfb366cd55ea56b5222929e5d3763d89ce`  
		Last Modified: Thu, 12 Jun 2025 09:23:28 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
