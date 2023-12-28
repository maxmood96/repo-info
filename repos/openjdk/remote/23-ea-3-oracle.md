## `openjdk:23-ea-3-oracle`

```console
$ docker pull openjdk@sha256:5e333186211696ade7feb657ee4495f2f1447614fd1e5653ad3f8eab4a0ebf21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-3-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:cca168fdde450d731363a548152312737de5a6e1a97453daac3bcc18484640f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269309792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0557637904027f63fd0f73dae6385fcfcdf55721d9a6cc5b03ec8cdf4f6689ae`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:40:50 GMT
ADD file:da89b67e484bc45f357250a868fd78e28086b13e4315635d19648e5d43812e89 in / 
# Wed, 20 Dec 2023 22:40:51 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bce031bc522d421fb188ef82a530f85c5477bb87cdeacdb911ea86f3f7cd3b66`  
		Last Modified: Wed, 20 Dec 2023 22:42:00 GMT  
		Size: 51.3 MB (51323468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe40f6add29e64183cc60f9695aa07b6aebdf0de0c779e8411b4470c920df739`  
		Last Modified: Wed, 27 Dec 2023 21:53:51 GMT  
		Size: 15.0 MB (14995391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efbdb523f54bbc2525b2b41c360f7513b64a94897c18e31e993e4010855909`  
		Last Modified: Wed, 27 Dec 2023 21:53:57 GMT  
		Size: 203.0 MB (202990933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-3-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d068d9dfe544c9476ef7e2d948205a4d21f7441ada270b34134b7d8a738db93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10301d247eee26ea58d816392543c66b814dca4e8d715f6e862e848539db24f0`

```dockerfile
```

-	Layers:
	-	`sha256:da6a4a3e7be2181e7a6ce11eace8b973591ba1468332c4dc3581671646096fe6`  
		Last Modified: Wed, 27 Dec 2023 21:53:50 GMT  
		Size: 1.9 MB (1915835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66087d97dd49a971e876f2cb773328155b357c6b9c25cdfc842f3c9091c0e51`  
		Last Modified: Wed, 27 Dec 2023 21:53:50 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-3-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5695357d1f858fcaa96c904e0831442e85b16f6fa5f216f23ebb2237cdc52d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266662359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54802f9da5a1aab5eab9d4226b8ca73577b1f9140785f9f0896593b98bc10798`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Dec 2023 22:53:14 GMT
ADD file:b736c1bb75174fcadec81f68a30d2db09432c3999d3df92c07c057a5cc8b07a6 in / 
# Wed, 20 Dec 2023 22:53:15 GMT
CMD ["/bin/bash"]
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
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
	-	`sha256:f783d34dbc02e7f32e56fa0529c4cdfbf48273a6d2f63207f695a50391edbcb1`  
		Last Modified: Thu, 28 Dec 2023 04:48:28 GMT  
		Size: 200.9 MB (200892604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-3-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b119706d1758d523139ca5eb0cd0f9254ff825bb013fc949c59ca2d949598e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cbea01ac438861443ef7bf1e3be1b2fb755d752d05fab400d3a04f18a5855d`

```dockerfile
```

-	Layers:
	-	`sha256:2721003dd35cf42aab9e779bd7bc0cf3acd6733455f715afa0a338a4ee4c5fc2`  
		Last Modified: Thu, 28 Dec 2023 04:48:24 GMT  
		Size: 1.9 MB (1914413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:296a51e461d22f5fe1127bdb0a018493a6b27e743f58b9d5cfb4c7f2f73d51b5`  
		Last Modified: Thu, 28 Dec 2023 04:48:23 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.in-toto+json
