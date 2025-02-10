## `openjdk:25-jdk-oracle`

```console
$ docker pull openjdk@sha256:9aa94d33bce24825c0a2a648f26ba1dacda304021e0414432ce38391b2d1cdd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:27318470804dafc1a06eba2ee10b751a580d6694b340362ba62e8dc4b57123f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309635674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27774a55d98db57f08abb34d4072417953905e3ab8268a91d0f9ba3f018118fe`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:53:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
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
	-	`sha256:1d19e87a21f588780c1e2041d7a86fa8c5b805988de43968a7ad8419eeaf76d5`  
		Last Modified: Mon, 10 Feb 2025 19:28:42 GMT  
		Size: 49.1 MB (49097200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af5609dab6f383519dc547e3f5bf1294139dada723621de8d589d7969995325`  
		Last Modified: Mon, 10 Feb 2025 20:09:21 GMT  
		Size: 48.8 MB (48768035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e022e91f0b296caacd4ab6748cb3b8b56aadebdb477d25c998db7469221acd`  
		Last Modified: Mon, 10 Feb 2025 20:09:23 GMT  
		Size: 211.8 MB (211770439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:41275c6c1cfd629d82e7d01a579f16193f08876501911920c599565d6c8058e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c355afb74842c717903661824c8a6582784f7ef8f4fe64a7e3a2c62d57a9ec`

```dockerfile
```

-	Layers:
	-	`sha256:3eadc65fa29342bf88ca50ea361961330a9cdd1fdab4e6530e476ccb9fb5559d`  
		Last Modified: Mon, 10 Feb 2025 20:09:20 GMT  
		Size: 4.9 MB (4906973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f248720e3d57d55d8c184b33644ff4459c20d48554e2287b4d64c8446aa2a0`  
		Last Modified: Mon, 10 Feb 2025 20:09:20 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8208b8ece5ba6f138e240805c084a351044c3579cef77c2ba13b1977565bb600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306600529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7808ff6c047e79142fb779204e2bf8bfb940284aa150573b581cf7d61e4b435b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:53:00 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
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
	-	`sha256:63067de277ccb20d99a5e9991dc66234bee83ce4c0d53f55d9f51995ad436f8b`  
		Last Modified: Mon, 10 Feb 2025 19:30:53 GMT  
		Size: 47.7 MB (47669546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e55e0b8b34ea5b3ba919ce4a6401eeba17103634f66be3d05c3f942cc693f8`  
		Last Modified: Mon, 10 Feb 2025 20:38:02 GMT  
		Size: 49.2 MB (49194060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a87368a8b3e2c19ca0da275e697427cacda83a642f1c6592f8267841818dc2`  
		Last Modified: Mon, 10 Feb 2025 20:38:07 GMT  
		Size: 209.7 MB (209736923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:635b541eeb1dc7a36482352dfde9648b3a3503be71213ff0db507e76d6d3551a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65fc93d3c597048ed3a0a00ca066d5bc140b4271517f740fc001f69c539cbb1`

```dockerfile
```

-	Layers:
	-	`sha256:4e9dbf554c095b9d512a5dba397ed5a5d06b7e4ceb345946bea62a25c2615444`  
		Last Modified: Mon, 10 Feb 2025 20:38:01 GMT  
		Size: 4.9 MB (4904735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c92cb165b5fe98a6cc219f17b94076e4e0c24e72b46474d977c48e51ef93d08`  
		Last Modified: Mon, 10 Feb 2025 20:38:01 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
