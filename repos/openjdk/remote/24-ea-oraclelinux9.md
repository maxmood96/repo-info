## `openjdk:24-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:3e21db8d6340d5c5594ebcd1f9f5854cfa53d88622f86563c4f701724a6c0676
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:a1409f227791beb4e58e555d1ed451e8649ace311d4687edb818ced5f437b1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300534186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3ead23434994633ad7e52277b89cc539ea0ba29c4bc57ce788c09bf90c25b0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
CMD ["/bin/bash"]
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27a9dc5a649ca6a8adacef3d2d1f7c7b58fa18e5776d449d8f3e8d44f8c9413`  
		Last Modified: Tue, 08 Oct 2024 00:01:45 GMT  
		Size: 39.1 MB (39059662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5373b51af8e3e1fc9d9df44669e042e0e7efdcacc24e2462e4e4503ff43e9f`  
		Last Modified: Tue, 08 Oct 2024 00:01:48 GMT  
		Size: 212.2 MB (212227582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:283f22b6de310cd929678ff685693aebe371db5827a52424a298458e5c3a5e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33f1c136cf463a9f0d0eb168e1bea005a7c7507404b1f60ff1a2b5f815779ad`

```dockerfile
```

-	Layers:
	-	`sha256:943bd6a82c0dec7db3a3b79111c7e0343c6af93fa81b1b1606e7f3d71e58b4e4`  
		Last Modified: Tue, 08 Oct 2024 00:01:44 GMT  
		Size: 3.8 MB (3782218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9a95fa10bf716d082ead466e65166c5170e7051ec1e6d6f51baa0ab61e9ce3`  
		Last Modified: Tue, 08 Oct 2024 00:01:43 GMT  
		Size: 19.7 KB (19717 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2050c1f04eb7ef012320847faf81125b561a89fcabfc68f3091f7c66dad7ecee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297361283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea37e70324e7390e9fb9cd2160cc05d37f62430608159d3870500e453c2e546`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
CMD ["/bin/bash"]
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 27 Sep 2024 06:48:27 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 06:48:27 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_VERSION=24-ea+17
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='983faf25eff38b5b396afabd191a91b239a1d803a0dadd01863861ecf731f034'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9eb980b4f1fde9c2387e0fab6b91b6f68cb109e3ddd43eda0013d9ee345f2dc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8012429b70e0979dd49dcb64d258b15c848e133db0919f7c15e7acb1c1da0ad`  
		Last Modified: Fri, 20 Sep 2024 18:54:09 GMT  
		Size: 39.5 MB (39489281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf298d771d6bfa137fc7aa565b5dd112615129e6ab81b43563105d999797d2c0`  
		Last Modified: Sat, 28 Sep 2024 03:02:09 GMT  
		Size: 210.0 MB (209957419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:48acb9bc14138897f45a7b69d94beb9e19cfef95a40a3c5392f010337e1294f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24a3d87cb00e026724e98540f655fbb16b69d14cb30331ae9e63a69d4a98806`

```dockerfile
```

-	Layers:
	-	`sha256:0aae6a5b574bea68827f2deb1f05258b32661314f83a1dd7725960d1326e2ce7`  
		Last Modified: Sat, 28 Sep 2024 03:02:05 GMT  
		Size: 3.8 MB (3779354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b852cf7888d82cadd9162606f04521a603aa3ba7f61c1e491b4d21a20c501e2`  
		Last Modified: Sat, 28 Sep 2024 03:02:04 GMT  
		Size: 20.3 KB (20265 bytes)  
		MIME: application/vnd.in-toto+json
