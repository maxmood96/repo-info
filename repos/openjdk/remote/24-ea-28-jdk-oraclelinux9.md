## `openjdk:24-ea-28-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:887ecea0c5e1f83eba5c1fcc46de1c7753072c21483b4186964567d5edd2300b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-28-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:f5afe12ccda00cfe28e4aca5ba648649a574429d2e2ed502a07f997e7e5f915e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310606853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc0ff1382411aec636ed9fe94ec98771716c867daccb96baae629779cf068d0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c018680c56821d8fe24b3e63efb1afeab379aa93e2f0fb9c80bda8f193a36620`  
		Last Modified: Sat, 14 Dec 2024 00:30:44 GMT  
		Size: 48.8 MB (48765766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac7d3c0f5c7bc4714e1085bff2f6b1e177c2827b43dee345836ae20cd43b339`  
		Last Modified: Sat, 14 Dec 2024 00:30:46 GMT  
		Size: 212.7 MB (212742385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-28-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:a99a9a5f0300f593352f8c020b3558937209f332354507669de76641d66da60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4937412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30878c51afd4f6b199eb3c21ba44bb1789ecc61acc7d4caf3ae3c091a76b2905`

```dockerfile
```

-	Layers:
	-	`sha256:b5407aa1405eeb230a83737c93c1425dc8a932710b523f4f649f28435a59b9ae`  
		Last Modified: Sat, 14 Dec 2024 00:30:42 GMT  
		Size: 4.9 MB (4917666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6c490efb333c46af5491329602d0f7eb594c547c78acd89c5962f172327b99`  
		Last Modified: Sat, 14 Dec 2024 00:30:42 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-28-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ad64b0fc58317391c1ff1867ac8b16572dee2972ff69f79e6eb086e19fee2f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307568694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a7146d759e4cd4f3142551f0269abad84111edfe66cc637db934f268feaa29`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50730d7cdebc9dd971fe547b229ac9b36632531d0634a0903681766460bf2cf8`  
		Last Modified: Tue, 10 Dec 2024 01:26:17 GMT  
		Size: 49.2 MB (49196487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c5fe044823a64e0ba76a7cf5b781443e6b5a4f3686c0506745b88ee95e7c8`  
		Last Modified: Sat, 14 Dec 2024 00:35:09 GMT  
		Size: 210.7 MB (210704815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-28-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:9250e43e0fe498ccaa95c0fb631e18cd52278787905924e9c89003bb642447ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef282eda9bc403f96395c6f501c2b4f76633622597c32ebc13e337d1a12bcc9`

```dockerfile
```

-	Layers:
	-	`sha256:805100ea3466ae871f997bdbbd55cad37263aa097bd26bd2ce1ead0f96d56cb2`  
		Last Modified: Sat, 14 Dec 2024 00:35:04 GMT  
		Size: 4.9 MB (4915424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1107f342101b322b0e27a382a437eee7119b316b842b2d5f44ad534a14e86ea`  
		Last Modified: Sat, 14 Dec 2024 00:35:03 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
