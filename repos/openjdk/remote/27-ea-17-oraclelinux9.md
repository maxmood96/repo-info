## `openjdk:27-ea-17-oraclelinux9`

```console
$ docker pull openjdk@sha256:79d8695386d139c28f41c72d1387d71f81a455478a3678bf4528ecdc751b4f8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-17-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:ecc540d4c768951a1c4db13c4c30a83d4e0219a1d08d9bd99edddf2bc01dc90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314430546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29079ab0b8c447534cd77c26dc86a6e3830bf40e4cb5aed070ba3bfb60e0ba6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Apr 2026 18:56:39 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:56:39 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:16:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:16:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 14 Apr 2026 19:16:45 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 19:16:45 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 19:16:45 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 19:16:45 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 19:16:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c9513d9d1269ed66e93cdd86e573688d09e1e04c4a2114eb2109b350a272694`  
		Last Modified: Tue, 14 Apr 2026 18:56:50 GMT  
		Size: 47.3 MB (47310406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5088dede4f010cf9c38f3f7fece1c6a7c31c74bfaa4cfc9b115962b6ec9e8799`  
		Last Modified: Tue, 14 Apr 2026 19:17:05 GMT  
		Size: 38.3 MB (38271130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e2f664c2154fae872ce9900cbb42a7f4daded71e3b862a8f44d7950a4991e3`  
		Last Modified: Tue, 14 Apr 2026 19:17:10 GMT  
		Size: 228.8 MB (228849010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:b91426f1c4a0917e45fc2bc365bd76622d35ab805443d011c44450fe747303dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b966ec337ccbec6d57aa1dcf8fbb4287dde6584c2fe138daeafc667a34c53f1`

```dockerfile
```

-	Layers:
	-	`sha256:fdd365a271831ff63a828bacc2c12e3cfb491cefda47f1194a13b373788bc4cf`  
		Last Modified: Tue, 14 Apr 2026 19:17:04 GMT  
		Size: 3.7 MB (3652963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb7ad9843ce4c1b5b9d918e31e9127438ce46a1d89b1f34b87e4de9c856ac553`  
		Last Modified: Tue, 14 Apr 2026 19:17:04 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-17-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ff21182e12b00e994cb9544d280428b4ddbbf736c8aafb33422a981bfcc7b776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311370588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28eed528960b054b80777d3d1347147cd353b193889d4ff929d9fd9b89873b95`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 Apr 2026 18:55:59 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 14 Apr 2026 18:55:59 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 19:17:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 19:17:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 14 Apr 2026 19:17:35 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 19:17:35 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 19:17:35 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 19:17:35 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 19:17:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ab1b3740ab5d52e59354cefa3b78196051bc32a00c53e2b24066eb5280dfda3`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 45.9 MB (45899688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a96e83aa34afb17fc2ce6aae9d02a750a66dc338e194ed5e96b310931c967a`  
		Last Modified: Tue, 14 Apr 2026 19:17:58 GMT  
		Size: 38.7 MB (38662870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24089fbe40c59ab0d48671f693a426ccdcb5e5b5a53d6ab3db22f40779cadcd5`  
		Last Modified: Tue, 14 Apr 2026 19:18:06 GMT  
		Size: 226.8 MB (226808030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:7609e3417082aea4f6dd00417489421f4e13080423ecae99fee9eabb26b68f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3666019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80f4ad24a9e7e5f0d785becfb9a1b6787ed3ad87e313337515c18843e5e185d`

```dockerfile
```

-	Layers:
	-	`sha256:7e73295cb20f1a2c7736ec5af63e5d3e4293e95c361e28af508afe1f2dd7b53b`  
		Last Modified: Tue, 14 Apr 2026 19:17:57 GMT  
		Size: 3.7 MB (3650557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce5a42a40c9ecbd8bdd25c971b0dec60ada56e915cf720dfe15c66dcdccff17`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
