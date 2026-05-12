## `openjdk:27-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:a5120748022e7cf9ac30b8ac376828cde705814a2d5a041eecb91ff03ae59789
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:3553f0e7b46442646a0b847b82d58dd15dbf16a25c10a849f23e41a577ff99f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309411672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8e55006ab5d1d1db2c010a8d413ac7eb81c1a4457a337d4f6a1622417fc40b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:11:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 12 May 2026 19:11:42 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 19:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 19:11:42 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 19:11:42 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 May 2026 19:11:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbc3c71e4ca9051b889ff9d368cc1bc7887e79927580798907987788dd5ba77`  
		Last Modified: Tue, 12 May 2026 19:12:06 GMT  
		Size: 37.7 MB (37688514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41179164fc862c0433a06bec7e15dc883c53907e7163fe4361d840f8f48697d1`  
		Last Modified: Tue, 12 May 2026 19:12:09 GMT  
		Size: 228.6 MB (228642576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:aabf1f416e168f2b927ed3d538546697dfe04b1bdad824db22fe34de08a8374b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1498b50dd58418db11ba9ea1a80efd632823e1abf93271e4ba33c7d47f184df1`

```dockerfile
```

-	Layers:
	-	`sha256:e65a9ed1df100bb738b087355d269f08fe9016e360972b086c8346b7121849cc`  
		Last Modified: Tue, 12 May 2026 19:12:04 GMT  
		Size: 2.4 MB (2367743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af35aadcb307390ca5492a5187206abce93983705c44604cf451e8daed874e2c`  
		Last Modified: Tue, 12 May 2026 19:12:03 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ba2eda0bb361707a15a816b497cfcc97923420b0754970888cf6d79cece2ee91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305795168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2a6a6dc01a7ed03aa5ffc92c07d9e34114be227977563431452db08c41d2c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 19:11:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 12 May 2026 19:11:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 12 May 2026 19:11:45 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 19:11:45 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 19:11:45 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 19:11:45 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 May 2026 19:11:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a754f7386ed64b39841fdeadbe3683c6dd73af5daa11e9118bce59a68a24ed5a`  
		Last Modified: Tue, 12 May 2026 19:12:08 GMT  
		Size: 37.7 MB (37701854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19265d8248c5822378ed73f15bfa4129e392be42e16b09ff4cf767e6c5223ab`  
		Last Modified: Tue, 12 May 2026 19:12:12 GMT  
		Size: 226.6 MB (226597619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:3a353a7f24976d7f12a1598faae27c0803d6e23276c2bbd6349d61fe11e7aab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0077f54ef95a60ca3380cf1581e060771639cc4ac482639b5bdce7bc03a3f589`

```dockerfile
```

-	Layers:
	-	`sha256:c3f175ec1d82e5f9dfa0b2f1ba180d2f0a342e5a45ef31626fd06b2221aaeb8a`  
		Last Modified: Tue, 12 May 2026 19:12:06 GMT  
		Size: 2.4 MB (2367271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93340b91f0cd32bc8b3247448cec959cf47d73b8f4b524a5c088e231d2abb735`  
		Last Modified: Tue, 12 May 2026 19:12:06 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
