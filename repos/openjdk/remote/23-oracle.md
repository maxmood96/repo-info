## `openjdk:23-oracle`

```console
$ docker pull openjdk@sha256:5dadc581e5faf5fbcb06d87e494fb66886473295589d623d7ac7ad03da8d9c15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:7c6ac7bf6339392246f132027dc98b9e14d84cd3f96a2deeae08effbe1a98268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269375814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcc213c5e90a33df554f84628610d950f95319077c035677009d50ef510d16a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Jan 2024 02:00:35 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c298c487a5cc881366a213083ae3042c7d820ad2b183ed903e6b9f5804c66c2`  
		Last Modified: Wed, 17 Jan 2024 22:44:11 GMT  
		Size: 15.0 MB (14991002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd3c1dcd487a588b5218faf8cdfc313261b938db1564c7ad4a19d7e39dbb56c`  
		Last Modified: Wed, 17 Jan 2024 22:44:13 GMT  
		Size: 203.1 MB (203063081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c63eb8382c76338f1b9aadaa4d3606e501cfce21aabbf4a6c66cee26a69ba3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cafe0532bf8f692c9c559835c1c887bc5dbc118f3de88f61dec2c7f1510e993`

```dockerfile
```

-	Layers:
	-	`sha256:76cf4ba10676b5458927ed34199897efce58bed7d843df450160952ccb4c4920`  
		Last Modified: Wed, 17 Jan 2024 22:44:10 GMT  
		Size: 1.9 MB (1915843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f4c1f37958c274b6ccfe31e5bff75a135847ec894a95b82f646d2224bad8502`  
		Last Modified: Wed, 17 Jan 2024 22:44:10 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:db5b5ca2f5308b713ffd3ac0428efa36d50e58ecdba954785147e1dbcba810c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266742221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93569645852b3b5ae0881b2f8ba6fdda00be73f6ae155e00dbb2a14de87e25ab`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:53:14 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
# Wed, 20 Dec 2023 22:53:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f065eb68ef2e8ae9b60daa693d770aedc4bf77fb5bacc4b006960acc8eb01f28`  
		Last Modified: Wed, 20 Dec 2023 22:54:12 GMT  
		Size: 50.1 MB (50079714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f352f0f1de3c800e109fad5b2dae0cb9097249a14ca89d420642f858cc188`  
		Last Modified: Thu, 21 Dec 2023 07:07:40 GMT  
		Size: 15.7 MB (15690041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5880b75eb2d16c7561ea32d09d871fec6e424cb5eef6e5d53fc898500563d6`  
		Last Modified: Sat, 13 Jan 2024 01:37:52 GMT  
		Size: 201.0 MB (200972466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:fa1f813dc56f08e9a6b902e97d550447dc5b534225e2d6ad0e6cf721c05a0f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616966d7386613001fffc3cd883e2ed13ca6fcc664cbecac5ab6eec112875de2`

```dockerfile
```

-	Layers:
	-	`sha256:1bd101af3d3af0584da707954529155c04d2e544f24193ee61efe10108ee37f4`  
		Last Modified: Sat, 13 Jan 2024 01:37:48 GMT  
		Size: 1.9 MB (1914413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa74fe4d2ee534e488eac7b11fd01496034312a5618c2a98ad999154f7a44573`  
		Last Modified: Sat, 13 Jan 2024 01:37:48 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.in-toto+json
