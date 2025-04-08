## `openjdk:25-ea-17-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:31058ab4dceffde3fc27a0cff9ae9255434442aeac51d1f2d10be618abc90e3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-17-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d4e509cc43b4c2671689c7650d53f2b7066adfc368b7512b8a3f2b34cdb3755a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (278983378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7f4c3f97e8bdced426797784d214750f4b19aa9b32a8f836e1e45a5de20a80`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Apr 2025 00:24:58 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 01 Apr 2025 00:24:58 GMT
CMD ["/bin/bash"]
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:079caf22b235d19accaab46f0177ccda24bfe8b1c7622e0cd0cfa34e087ba3ad`  
		Last Modified: Tue, 01 Apr 2025 17:12:53 GMT  
		Size: 51.3 MB (51287468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877ce9d0a616a82cc5acd0bec93cd40936b381c4d2b8ebf9d6b569a9b1784eaf`  
		Last Modified: Mon, 07 Apr 2025 22:38:31 GMT  
		Size: 15.0 MB (14987194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa77bb6cb24264838ab81029c4e146d29c36a895b8116ae50852a262f028020c`  
		Last Modified: Mon, 07 Apr 2025 22:38:35 GMT  
		Size: 212.7 MB (212708716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-17-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:3086e9447d7f0ef236781e2040e24fc93897f8bd3caa8174ebc9c9278c16779c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665f3ca680c71ca9d96c1530508f80386cece404ac3dbbaf84c94a72cc6fd576`

```dockerfile
```

-	Layers:
	-	`sha256:e0473f411f66a856e67fa7ced64fa7f1cea4a29b96392a92d87230fcb8ca4a57`  
		Last Modified: Mon, 07 Apr 2025 22:38:31 GMT  
		Size: 2.4 MB (2442869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c08357b51fd76547c045c4a8f0f871e7b6d029d8eb5b0182c539ef2b53f054`  
		Last Modified: Mon, 07 Apr 2025 22:38:31 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-17-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c72c74651bd5d2fe2a0dd647cf6c160a3862524b67adb8548b4bcf6465927a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276236072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f927d6ddef499c3737dc25fd14ba768b8d37850f4e6e505b93da461d031985`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Apr 2025 00:25:48 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 01 Apr 2025 00:25:48 GMT
CMD ["/bin/bash"]
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4489284649094031c9d59de175b95cba54b287149fda3f89f7719455b8603092`  
		Last Modified: Tue, 01 Apr 2025 19:38:33 GMT  
		Size: 50.0 MB (49996692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba176abe09fb788fa0b796b3296cf07cd69db81d25317a0f58604e54b22f960c`  
		Last Modified: Tue, 01 Apr 2025 21:58:57 GMT  
		Size: 15.7 MB (15686748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0756faeb71c7dc77d916db7bd72c6cd2698b0a35f32f63d1c6190f493b5162f6`  
		Last Modified: Mon, 07 Apr 2025 22:52:53 GMT  
		Size: 210.6 MB (210552632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-17-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d6952051cd8d078e17711f7003da8be53c4b2072e007741c1bae0b4f3331157a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16eacf5b82d50ac36efddad3fa0e3683588ceb8fd47a29588ecfd1f079a249c6`

```dockerfile
```

-	Layers:
	-	`sha256:1066c047c1584af01dad5bbe00018679b9ea923195566ef6dd7dc1a40dca9894`  
		Last Modified: Mon, 07 Apr 2025 22:52:49 GMT  
		Size: 2.4 MB (2441715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0171994f27c278f0ab65fc6a627e76e0b024a244ef34778fa9b6372fe66922c1`  
		Last Modified: Mon, 07 Apr 2025 22:52:48 GMT  
		Size: 16.2 KB (16180 bytes)  
		MIME: application/vnd.in-toto+json
