## `openjdk:24-ea-16-oraclelinux9`

```console
$ docker pull openjdk@sha256:13edfff0729d0889c679a3bdcda7438f60601944097aac7872f190a91d99ec08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-16-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:5c63c9b2ec3362b971dcd0f93fdf990433061d96f2085d3fac2a52da5e4e045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300203777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff923a102b2c20c154abbf102402d3717af79c0b52c61d832e7e5d16bca6a4b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 00:48:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f341352316cc866e547498216e96bb74dffced820c84eca75eabdba461fccf2c`  
		Last Modified: Fri, 20 Sep 2024 18:49:44 GMT  
		Size: 39.1 MB (39058897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7691e0c89fe3257698a1747d8a43ec0947d898b84be8cdac40c0cc127fff8`  
		Last Modified: Fri, 20 Sep 2024 18:49:46 GMT  
		Size: 211.9 MB (211897938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-16-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:95b046060d9f40221e12ddb2783bcdaedf7476f674bf9ecb49601d9fef42367d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aec240694c9e65f2da9bce4a888a460719eeeaaef0876a19d2a0b4e1f8eef65`

```dockerfile
```

-	Layers:
	-	`sha256:9307c0632fce6d75388cb140472a7bc7e509c8bcb11fb356bcd3b11806465763`  
		Last Modified: Fri, 20 Sep 2024 18:49:44 GMT  
		Size: 6.7 KB (6719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904769c69f4eef98e412ecb04a7de646bce8fb8e2cf4a32250e374e5fa022719`  
		Last Modified: Fri, 20 Sep 2024 18:49:44 GMT  
		Size: 19.7 KB (19712 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-16-oraclelinux9` - linux; arm64 variant v8

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

### `openjdk:24-ea-16-oraclelinux9` - unknown; unknown

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
