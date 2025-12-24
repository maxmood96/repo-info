## `openjdk:27-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:eacecbfbefbb1b9b18bff28f61ec45d735a0a584316ec29513919e1b769d744d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b9fb7da4e2dd147c6dfdc867050b96ae05b63d84411bbdc86a6927ff545c94cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294834980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec0dab73a54c3f5662eee2552e98aa200702158c3e113e5c0f1f4a2f9e6ac34`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 24 Dec 2025 06:11:56 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:11:56 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 06:11:56 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 06:11:56 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 06:11:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8733b0acee0106c8f62efb14cb858ac390eff6684a633a6bc8fae842fc784d6`  
		Last Modified: Wed, 24 Dec 2025 05:20:01 GMT  
		Size: 51.5 MB (51465497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19883a14511a7de1ea71078348d80633cbf14d2b203566fa125c127fea217151`  
		Last Modified: Wed, 24 Dec 2025 06:12:29 GMT  
		Size: 15.0 MB (14988253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aaf7780906280bbb6fc806de5bd886e303da9aee6d7bc9d2acb61031a25398e`  
		Last Modified: Wed, 24 Dec 2025 06:12:39 GMT  
		Size: 228.4 MB (228381230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:59bd93a9c358c14aa52d3d8c8f13e1549038c09722354780ac16249d5512cd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14430cdbc11b2b45c00561925aa4c4cfbaec1fefa9ddb652eb17032a074a2274`

```dockerfile
```

-	Layers:
	-	`sha256:57266bed9f8204dcea0679ec6b9b128a659e6bff049d5894182a39e8d2a7a446`  
		Last Modified: Wed, 24 Dec 2025 07:26:40 GMT  
		Size: 2.4 MB (2448664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d646e7e67c53d33cea6e60f0ef862303158aaa6880e8d8eccd2535694ac08834`  
		Last Modified: Wed, 24 Dec 2025 07:26:40 GMT  
		Size: 15.3 KB (15325 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:76cfe18bf36f95522f7d20d6b8bf78305cc0f6d93ee13aedd954ae813ad8c5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292208476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15b217d4ca794a60e37a230fb61fa0992f8778f372b5c7034cc6ae146239e5f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:42 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:42 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:12:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:12:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 24 Dec 2025 06:12:35 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:12:35 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 06:12:35 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 06:12:35 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 06:12:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c56c47048941ddf04da7dcfda383c6b40da72e218826ef10c27b29f2fb9db04`  
		Last Modified: Wed, 24 Dec 2025 05:20:02 GMT  
		Size: 50.2 MB (50177032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc0bb04486aaee3e6390f8b4c4d45615fb1a38fa98dfc77534a5e1a877627d1`  
		Last Modified: Wed, 24 Dec 2025 06:13:08 GMT  
		Size: 15.7 MB (15697409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb81abbca05c89f9d64114d0aed6f18cd9b31389555048b5d0792943e8434c68`  
		Last Modified: Wed, 24 Dec 2025 06:14:14 GMT  
		Size: 226.3 MB (226334035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:543f60eec43759b97e96a328c7e264902000553c14698bfcbb425a757280215c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89accccd688af621c52f3a50bd6f67e2ea05b3f1400c1024657867083f6f09c`

```dockerfile
```

-	Layers:
	-	`sha256:1066fc95fb26c96dfb4acef4dd8022c3c600e72b500a3059c9ed3e7f423b16a3`  
		Last Modified: Wed, 24 Dec 2025 07:26:44 GMT  
		Size: 2.4 MB (2447474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b223f0cb20796b4e5f9a3feebff6f6ec7cf40fbd3b8d64cd2620888ea976e9`  
		Last Modified: Wed, 24 Dec 2025 07:26:48 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
