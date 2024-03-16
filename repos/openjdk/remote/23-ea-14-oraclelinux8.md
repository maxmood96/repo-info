## `openjdk:23-ea-14-oraclelinux8`

```console
$ docker pull openjdk@sha256:bf7437c4bbcf57aea5e62b6fdac54ffb58f6af35b7bd38df4e94daa779667e86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-14-oraclelinux8` - linux; amd64

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

### `openjdk:23-ea-14-oraclelinux8` - unknown; unknown

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
