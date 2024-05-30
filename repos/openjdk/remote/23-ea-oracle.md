## `openjdk:23-ea-oracle`

```console
$ docker pull openjdk@sha256:a2f2a71e827face2abf8be77c81c7f656dbb57a1c951ed4dcd7b20adba7bf6c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:f3056a4503c4db9ebe99fcc07ff1e26c7ec4d5078adca84a07596d09350d3eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297340037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044abf4d87595bf58d551c36afe074870682a97381f73292b8d2dc100a275f4b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 22:30:14 GMT
ADD file:95cf7039855dd392d2faa5bb16415fdb79680afe50aecf7c299b8b2dd377328e in / 
# Thu, 09 May 2024 22:30:14 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 29 May 2024 17:23:46 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 29 May 2024 17:23:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fcbdc4090331ae224779b095ccebf7fa4fd896fb807b7d6bdb37776132e9710f`  
		Last Modified: Thu, 09 May 2024 22:31:50 GMT  
		Size: 49.0 MB (48998671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b376214fec0bdd909b74c38e0b0fe9243555cc0224fbf4a0e17c5162b7724ca`  
		Last Modified: Wed, 29 May 2024 23:01:17 GMT  
		Size: 37.9 MB (37862384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b259f4a84e66ca4287e8f6b49ae3c793b41e801996fe54878fd547385ecea5`  
		Last Modified: Wed, 29 May 2024 23:01:21 GMT  
		Size: 210.5 MB (210478982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a08cd7c15adcd5eb66828283f7b342a18077014905bf3baab44d7c985ad8b48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a044e50a2e58bdd5f8ebdcc030f7499818af3af68fd23e86ca4db3c32d6bca75`

```dockerfile
```

-	Layers:
	-	`sha256:413a1e8710497e56ce830166df83798e141905515a9dbda14de23e42cabc1b0d`  
		Last Modified: Wed, 29 May 2024 23:01:17 GMT  
		Size: 3.3 MB (3333220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:053198caa794b52e9e7465b56ef57f77ee9bdfdabf3d16c1e1255e226509f04a`  
		Last Modified: Wed, 29 May 2024 23:01:17 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-oracle` - linux; arm64 variant v8

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

### `openjdk:23-ea-oracle` - unknown; unknown

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
