## `openjdk:24-oracle`

```console
$ docker pull openjdk@sha256:6989f133751c14c37112711f74b7307e8304e4bbdb13d6d1d56e0c2e1c52608f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:b008bd2eb168964aeb50701850d50da055fa8ba1ce5239bfaf58ec084dde8be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301518849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb3e19ea5f2c0b9accede63d3ff74b8910736ef42b971914a612dc1c2b36b86`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 14 Sep 2024 06:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Sep 2024 06:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_VERSION=24-ea+15
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='b41d4867c348d7f1991085d8bcc8797eaf032d9dfaa3419bc9db15eaea75e91e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='165b7c19403e9708ca261cdfe4c385e837df683049203e33ad2bf76228054a25'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5e407bf3af905fb1f6edf271f870052697e79b018f921119921615cd25365fdb`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 49.2 MB (49239252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b827a6775178595a4e839f335fb59d678dace1d642b33f76e68550f367346f6`  
		Last Modified: Mon, 16 Sep 2024 18:58:02 GMT  
		Size: 40.4 MB (40417947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fb5533ac77b9dca88397e870dfc5032b19a0478d14ea72b95dfe64dbfba361`  
		Last Modified: Mon, 16 Sep 2024 18:58:05 GMT  
		Size: 211.9 MB (211861650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c42f882692a731764cad821c83d01624ed013032860e6213c3e6c4a68a3165d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602333ce284b5c82c5e16a1892ec8d83002cce9906404a10e073168a74d5773e`

```dockerfile
```

-	Layers:
	-	`sha256:030c526d3d5041c535b9a5d454a9626f2b10776311bf96094558023dd48aba67`  
		Last Modified: Mon, 16 Sep 2024 18:58:02 GMT  
		Size: 3.7 MB (3670499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef8978d8b8406e1d7586d39234697e856c03f6d1cb5d4784c32d4e8137bb57a`  
		Last Modified: Mon, 16 Sep 2024 18:58:01 GMT  
		Size: 19.7 KB (19712 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0f84e714d9ced149e8ef09ba0b5967296750cc1887f398937ef4bc1837b931ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297122449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c815988d71c3bd9f745411b8b50e356c9c91ba4a120a5d9f2802ae573644378`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 00:48:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 20 Sep 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Sep 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Sep 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+16
# Fri, 20 Sep 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='46c9e29e1e700ac596a07ef1795142939bcfd687dcc7f959043886bf800a3bee'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/16/GPL/openjdk-24-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='f42ff15af07babf02cf4dc52c121b18be22bc6f54d6b041b424687f82cdd9919'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Sep 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8012429b70e0979dd49dcb64d258b15c848e133db0919f7c15e7acb1c1da0ad`  
		Last Modified: Fri, 20 Sep 2024 18:54:09 GMT  
		Size: 39.5 MB (39489281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78baeda8008f5dc6942ad18ef635be964181a794c451b1d60fd3425731980d3f`  
		Last Modified: Fri, 20 Sep 2024 18:54:12 GMT  
		Size: 209.7 MB (209718585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b093a7605da2b2f07e3ce7d460eac1a0ec177defe613cca4f545dbfdbd346694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3662959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16965a98fe9a978021f3a3265082ed91c64e6560ed642d6b2f0e86a4d3861f98`

```dockerfile
```

-	Layers:
	-	`sha256:8aba7302c2fdecaabc6fea7c8bd7a574f2756d483cdfad4368e2a7a17dbb21c7`  
		Last Modified: Fri, 20 Sep 2024 18:54:08 GMT  
		Size: 3.6 MB (3642694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00c8256a804322100ff7413ac64af2baf119288dc004c3181345609cd6b5941`  
		Last Modified: Fri, 20 Sep 2024 18:54:07 GMT  
		Size: 20.3 KB (20265 bytes)  
		MIME: application/vnd.in-toto+json
