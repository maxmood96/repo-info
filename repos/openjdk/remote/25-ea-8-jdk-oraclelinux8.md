## `openjdk:25-ea-8-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:608dc6479072c98383d1616dfc49ff3f696cb8df5fcb7ad05494f5ea7c6b4f6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-8-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:cdab71800975a9e72a6d6234ad4c4e645bad2451cf18ed9d21efa5238f886c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278491482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ea30d4e5c7be98b7a3d4cdfcf942be294709bec486c17aeee1ca40ea071159`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 18:59:24 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 30 Jan 2025 18:59:24 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b976166ae00f0fda8e12b934d92a7265904c082bbb675e0cb9bd4bbe93bedb30`  
		Last Modified: Thu, 30 Jan 2025 23:27:50 GMT  
		Size: 51.3 MB (51277963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ecb9734a919cc9edcd81a8e030bd2f8a347a7a29b7d64bacc741635196769`  
		Last Modified: Fri, 31 Jan 2025 22:26:40 GMT  
		Size: 15.0 MB (14975083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd0130a89a9dfe4d99a4628f18e98abd0bd1ae64a56f1c36e76661c6d94345c`  
		Last Modified: Fri, 31 Jan 2025 22:26:43 GMT  
		Size: 212.2 MB (212238436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e02b16e37a645330d460a99bd71ac28a16a90af4e7c243232b03b1fe3652ea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb9b1da3a567c94a8b68e4e1f39981468abdd8fa4aa93c286648003c3d2a364`

```dockerfile
```

-	Layers:
	-	`sha256:8ceef205fdc1b5a65eb24cbb2e4379ce12ebf0ee1d896f42c46803c2b3cec006`  
		Last Modified: Fri, 31 Jan 2025 22:26:39 GMT  
		Size: 2.4 MB (2440961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3be1633fb5cc7858736a66c1e50190b2b5dc46866139464ba1be3a7d8d05799`  
		Last Modified: Fri, 31 Jan 2025 22:26:38 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-8-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:12d5dc65b0dd6269442b860890177d0290a1e5aa753580a3bd7064e3c2b26e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275845554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dad0ed6790e619e0ad8bbdc51f29d60fff1b40e27665f1a68176140392f09ce`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 19:00:17 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 30 Jan 2025 19:00:17 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bce860c27508f058f4bac6fca02fb3ef33ecf5c8331d2635b7c34a8b0af94e0`  
		Last Modified: Thu, 30 Jan 2025 23:30:11 GMT  
		Size: 50.0 MB (49984693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20da80e2bd804d65a47238fa85705492fc406b2b8cbad4cb1a153d9b26b0720f`  
		Last Modified: Fri, 31 Jan 2025 00:27:46 GMT  
		Size: 15.7 MB (15659413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc59c4fa52c169d542847fc7e905086062255821500a0730f29699183cb6266`  
		Last Modified: Fri, 31 Jan 2025 22:27:08 GMT  
		Size: 210.2 MB (210201448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e8e0ec29f1ed4a16aebd1a350fa857f09cdef5a8febd987565ce68db39ec4062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97e40b7726452cca67b95e91ede8133a1a21e179a44bcb0dd139543b2bc7993`

```dockerfile
```

-	Layers:
	-	`sha256:c8e7ac78beed2c2f0ba19c3d3b94daa139af37ea7b58d395ba1f76bd18e90c0d`  
		Last Modified: Fri, 31 Jan 2025 22:27:02 GMT  
		Size: 2.4 MB (2439807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f82196b024dfa0cbc0cde84a1be1e7e04bf9d611b1eac514ec6643dc6d0df15`  
		Last Modified: Fri, 31 Jan 2025 22:27:02 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
