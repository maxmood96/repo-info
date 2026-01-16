## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:8a23328bc8ea996bc831afbd2dd23167d7cabef0188f6f01e323a1c970e556c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:361b35bdd0d90f8f48c4cbb4c8a2e3f4ada21410a87d4146433b027611ee0eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294752788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7f9b09bfed5af39bea7c9a8119643c4ce9e826423cb587fab945083af0e156`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 21:43:04 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 09 Jan 2026 21:43:04 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:07:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:08:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 12 Jan 2026 20:08:03 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:03 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:03 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:08:03 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0ddc6852d18db715e5e4c3edd3fa8bdf8afc37b9507d95d8bc0194012c32432`  
		Last Modified: Fri, 09 Jan 2026 21:43:27 GMT  
		Size: 51.5 MB (51465737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8ddaa2d84ccfc44c7012344f365e7ae9e1e9e5aa1ea14380dc47f4d368fb45`  
		Last Modified: Mon, 12 Jan 2026 20:08:36 GMT  
		Size: 15.0 MB (14989345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b447864141b747134f40cda037dd05f565a885449404a87de9fff74bf9d2874d`  
		Last Modified: Mon, 12 Jan 2026 20:11:58 GMT  
		Size: 228.3 MB (228297706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8bc98e439ff1175688735761746329823547b356cf304f04f4b7b40443a8f39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae797876b958c67a3cf3ec6f2e52ebd3f27be4e2de1927675dec46e74c98e83`

```dockerfile
```

-	Layers:
	-	`sha256:07fef53379328057b84ccad48cf4f1dc211ef986bb729c0113d53625d5c4a1e3`  
		Last Modified: Mon, 12 Jan 2026 22:24:02 GMT  
		Size: 2.4 MB (2448682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3dc0982d3112730618db88cd7f5e23d5abfbf049aaffe752ae145092af6c92`  
		Last Modified: Mon, 12 Jan 2026 22:24:05 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5bec62bf5a0c1885ad45710f863a5ef38ef60dbaea8ea163eb0f30207e82b99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292119012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5e1f5063bc8d8b811b936eeaa4d4879a1826ffd93d07fe759708e58f81c8cd`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 21:42:51 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 09 Jan 2026 21:42:51 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:08:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:08:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 12 Jan 2026 20:08:51 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:51 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:51 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:08:51 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5daa2797aa97d66d1615bd1c3686dd694a6f5fa7082128bee108f37838f634ba`  
		Last Modified: Fri, 09 Jan 2026 21:43:15 GMT  
		Size: 50.2 MB (50181216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd84d78fbc29b1354ced89c1bb3640e1bb8c08609cd351064c10a469e434db45`  
		Last Modified: Mon, 12 Jan 2026 20:09:23 GMT  
		Size: 15.7 MB (15700509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6c90f847d5fae81bb122814502c6ab7f9edb9d66255f47172c0421e8c5796`  
		Last Modified: Mon, 12 Jan 2026 20:09:16 GMT  
		Size: 226.2 MB (226237287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:fb419c1a26d520f14ea9825434603f6f9551854c7123b6b5740ff7a4f6de803c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4ec5c2960ce273d95d036fc46bf5b1ed07261b915896355dc947ea596f0cda`

```dockerfile
```

-	Layers:
	-	`sha256:4dea07500f3e1252228309cfe601600a646e4211d623361388371310749b5501`  
		Last Modified: Mon, 12 Jan 2026 22:24:10 GMT  
		Size: 2.4 MB (2447492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5ad822374544c4538cab9c6ecca7dc3357a58214ec75a6a983dec6c48dd73c5`  
		Last Modified: Mon, 12 Jan 2026 22:24:11 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
