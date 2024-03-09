## `openjdk:23-oraclelinux8`

```console
$ docker pull openjdk@sha256:a03759fec4fa7bd287177b85ae924a520a055f77246f19a1d1a24405fe8d726d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:959e72b2ca583c0d782f3235c93e07b840b0e235d974e3b6ac7efda3a1be8c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269165265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5995c1f043dbc74760c31048cdaf091821e7bdbd5ae19e9579937c967c70eadc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 01:48:16 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab0ff0d1f1ef791d4d90d71939d7e4c6d169142c92e21898038b2687d1ee1a6`  
		Last Modified: Sat, 09 Mar 2024 01:49:34 GMT  
		Size: 15.0 MB (15024082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851e9efb5e918e3625dc45dc7a4524cac60137cea1f17e15ff773c7117103bde`  
		Last Modified: Sat, 09 Mar 2024 01:49:37 GMT  
		Size: 202.8 MB (202813763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:68f218973ea83b5f3cc27c2d2f1dce7f526c49302546d9f69e821ce566c871fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d406d0f2e208c51262618de953d48a22df0c85a402c9f9685fca514c4d4fe5`

```dockerfile
```

-	Layers:
	-	`sha256:df0d5baa79eb0c1f9d4e79fa708e23d1df1422db77f8e03cf561240c29b91485`  
		Last Modified: Sat, 09 Mar 2024 01:49:34 GMT  
		Size: 2.3 MB (2271204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ef41ef5fe3c0b0d3611b9219e8714fa54419c511de6570dd2768fc51ff4a850`  
		Last Modified: Sat, 09 Mar 2024 01:49:34 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a7e5723b95ca8ebb5cd48e952cb9618e3fec79b7a6a60c35a42a8688b9ea4978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266441434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3d2a94e2256c25545ef3c35b4e27d346001ec6e9eea7c7ff2f618dc7946265`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af35d928931c3ca203151c89e36f80ba86ce2c97d68e06bcf670bc27c9fd502b`  
		Last Modified: Sat, 09 Mar 2024 03:44:57 GMT  
		Size: 15.7 MB (15689279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43984a524e592351e9feef17775b6422369934d25e03ef8e44a30989be5f0f9`  
		Last Modified: Sat, 09 Mar 2024 03:45:02 GMT  
		Size: 200.7 MB (200679241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:23cd82467e726b39b8c2ff40009b60092d16da49d9c948588ce29a5fe525b611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216b623d393fd0b87af5c731319ed6989099e52fe80f6a0238b568aedd3c5c5e`

```dockerfile
```

-	Layers:
	-	`sha256:bfbf140b7db7a69ffbc95605752fe19e2493e388a9c721a92f284402e541c8d7`  
		Last Modified: Sat, 09 Mar 2024 03:44:57 GMT  
		Size: 2.3 MB (2269674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac055661c863f811e4841f66f3181943a296a2684ccb5e438ad64074410bd76c`  
		Last Modified: Sat, 09 Mar 2024 03:44:57 GMT  
		Size: 19.9 KB (19927 bytes)  
		MIME: application/vnd.in-toto+json
