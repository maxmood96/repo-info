## `openjdk:26-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:2d18688e93448c2ec5f60b0e1d4f3b6c84a34a37f9dd7541ac983bdf8e071b9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:17fe272adb30df70a0e185c5a7483d7648157e513b97b2763198780f1ca7d0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289788674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c658e405bd8597bbf5f797504f44f3c69eaa2f9289fea6a8988c9527b10b7fb7`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Aug 2025 00:56:10 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ee7925f71d4436611f8a3f69e3772842241f660c27b5808f5b26aeade34859`  
		Last Modified: Thu, 21 Aug 2025 19:09:49 GMT  
		Size: 15.0 MB (14977020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fa3b2cb2a00d50f710353798b8c395057a0d0e60a967cc526d70394c6a22a3`  
		Last Modified: Fri, 22 Aug 2025 01:06:46 GMT  
		Size: 223.5 MB (223488091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2c249be0bd44016506a39a599f45791d44c2428a40fd4f7663185e475be521a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aeeaad56975fe631ad64073521ea96be13e8a548f03baf5db3686ab23dbcf63`

```dockerfile
```

-	Layers:
	-	`sha256:8a130ead4145399bfd313dc9bb389ea127b739f154a1090ff776eafb91b86ed2`  
		Last Modified: Thu, 21 Aug 2025 21:24:23 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cb1b4dbc7ecac43b6518a4f197182dfc0b7f5f908a892620f33746f44f763e`  
		Last Modified: Thu, 21 Aug 2025 21:24:24 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c0394e876de74f0f42abe4cd6fd5a633329b9c24225e6c22d8ab75e346545a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287053418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1267788fcf283c12a3379b575df0fa990cd8da170afc8b986f0ed46d54d53a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Aug 2025 00:56:10 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9866c68be293aa81b529074549b7f38395dba71a8ea8fc528f721fbf8543b957`  
		Last Modified: Thu, 21 Aug 2025 18:57:24 GMT  
		Size: 50.0 MB (50039817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a01811484fdc87c21c7358e9f38ab4c42443d4a91eff20c2aa855940ad8b39a`  
		Last Modified: Thu, 21 Aug 2025 20:17:11 GMT  
		Size: 15.7 MB (15672244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c20a65d2ef7a05f62661383c75355a6aefaa476ec6e74ada234b4d3b32775f0`  
		Last Modified: Thu, 21 Aug 2025 20:16:49 GMT  
		Size: 221.3 MB (221341357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c8213b78edf95e253ae23a20ae619e37bad47bbc07c898eda319397a4e593973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4467e580f9a4c4a3875b66c44ffbb27335c71d94d4e3a811d9479ce0ba7a0e8`

```dockerfile
```

-	Layers:
	-	`sha256:b03831a9495769cfbdc8ceda6266b39693370ecc7bcca56b2089c276ba2d1be3`  
		Last Modified: Thu, 21 Aug 2025 21:24:29 GMT  
		Size: 2.4 MB (2449933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae6d4ab04fae36e936f9e274e190cf0e97765172d9f7f4d8edfee8ff0bdd43d`  
		Last Modified: Thu, 21 Aug 2025 21:24:31 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
