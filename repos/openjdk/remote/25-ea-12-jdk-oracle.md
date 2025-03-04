## `openjdk:25-ea-12-jdk-oracle`

```console
$ docker pull openjdk@sha256:01fdce68ff54b62112deca5bbd68665fb341ad08d9e0addcd7fcb29f4fe657a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-12-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:7f8f35c1c415335fb94e7960436d3d71d37fa93a3bbdf000e8a74c5d2e4a7b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309642336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937123708cfacc0c426412632650283e9e4b33a881ef32689f8913e62c501894`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 17:38:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 17:38:59 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Fri, 14 Feb 2025 23:29:27 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46559101bcc3bed5742e2831c931a16181838853eddcb0d7217ef7b0b4f1a2a9`  
		Last Modified: Tue, 04 Mar 2025 21:57:44 GMT  
		Size: 48.8 MB (48765839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902e05a1046d111bca3bc54d37706b632073f9e12b205c52c1d30324b10e62f2`  
		Last Modified: Tue, 04 Mar 2025 21:57:48 GMT  
		Size: 211.8 MB (211785606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-12-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a964fb6d6832eb297edbebeb18dbebf537fbea25262e17f0eda264f215656954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0175e6d6066c904acf94642d72132085529738aaf43cb48a02fe9dc939e351c1`

```dockerfile
```

-	Layers:
	-	`sha256:d0244940521334db0e32f42a495a82b40182dea66f7a60d594a8f1056b64800d`  
		Last Modified: Tue, 04 Mar 2025 21:57:43 GMT  
		Size: 4.9 MB (4907013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0554bbdf5f4c11a108ed5ff3ef957682073d6146284fe3d5cbbec6f154bfa0`  
		Last Modified: Tue, 04 Mar 2025 21:57:43 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-12-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a174ad52e3f15374fb580ce880e211bf4a9066e773ac3c1ed7f446ce93d55754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306574717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e27921cc4e338dd38e9389aaf9bc8776247f1ee3a4ca4072c2130cd8bf215d7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 17:39:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 17:39:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 06:45:29 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b0d69a874386856ef53a0253c98018d354dad7da9fb44540d22e351f1c97ae`  
		Last Modified: Tue, 04 Mar 2025 22:06:08 GMT  
		Size: 49.2 MB (49187852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc188d90187129eb6e826523433229f0d5160bd4ff0490b84dab55e5c755d8`  
		Last Modified: Tue, 04 Mar 2025 22:06:11 GMT  
		Size: 209.7 MB (209717650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-12-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:44815a3175755cd1717d33d87f3d66dc014b58f45578683a47bb8941ba184c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f6ab4ccc0ccbbdaa8e9ab32444d99915e8aaf85d4b5ef05cec1d0f6ad15fbf`

```dockerfile
```

-	Layers:
	-	`sha256:5d378c82120351c1ac90a3deb1f7e687a7373af7c67bd604ae62ba70d7048930`  
		Last Modified: Tue, 04 Mar 2025 22:06:07 GMT  
		Size: 4.9 MB (4904775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c9909c1454abae7778de00ac6469959e36514d28eb3765c156c71aad6d9727e`  
		Last Modified: Tue, 04 Mar 2025 22:06:06 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
