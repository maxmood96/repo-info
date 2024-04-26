## `openjdk:23-ea-18-oraclelinux9`

```console
$ docker pull openjdk@sha256:2b9848fa2961ffa276ceec44bfa3760fba26e0b7718567c3d025ea4ad0922a79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-18-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:b8f01156f9b7b63addb2257d3e564e2c963f8c9f7a16dd238b161781251583e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297546474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73913e3a78874b1fdfe8fe2517e2f4a7014202023821363bf244f5b90cd69069`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Apr 2024 18:48:10 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42c936f6a49ca30c0c679e7d5a2c22a2840f747b55d1d5b95831b4d948220b`  
		Last Modified: Thu, 25 Apr 2024 02:55:39 GMT  
		Size: 37.7 MB (37728436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfbda0f11910b55dad8f538a3371f98acc7fa3ba6d81f2bd8818876afb6ebd5`  
		Last Modified: Thu, 25 Apr 2024 02:55:41 GMT  
		Size: 210.9 MB (210852894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-18-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:88b87f1c2b9cda5bcfd85f9e7ff8a11e40f2c4ab86392c815025b074177e8063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3349454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee486e8b79c0e75a5da635210fe5b449f90c2fc901e3e406bb08338a25fbfd7`

```dockerfile
```

-	Layers:
	-	`sha256:b2ab1b36a0a10396ba9b146f036537657810b99b68badf72ff67795595b8435d`  
		Last Modified: Thu, 25 Apr 2024 02:55:38 GMT  
		Size: 3.3 MB (3329561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd8028353c594881dc923a03ac82a064d202794f44116d4ec2d05f33e6c54d3c`  
		Last Modified: Thu, 25 Apr 2024 02:55:38 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-18-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:54b2b3461c161cd6ca9d852e536206526f2c2fff1bc9dd36704d98d1b4c9f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294540512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669d197c22957cb711f6a89f3d0446dbb44f5001d3b4046ea8f473f0f9090dfe`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Apr 2024 18:48:10 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5998d81da777dd4f81d01a63cd4676cc2bd3824fbd23c02af639d3bfbc80f43`  
		Last Modified: Fri, 26 Apr 2024 08:23:15 GMT  
		Size: 38.1 MB (38142556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b7bef8bbbf8792d8ce4e69762522349aaae4a93772bff6592527432031abed`  
		Last Modified: Fri, 26 Apr 2024 08:23:18 GMT  
		Size: 208.7 MB (208735480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-18-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:4a9364b3163a521968db1aaf8375392e1c04063ea0491fe24a353000c705c982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3347689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc53a75a1c1b6e200bbc511aa7ab872b6a756f5cfe8a6d010252a8e9ae40b7`

```dockerfile
```

-	Layers:
	-	`sha256:af3e25353f706d984af4fbaf8581d734efa78d2349903ea2b3abad80be392f53`  
		Last Modified: Fri, 26 Apr 2024 08:23:14 GMT  
		Size: 3.3 MB (3327759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d8032e7dcc48e0ea779943dd24d20306437d20d9bdb91ca793b8430c8caf8d`  
		Last Modified: Fri, 26 Apr 2024 08:23:14 GMT  
		Size: 19.9 KB (19930 bytes)  
		MIME: application/vnd.in-toto+json
