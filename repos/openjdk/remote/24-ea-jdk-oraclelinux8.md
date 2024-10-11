## `openjdk:24-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:110ebcd77ad9decf59c47f796f2f49a10ad9c6ff3fc244bc63fe4f9ad6bed3a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:36e171fc8cdb9de668d08313acbee631a35e8261cb0a7e28c7e63d170c160244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (279049985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a9c9ffdbf5b510d4524d7708aa979f18bbe184c159b0e5d55c45cb1800130e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 10 Oct 2024 22:15:38 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 10 Oct 2024 22:15:38 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 11 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='b283aeaeda2e1fb83a01a61a370e2e95e217a00aa3a51641d1b65244b60b05f6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1f125899b06296b1948e650bece4c424c5ac572793c9446bac6f39c68a4545fd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ccec4de1d50efaab175e979c24b513dacdec266a6a00f442167c614564b83ef0`  
		Last Modified: Fri, 11 Oct 2024 00:11:24 GMT  
		Size: 51.3 MB (51295624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b60630447774571944d24fb377561084f1a7449a35b1e176652b5ebb91d15d`  
		Last Modified: Fri, 11 Oct 2024 18:58:16 GMT  
		Size: 15.0 MB (15036736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9992ca8a1eb87f12f45aac88bf93701f791291653e3e88afc0b71a021f3fd4db`  
		Last Modified: Fri, 11 Oct 2024 18:58:19 GMT  
		Size: 212.7 MB (212717625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:fe05630b6ab499235c16bd9ce1e5a7b5439ffe39449ed08b84db4a2b77659559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2441854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125de7cb28bdf2cef1a6dec5bf6fe552266118cb125a5c2dd56cf417054572ed`

```dockerfile
```

-	Layers:
	-	`sha256:b13b2d1a7ed6268ed50f4ccce11f6efabc57d0a97a692eeadcf5aa65e47ad43a`  
		Last Modified: Fri, 11 Oct 2024 18:58:16 GMT  
		Size: 2.4 MB (2425812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9890cbd92261403f3dbbb7384dfc191b2b553a0fdeffc3d355706b3291d8b88`  
		Last Modified: Fri, 11 Oct 2024 18:58:16 GMT  
		Size: 16.0 KB (16042 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9540614dfbe4b6d305ee0390c919996ae1ddb78533ec98cfe22dfdaf1837c397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276313234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d12f3261fd335ff9c75d1ea7a07fc5be61a704f375fa1587d750cd93522db`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 10 Oct 2024 22:16:27 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 10 Oct 2024 22:16:27 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 11 Oct 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='b283aeaeda2e1fb83a01a61a370e2e95e217a00aa3a51641d1b65244b60b05f6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1f125899b06296b1948e650bece4c424c5ac572793c9446bac6f39c68a4545fd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5aa1f5d85d147a7c16d0057c3fc21b1ae3d482ca5ede955163a95cc540b4244e`  
		Last Modified: Fri, 11 Oct 2024 00:11:55 GMT  
		Size: 50.0 MB (50004038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096a2c0e68dd1c814c85ae00b2652f096632e44095b6ac5ff4756a756a3ef3bb`  
		Last Modified: Fri, 11 Oct 2024 00:50:19 GMT  
		Size: 15.7 MB (15706108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3512c4fffa3b3457400b3b4f91ea966fb53ef42ef95eedd6382223ee7205f838`  
		Last Modified: Fri, 11 Oct 2024 19:25:51 GMT  
		Size: 210.6 MB (210603088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e1771dc77ef7a5586f9ee965e91cd6e9d4976d2aa54c642fabbd403c59a99068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbbf090aae01b1498c9f89c2ba40f6d8690f0c5cb1c3e815d4986d91c5ad3b7`

```dockerfile
```

-	Layers:
	-	`sha256:276836c8c28312c2f32fca559eb834b9ec69778b09a96253f7e7c8e658d6f3d6`  
		Last Modified: Fri, 11 Oct 2024 19:25:46 GMT  
		Size: 2.4 MB (2424034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca84b320f7ec8d6bc645c47ef9f8bd0a4263c11f8a255ec7402181ae6fb54fd1`  
		Last Modified: Fri, 11 Oct 2024 19:25:46 GMT  
		Size: 16.2 KB (16185 bytes)  
		MIME: application/vnd.in-toto+json
