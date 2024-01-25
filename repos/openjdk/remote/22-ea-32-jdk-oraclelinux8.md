## `openjdk:22-ea-32-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:6f66c0d50df4fd2c5bd83faac8b294b64311a6517e68a999ed862935b8c378a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:22-ea-32-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:31afa4a4438d970ee3c9d68cf82535a5a7c474bcd5706c0a1811a5ccfdec77ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269080138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d691a10226d37819f4e9f3ee2f504eddbb6d40ca0f058312343316586b796c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:34:45 GMT
ADD file:a1f24204c7f65fe2362a45e81d2d867cc73405d4bf548fd36ff720ee36fe25ef in / 
# Wed, 17 Jan 2024 21:34:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 23 Jan 2024 19:48:26 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 19:48:26 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_VERSION=22-ea+32
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='7ac0b8815f22c852796fa13b7680e07fa1dc340aa93f5e2bf1c5502337d952d6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='7c565754b2926817c1779683d6b8f1975a94a8731fad35a670ea669a77aea182'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:558b7d69a2e576e93c7cb18ecd087a92959e912b116323c188183d5cf8ab5b17`  
		Last Modified: Wed, 17 Jan 2024 21:36:52 GMT  
		Size: 51.3 MB (51321731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e67dfd05b0269f7296b15d6c3eae2c96f50d3f45e2df00d2fe7338ca7d320b`  
		Last Modified: Wed, 24 Jan 2024 20:50:28 GMT  
		Size: 15.0 MB (14990931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785d85712376f9db22b3fab3b324efe06d639c97c2f013e23a61a17a532b819d`  
		Last Modified: Wed, 24 Jan 2024 20:50:30 GMT  
		Size: 202.8 MB (202767476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-32-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f07b58887cf63ba6230334d5156d2ac2c5d42bf5bea2d873203e303d1cc0897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a4a96efcf5b42f40dddd167ee3a04b0a49491b787f439a8d3c93d474760fe5`

```dockerfile
```

-	Layers:
	-	`sha256:507ccdaa6cc660ef176c5b8aaff2587619bd1fa2ae7809b8e580b42f4e54300d`  
		Last Modified: Wed, 24 Jan 2024 20:50:27 GMT  
		Size: 1.9 MB (1915859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935ad95554d1d6ace76c57e04f451f9a93e672f981d93e45a4a98cded9975302`  
		Last Modified: Wed, 24 Jan 2024 20:50:28 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json
