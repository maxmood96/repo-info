## `openjdk:25-rc-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:03d5f390dbe4ac41133560bcd76b198e884393264a0ba4e27878ed3f54a895f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-rc-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:65b1da9adedab0fca40f97617372e0173b5b81a06bf60eae14453ffad1309e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310570684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19b487d0613b8d6ffdfeaceeb84576346f23486639b7f7e9b3c979e6e377f7a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Aug 2025 00:48:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6ad5d5a48937ae636b7d1387fce61ca66f85bcde401fec14d2e6c4ead9b9c3`  
		Last Modified: Thu, 21 Aug 2025 19:09:44 GMT  
		Size: 38.0 MB (38005223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a166cf2b0e741aee65ec9832dc660899b85c4ea2911435fe68f17a7e70b2ce`  
		Last Modified: Thu, 21 Aug 2025 22:01:33 GMT  
		Size: 223.1 MB (223068445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:2d7cf7b6a1e1e9fbb48524d3defa9598fd26941a5025fe21a3cc18c1925ac70c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3657300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40739ce8da9159dff67136748832b2fbde4d37ba82f7014e64d53bb4fa6b672d`

```dockerfile
```

-	Layers:
	-	`sha256:d5aaa2eca3b7c96680a248309483b0222f1491512ca737c02e9421b28aab224a`  
		Last Modified: Thu, 21 Aug 2025 21:23:22 GMT  
		Size: 3.6 MB (3639418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cac2ec64d62015b76ca6dea2a34a1f9a189a370d2d2ba3ac1cdccb68100fff`  
		Last Modified: Thu, 21 Aug 2025 21:23:23 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2c4f8a398ce73ab47d59a31f367ed771fa1d3b644da75f6707324087cd5cc486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307361863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a6f6a8abc78c39946ee1a3226912f417977f2e62c293bc3d48931aa96b6a3f`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Aug 2025 00:48:25 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f251bedb6d0a7854cec601a06650a41a8800628c25948fd9b15b8018354d6f6`  
		Last Modified: Thu, 21 Aug 2025 20:15:43 GMT  
		Size: 38.4 MB (38406411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695473080251df88385085b9e25be2d5df959c8470422d01ac15c587b472ca7f`  
		Last Modified: Thu, 21 Aug 2025 22:01:52 GMT  
		Size: 220.9 MB (220868729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:e5c126ff54a12b34a1ab39e1de624253f34a9f2fb089180905cf78cfb7fbb2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3655202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652fcbd2124f207c644a5c169fdb5f2f86a56f38f5a52c08334573a5c6491fe7`

```dockerfile
```

-	Layers:
	-	`sha256:343a93b9409a36778d4fc6878e669d09fc7e2ce59d6a58ff7e727f0f180f1a39`  
		Last Modified: Thu, 21 Aug 2025 21:23:27 GMT  
		Size: 3.6 MB (3637108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5795064623fbaa69de1e62965fb1f671d1bcfc1eb8638064559f1af6a310f13f`  
		Last Modified: Thu, 21 Aug 2025 21:23:28 GMT  
		Size: 18.1 KB (18094 bytes)  
		MIME: application/vnd.in-toto+json
