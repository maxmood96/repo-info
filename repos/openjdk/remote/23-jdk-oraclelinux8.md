## `openjdk:23-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:74ca21c83374b93ac36de99dfb8e49c572602c019a2c3e9a3aac10fd5cd752ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:8b332b9b0a96984a6565944e2326932600e324d1d15ffc3cf3165b7ab72c3d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (277989048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd5bd9c91a9369a1386e28b4d244b2e2be40065eb3d21548129a27dac2f7d17`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:48:53 GMT
ADD file:6f8c3cf297caf3b2a501a32c94a4fc0d2c7024f63d5e4b2215730b56faa6cdfb in / 
# Fri, 07 Jun 2024 03:48:53 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:427bba466fea4df7396a02ec368c5aa24d07ac80d02aa94eb57ba7af7b84b5a3`  
		Last Modified: Fri, 07 Jun 2024 03:50:01 GMT  
		Size: 51.2 MB (51219315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896a5385137692872babd30fdd1501638275045952b6ddb4b234395fbd24ab04`  
		Last Modified: Fri, 14 Jun 2024 01:01:30 GMT  
		Size: 15.0 MB (15035322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6007d4ecee68ceec17d05fdaa05e3a90234438f51e0149b69d8b32e1c2f7140`  
		Last Modified: Fri, 14 Jun 2024 01:01:33 GMT  
		Size: 211.7 MB (211734411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c0cdc5b44b28423f58d0929ee8fcee7e0132549ee9f3eedd02e3407251b01aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1ccff3bca9c53db7436bb5b790fdb6eb0ccc8a2382bb8ca0aeca3d718dee4b`

```dockerfile
```

-	Layers:
	-	`sha256:489566c7caad0d53f4214df3b97d1ed788f3d4b811231085db86bd918612b44d`  
		Last Modified: Fri, 14 Jun 2024 01:01:30 GMT  
		Size: 2.3 MB (2267558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f20cc6283d880976d3668b11aea7329de79c2d4afb543d459a2306e0ff7871`  
		Last Modified: Fri, 14 Jun 2024 01:01:30 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e4d59e24a693ede0978cf6009377eb984d98f395b1a2f1cb89be0e6839fbea5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275227686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23b9c66161d79fc03fdb89b93e213b3efe92d5f953643f3cbfc2bec3efd7a30`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 03:11:59 GMT
ADD file:28329ccaf9d0f8718e6c37965272b9ac3d23fdb6d109ca304f4cdc12c515a2eb in / 
# Fri, 07 Jun 2024 03:11:59 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5522c693c44935bd999ae97ef2649e6707ffdfcf11d7d226a3b78066d03f8ac1`  
		Last Modified: Fri, 07 Jun 2024 03:12:59 GMT  
		Size: 49.9 MB (49926502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224c310d8d2c96f49a742c5059029d51003313d8a587e51fed9a9aedb25695b`  
		Last Modified: Fri, 07 Jun 2024 07:39:04 GMT  
		Size: 15.7 MB (15689949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9c3bc2d75c9df89ddb0aac51aea9e3688acf82d66840585370a01f78dca44a`  
		Last Modified: Fri, 14 Jun 2024 04:10:46 GMT  
		Size: 209.6 MB (209611235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:42d9917ed157d2b4047b5f2a99f477e1f22432146666c08d590c77e629177731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a160197a5c39d2700516a13e5f42b26a197be1adde2f78cae6e8f41574ce8e`

```dockerfile
```

-	Layers:
	-	`sha256:ad8047154ed71b89d6b042bcbad3945b26ce4c3b8a2da81e8bfdab252e2e187e`  
		Last Modified: Fri, 14 Jun 2024 04:10:42 GMT  
		Size: 2.3 MB (2267027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022c2e4c33a490218140d7155e0e9b3d120b6850845890da23137acbd47336c1`  
		Last Modified: Fri, 14 Jun 2024 04:10:41 GMT  
		Size: 16.1 KB (16150 bytes)  
		MIME: application/vnd.in-toto+json
