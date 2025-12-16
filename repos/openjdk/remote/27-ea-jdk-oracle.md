## `openjdk:27-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:03f4c475eb6283743e54cdfc85bd91cf106b9d8d96f8c29bba7994a944b0a55b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ea784423b47d9480ce8a42b1efcc043e2e0118ca0ca4250f91ed27f306698fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313616907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4450e03226448ded2f1d3e5c58e994a5dd058def7662824486859307ccc2f842`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:04:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:04:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 16 Dec 2025 00:04:23 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:23 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:23 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844328ba8fa952b4b4cc108799cc7afeb146fa4db82d7162e548d6636e80c27c`  
		Last Modified: Tue, 16 Dec 2025 00:05:00 GMT  
		Size: 38.3 MB (38297408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b010bce3c92964a7f0c34f93079776788067d44ab11d8fe4dc7b0003f51396d`  
		Last Modified: Tue, 16 Dec 2025 00:05:02 GMT  
		Size: 228.0 MB (228004751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:0a96665e6b2798caeb3a3298e24b6afd0e9cebed4b8799195d56d57fc244cb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86dc516b4a20c77fadd3f44829e8e0b867354b841a246542747e9fc569678bb`

```dockerfile
```

-	Layers:
	-	`sha256:95ac6fc09ae66b431620bc74e0896344d5bd25ad878a189b690aa51c847d11d0`  
		Last Modified: Tue, 16 Dec 2025 01:25:44 GMT  
		Size: 3.7 MB (3655313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:303f14056ee9931deb4b9131877f8d10c2de123acadd8b380641862a0b42a2a1`  
		Last Modified: Tue, 16 Dec 2025 01:25:45 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b9f60cb3bf8fc2707bc32f3597abc7df32e4e4118e10f866365cc5e31ac0175c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310529707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d198853a14b2dc7fadb1056fad16da612107335da71313e62f2d5db23b6b06bc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:03:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:04:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 16 Dec 2025 00:04:06 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:06 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:06 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c33c5358a1c0461404c3dde954e3137693345097c24a04a13da043f8e55f649`  
		Last Modified: Tue, 16 Dec 2025 00:04:42 GMT  
		Size: 38.7 MB (38700742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06cf1cf98a68173159cd932a8056253016488b150f2fc5273c476858a58da75`  
		Last Modified: Tue, 16 Dec 2025 00:04:49 GMT  
		Size: 225.9 MB (225931933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:1dd216d039e71c9a5c6eb5d45bb9c9c6e2c53c19204e924838b93d85a5c5e14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cd1474ca2a7b177c6b66a566ff574f13708c553c63a38d9d9fa15ebcb221a7`

```dockerfile
```

-	Layers:
	-	`sha256:a4c2001e972498543c5348fccc6fa6e9233e5ad41998f451e50cf5374bb33f1f`  
		Last Modified: Tue, 16 Dec 2025 01:25:49 GMT  
		Size: 3.7 MB (3653003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b428959c71669950285a7878cddbf57bfe2eeb115e2e89e8df119a9992b130`  
		Last Modified: Tue, 16 Dec 2025 01:25:51 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
