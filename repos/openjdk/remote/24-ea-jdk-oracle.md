## `openjdk:24-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:ba7b36d24b758627f372ff1d6e8b0a7009f68907108cb9d8008ce452244253c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:56eb57c30267cd68ab05a93dba90c479feb0e6b218de1308fda1266233e8db49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300440862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d385bdc8de8a9f6adf8b3bc2635a65272754b9aa994ea7f433a48f4f68e02d12`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
CMD ["/bin/bash"]
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 27 Sep 2024 06:48:27 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 06:48:27 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_VERSION=24-ea+17
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='983faf25eff38b5b396afabd191a91b239a1d803a0dadd01863861ecf731f034'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9eb980b4f1fde9c2387e0fab6b91b6f68cb109e3ddd43eda0013d9ee345f2dc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e646149b36fdec6d4c532f77f5500952e677d7fc8a2c95fcd14dd3cff7a17b73`  
		Last Modified: Sat, 28 Sep 2024 01:01:23 GMT  
		Size: 39.1 MB (39058916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa30e0b5cb8c9aa59b3a131a3769d0ce37c63c3ff14e27ccb3c45e56038a18`  
		Last Modified: Sat, 28 Sep 2024 01:01:33 GMT  
		Size: 212.1 MB (212135004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:ec17ab611ca73debf8e1a486fa402f1626e5096dfe64922119b8dfed45ddbf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68564f989587a6f464dc499606526ffe249b2f1d34845cba27d1c030418e5dd9`

```dockerfile
```

-	Layers:
	-	`sha256:01d2d6598e90b0ff82780733324343b446f736d38538c91f1a6debb0a268bdbc`  
		Last Modified: Sat, 28 Sep 2024 01:01:22 GMT  
		Size: 3.8 MB (3782218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ed3425cf352980b12f6102eb48c657c907ac1e379b2106f373d9c4b50cd47c`  
		Last Modified: Sat, 28 Sep 2024 01:01:22 GMT  
		Size: 19.7 KB (19712 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-oracle` - linux; arm64 variant v8

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

### `openjdk:24-ea-jdk-oracle` - unknown; unknown

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
