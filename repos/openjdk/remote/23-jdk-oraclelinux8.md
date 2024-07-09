## `openjdk:23-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:ea1b89ce6641ae8ee1a8fe26228696b27b7dc6adf187eb161a204ff9cee40197
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:101cac80df746e9b3690567e461879cb842a92811195a60008b9a5eb33d6e575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278033745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a3acf07de4c5ce34707e81613bb584104293c1753bd6804450216fe3e9c803`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 23:20:38 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Wed, 03 Jul 2024 23:20:38 GMT
CMD ["/bin/bash"]
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac91321cf4624d6172970363727db1c00999ed86f03cfe53153d03102461b404`  
		Last Modified: Mon, 08 Jul 2024 20:57:12 GMT  
		Size: 15.0 MB (15036287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b175fb214a44f8ccee19ef0629ff64a956a816de2fb8298dcc0cb0e94666cf4`  
		Last Modified: Mon, 08 Jul 2024 20:57:14 GMT  
		Size: 211.8 MB (211777834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:28315c96cd22f5b5f95bc69cab74ccc047b2037d4ef8e30ca6966adf33f32988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9abaf3a266d7a4f3952329d4e79ba74434248d2c7af2c3b3b1ad58a319888b`

```dockerfile
```

-	Layers:
	-	`sha256:b1bb1a117d77bf01cd7d01d3dae56c9e237fdd5312e1aa53782d1cfab82fafae`  
		Last Modified: Mon, 08 Jul 2024 20:57:11 GMT  
		Size: 2.3 MB (2267577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda5be5fb8cd159ad6c001fb4477f1bb64a742c1a896aa390ba638eb64307cae`  
		Last Modified: Mon, 08 Jul 2024 20:57:11 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5390d92561ec1cd90180cac00a35d8b7e602323d4d1a18d6088bf54be0e24f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275251147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7174b31002dfc4086620a79b3f387571b0ece342bfe1270ffabe48c358162587`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 22:40:38 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Wed, 03 Jul 2024 22:40:39 GMT
CMD ["/bin/bash"]
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6708363575e82894d4714b00358e6cfc904f5e8213ff218080d18d8c0a3aea8`  
		Last Modified: Wed, 03 Jul 2024 22:41:29 GMT  
		Size: 49.9 MB (49925030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53325ebdf5962703e657719964570a5baf1824ea843ea45441c78f115b80fb18`  
		Last Modified: Wed, 03 Jul 2024 23:56:52 GMT  
		Size: 15.7 MB (15686023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedf769dd7fba0e16aac0036ae8222e3c1691f7c1a9b958075eeb1096ddf359c`  
		Last Modified: Mon, 08 Jul 2024 21:03:58 GMT  
		Size: 209.6 MB (209640094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:11b3e65207ae5fd3dc875cfb9160d037ea5644bade873fff53f5c9bbc815ac29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1467c08a281690c6ff82b3fd41f6f7b30f0a66722fdca1d384909685f40972be`

```dockerfile
```

-	Layers:
	-	`sha256:6a10abba1ee1182f44c901c2c7a9bc95b18ef627c47a1a99dd5ddb8b98b850b6`  
		Last Modified: Mon, 08 Jul 2024 21:03:54 GMT  
		Size: 2.3 MB (2267046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41040dff5773efe55dc224bb2615098e4be07987c8d79226a86aa43c5cdbe97c`  
		Last Modified: Mon, 08 Jul 2024 21:03:53 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
