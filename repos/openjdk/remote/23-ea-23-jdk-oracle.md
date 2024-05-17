## `openjdk:23-ea-23-jdk-oracle`

```console
$ docker pull openjdk@sha256:03749b6bb7c36ef2f5f019010611293123ca3e58212700e59878af0221bf03b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-23-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:f2114784adfce1b9be86ae80441920c96f59b23702407b398f02b92a1b19fd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296603142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b670d2fd595b413c4e96159e1990f1d43d8907543a31e10f7874d46617850c71`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 22:30:14 GMT
ADD file:95cf7039855dd392d2faa5bb16415fdb79680afe50aecf7c299b8b2dd377328e in / 
# Thu, 09 May 2024 22:30:14 GMT
CMD ["/bin/bash"]
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 17 May 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+23
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='ebb29aa3b7c39ccf29ce564c797c5723b7355880f5dafd239570f7e7f2166bfe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='feef29529ab1660b95345ebbc6f47ba2823e28e87596225a25d2c45fc4537f29'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 17 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fcbdc4090331ae224779b095ccebf7fa4fd896fb807b7d6bdb37776132e9710f`  
		Last Modified: Thu, 09 May 2024 22:31:50 GMT  
		Size: 49.0 MB (48998671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c834a861e15b749f5f5037338423ca8b5e8e4f5afdd7769d1440f3c1a36345`  
		Last Modified: Fri, 17 May 2024 18:53:36 GMT  
		Size: 37.9 MB (37862398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c50a685e639a97defbe5b26e2babe159f607fcc6c2da8db55a37a6a58e6ed`  
		Last Modified: Fri, 17 May 2024 18:53:40 GMT  
		Size: 209.7 MB (209742073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:4d4b1e853b31e95a920bc1cafcbb45bb076eb3affac99ffeca9c2a3f432b6c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9483f748cfb26c5b47e5c4ca85fcc89a96dbb362d1af16021688e5e270589596`

```dockerfile
```

-	Layers:
	-	`sha256:6f06e01a22578b1b07e9a37a0f4dcea96fc83e3f1fcc1f5574f9fbe5104786a9`  
		Last Modified: Fri, 17 May 2024 18:53:36 GMT  
		Size: 3.3 MB (3333220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3739549d4ab376bd671b909408a8fe45bf8e9e655e634d4d5fe50e2d6b744e3`  
		Last Modified: Fri, 17 May 2024 18:53:36 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-23-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ada6f917274638b91400263086af22386d475c37574578a4388f00451ab9dd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293541354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125fd08aa229f9089945bb81d9e7f1686eecd9e7457f57c9329edf63f1570f74`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 22:06:19 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Thu, 09 May 2024 22:06:19 GMT
CMD ["/bin/bash"]
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 17 May 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+23
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='ebb29aa3b7c39ccf29ce564c797c5723b7355880f5dafd239570f7e7f2166bfe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='feef29529ab1660b95345ebbc6f47ba2823e28e87596225a25d2c45fc4537f29'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 17 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a4be78b09aad15f916c85a97d9c9410e09e7e9b619c370b687ef5f9e20a44d`  
		Last Modified: Thu, 09 May 2024 23:52:47 GMT  
		Size: 38.3 MB (38259792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed50f10a89932f7399847611b4cb5cce1a6cbafefb90bcbeb60f83cb0464013`  
		Last Modified: Fri, 17 May 2024 19:45:06 GMT  
		Size: 207.6 MB (207627762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d97ea138d6d4b151c1cdb9d9296ccbef8c3cefb13cb14fe705a288ad8a88b061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd012b639a4d2e916c0308e0428d067e966b156b6a2b1114b05447e135d590`

```dockerfile
```

-	Layers:
	-	`sha256:8a5873b472a7549286a1956afab8f04da9bb3d9eb358b830d0e9d4c8f99bc441`  
		Last Modified: Fri, 17 May 2024 19:44:59 GMT  
		Size: 3.3 MB (3331418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fbe32bf784d3c33ec4ff9b7ba150c617d207fbc3898c433cccde0fd423e9afe`  
		Last Modified: Fri, 17 May 2024 19:44:58 GMT  
		Size: 19.8 KB (19764 bytes)  
		MIME: application/vnd.in-toto+json
