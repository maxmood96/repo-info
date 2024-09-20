## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:8de121faa84f150ccc88449bcbab1e729a8e538407c9ac82228a9ef7b1a6a79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7b2a474abb5f383302ebfc72a15476a1c8fb0974674e63d5a372c202e7757854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278697983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ffd5042e772d594881fdbbf0f36d5af56696e9ed8c8f49992e80af7a025df1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
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
	-	`sha256:f7d760ad2fe664c6995a4d9508e389d78b6bdf1b1f154b4a216d0fd3ad9a46bc`  
		Last Modified: Tue, 10 Sep 2024 01:03:41 GMT  
		Size: 51.3 MB (51293960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c04c59ff8116e3833e79e0ed3f92a081b89c61c2eda0c832d663bd948f3b98e`  
		Last Modified: Fri, 20 Sep 2024 17:58:01 GMT  
		Size: 15.0 MB (15040893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb35fd9f224d8bf1429f8f0bd62497a3a55e604b3767df02869b2831508abb5`  
		Last Modified: Fri, 20 Sep 2024 17:58:04 GMT  
		Size: 212.4 MB (212363130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b559c2dc155dcceefe16020418ca2b6eee2805a6441ca1e3da01902a7986823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134dad57537fd514171226321ec2537d078196cae95393f7b911e5f2faf07a34`

```dockerfile
```

-	Layers:
	-	`sha256:150a6c6109cc414fc2d8bde4a8a72c7c8e3d392fd3f3c9dab5bd7e2b76e2ff20`  
		Last Modified: Fri, 20 Sep 2024 17:58:01 GMT  
		Size: 3.0 KB (3011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff4789662ad4b05ac8b78595f4050c3de553615107b007f48add0aec0179b4e`  
		Last Modified: Fri, 20 Sep 2024 17:58:01 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:55c8ea97704e02187a423e4c23c4ca93681ef1ca84df92aa631e13dc396cfce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275893462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcaeee4d39c66880601feb152096c8555109800c13778f95088a63927fb0f4e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:35:51 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:35:51 GMT
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
	-	`sha256:26021d1fe840c0392b944d95d8144754412f70a5f838918b647f05d3328586c0`  
		Last Modified: Tue, 10 Sep 2024 05:36:16 GMT  
		Size: 50.0 MB (50007854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8f1fe5883f1349449977ab234d0a93bca6d93708c0b7fbc87d663587cc3b10`  
		Last Modified: Mon, 16 Sep 2024 19:21:20 GMT  
		Size: 15.7 MB (15702876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f848e3b9b55cfdad398aabf2eb9bc02ced160a17f8733caf86556dbaf88341`  
		Last Modified: Fri, 20 Sep 2024 18:01:33 GMT  
		Size: 210.2 MB (210182732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c974331e95bb89cffa9ee548c88cb8785f2e3fa22eabfd4b16d7bb1b753ac013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824f54d8cdc20526a2c3ccd68d02efb64780e9f22f55f8f1c0b225c9bad5221c`

```dockerfile
```

-	Layers:
	-	`sha256:a5344c18f756c6437b6c35337c433b833a2c43d3ef4b455bc68275004b7037c3`  
		Last Modified: Fri, 20 Sep 2024 18:01:29 GMT  
		Size: 2.3 MB (2287338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4348221e4365b40639d9484d1034b5f2de4673489d1f3bb62fbd067552dbecb8`  
		Last Modified: Fri, 20 Sep 2024 18:01:28 GMT  
		Size: 16.4 KB (16413 bytes)  
		MIME: application/vnd.in-toto+json
