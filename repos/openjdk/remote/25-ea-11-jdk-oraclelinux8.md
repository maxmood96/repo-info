## `openjdk:25-ea-11-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:9a871f4e50e307bd10c2b3e6cfab8694520d715c0c673f5fc4ea4958b3dcee99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-11-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:0715f7ac41a939ee6f799dd9800c54efb54d96599859f27ea68a53317674dd51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278526003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d660462ab5a681cdeb0ca036c31381fd3bd812a1c1743173c8b300744cadb6a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Feb 2025 17:31:06 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 19 Feb 2025 17:31:06 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07087e9c7fccbae68acd597cafa717397418263ef1da41fe5445a3d4776d1df8`  
		Last Modified: Thu, 20 Feb 2025 02:28:06 GMT  
		Size: 51.3 MB (51282175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0de2b2f7a148266b40b402d534f3e35b9f663256f25bf0d3ea238b60bcea57`  
		Last Modified: Sat, 22 Feb 2025 00:29:32 GMT  
		Size: 15.0 MB (14976479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e68acb4785deca9a7241eb57b8d44e133c06dfd8cec103e504f1a98fd8f59ec`  
		Last Modified: Sat, 22 Feb 2025 00:29:35 GMT  
		Size: 212.3 MB (212267349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-11-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:298f8a53f33aa49922bd321d1ff4d430bdc16138b25d40984ce410acfc8eb8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a1c0ecf32e5a4018c0d8f912b6d0c164a6512e6cd46f2f47731f545518d6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5a59fedd8461b33f7712c9041d4dd5c56d9a5a772a261c1d0538618a39587b0c`  
		Last Modified: Sat, 22 Feb 2025 00:29:32 GMT  
		Size: 2.4 MB (2444723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688db18b16d90ae2dd1341e81ab609376662cb15f1188474675d1d6758b37fc8`  
		Last Modified: Sat, 22 Feb 2025 00:29:32 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-11-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:76b43364e300e4f764af06e71a9b0ac0e70ca1f0f48e99b1bbe2f08cba5b0db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275898146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399478ec7e7fe5c07b4d9f2d957a92dcb6d3c0bafecd154d04fc500d241fba5d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Feb 2025 17:31:56 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 19 Feb 2025 17:31:56 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:978d351c82d6622560a8ee00b3a217333d2e989aa95df7bcb554a799b63d5a32`  
		Last Modified: Thu, 20 Feb 2025 02:30:36 GMT  
		Size: 50.0 MB (49985763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9e541b16ff664cd5febbbec24629b72164916363b1de234600bb25a76ed4c`  
		Last Modified: Thu, 20 Feb 2025 04:11:52 GMT  
		Size: 15.7 MB (15671745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def162086cabdaff48e5fdf59dea19b428a629d36da18e6673a19ebbbbfa120e`  
		Last Modified: Sat, 22 Feb 2025 02:35:25 GMT  
		Size: 210.2 MB (210240638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-11-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:800911eb106ddd3eea9be7b24a178ee3750990b03272230b86e8cbc38d6435e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cefa00146b6da3fbf84be0b31f54727f75cda73e009cf9227ebccb983971c6e`

```dockerfile
```

-	Layers:
	-	`sha256:cc8a401fffa9799e30e62182ea7db5f39ad5203cdfa0bc17a27c5934f72e00b6`  
		Last Modified: Sat, 22 Feb 2025 02:35:20 GMT  
		Size: 2.4 MB (2443569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c8a95ec68d8d964115df469d9bf03b3b284317424c62824bdcc223a58bf47a`  
		Last Modified: Sat, 22 Feb 2025 02:35:20 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
