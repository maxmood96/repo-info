## `openjdk:22-rc-oracle`

```console
$ docker pull openjdk@sha256:08b2d714025cbba08c787f5395d931bae89345a856e4ab1be20891b8926eed82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-rc-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:aa232ec30b86617a044994b3898a1a61d7ee739cb6aae7944084c37b0aa1255b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289480248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a271298cf196c7aaa694279395e0c7e10640b40f3071042ffd3a0740c1598f1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:04 GMT
ADD file:9bcef05fa351e2fb72a4b6052a0252eeaa2cff794ed089a482670c67961d2e90 in / 
# Fri, 08 Mar 2024 19:21:04 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 15 Mar 2024 16:08:04 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 16:08:04 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_VERSION=22
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:972029ff9873af36c6c0fcee05b14acbc57a61ecd0b8bf86b167bdf46f973823`  
		Last Modified: Fri, 08 Mar 2024 19:22:31 GMT  
		Size: 49.0 MB (48978454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04e36430406bb6588fe835b6268588b825205320c94fbd96651f340a618da24`  
		Last Modified: Fri, 15 Mar 2024 23:56:11 GMT  
		Size: 37.7 MB (37733618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c9b018c642931f767eff0ee01c56b4805e644ebaff9ba39c4e2ce5d1f174e7`  
		Last Modified: Fri, 15 Mar 2024 23:56:14 GMT  
		Size: 202.8 MB (202768176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:03a821ae7863e1d4fb951c920442a09281960eb7468d43006cfddca019d960ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989f6e5925fb1a36b7a63fc4a063afc841dbdfdf6f52934016dcb3de3a576817`

```dockerfile
```

-	Layers:
	-	`sha256:df3900d63d29682f3a3d17ecaa8de3563b7259cd06a78831d3594cdecff5a87b`  
		Last Modified: Fri, 15 Mar 2024 23:56:11 GMT  
		Size: 3.3 MB (3327582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebbd60a7e7ac1c2b8e00c836cf3306c543d50f09287d94e2aafcad26cb24179`  
		Last Modified: Fri, 15 Mar 2024 23:56:11 GMT  
		Size: 18.0 KB (18025 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2e2dda869133a39b87202ab5d21b086aba6fa0ea6a01839d97c438d6263d29ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286630478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41bd84932036f8ea3704bc08d578f9262c820a99eeedaaa60e7ef8504d6d3ff3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:48:53 GMT
ADD file:71724b501850c3e6cd72efc58b3430394f691a428c2c62755eac0b93c5579f35 in / 
# Fri, 08 Mar 2024 19:48:53 GMT
CMD ["/bin/bash"]
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 15 Mar 2024 16:08:04 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 16:08:04 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 16:08:04 GMT
ENV JAVA_VERSION=22
# Fri, 15 Mar 2024 16:08:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 16:08:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c53b3bc8702e4b172b3fdde99731082a493b5f5fdd7e9632b3cf7dea02a52b4`  
		Last Modified: Fri, 08 Mar 2024 19:49:57 GMT  
		Size: 47.7 MB (47664888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71597242e3bc84850918d978b72bcf84c5867bfb6441051c67b805dca13e66a`  
		Last Modified: Sat, 16 Mar 2024 15:50:44 GMT  
		Size: 38.1 MB (38140694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617d9a96a67e81b1d822d05c7707fb11c827e74407b9293740179cda158a5d0`  
		Last Modified: Sat, 16 Mar 2024 15:57:04 GMT  
		Size: 200.8 MB (200824896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:138d24261602a5b922c097e7d7ee61ee3102a95b9fa10dfe736cd4ded881a14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf458e6d040f8f746b01228e02b1fecab4021beefee293b3a733530fe2d0b054`

```dockerfile
```

-	Layers:
	-	`sha256:19564e4f82d25d9f92b41f4cd1e59b69dedf3ed6d0925fbd1b5e503f53fe647c`  
		Last Modified: Sat, 16 Mar 2024 15:57:00 GMT  
		Size: 3.3 MB (3325768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6befa1820f7b80e492eec319c68685b359a2dd1eaf4bdd0ced4b2af4fb4ffae9`  
		Last Modified: Sat, 16 Mar 2024 15:57:00 GMT  
		Size: 17.9 KB (17884 bytes)  
		MIME: application/vnd.in-toto+json
