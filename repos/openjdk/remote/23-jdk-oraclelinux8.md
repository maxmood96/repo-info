## `openjdk:23-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:4e096d673aaa2f04b4b0f1494e772852fe7adf2ba24c03f0255d5f6dfd7fed3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f61ebb49cc27a60f77ee75624a28f14aceeb058ba291aeacfd7c696f3fb8cc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269069804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637ea04c20ce35d4a255853a2a714510d9ad586839c7ce15d78ea2e3d7221856`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:29 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Fri, 08 Mar 2024 19:21:29 GMT
CMD ["/bin/bash"]
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 22 Mar 2024 18:48:16 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Mar 2024 18:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_VERSION=23-ea+15
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='c17995b5c67b845af47704e2a664f5b6ab540f968cfae06972a7562144b7634a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='804a15db8c406a0d70ad5a2da125339de3ff66759107fdd75bc6323d6d0cc5d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d4dedb07bc16210b98e165cd376617647546fe0412810fbbca98ba56d9589d`  
		Last Modified: Mon, 25 Mar 2024 19:12:57 GMT  
		Size: 15.0 MB (15024142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff8de7cb060305a83646ccf1304bafb9c0df550f19bbc741f55d676cedb378b`  
		Last Modified: Mon, 25 Mar 2024 19:12:59 GMT  
		Size: 202.7 MB (202718242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a81f545a78fe4c5ef6f99ed70b9b9275d9e6da044f9a1b7390cedd8c7911a843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad8639637c9922e0f3e0e6f058d9c709bd0d5ebf8bfc676600e1aeb7326f96c`

```dockerfile
```

-	Layers:
	-	`sha256:84fc392e23a4e1202b9a03c7d52522cc503e37292995d54a8cb2eb1e0002f622`  
		Last Modified: Mon, 25 Mar 2024 19:12:57 GMT  
		Size: 2.3 MB (2267466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01b409f9faa38d802712a9f96ddf3ffcb860fc3499aaf447e2dae4907afbba6`  
		Last Modified: Mon, 25 Mar 2024 19:12:57 GMT  
		Size: 16.2 KB (16180 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1717133ae164a23119606d246cbcbd49d5e71258dcf99ca742e40ea000883177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266375464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c02dd472bdc5f5dfd753444ca7acac2a373bbfea27120350535c33eaaa8879`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 22 Mar 2024 18:48:16 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Mar 2024 18:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_VERSION=23-ea+15
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='c17995b5c67b845af47704e2a664f5b6ab540f968cfae06972a7562144b7634a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='804a15db8c406a0d70ad5a2da125339de3ff66759107fdd75bc6323d6d0cc5d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
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
	-	`sha256:1960df209637b4caf792450f0fb94da3f5114b453b4f7ba54c740e17e5c8a2f6`  
		Last Modified: Mon, 25 Mar 2024 19:55:42 GMT  
		Size: 200.6 MB (200613303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:81c96504eabff37adaa487d7f257bbc78fca8f19c28589dd76692dfcacabe6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7819b446e55fcef462c9b587f96ee3f0e41de572919ff84e2f74c67b83c1dae`

```dockerfile
```

-	Layers:
	-	`sha256:9446faa3085bf8bce1e0b5bfcd3ddb90071c8c8bbfbfd4597bde443e1508d364`  
		Last Modified: Mon, 25 Mar 2024 19:55:38 GMT  
		Size: 2.3 MB (2265910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee7a55abcacc498925d1488122626014724b19e4d35eea0fe31b30277da17ead`  
		Last Modified: Mon, 25 Mar 2024 19:55:38 GMT  
		Size: 16.0 KB (16027 bytes)  
		MIME: application/vnd.in-toto+json
