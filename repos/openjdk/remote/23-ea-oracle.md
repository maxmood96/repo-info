## `openjdk:23-ea-oracle`

```console
$ docker pull openjdk@sha256:e5b3050d3e315c219fd48c87eb4cdb958ff5951620491480e7173b2f816d1596
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:c329ab040a61f849a3f44e8b341aa7d8354afa8060dd8303d8278b21bf0eb979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269381701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c61ebf42fa07e7bb1201a96378d20af83bf3c103bd44b0f656f3e41a69991a0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:50 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
# Wed, 20 Dec 2023 22:40:51 GMT
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
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659d0677af8842c6956e905440ede8452af877533fd80245378f6060a40fbc5f`  
		Last Modified: Sat, 13 Jan 2024 01:07:30 GMT  
		Size: 15.0 MB (14995174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01053fa9f654022d42232fc8e33d44e8750985dc6fec31202a9cb8893a30ac8`  
		Last Modified: Sat, 13 Jan 2024 01:07:33 GMT  
		Size: 203.1 MB (203063059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f90986d79b2460314da3128d326f0378777def2fdcf9c33f032371162e4ec349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f2cfcad7c08a931bb52e31bec1ad6e6c6885280be23eccfa3f1e90ae7d56f9`

```dockerfile
```

-	Layers:
	-	`sha256:0e05adaa6e353c7db8fa4ab7d14473915f002ee89b8375155b4667e7574713db`  
		Last Modified: Sat, 13 Jan 2024 01:07:30 GMT  
		Size: 1.9 MB (1915835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20bc4132f01305430f7cf8562b3dbc42e06c00ced0556a9a7a902caf41aeacc4`  
		Last Modified: Sat, 13 Jan 2024 01:07:30 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-oracle` - linux; arm64 variant v8

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

### `openjdk:23-ea-oracle` - unknown; unknown

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
