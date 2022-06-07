## `openjdk:19-ea-25-oraclelinux8`

```console
$ docker pull openjdk@sha256:9d695166ac057e43b38e285a6abe357a7fe55a14ebe337422c1e7394c2e2bdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-25-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ee61f4d332404ba29ea2b818f471493c30fa8bc0bd3cbe00cf9aab761b0e6558
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248527807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e99921f1715fb472a11a27be5c3bbe3cf7becda5d2e7f7def2e084950487cd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 17 May 2022 22:41:42 GMT
ADD file:bbaf69bdffd0f506e447fbc52dca450a8966d950b8fa9aebd3a1bd5bd98f8b28 in / 
# Tue, 17 May 2022 22:41:42 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 22:58:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 17 May 2022 22:58:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 17 May 2022 22:58:38 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 May 2022 22:58:38 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jun 2022 19:43:50 GMT
ENV JAVA_VERSION=19-ea+25
# Mon, 06 Jun 2022 19:44:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f03ae5efd6a8fe2211e9c3e0566289d405193244c67af680e202aa9f44473cb0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f0c7f51bcf0bcca03127dd1dc7f9b59a88636714ea2bfd0707da665f98011237'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 06 Jun 2022 19:44:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90a00d516db16c568d3da8e0a7a5a78fa6fef5a39f3d688f831d254b77791565`  
		Last Modified: Tue, 17 May 2022 22:42:38 GMT  
		Size: 39.2 MB (39220501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fc60984518a14e9454222efb6ec0a4e8c3d479f4aaf21961fa45df6b0622e3`  
		Last Modified: Tue, 17 May 2022 23:05:19 GMT  
		Size: 13.5 MB (13504594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00966909e6f885f95da1662eee7370888f27587ac7dac65f090e275fececf18f`  
		Last Modified: Mon, 06 Jun 2022 19:50:33 GMT  
		Size: 195.8 MB (195802712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-25-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d90c8fd766285fb188e5eaf252ccc95ae4899ab40ee86840fa84891076218832
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (246978648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aed53295e65ab8bd4547f5d0caea293f8964f2de323d3e7a293ab073601575a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 17 May 2022 22:52:38 GMT
ADD file:263fe8ce0663428b324fa2909814084a77bf17118d772058d41546b804a4b968 in / 
# Tue, 17 May 2022 22:52:39 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:12:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 17 May 2022 23:12:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 17 May 2022 23:12:09 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 May 2022 23:12:10 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jun 2022 22:45:01 GMT
ENV JAVA_VERSION=19-ea+25
# Mon, 06 Jun 2022 22:45:22 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f03ae5efd6a8fe2211e9c3e0566289d405193244c67af680e202aa9f44473cb0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f0c7f51bcf0bcca03127dd1dc7f9b59a88636714ea2bfd0707da665f98011237'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 06 Jun 2022 22:45:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dbddf5847a3e154a061766ddebe6a3cae471c97cabb3be2871f6d91f265d137`  
		Last Modified: Tue, 17 May 2022 22:53:43 GMT  
		Size: 38.0 MB (38012703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6f1a9466bd7ec91933e510c0258839b2df2301b1d385203492a27a3d66f0ab`  
		Last Modified: Tue, 17 May 2022 23:23:18 GMT  
		Size: 14.3 MB (14273985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4facbe1354797ad65609bb717553bf718d6c1d41eb145a96b3072a866e2cc06`  
		Last Modified: Mon, 06 Jun 2022 22:57:38 GMT  
		Size: 194.7 MB (194691960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
