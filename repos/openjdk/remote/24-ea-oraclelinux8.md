## `openjdk:24-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:1c31fd7c3e175bd46c825f478636c9f26facd2876f25f6cdcc15089b310ca660
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c742a6e35d01e9b9f63d4d23cb258c154fb5ebacb6881a172f1469148c26dfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (279024624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1b6b4eb7725129ca8201f5b99c2c29193ac719f3995c1489b6ead377071656`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Oct 2024 18:48:13 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["/bin/bash"]
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ccec4de1d50efaab175e979c24b513dacdec266a6a00f442167c614564b83ef0`  
		Last Modified: Fri, 11 Oct 2024 00:11:24 GMT  
		Size: 51.3 MB (51295624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5915e1e0c989e6c6c3d91b4a857bd4bff65509df333852b1f1b99caf75b209`  
		Last Modified: Fri, 11 Oct 2024 00:50:38 GMT  
		Size: 15.0 MB (15036577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d57a6e825d0bda42fdffe267399b2f1a7b3d2b458372fa11cc52ad4d32459a3`  
		Last Modified: Fri, 11 Oct 2024 00:50:42 GMT  
		Size: 212.7 MB (212692423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6d17470edf01ff3086c39e3e15cc45957552689102a6ec92dac40543ea1d198d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2441821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a253bdc6c7260d04cc6dfc61e5d320f0360500d7479bca1b75a0a4984fff7c`

```dockerfile
```

-	Layers:
	-	`sha256:7645d3534ed387f58c2e1f73714058d1a5905cc4586bd03ef45abee4b3e0434d`  
		Last Modified: Fri, 11 Oct 2024 00:50:37 GMT  
		Size: 2.4 MB (2425812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fad41eb737e203756409181b1a10a39a2515a8d55bc8447b2ac8b31f8c6eb91`  
		Last Modified: Fri, 11 Oct 2024 00:50:37 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0b6d70567a69b96c18e47b97ea15abf1c8967ac342142a103f9494ef4812038c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276225988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8882b8b5053ef4141b5c7e59927d02b12e81014f87ae8d37acc9d854fbeced0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Oct 2024 18:48:13 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["/bin/bash"]
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5aa1f5d85d147a7c16d0057c3fc21b1ae3d482ca5ede955163a95cc540b4244e`  
		Last Modified: Fri, 11 Oct 2024 00:11:55 GMT  
		Size: 50.0 MB (50004038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096a2c0e68dd1c814c85ae00b2652f096632e44095b6ac5ff4756a756a3ef3bb`  
		Last Modified: Fri, 11 Oct 2024 00:50:19 GMT  
		Size: 15.7 MB (15706108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f507085e9b971a01ee255037bc5df0419e5e72102559d91c1d1f0368802e2ed`  
		Last Modified: Fri, 11 Oct 2024 00:50:23 GMT  
		Size: 210.5 MB (210515842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a4c66eaba1e3975cdf215673f0e8f6d007b01fc75a93bd25edc46d5c2cc93172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012ff4386d16b7c3da7f70c62fd553c38b1ccd02609b696b5f8604c7d15e0972`

```dockerfile
```

-	Layers:
	-	`sha256:6aac622a226ba441a53b6c602184d209ef6a9c44082d48102db60e828c36e1f0`  
		Last Modified: Fri, 11 Oct 2024 00:50:19 GMT  
		Size: 2.4 MB (2424034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954b45a92e1375809666203ed1802ddd283144ae49ee43b5bee6594db78f8219`  
		Last Modified: Fri, 11 Oct 2024 00:50:18 GMT  
		Size: 16.2 KB (16152 bytes)  
		MIME: application/vnd.in-toto+json
