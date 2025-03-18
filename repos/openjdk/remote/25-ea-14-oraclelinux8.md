## `openjdk:25-ea-14-oraclelinux8`

```console
$ docker pull openjdk@sha256:34325022f5a761c536f4f4c73ab70e66f36171e078363a31febc2672ad0031a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-14-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:e947481f2fe63333e29b1a3d5794e2136b114249abe4df113d44808892a665c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278526068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f462748609cd50d9947ed6625a4fc5a3c3a8545a83c0bc4afa675eed0978e1e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Mar 2025 17:20:06 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 14 Mar 2025 17:20:06 GMT
CMD ["/bin/bash"]
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:035e56311411a7644fa1341dfc093e1b278feac7d55c98ae09177e1755672600`  
		Last Modified: Fri, 14 Mar 2025 19:00:09 GMT  
		Size: 51.3 MB (51288940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d680462518fa2f9e9da664950380dbb25069808cedf8f35c4b2bf9aaeff93bbe`  
		Last Modified: Mon, 17 Mar 2025 21:11:13 GMT  
		Size: 15.0 MB (14996319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c1c1041b57a36860d3b962cbf70f7b7ba0d059b8935a74c15e2257cc90ed77`  
		Last Modified: Mon, 17 Mar 2025 21:11:20 GMT  
		Size: 212.2 MB (212240809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-14-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6134031a85b000f82181e82bed6df26f1e9eff1eaa7cb8c7033c73c658e8fda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7c16444f4af25f095ae4df1714899215dde74da5b8d047f3dbc6a39bdb8b24`

```dockerfile
```

-	Layers:
	-	`sha256:e8f7bb9ff14bdda30fa99331e3fefe07dfd278c4df9dbaf190242a529a474cec`  
		Last Modified: Mon, 17 Mar 2025 21:11:13 GMT  
		Size: 2.4 MB (2440967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc0030ab6eef48104feb39819f43c89ad5f5bdb1749a04bb2b07446e925f061`  
		Last Modified: Mon, 17 Mar 2025 21:11:12 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-14-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:08059c615fe752c7b8270d7503beb1aad948bf6271b5b07354361a8227aa2e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275859803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65d98a00503c11d80b71cc434798de43fed71ba0f1890495d010a3664870151`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Mar 2025 17:20:57 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 14 Mar 2025 17:20:57 GMT
CMD ["/bin/bash"]
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f8eb825c1fc22ded5eda8a11c91fd13cd2b63722a0fdbe5ed89339ba10aabad`  
		Last Modified: Fri, 14 Mar 2025 21:52:22 GMT  
		Size: 50.0 MB (49989226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4c823150405b1ef7ccbc1dc0f1e827fe6ed012030d38106e8e85863c6e52ef`  
		Last Modified: Fri, 14 Mar 2025 23:48:44 GMT  
		Size: 15.7 MB (15683327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5772f4c40bf66ccc6d77ba325da4c3844e07a5f9fd0f83c056a0de9ef40c20de`  
		Last Modified: Mon, 17 Mar 2025 21:25:13 GMT  
		Size: 210.2 MB (210187250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-14-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:720fd390f3761929d79a1af8d6887e7b714fa79be97ab85af94d8ef0d10bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c48fa2a55bfce27133ea5cb6d16b762a8de80834c2446f15a8c00f1fa5f66a`

```dockerfile
```

-	Layers:
	-	`sha256:b2c2ece4bf76108531f85c2b18ea40eee6f7261519b7de07ea357dc5ff480f9f`  
		Last Modified: Mon, 17 Mar 2025 21:25:08 GMT  
		Size: 2.4 MB (2439813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffa2250a3ff538959f97e80c3d92a207a537b999a16bb8d5672b09d1494dc09`  
		Last Modified: Mon, 17 Mar 2025 21:25:08 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
