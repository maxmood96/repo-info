## `openjdk:25-jdk-oracle`

```console
$ docker pull openjdk@sha256:3d63bfd681d2969c1dd545ca52c4080a62c8f6b88ee42cbb592a5dd527bd6636
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ce427b3427058b226e677591e514cea8ccea95d7ce810283479f3a5d731d65b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309611985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a0b17545d919bc2db0a36fb4bc12c3c7a54e12571fe9da7db9c10403cdab7f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 14:53:19 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 13 Mar 2025 14:53:19 GMT
CMD ["/bin/bash"]
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:804bb8ae89decacdf918af27c892df04e6f2d3038e3a7d1e34475eef6be9aba3`  
		Last Modified: Thu, 13 Mar 2025 17:46:19 GMT  
		Size: 49.1 MB (49091441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5775166297c2bf11327fed542f4553533e31fbaa2c82828b10f3ba5fdd8ad1a`  
		Last Modified: Mon, 17 Mar 2025 21:11:22 GMT  
		Size: 48.8 MB (48758850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0db4449e0a06b0ab8720edfc4af6193d291eb02811900fda25f21f75c2c10f`  
		Last Modified: Mon, 17 Mar 2025 21:11:25 GMT  
		Size: 211.8 MB (211761694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6acf24d2e2bbb0dfad5d406e65496253a19f1eb0c1e10787ac9773bb7686231a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe16230c3f607d1c57738fb999eeeeb419edde609e02e57f38f4964c957f6d3`

```dockerfile
```

-	Layers:
	-	`sha256:610f84ce657c22f0bd2aed54528a9b1fc6e119ca536760b990fdde5ddc2361e0`  
		Last Modified: Mon, 17 Mar 2025 21:11:21 GMT  
		Size: 4.9 MB (4907013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3acd83c6cf4bafa6542376c6058abda5047fa4491c329039a25d1f16f7bb1594`  
		Last Modified: Mon, 17 Mar 2025 21:11:20 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1f291e09acf6794b6015ffd621ad4bbe980943cf25e5e50b9fb89cf6f6dd4d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306565350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfec4f9fa4a73ff7be6fb20ffd8eeb59ca420d4e47f3d492dc31ca0c86dece61`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 14:54:08 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 13 Mar 2025 14:54:08 GMT
CMD ["/bin/bash"]
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 15 Mar 2025 00:48:15 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Mar 2025 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 15 Mar 2025 00:48:15 GMT
ENV JAVA_VERSION=25-ea+14
# Sat, 15 Mar 2025 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5fc0ecfeaad76f5acd86d6f0d28755072d9b2531d87629a245059f33b7d31c9f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='655f70de3b6c5247ab18bc41b57791463b6bbd0275845c6026201fb9a1a04032'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 15 Mar 2025 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce92cb0849370fbaafa6ab88c7b03cebc3063fa56835d9dbf7d0b47c679a0097`  
		Last Modified: Thu, 13 Mar 2025 18:10:14 GMT  
		Size: 47.7 MB (47668022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4526627be0e2d666f68ddd55808801d398e443da5584c4a85a1289885b0191af`  
		Last Modified: Thu, 13 Mar 2025 19:16:07 GMT  
		Size: 49.2 MB (49185276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedc20040935d77207a8bce29fa72f2bb6e4d586ce86af5069a003991f66e35e`  
		Last Modified: Mon, 17 Mar 2025 21:23:35 GMT  
		Size: 209.7 MB (209712052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6847af345ab322710c10b039584ff951e94b1748f2b088bb365b8d7dd3f080b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9291a2be1f5951db6a645e17c479c16dfe04ee9d98cd5b18f50954fcf8779aed`

```dockerfile
```

-	Layers:
	-	`sha256:af1119c06c6774237549651d9cd30b5d77e343c332e4164787aeb2b0acf95a14`  
		Last Modified: Mon, 17 Mar 2025 21:23:30 GMT  
		Size: 4.9 MB (4904775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:997deaa940029706e22a75a0418f89d7fb6cb596f47470a3abd8b95b22ed3d46`  
		Last Modified: Mon, 17 Mar 2025 21:23:30 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
