## `openjdk:25-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:aed80866a67bac2f4c20c53aa3616e41f85c41881048b5494cdb2bf6da0f58e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:840a0d188c0c9eaa6046e2c6747903cc046535d1097205965f0c6d107f2e9e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278367130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af23bdd1f03204b21e7cdf2564fc8e7fea460fbd452bfa02c3524e7ff01f3d0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Feb 2025 17:31:06 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 19 Feb 2025 17:31:06 GMT
CMD ["/bin/bash"]
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 08 Mar 2025 01:48:16 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 01:48:16 GMT
ENV LANG=C.UTF-8
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_VERSION=25-ea+13
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='456a1dced4795cf35e28459b6289a9eb1d6921f83c79cf460c5c694cb52e11ba'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='518a0d1c64c68f4563c167e052f135827c1b218933dd68a481a7973694fc64b2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07087e9c7fccbae68acd597cafa717397418263ef1da41fe5445a3d4776d1df8`  
		Last Modified: Thu, 20 Feb 2025 02:28:06 GMT  
		Size: 51.3 MB (51282175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0890072a934eb96df39bb30fe95b106134a20cbbbed7bc0a6de2c96649856323`  
		Last Modified: Mon, 10 Mar 2025 21:06:19 GMT  
		Size: 15.0 MB (14976466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8055a5463d74dfed7dcc5d93c83125996f20870b2d265b145cd962e063be7b6`  
		Last Modified: Mon, 10 Mar 2025 21:06:22 GMT  
		Size: 212.1 MB (212108489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:44ec3d9f94131eae12d1ca65c799880ee0cb930ee4941ec71af0435286589bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8a9649e37be26391473042ec1876376f86e51ad4f8feb06fbf25c96f2c78f5`

```dockerfile
```

-	Layers:
	-	`sha256:f393a41745f0cf167b18be6f9d6d4025339885168805f9a5ab38f1bb881810f4`  
		Last Modified: Mon, 10 Mar 2025 21:06:19 GMT  
		Size: 2.4 MB (2440969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35865cf5cdc167c3b1ccd4722a952aa235283724cf85e7a9bf52db1ad61cb3c6`  
		Last Modified: Mon, 10 Mar 2025 21:06:19 GMT  
		Size: 16.0 KB (16036 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d6a4b9de6669505eb649e4f5ece2797c0e1c7e221ec57fb8b26f6d8c5f8a7bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275739681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978ef993640235e4c69230551e20954a26284d5b482845134580adeb1fcf46ec`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Feb 2025 17:31:56 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 19 Feb 2025 17:31:56 GMT
CMD ["/bin/bash"]
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 08 Mar 2025 01:48:16 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 01:48:16 GMT
ENV LANG=C.UTF-8
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_VERSION=25-ea+13
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='456a1dced4795cf35e28459b6289a9eb1d6921f83c79cf460c5c694cb52e11ba'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='518a0d1c64c68f4563c167e052f135827c1b218933dd68a481a7973694fc64b2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:978d351c82d6622560a8ee00b3a217333d2e989aa95df7bcb554a799b63d5a32`  
		Last Modified: Thu, 20 Feb 2025 02:30:36 GMT  
		Size: 50.0 MB (49985763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20b66a0de13ad014c01f41cb19d71b7da9df4146e44920c3f1289afa45bf268`  
		Last Modified: Tue, 04 Mar 2025 22:03:16 GMT  
		Size: 15.7 MB (15671676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6740fec507ac2a5c6e237c70aa329871ca2a01a0345b03dea376daff8c1b1a32`  
		Last Modified: Mon, 10 Mar 2025 22:01:31 GMT  
		Size: 210.1 MB (210082242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:32a4a1bae66f6caec188fc2c34e1176e0e41c2b47f5520f91772433ebc258e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bf7c5787e57d23cd63119559e5a9d85b8d54dbb5374131ea941bc8b127b2f0`

```dockerfile
```

-	Layers:
	-	`sha256:f6a662af9b7e7d0b53dbfff2fe3d650f9aad7a893c5e4b5058b9d5ada44c0b65`  
		Last Modified: Mon, 10 Mar 2025 22:01:25 GMT  
		Size: 2.4 MB (2439815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e853a588e263604022908dd825be724a355f93828b19c3d15eea6f3bf36714`  
		Last Modified: Mon, 10 Mar 2025 22:01:25 GMT  
		Size: 16.2 KB (16180 bytes)  
		MIME: application/vnd.in-toto+json
