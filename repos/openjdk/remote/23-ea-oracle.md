## `openjdk:23-ea-oracle`

```console
$ docker pull openjdk@sha256:2dc248e62f1c00cd2acdb7f0c22bad5aeabc51fb0665eca8069d067b77ec2ba1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-oracle` - linux; amd64

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

### `openjdk:23-ea-oracle` - unknown; unknown

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

### `openjdk:23-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e982f89aa2ce2f68408865ec0cffa920acbbac1ba0c8f529ea7c2cdc13c1c096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266749154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc3b4d50a7be41f96b58b72309febea890d0fca8436be8097e5c9b25c0ffc84`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Jan 2024 02:00:35 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
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
	-	`sha256:6988ac25ab22b91e9e2b9b71df8fcdc44661212c4214d47ad649398b4192a99e`  
		Last Modified: Wed, 17 Jan 2024 22:09:30 GMT  
		Size: 50.1 MB (50074578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbecf34c8e1a9b9949041e4c9e805d7ee8c1f00ad6362349a4579d6db495c27`  
		Last Modified: Thu, 18 Jan 2024 10:42:33 GMT  
		Size: 15.7 MB (15702213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65ec951c35e9340866a21125356fa3a12362ac633aff52fc99c48b6a28bc32`  
		Last Modified: Thu, 18 Jan 2024 10:42:37 GMT  
		Size: 201.0 MB (200972363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:352a695cd4d4e8ae9a1bd09bb9178aaa8c307c048b4527d77ac21861bbfe0a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b16085136149afb6a9c39d7f7612381cf674f025fc85f4b00107b3a5d83d1b7`

```dockerfile
```

-	Layers:
	-	`sha256:67464768abdfe56eeebec04fbdfe7e419533ceacdb2efbdff723eb04090232b0`  
		Last Modified: Thu, 18 Jan 2024 10:42:32 GMT  
		Size: 1.9 MB (1914421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9bfae62b69da9fb25bc1ff6751491e21d8726f759075b2dd47810a797256029`  
		Last Modified: Thu, 18 Jan 2024 10:42:32 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.in-toto+json
