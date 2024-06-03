## `openjdk:23-jdk-oracle`

```console
$ docker pull openjdk@sha256:5f9da412b0ecf8d04e13fda83530b9c10d4cc1f4f71a72a1cdfe081cc1ac660a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:2330032dbaa5e5a26a27f35cbc873648b5a6b0066a10bbc6aa505a1c8e802a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298032452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5636b90f15d09b8f6750c6c57d046e69258b7d363a74f68c5d1e4d5c4cc00885`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2024 00:48:11 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Fri, 31 May 2024 00:48:11 GMT
CMD ["/bin/bash"]
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 31 May 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+25
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='155a1386301d0ac6cd1ce5769b31f550bb400d652f4211454b9988bf25fa173d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b00cd1591ad9727c48c07e598f57cdec15fa40b605ae712b67f35f221534d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b697b9633f3095e03b7c2f6c799942a12e6f626d3aa8936bb6032548b8e4a8`  
		Last Modified: Mon, 03 Jun 2024 19:01:02 GMT  
		Size: 37.9 MB (37862598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c3a27ca778663f8f208cf61903b61549b0cadb9c3ecff9539b90c2b1f44051`  
		Last Modified: Mon, 03 Jun 2024 19:01:06 GMT  
		Size: 211.2 MB (211174976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:394c92d1310966915783986e9892192c8f725d2781f3be9d35b3256b9327e79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913ca7f56c39f3dcb50caaf2c29b1f5c7e4fc2f2878f416e5278b11e9595a3a0`

```dockerfile
```

-	Layers:
	-	`sha256:84680f3a7c56fbbaf779233ea28e2a72fa2a141a9d0dd155d335588ab240b918`  
		Last Modified: Mon, 03 Jun 2024 19:01:02 GMT  
		Size: 3.3 MB (3333243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d8568ddd5b12e69880045074e8904730938130ccf0b3819a0a80a8bb8a99ed`  
		Last Modified: Mon, 03 Jun 2024 19:01:02 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e57a495caccb43ebd70a29eb2307f97d21ea63fe487d1494d26da15a5e3a984d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294284429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7d128081d08e8f7ab34042326eea4d9d514451087aac6506ea38adc3a3f982`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 May 2024 17:23:46 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Wed, 29 May 2024 17:23:46 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 29 May 2024 17:23:46 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 29 May 2024 17:23:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4126ceeefbe5a1d06272578a6b6a99a1d422489b25511cbccbaaeb1576551bfd`  
		Last Modified: Sun, 02 Jun 2024 01:54:26 GMT  
		Size: 38.3 MB (38259157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42008cab5fa16551b15c7aa00cc3ed7d8326f13b1bc90362379327d2277cc`  
		Last Modified: Sun, 02 Jun 2024 01:54:29 GMT  
		Size: 208.4 MB (208373281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9a14853f66ff60207673b25d04dba6e57650e51a1237ef1c5c5d2a590610d774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95874cbfce7f3eb9e9d739fcbc9e8c162225365c8a78dd0440770ee1bb004926`

```dockerfile
```

-	Layers:
	-	`sha256:fee9bbd78aadf19ccb845531afdb73b993b3bf6396378a88d196c5dea9ec59b5`  
		Last Modified: Sun, 02 Jun 2024 01:54:25 GMT  
		Size: 3.3 MB (3331626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d20ba55a69725b86a122749e51f1dbd2d16670356bca63157fbebae7a3969c`  
		Last Modified: Sun, 02 Jun 2024 01:54:25 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.in-toto+json
