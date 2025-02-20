## `openjdk:25-oraclelinux8`

```console
$ docker pull openjdk@sha256:efb0186773edc5740dbce7a9636021bccf0fd055cf18e7ac78dcc7aaa73d301d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c194cb93b089fddad4778a37b88fbd5d8a89486725b3e00a8ef4f0569d5761f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278568528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8a5dce95406838ce912ab27346e5f79541ffdb598d5bb4b40ebff839d0a57b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 19:48:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07087e9c7fccbae68acd597cafa717397418263ef1da41fe5445a3d4776d1df8`  
		Last Modified: Thu, 20 Feb 2025 02:28:20 GMT  
		Size: 51.3 MB (51282175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e4b2456a3cb21006ee0d94c58986768600c047b5a7bf650cce0a20e0af60a3`  
		Last Modified: Thu, 20 Feb 2025 04:11:45 GMT  
		Size: 15.0 MB (14976446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90322098f685a65cb256539474dbb97a83f18118b40b258ac78d1868e39f1df`  
		Last Modified: Thu, 20 Feb 2025 04:11:22 GMT  
		Size: 212.3 MB (212309907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:18f72f17791ee87aabff2e4ab0a8ead145859c56aaa0cb82c61aa15bf62362ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f39f648cf123c56a4669702de13d68e48fe1b2ecd0c462c5c17d12ad74aec8`

```dockerfile
```

-	Layers:
	-	`sha256:ab8951040dd0e0ce41e77986f730c2b69ae5e5b1a239b56fdaf85f07d6dbe696`  
		Last Modified: Thu, 20 Feb 2025 07:24:19 GMT  
		Size: 2.4 MB (2444723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d821ae28b71916655ebb1e87184f04b54e6b73915f8d4e2827b72d093c158dec`  
		Last Modified: Thu, 20 Feb 2025 07:24:19 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bc97c856cabc41d2af8c03dc62d0aa0dbc830eaf5d637b7b823b46ffa3877709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275925422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753c468d42340a38e15c548bf0689c94b2f7ac026d272ac8dbd96619149e28a6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 19:48:17 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:978d351c82d6622560a8ee00b3a217333d2e989aa95df7bcb554a799b63d5a32`  
		Last Modified: Thu, 20 Feb 2025 02:30:53 GMT  
		Size: 50.0 MB (49985763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9e541b16ff664cd5febbbec24629b72164916363b1de234600bb25a76ed4c`  
		Last Modified: Thu, 20 Feb 2025 04:12:05 GMT  
		Size: 15.7 MB (15671745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e92623c3c40910d915c4340562cb2f38b4bf73ac0157c60f932722e770a396`  
		Last Modified: Thu, 20 Feb 2025 04:11:55 GMT  
		Size: 210.3 MB (210267914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d48cd4049b0673e3fd673adf260692935af87ade50f46ffc465619f548ec5053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f8217f43caa6dbb30e47c52c37a1755226d3059282d43a30d0fe43ce7b551f`

```dockerfile
```

-	Layers:
	-	`sha256:c82ac443286a115967c8f3e5f744de57387b9a9cb7353a7b4987e0f2178269f2`  
		Last Modified: Thu, 20 Feb 2025 07:24:21 GMT  
		Size: 2.4 MB (2443569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02765d21981bc9be2e19253fb7800ad4422a6df460170f190f14bfffe69286a5`  
		Last Modified: Thu, 20 Feb 2025 07:24:21 GMT  
		Size: 16.2 KB (16179 bytes)  
		MIME: application/vnd.in-toto+json
