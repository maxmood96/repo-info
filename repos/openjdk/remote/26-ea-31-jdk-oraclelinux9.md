## `openjdk:26-ea-31-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:adf6228fff6ba27b4f26c3a9ad616d8e9135655206df98611aa984bafbab492c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-31-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:667a396119dd258d6da8325b751a9c0299ceb471c0ce4d12de707169e5f4ffcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313456186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80950ca54923a6baed7f4e8d3b9ec7df791ce6c699ef5b9c09d050cf0948b3d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:47:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:47:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 20 Jan 2026 18:47:34 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:34 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:34 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:47:34 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:49 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4260416a8dbb6a16d4af2d8e2cf5d3ffec20bd15ba7d2c25ee05bc2897b658a`  
		Last Modified: Tue, 20 Jan 2026 18:48:12 GMT  
		Size: 38.3 MB (38295939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45a352e4f995bd27d86306ce1e227f327880604be2db220020eb505223b26de`  
		Last Modified: Tue, 20 Jan 2026 18:48:00 GMT  
		Size: 227.8 MB (227845709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-31-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:4ead0b59da8fbb5913d6f5e5d0d742f844651d2fc6f7678f0346d3ed849d8649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fef84062e81b1df652f80a9d0d2c8557b146e2eff840cda1dac1dc07a811fa`

```dockerfile
```

-	Layers:
	-	`sha256:96b7f5791a2e1105fbb6e01abbfb8625418d6e72c7b2d1fcf584a017eae10d64`  
		Last Modified: Tue, 20 Jan 2026 19:23:36 GMT  
		Size: 3.7 MB (3655371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c95d419a6c09e7c4b9aa0bde147c123a87905c34571f700ad9a2996571ac91`  
		Last Modified: Tue, 20 Jan 2026 18:47:55 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-31-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:db808bd1bab17ed45b0281b2154af3daafc5595aedf107b07c45fdd9728d405e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310370228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f4bf460654783d53089a5f49bcf877a2378ef0db2d53681d2f5d38226c4d09`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:46:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:47:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 20 Jan 2026 18:47:05 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:05 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:05 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:47:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976787210cd0052337f52829189fcd9fb17bddb56066582df7bd9d38d6b1e9dd`  
		Last Modified: Tue, 20 Jan 2026 18:47:28 GMT  
		Size: 38.7 MB (38697813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b284fe9e98366757526a85e4b921afad2113c31639fb72839c65b11e0621c30`  
		Last Modified: Tue, 20 Jan 2026 18:47:31 GMT  
		Size: 225.8 MB (225770512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-31-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:bd9a7e7ce01f8a0c800f25681dfcb445239f70b1065aad644480f323ac9b4396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb455293b17579f939a01b29729bd667153a378b41af666554d16abddf50452`

```dockerfile
```

-	Layers:
	-	`sha256:297d97adf58040bf9195a95a20f9f9df318d565ba53e31df9395079662b9f85b`  
		Last Modified: Tue, 20 Jan 2026 19:23:41 GMT  
		Size: 3.7 MB (3653061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4143b069d10dfd2e2e4d732d55c8543c55a7ef3a2532718eff725b5d2d58820c`  
		Last Modified: Tue, 20 Jan 2026 19:23:41 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
