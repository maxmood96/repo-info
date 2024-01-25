## `openjdk:22-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:e0fa5e79c34f77f18cc0562dbc972e2edc4bd0369ee2df2033890d73a10f8f78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-jdk-oraclelinux8` - linux; amd64

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

### `openjdk:22-ea-jdk-oraclelinux8` - unknown; unknown

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

### `openjdk:22-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4114998ccba14935a706c925b6267c7d3d12098f0c9d161129ea332ee96c198a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266593385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55f13477f769fdb32de3e1ca4e5460637d44cc07324fccd97f594686cbbf706`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Jan 2024 01:48:33 GMT
ADD file:d9c5a5624a292383f8c072d816e66770afc4dfd0215037516136df1ced9a2994 in / 
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
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
	-	`sha256:39771e196bf8284fc24126bc46b73f5f346eca1159f7c4d7904d0026aa830392`  
		Last Modified: Thu, 18 Jan 2024 10:44:45 GMT  
		Size: 200.8 MB (200816594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b3688b2de8c050aa75dd2006788a6827f9983dd904e7d7613c0dcbd473ab4eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1934193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c84cb9017c384b6ff9f8f4bae45fa7aab04799f52f14c85ec5d6bc0ae7bd337`

```dockerfile
```

-	Layers:
	-	`sha256:731e295fd3ba8d47f33d3c974e92651ab3a862b7ac1445c4e3200ab61c384d98`  
		Last Modified: Thu, 18 Jan 2024 10:44:39 GMT  
		Size: 1.9 MB (1914433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b471e6f0d35d87035bf67ebdc349df0dba11beb0a8ca13ce312dc55a1e065e9b`  
		Last Modified: Thu, 18 Jan 2024 10:44:39 GMT  
		Size: 19.8 KB (19760 bytes)  
		MIME: application/vnd.in-toto+json
