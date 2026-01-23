## `openjdk:26-ea-31-oracle`

```console
$ docker pull openjdk@sha256:3c1a90f1d9569d19fa6c6f653c68e2fd4a8b44ae1940c78208585389de5586ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-31-oracle` - linux; amd64

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
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4260416a8dbb6a16d4af2d8e2cf5d3ffec20bd15ba7d2c25ee05bc2897b658a`  
		Last Modified: Tue, 20 Jan 2026 18:47:57 GMT  
		Size: 38.3 MB (38295939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45a352e4f995bd27d86306ce1e227f327880604be2db220020eb505223b26de`  
		Last Modified: Tue, 20 Jan 2026 18:48:00 GMT  
		Size: 227.8 MB (227845709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-31-oracle` - unknown; unknown

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
		Last Modified: Tue, 20 Jan 2026 18:47:55 GMT  
		Size: 3.7 MB (3655371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c95d419a6c09e7c4b9aa0bde147c123a87905c34571f700ad9a2996571ac91`  
		Last Modified: Tue, 20 Jan 2026 18:47:55 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-31-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0acd132dc14def81e7402080b503d9197d48b65338012db9e11f5afc50293934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310372235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb94a23efdc56b7e45293b0117a1c16a381f3124a74b612eab9ebc85a1905647`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 23 Jan 2026 01:03:07 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 01:03:07 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jan 2026 01:03:07 GMT
ENV JAVA_VERSION=26-ea+31
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10149318b0d3fb31545f370908584b5804c5ac797fe8224b0f91ee6dc712ac13`  
		Last Modified: Fri, 23 Jan 2026 01:03:30 GMT  
		Size: 38.7 MB (38699886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63b73fda125793a74fa17da84c0678c3d1c60fdffe943ff5789a6177c211511`  
		Last Modified: Fri, 23 Jan 2026 01:03:33 GMT  
		Size: 225.8 MB (225770439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-31-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9fb9cac46e361014a6f8a828c165be7722579c99178426ca4194ed0133aa524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fda278c29fad9682298a7cb7e2b7d708fc5e45118344dcc1e1785afe55996c8`

```dockerfile
```

-	Layers:
	-	`sha256:5c403914f637ee7eaba0238af4c40b5fd8e68ca0930d67ecd048a563cdab3c47`  
		Last Modified: Fri, 23 Jan 2026 01:03:28 GMT  
		Size: 3.7 MB (3653065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244760da3829ed1e8f9051d141bd063fa8168afad3a57716f2743ae71170a16a`  
		Last Modified: Fri, 23 Jan 2026 01:03:28 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
