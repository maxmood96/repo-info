## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:86465ae008255f3e48799de2b981b155b6d4126ba0b0c0680b814a5eafffe132
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:008bfa9e18761bc7dcf64a5505e47db1d201ae7967bbe6e7a9e32ad53594b537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294750111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23e8510f226ba5029a50e9574f119c8cc5c6d0cee0712751e3eb7d66bd94f9d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:11:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 24 Dec 2025 06:11:48 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:11:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 06:11:48 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 06:11:48 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 06:11:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8733b0acee0106c8f62efb14cb858ac390eff6684a633a6bc8fae842fc784d6`  
		Last Modified: Wed, 24 Dec 2025 05:20:01 GMT  
		Size: 51.5 MB (51465497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92436c6c5bfd49c5f3274778bf6ad67205a9e62f11eee0e338f2bda61f96216b`  
		Last Modified: Wed, 24 Dec 2025 06:12:19 GMT  
		Size: 15.0 MB (14988314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340e94e50f097f58f218aa325934307912f1678934db6883041dcddc120fe170`  
		Last Modified: Wed, 24 Dec 2025 06:13:31 GMT  
		Size: 228.3 MB (228296300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9035bf30109af1976334e025c5c70f067d6b5159c1754c351e0a9d84bdd915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb5be7dfb65a36d81a2bd43d229381870bd0cb40d4e037bac205376acd6a89f`

```dockerfile
```

-	Layers:
	-	`sha256:cd5667a6c95235b21b8c841a951da8dcbfe865b1165bffdfc1b11c695d680926`  
		Last Modified: Wed, 24 Dec 2025 07:24:04 GMT  
		Size: 2.4 MB (2448672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:006dbe15522157621c846d7fae67b42faa6d943ec28ba17932bdfe6023302e49`  
		Last Modified: Wed, 24 Dec 2025 07:24:05 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:21bf35fd13545ce19621a8f55ecde09ed203290bc2821d003b947405e9390ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292101903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223ba6639da9ad495f8e4d3d8fee061a31a9801157b83817f261bfc69f2bca05`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:42 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:42 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:12:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:12:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 24 Dec 2025 06:12:22 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:12:22 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 06:12:22 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 06:12:22 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 06:12:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c56c47048941ddf04da7dcfda383c6b40da72e218826ef10c27b29f2fb9db04`  
		Last Modified: Wed, 24 Dec 2025 05:20:02 GMT  
		Size: 50.2 MB (50177032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2aafad89680ce7aae09a351aac5dea7d7c065b1af9b97a1a4f16b68455da7e`  
		Last Modified: Wed, 24 Dec 2025 06:13:00 GMT  
		Size: 15.7 MB (15697396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4084c0df3f48486b868595c6853a26862a186680a81419f6a19f893daaa1b26`  
		Last Modified: Wed, 24 Dec 2025 06:13:05 GMT  
		Size: 226.2 MB (226227475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a8d0015fea7d463ff3e618fab3615abd46e285c51cb570336b6a2e3bc05f78c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b964ed57f9fa4b43623fd04917867d7057b06d88d643333e3869d202e656bf07`

```dockerfile
```

-	Layers:
	-	`sha256:3df044f52c9a738907b90b95a9a52caeb4e7638d880740eb6b96c8c42c6c172c`  
		Last Modified: Wed, 24 Dec 2025 07:24:08 GMT  
		Size: 2.4 MB (2447482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeef9fd2779d56cca7dfa22bc62dd6604d3d92721f5e8a775ba743114f39b0d8`  
		Last Modified: Wed, 24 Dec 2025 07:24:09 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
