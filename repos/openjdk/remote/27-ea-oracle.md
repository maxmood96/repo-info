## `openjdk:27-ea-oracle`

```console
$ docker pull openjdk@sha256:916df6dd48fcfaa88fc632e97ebb94103e42495c70c0ab6518348739ab047544
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:fa8f624eef77f67158b3c8c8f886509ca35afc5f3252c8967172d2f70517d19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307715672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce02b6562ef13642347a98c1f9d7a879dd8c44cb1c47ab8dafe3eac3128e6f5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:37:23 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:37:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 22 Jun 2026 22:37:33 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:37:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:37:33 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:37:33 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:37:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67891505540a6bb44e488b874e37e31e860e46cfe6e0fe2cdf5c64cd3a8c9ece`  
		Last Modified: Mon, 22 Jun 2026 22:37:57 GMT  
		Size: 37.7 MB (37687115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcefd717c7552e4909ff47db61dff7cba2ea07e955948f8d518794e03bf52a5b`  
		Last Modified: Mon, 22 Jun 2026 22:38:00 GMT  
		Size: 226.9 MB (226947975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:022657bf1c47e39f3a899ccf518bcc72b76096a101e16cfaad845f552d16ff6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57893277910a7a6e17ce58596f83eadf677ca3bc2a4abc8f715b1a518efce4f5`

```dockerfile
```

-	Layers:
	-	`sha256:e7dc1287f26d07f049c4092a0ff55f6885d23aa1671de605dc8335b0b6db19f8`  
		Last Modified: Mon, 22 Jun 2026 22:37:55 GMT  
		Size: 2.4 MB (2366462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddca57e6200add1088dd7a983e3399f35dc69320a62bd21d9f8e3a001dd2b4c1`  
		Last Modified: Mon, 22 Jun 2026 22:37:55 GMT  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:da794d72b97accba444a5148417af945f38f7917b99205c6c41d99dd072db2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304126100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a807a53e1e8a9c60ad1c4516c32306eab2e9b4b12b3baf0e0c4ca0212ee49690`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:37:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:37:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 22 Jun 2026 22:37:17 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:37:17 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:37:17 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:37:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:37:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7794d6854b519666fc859dd76426bc35de4170b704c06948c2017fe6d9b6fb04`  
		Last Modified: Mon, 22 Jun 2026 22:37:41 GMT  
		Size: 37.7 MB (37696104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5a4ff07b62e314045fab799dcbf40f7d87769dd158659a50abf141b55e1acc`  
		Last Modified: Mon, 22 Jun 2026 22:37:45 GMT  
		Size: 224.9 MB (224934301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5eba6d83b3b986518a1e0a8afa7f8a24bff220d389103b083672a6946183e1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d100eb579b442dce7274124e95b2ac820e24cf8a1c1281b2ba559af1d27de`

```dockerfile
```

-	Layers:
	-	`sha256:924bf57963087f9d71c22cb2916286c5055742da82435b48a13804ccfb006ef6`  
		Last Modified: Mon, 22 Jun 2026 22:37:40 GMT  
		Size: 2.4 MB (2365990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d3f453622a0fcb2567532659b77fe26fd49f0f7ebfb0dd9ac67aa07f679832`  
		Last Modified: Mon, 22 Jun 2026 22:37:40 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
