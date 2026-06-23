## `openjdk:28-ea-jdk-oraclelinux10`

```console
$ docker pull openjdk@sha256:aaa162f2135c43322e11dbc30a0e889916ca582b82b867e28462b27daa335916
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-jdk-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:df303fde93f71f5da5f424dd3938aca8d7c4baa0378ef8637b23262d0a09fd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308153273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa22acfaab4631d0f9498145fc48b3240633ff31ffa6546aac5434fee951df82`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:38:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:38:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Mon, 22 Jun 2026 22:38:39 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:39 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:39 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:38:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7371e6244a01086c433ffe031a2039f7d26f9d0f39ede29f5b95676d39b6f9d3`  
		Last Modified: Mon, 22 Jun 2026 22:39:03 GMT  
		Size: 37.7 MB (37687485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6431e481a286ec3babe9ac533e24c5542098ad395db08c8d6c756d873852f8`  
		Last Modified: Mon, 22 Jun 2026 22:39:06 GMT  
		Size: 227.4 MB (227385206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:93a6fa39d435741f2609c27f1eba8cbbd7fb06e6f00f7cca84852149f04126ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c115e3f37ba349bbc7b6d6607cb10b6848427f6b122d47ea9b83bcc898d5cded`

```dockerfile
```

-	Layers:
	-	`sha256:9e10050878b053b470809ecfd73b905a56fe3c1164f3f831dfaf03bb4b83ab15`  
		Last Modified: Mon, 22 Jun 2026 22:39:01 GMT  
		Size: 2.4 MB (2366446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7851fad2ac44f48bb0195714b0537c4b695535152a81f015aba66f43b12935ab`  
		Last Modified: Mon, 22 Jun 2026 22:39:01 GMT  
		Size: 17.8 KB (17829 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-jdk-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:271f244da62e433cc537b95effff33e03bb8441828a5bb6b08638f041d6dbddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304609919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e74ef2bbac55abf15b735b68932e242be94b764760dd8c4c677373ae4c5b29`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:38:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:39:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Mon, 22 Jun 2026 22:39:01 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:39:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:39:01 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:39:01 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:39:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08168a2f34f52f07d826fa9a0d36c4374ffec9018ccc11abfcc6e6111e074be6`  
		Last Modified: Mon, 22 Jun 2026 22:39:24 GMT  
		Size: 37.7 MB (37695921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd130a9054892dc5032f236e9e2d99e90bd778b2d7fef569d716bd0543ba1be8`  
		Last Modified: Mon, 22 Jun 2026 22:39:28 GMT  
		Size: 225.4 MB (225418303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:ba8f7befc9e41c3f71f8771d4c3d216e27784fb23e667793d6a12fadbdf9f19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc050abb862909ffc181ef29d40934460f40826dd337943e95f1a8c53da89a9`

```dockerfile
```

-	Layers:
	-	`sha256:053abf6ce031f9b64c81f847523150027216c0724fa70363e979edbec8e5db53`  
		Last Modified: Mon, 22 Jun 2026 22:39:23 GMT  
		Size: 2.4 MB (2365974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db09ed71ba31f16e13f4a6219a05d1d948a09d3ddfb490e1e4afb130a01534ff`  
		Last Modified: Mon, 22 Jun 2026 22:39:23 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json
