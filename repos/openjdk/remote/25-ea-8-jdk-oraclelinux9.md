## `openjdk:25-ea-8-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:ba550f9bebcd7c696e0a8b3ed0f6b38b995a74669c4c97cc20ab7b98f3da4d9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-8-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:7cb2dff614e064ab8b0904332fe6b15d33a27ee9410e231bb79300f07e42bd04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309643780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430c184cf7fdc33778235e0cb85f0d6b7676c9dd2190a878b97865691a46322c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af364d2222e6799ff4d4977e75f066deadb2c7bf62cb6af8c92d2b8ad7efbe15`  
		Last Modified: Fri, 31 Jan 2025 22:26:43 GMT  
		Size: 48.8 MB (48774607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6286401481d0a62aeae0921751679e58803a7c5bd491cf5495ad51cf2f78faa`  
		Last Modified: Fri, 31 Jan 2025 22:26:46 GMT  
		Size: 211.8 MB (211770471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:77b526504886b82330bb4b9bbf5e9027c602ddd9f610f5b3be141618eb25cdc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d310eb2f3196a029b5bda1b8bb4747acc3d5bc4156a14896a5148320c1e4f02`

```dockerfile
```

-	Layers:
	-	`sha256:e1d9192485ad12ab8202618cfdb99e852c6aa310d4df68300aba3191bb7f4d7a`  
		Last Modified: Fri, 31 Jan 2025 22:26:43 GMT  
		Size: 4.9 MB (4906931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c0dae4fb60b88b00b79b0522d77719f2e153592e075188c0e3e140fa05a781`  
		Last Modified: Fri, 31 Jan 2025 22:26:43 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-8-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:37837481e0b826f095781280c18960bb3c94b136e9072f98bdcfc6183c455ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306608091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed7e7177c372aba34af5823ec8756a1c5dc94778e1c826cd02b08fcd9b63efa`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9527a70a5df0c50a0919b2bbc807b6789f8d6833d49f997079d3ab5dd2e735`  
		Last Modified: Wed, 22 Jan 2025 02:29:30 GMT  
		Size: 49.2 MB (49203729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9658c6f4f12d1eb8451bd501846260bcb84c144103d69aa20a591c56c20645`  
		Last Modified: Fri, 31 Jan 2025 22:26:12 GMT  
		Size: 209.7 MB (209736970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:18c1c85d5d0f083879cfae93acc3bc8039d802f728415f89f0d7be3e5530142a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d350da3f1f493b61d38cb6a066d2da221e13279706dc960bb3492fa4cbf71223`

```dockerfile
```

-	Layers:
	-	`sha256:30945bd7c39cbdec6a4d042da1a94c5803f745305852414e30d226b4dbd748de`  
		Last Modified: Fri, 31 Jan 2025 22:26:07 GMT  
		Size: 4.9 MB (4904693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4645a5a875d03c60d44f93e30f12bf907cbdf7f3ef351811579cefc24ef1d87f`  
		Last Modified: Fri, 31 Jan 2025 22:26:06 GMT  
		Size: 20.0 KB (20007 bytes)  
		MIME: application/vnd.in-toto+json
