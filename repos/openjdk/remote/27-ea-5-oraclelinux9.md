## `openjdk:27-ea-5-oraclelinux9`

```console
$ docker pull openjdk@sha256:5f25ad217dda264085d49a65dd56e7563b385736a8433413a5bef1b83e91b63b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-5-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:044e00e7d725c97bf09d62ac0be5c5715383bd92e521feadece148a1a19bd964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313677188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2879c4a8eabe2359074e4a0478fe01f8b476105fc51f084c687013e0a000782e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:46:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:46:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 20 Jan 2026 18:46:46 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:46:46 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:46:46 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:46:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:46:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5c65ef8298a36f2091528dbc70ce16fb2b685fe9e234aa80bca9294ddb27f1`  
		Last Modified: Tue, 20 Jan 2026 18:47:28 GMT  
		Size: 38.3 MB (38296097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cb17f06827a1bc4df9d04cbc37bef169d7852266770da1be1a3dcdcd75c818`  
		Last Modified: Tue, 20 Jan 2026 18:47:13 GMT  
		Size: 228.1 MB (228066553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:bba8ae143115ea33ee3e0aa829a696ed4c083c04f4a8f45760aa98d02308d059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6340f8a01a0d70bf344d12e1d82a809915665d818a9b7c9f72270c06aa3b077d`

```dockerfile
```

-	Layers:
	-	`sha256:03fccd02d5aeb1dfcb45673e60e8e17350aa807c422318e6504f9d92dcbc1a00`  
		Last Modified: Tue, 20 Jan 2026 18:47:08 GMT  
		Size: 3.7 MB (3655355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3eb66a3e293b7bdd85bd5ad8ca2b5c2448cae9c4cc4507f9d48d9dbaf84726`  
		Last Modified: Tue, 20 Jan 2026 19:25:47 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f78f244bfca1718a51e097ad984f9d6211f8d9755b16b6554cc5ceb82f1396ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310599400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a53943beec9fd811937b6451011dc432a3f09d3b109084bfe3320a714d8b9ae`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:47:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:47:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 20 Jan 2026 18:47:41 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:41 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:41 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:47:41 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54694fd53c4e9bf4539655dc2b3285316d7e10f220d35530e8e15fe69525013`  
		Last Modified: Tue, 20 Jan 2026 19:21:40 GMT  
		Size: 38.7 MB (38697975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48790a6f53d4070c040a390a332e97a6ea469bf5389ebbc4bf206a2b7d9a3f8`  
		Last Modified: Tue, 20 Jan 2026 18:48:07 GMT  
		Size: 226.0 MB (225999522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:4522cd89bc67e9d4068dc40b993a7771c290d532ed0a145e1ba87989ebdc7719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c546145b606ee5dda7f8dae53d36f6c909a4019d3bd508eedb5ee97420a092`

```dockerfile
```

-	Layers:
	-	`sha256:ee3396d12ff707554c774b0ec169a48486bcd8124484e167dc1aa4ce7372b471`  
		Last Modified: Tue, 20 Jan 2026 18:48:03 GMT  
		Size: 3.7 MB (3653045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:812a642d61120ce61f5148dc751a78fa0c2bbcddb5ee9ba17e3105b2f0920b2d`  
		Last Modified: Tue, 20 Jan 2026 18:48:03 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
