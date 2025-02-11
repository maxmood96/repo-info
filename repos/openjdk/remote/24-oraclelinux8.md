## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:72597aae8468cb822ea2e5a85bf8426554afaf3ba3e4e15615a11bad37026da2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:eb34592a6ffd05a7b9dc60f8dd66f2fd7862d054e3fb82acf936438fcb8104d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279575742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54faf04e48eee8b65883feea003eb1d6991272dfdbebff731405bea1c8c704ba`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf5a3c7d8890a64c60d60ea38b6b8682451c6b3cd9ae69910ffebb43788bbd38`  
		Last Modified: Mon, 10 Feb 2025 19:28:36 GMT  
		Size: 51.3 MB (51276195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fd230abfe7ffce81a1e17f41e0859fbe20d2b7598c8e15004086c5396d2e05`  
		Last Modified: Tue, 11 Feb 2025 00:28:24 GMT  
		Size: 15.0 MB (14987399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7c8c51f10e490d13ed629797e5d1711146642759d76e6534678cd8a0ebf5cf`  
		Last Modified: Tue, 11 Feb 2025 00:28:26 GMT  
		Size: 213.3 MB (213312148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f0cb18e7add41a4adf1f0200c75ae769a21dd7daee54b141560796acd1635fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2e59eceb1f51284d4d3606ab58976732d98d8b234a5965d15cce546442cbc1`

```dockerfile
```

-	Layers:
	-	`sha256:72d3f3df6cd79d953160091f5d4c8fadf4881053f26996cf87d163e42b8da455`  
		Last Modified: Tue, 11 Feb 2025 00:28:24 GMT  
		Size: 2.4 MB (2444671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2451de2ac1b6e2624e90438d7af92aec4b4966217618c358d2acedfb7057a99a`  
		Last Modified: Tue, 11 Feb 2025 00:28:24 GMT  
		Size: 15.4 KB (15434 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:553ae8290424fdc2fb1f196ce6c8af3f2acd7212ba13db1c0a21ee3ccefac179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276912628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690b623ecaefbff3fb8ab0346e53a2320e348cd0536c61f923ba8977a372bb15`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:98af9e98299537ec5803bfae733caa43c349cbe6b0be9c5471f90fab89c45c6b`  
		Last Modified: Mon, 10 Feb 2025 19:32:47 GMT  
		Size: 50.0 MB (49984203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9af9c67dcac1b4e361524cf6db54d3404388fae351d6ce90ba33475433a67`  
		Last Modified: Mon, 10 Feb 2025 20:39:29 GMT  
		Size: 15.7 MB (15669487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d7e4d83e8dc27f8a1fbdfe267922aba5b99c65865d0dae25279db5eb45d881`  
		Last Modified: Tue, 11 Feb 2025 00:39:08 GMT  
		Size: 211.3 MB (211258938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:06208791594a76cda1c83da12e58e1445e258ff0b1466a287486768ab937ed94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64972a174146db29f66d38cbde0bee14b172e28d12f8f3b664c2ce7def3995b6`

```dockerfile
```

-	Layers:
	-	`sha256:367a02443cf53f2c6ea3e423e91ea1c05e804f01649e26669a356ec78196bdbf`  
		Last Modified: Tue, 11 Feb 2025 00:39:03 GMT  
		Size: 2.4 MB (2443493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac47f82b3dc853a8b194acc59a4b06630224d5b875c1dce9c67ab3618ae84ec`  
		Last Modified: Tue, 11 Feb 2025 00:39:03 GMT  
		Size: 15.6 KB (15552 bytes)  
		MIME: application/vnd.in-toto+json
