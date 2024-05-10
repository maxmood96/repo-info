## `openjdk:23-oraclelinux8`

```console
$ docker pull openjdk@sha256:80cedebdf86bac8cff0c653ae1800db4a36a0e0a01f01d8ed25dba8c7160acc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:85e88b24b81cd26edb49a6ac800cb7ecff81b28c7662fc79348ab469fb67463b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276242087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe2022ec4804d4702a552408bab37b925f5d6fd9bc6a8dab8115baff014a536`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 18:48:15 GMT
ADD file:4ff19cbeee6ebf4bee966dae7b731f4e3b438445f959c2d77b362e6db8e75ece in / 
# Thu, 09 May 2024 18:48:15 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c51d994efc098621a8777bd1a698f8e622b9ded5d362c17301551077048d589c`  
		Last Modified: Thu, 09 May 2024 22:32:36 GMT  
		Size: 51.3 MB (51320982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e30400cb564151e37db1e92faaca62f870f0e3abde886218f41631819f8006`  
		Last Modified: Fri, 10 May 2024 00:52:11 GMT  
		Size: 15.0 MB (15015777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0829af380691076be6f53155b752eb8b6db46a5e4d27d5d7f85bc3b21c03db5`  
		Last Modified: Fri, 10 May 2024 00:52:14 GMT  
		Size: 209.9 MB (209905328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e090ebd69d403538eddf8acf03bd4c91158894bd99fe53eac9cb643b13c6ec72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f260fff1406a50ef92bb2a595a6937d6e89a3db26c769e55bb5533c66ad954`

```dockerfile
```

-	Layers:
	-	`sha256:11405b7a0325b9acb6e19ef4a4510ff9dd449141057edc183e693c2695337ea9`  
		Last Modified: Fri, 10 May 2024 00:52:10 GMT  
		Size: 2.3 MB (2267589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af541fd99abf918103d8c06bd709ca00b90380b801de9bad03a4bc03a6ac68b`  
		Last Modified: Fri, 10 May 2024 00:52:10 GMT  
		Size: 16.2 KB (16185 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:30fd17122767be03dddfcffca5e52bcba37ae66af320619e9c2c1d96cf987475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273568857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fba819203855c48a7813aa69ee35c3582c910477f7ce31906bde7702c1fdb4c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 18:48:15 GMT
ADD file:603b84a8cdf20851437bb944c9946c0ac32645e0e0946ffebf3ed5ad10c141bc in / 
# Thu, 09 May 2024 18:48:15 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8999f2c02994f155685ddf5b1c0822a620022aa57946ee7ba5c754261052b2dd`  
		Last Modified: Thu, 09 May 2024 22:08:16 GMT  
		Size: 50.1 MB (50082252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2621a0b881622f503ff8b218af9315ee5ba6b65472e45dd71e10ecaefc2a5cfb`  
		Last Modified: Fri, 10 May 2024 00:16:40 GMT  
		Size: 15.7 MB (15699035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86508d29e60d34ea7524df1e72fb9a8a10fcda5ad2295001bb49f44c530af20b`  
		Last Modified: Fri, 10 May 2024 01:14:32 GMT  
		Size: 207.8 MB (207787570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a2275e666be63eb4ad08b61b89425c1a31d1692ae3beb70132eae761daa5d0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00445c740bcc859824f5c7db5e21cb3bc1a6d613f4043eb85cb3d3fa56685897`

```dockerfile
```

-	Layers:
	-	`sha256:636bf741a3e8bc4930e63a5a500ba39899e68653905765b54afbf9085ed6e830`  
		Last Modified: Fri, 10 May 2024 01:14:28 GMT  
		Size: 2.3 MB (2266993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9eb5ffbb399e7767a160e13c9b8ff3863b14feaf734633d02930111da62b11`  
		Last Modified: Fri, 10 May 2024 01:14:27 GMT  
		Size: 16.0 KB (16032 bytes)  
		MIME: application/vnd.in-toto+json
