## `openjdk:25-ea-10-oraclelinux9`

```console
$ docker pull openjdk@sha256:f7eb16f605bfe99aa37d9c8e0a76d74802da999a1a550e0ecf572773226d30a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-10-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:74f648c28ce36fb952ef3a936c9ed7dfc86ba4753904e9b6e803eafa86b55ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309712532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f482a65db2b4a43874c3dc1f1b12edac455eccf45f65e43d0c4449e78139014a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 17:38:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 17:38:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606554b6fcdbcef8cf40173c823928d54e16f95896087ca83ec5ebcad5b4663c`  
		Last Modified: Sat, 15 Feb 2025 01:28:59 GMT  
		Size: 48.8 MB (48765811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e7c29008cd9892a2ac7710a8ac072317e4552b267d784387c0bdae5a568a0f`  
		Last Modified: Sat, 15 Feb 2025 01:29:09 GMT  
		Size: 211.9 MB (211855830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-10-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:94602a874fbce21bdf28e1d84fa87154b120fd0e6f6ed3bd9a138138a322b741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cdefe6286a7d9c1a52f7ea6a45a02b1b26cd474387f13971e037811079baa3`

```dockerfile
```

-	Layers:
	-	`sha256:0301b83a151739accb1babd1e1942527a4269e1afa10a7a0660a3ffaab18a029`  
		Last Modified: Sat, 15 Feb 2025 01:23:57 GMT  
		Size: 4.9 MB (4910767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b608568c986af149a48b9b4dff21614f01c7d697a1d444c45fc4a3ee5172084f`  
		Last Modified: Sat, 15 Feb 2025 01:23:58 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-10-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:78a0bd4d69fc9384cb01643cf179aef1941de85924f7138d4284bf3d0d6e45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306648128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35508456100572075b1b9f06b3d9ecf00f7b41f887c2980a26c311d6297dc18b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 17:39:49 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 14 Feb 2025 17:39:49 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:903087d703a78a4fd0935e14d3e7b29819d5f670ff2ee18f1691359f349f34ba`  
		Last Modified: Sat, 15 Feb 2025 07:11:23 GMT  
		Size: 47.7 MB (47669215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca163d5e019bf3d8fffa833ce86f630b0f296399ec45fe5da979a5e604b2e20`  
		Last Modified: Sat, 15 Feb 2025 13:36:07 GMT  
		Size: 49.2 MB (49187884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308e335b711e69fb95f2f620a9d8770e4392ee6e70ec17112f70aeba1e5288bd`  
		Last Modified: Sat, 15 Feb 2025 13:36:07 GMT  
		Size: 209.8 MB (209791029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-10-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:2f072da4d93aa6888c7e1e913f204f3dacc77c9e1b7ecb792c1300317372ce3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d2b3f97ec921b7d6a5794485fed3361cdb383d041193d2a53c5439718343a8`

```dockerfile
```

-	Layers:
	-	`sha256:e676754ed3332494aa9bd6e1b523b5d16551b8fed603c1315a413c222003018b`  
		Last Modified: Sat, 15 Feb 2025 13:24:02 GMT  
		Size: 4.9 MB (4908529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7696914a3a2122c91b9e2eeacfce3223ebeb52ddf8024fc2f28912ad8800255c`  
		Last Modified: Sat, 15 Feb 2025 13:24:02 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
