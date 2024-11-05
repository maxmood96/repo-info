## `openjdk:24-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:ffe749d71aa9bc30b93e5b4e14c3e870519e47ac0c57f13c573c522a75855597
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ed418b19b929aff8be27ee650928dada080b96681b2dec3a9ed6c8ae08585c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278839165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8187d28b5e8311dacedb5f2e810d1d092cbc1bb881e3323575d7e05c3e95ea4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 10 Oct 2024 22:15:38 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 10 Oct 2024 22:15:38 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ccec4de1d50efaab175e979c24b513dacdec266a6a00f442167c614564b83ef0`  
		Last Modified: Fri, 11 Oct 2024 00:11:24 GMT  
		Size: 51.3 MB (51295624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f2dba6556b6e2df0eefb57cfd47e34d3e6d254991fcbd579de1298841e018e`  
		Last Modified: Mon, 04 Nov 2024 23:07:55 GMT  
		Size: 15.0 MB (15036659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab5ee20f8446110005fa2442539f276507d188beed7c72cce0c0ad943b52ed6`  
		Last Modified: Mon, 04 Nov 2024 23:08:00 GMT  
		Size: 212.5 MB (212506882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9903fb5b6af4cce1b0517a74d73337de0ba8481024903bacdc4fad7234745bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2441837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5cf4e90c494a2ddefaf1cd5c062dd309b4b40c4a1ed897ef9462f0971fa008`

```dockerfile
```

-	Layers:
	-	`sha256:daf2536b23b5f4478c5109253d3343ac77eca4e313ce7da96ed5f7342ffa2a40`  
		Last Modified: Mon, 04 Nov 2024 23:07:55 GMT  
		Size: 2.4 MB (2425799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89dddc069c2c0993c1823909a8beebabd039d67b54630e32b6ac7d7f0ec14850`  
		Last Modified: Mon, 04 Nov 2024 23:07:54 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2f177fe9cecff43023393a5b24982f1ed4d3f50655982be7b48f4f873643eefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276055254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3676dbcc01792fc09f7d2d9e6a0222d4e52d598b9a67ed1297a360bba70a95b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 10 Oct 2024 22:16:27 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 10 Oct 2024 22:16:27 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5aa1f5d85d147a7c16d0057c3fc21b1ae3d482ca5ede955163a95cc540b4244e`  
		Last Modified: Fri, 11 Oct 2024 00:11:55 GMT  
		Size: 50.0 MB (50004038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648be44c45fee0bbcac8466e4b1e01e530143c1aa503a78171164f7ef9df3e95`  
		Last Modified: Tue, 05 Nov 2024 00:11:52 GMT  
		Size: 15.7 MB (15706075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ce500be2d2b9759c0d9018743079c5f6217aaa67b3459d7c3f3d54d115229c`  
		Last Modified: Tue, 05 Nov 2024 00:11:56 GMT  
		Size: 210.3 MB (210345141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:3ce9bc8dc35b4d40fb0530e2593cc4bdd8dc0ba050d81b8d36d24857d95f15b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c202aa14fa787018d56718ffe8649d0f2ae97785fe8746e5b4d11af42e8d076`

```dockerfile
```

-	Layers:
	-	`sha256:840200539e3299794a3ce682df701ff5fb3fff5745feb6fd5fe6cb219da7e650`  
		Last Modified: Tue, 05 Nov 2024 00:11:52 GMT  
		Size: 2.4 MB (2424021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5c7920bc3237ca5b4f425f6df36e12a51e466a85f1f493ddfdb191210dc5131`  
		Last Modified: Tue, 05 Nov 2024 00:11:52 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
