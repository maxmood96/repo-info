## `openjdk:27-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:cb5d945f8db031afd9756810e888f1ff7d67a65568b7d117c365b1ab0f18b7cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:4b367b88418862e16f1a278b8d95e2b5fa1179147db63edd9d4a4a8c2a3d3738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294836716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1c1034149e0b1914e3be81da0e1cd73c99e0f2d0d15bbf9f9ed628d681c6cd`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 21:43:04 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 09 Jan 2026 21:43:04 GMT
CMD ["/bin/bash"]
# Fri, 09 Jan 2026 22:10:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Jan 2026 22:11:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 09 Jan 2026 22:11:16 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jan 2026 22:11:16 GMT
ENV LANG=C.UTF-8
# Fri, 09 Jan 2026 22:11:16 GMT
ENV JAVA_VERSION=27-ea+3
# Fri, 09 Jan 2026 22:11:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Jan 2026 22:11:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0ddc6852d18db715e5e4c3edd3fa8bdf8afc37b9507d95d8bc0194012c32432`  
		Last Modified: Fri, 09 Jan 2026 21:43:27 GMT  
		Size: 51.5 MB (51465737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443a4c595956fed24dda84181abe9cb07dbbe906943f80033bdad8cf5cae3aea`  
		Last Modified: Fri, 09 Jan 2026 22:11:12 GMT  
		Size: 15.0 MB (14989233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f533e9f32708ea6e03abc1d68255ff3798d88d2f3fad0f08af7e8c0459e2e55b`  
		Last Modified: Fri, 09 Jan 2026 22:11:51 GMT  
		Size: 228.4 MB (228381746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6675fc8341b6e58c930bc8a52835bd62fe3660ec7d8a10c143205cd35bf9ebb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbe5935fda6f64c41f6c20e0bd04fd25c15677786f228d1ae08ee45cccc3af7`

```dockerfile
```

-	Layers:
	-	`sha256:80613d7ddedebe1bc5ff31657db36230a257a74c8a098022480f146b1e9edcee`  
		Last Modified: Fri, 09 Jan 2026 22:24:30 GMT  
		Size: 2.4 MB (2448674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf4bf1404f8a1ee20dc16b5c6041e8296cda628160137a46594c81fa09d963e`  
		Last Modified: Fri, 09 Jan 2026 22:24:31 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux8` - linux; arm64 variant v8

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

### `openjdk:27-ea-jdk-oraclelinux8` - unknown; unknown

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
