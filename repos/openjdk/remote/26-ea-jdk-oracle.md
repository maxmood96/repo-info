## `openjdk:26-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:2e3dd20a5f942da65cabceaaf3940030bb46861a9f853a09ec22b5243c746fb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:fc8c4b3885c26019892dee4f911d5bf987513ff28a83c5338f80d71aa2927c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313452269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36dabeb5f2e920192c2a513931db5eed70ee7b630679be560b58b5edb1c3ef4a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:08:06 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:08:06 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:28:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:28:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 16 Jan 2026 23:28:36 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 23:28:36 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 23:28:36 GMT
ENV JAVA_VERSION=26-ea+30
# Fri, 16 Jan 2026 23:28:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Jan 2026 23:28:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:658e67031dba87f37a087802d8564b84ea84ff3a83d5993b8c090fe7466c9934`  
		Last Modified: Fri, 16 Jan 2026 23:08:17 GMT  
		Size: 47.3 MB (47314538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fc6b1a1157059ffbac02377f85d44d8960a6d085ce336f896c6736e2579640`  
		Last Modified: Fri, 16 Jan 2026 23:28:57 GMT  
		Size: 38.3 MB (38295769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb26f8bced4f28a1377822f78e4ee81a2fd8a1662a6b2bc441b0d7032b22abf8`  
		Last Modified: Fri, 16 Jan 2026 23:29:01 GMT  
		Size: 227.8 MB (227841962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e56f0fa74434ff3fc4cad8b4d0d8095ead8333d532b8a2ade55e3d027f9f932b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff74983ca25d96c37c02e948cb106681b4dc782c9889c533cb914461f589045`

```dockerfile
```

-	Layers:
	-	`sha256:a32ec14f2c478c8ddc4bd337ff50cf7be357b989e7a6360054edd68db979c2e6`  
		Last Modified: Sat, 17 Jan 2026 00:07:51 GMT  
		Size: 3.7 MB (3655371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dd8d94640c73ad245406f6d62fef1141130595dad944873074cd1c7153b205c`  
		Last Modified: Sat, 17 Jan 2026 00:07:47 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8cffdb6e3efe96aadd2c5308d41dfcb9cdc19a9342bd607b4daa1651e04d8b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310358638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc87fda6faeba27fde3ed60824f2af6f596c4326dca89332e0664a5980697a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:07:56 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:07:56 GMT
CMD ["/bin/bash"]
# Fri, 16 Jan 2026 23:31:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Jan 2026 23:31:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 16 Jan 2026 23:31:16 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 23:31:16 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jan 2026 23:31:16 GMT
ENV JAVA_VERSION=26-ea+30
# Fri, 16 Jan 2026 23:31:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Jan 2026 23:31:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215869f0a490442d73ee5a088f5ff9c0c81a3fdc8ca1bb0d906ceecc38d4ba59`  
		Last Modified: Fri, 16 Jan 2026 23:29:32 GMT  
		Size: 45.9 MB (45901903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c993bdf110f826a9133d09627e93d2f6fbc63b05c7486e6cc798ec0b27a29b4`  
		Last Modified: Fri, 16 Jan 2026 23:31:39 GMT  
		Size: 38.7 MB (38697994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ee0e35d152abf65e410de9f73a4037d066826911656aa15ceceb1f6aab42de`  
		Last Modified: Fri, 16 Jan 2026 23:31:43 GMT  
		Size: 225.8 MB (225758741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:38b921bac7aeb7f40c5bd735801d7f49beff9b26d112e037903b17e72d42355e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb09aead8caac7eb8f73f2a78468fcb48825c17ff9a45a380637e2f6b3aa5b7`

```dockerfile
```

-	Layers:
	-	`sha256:cf7cac28a9bd2c1ad3878d6a0f894b720ada23eb95bbf19fa28f88fd43e016f5`  
		Last Modified: Fri, 16 Jan 2026 23:31:38 GMT  
		Size: 3.7 MB (3653061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc1179a90c273a972d7939f3709a1b23852b99453b8cde88e1ef376b48d4b57`  
		Last Modified: Fri, 16 Jan 2026 23:31:38 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
