## `openjdk:23-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:6a7f102f2d7ceccfe35305f46a57e63ae10caa6706204cdf514a392207e7b53a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d47f1d5ee8b8f4bd416c4851750c3c2e02d1e422b66c593c5d01a75c40ce6872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269116657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17266f061debbdacfec564871d48279a3a07031ef9d26b10bfd266361f4d12d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Mar 2024 00:48:42 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 00:48:42 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0a4f3843ef0ef0075f8dbadca852eb8fa40928a1b5397d8c9d1c78ddbbb92a`  
		Last Modified: Fri, 15 Mar 2024 23:56:16 GMT  
		Size: 15.0 MB (15024010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92d8a2d7a8eaa84bee2f38bc307474035197965e8c9cd8975e54491aa88848a`  
		Last Modified: Fri, 15 Mar 2024 23:56:18 GMT  
		Size: 202.8 MB (202765227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5014b0d76ecf0b403f3741adf1fb4ac3176b21454ed57897d783f614b84dbf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542a3413f1971f4034f446d0c73d1771a492d27a383c5f56afd78ccca8b0fae5`

```dockerfile
```

-	Layers:
	-	`sha256:0923c5c6a0da1580ffd5ccd46ea1c2ef708fc20ed655980a8172d9e710e486eb`  
		Last Modified: Fri, 15 Mar 2024 23:56:15 GMT  
		Size: 2.3 MB (2267498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd7224288bd0d75cb6ac692ccdb872a887f68e8b0deb73f3f4a43a038235ffc`  
		Last Modified: Fri, 15 Mar 2024 23:56:15 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:696887dbd131d54d9fc42ff30bf28a0e82b7cf62d909fe27acb4caaeb882306c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266384780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f9d932890a02353c8082e4e5d5c4cdfdc26edfde4ade1843d64e81c66bea45`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Mar 2024 00:48:42 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 00:48:42 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d68f32ba337d0cf2080b7122389f26b960df4be750efce6ce2c697e964cb10`  
		Last Modified: Sat, 16 Mar 2024 15:52:13 GMT  
		Size: 15.7 MB (15689247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88396b803c83bd58d12494606e519a28164d5c0175202f15bd925e1eaa0c7d50`  
		Last Modified: Sat, 16 Mar 2024 15:52:17 GMT  
		Size: 200.6 MB (200622619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f93a3b7c75708cc0838aaa3188fe1dd0b875361f42875456e67d29bf85ac6493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2c2eedb1e16c718574288d41e3be81e329fee088898be8ceb90fa800a8d6a1`

```dockerfile
```

-	Layers:
	-	`sha256:5b065e9afa6313b22702109e58aa5722c0e61201f8bd2cd2dd7cb5b7e3edbb43`  
		Last Modified: Sat, 16 Mar 2024 15:52:13 GMT  
		Size: 2.3 MB (2265942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d51af8490cc8fd7384709022b955489a7fb15adf961a021f50b19c249861d84`  
		Last Modified: Sat, 16 Mar 2024 15:52:12 GMT  
		Size: 16.2 KB (16195 bytes)  
		MIME: application/vnd.in-toto+json
