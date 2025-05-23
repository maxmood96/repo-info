## `openjdk:25-jdk-oracle`

```console
$ docker pull openjdk@sha256:3ff3ffbd097ad53d6e530a5a8476fe697dcad6f532705a623f5325d42ec06cbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ab5ad86b0880c56c186268f109361556fb765d76e2748e712ab57e0d1e27e670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301068532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1cd2d23246c5f5429871c5530e5f34400e3d28103eaaf46619c073337fd292`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:26:20 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:26:20 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2eb5d06bfeaafd2195d3612935e86f925a4620bf5bbcea5112a1fb07138dd80`  
		Last Modified: Tue, 29 Apr 2025 18:16:07 GMT  
		Size: 49.1 MB (49093011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b09137eff7817437c560700a8a51242fadbfbe748c2f4dcd9580f3533aa181`  
		Last Modified: Fri, 23 May 2025 19:55:32 GMT  
		Size: 38.1 MB (38104974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0eb8976d7d79bb41095d7d3e5adbdea912c7411acc5341d20c017fb82dec969`  
		Last Modified: Fri, 23 May 2025 19:55:36 GMT  
		Size: 213.9 MB (213870547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6d6dc2bca517cae8ce9b781c098092ff1d0f61c18d7602df326ae179a6e35af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3655707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f896b7cd6465fd5d42c4d6c646e641dabec74fa899665db6737fa6c9c5f10f42`

```dockerfile
```

-	Layers:
	-	`sha256:f8a888fe018fafd38f23ccb2d14c8af29c410cb558e88b8f75e9f95195e22667`  
		Last Modified: Fri, 23 May 2025 19:55:31 GMT  
		Size: 3.6 MB (3635962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:831efd9d668737b6de9291abdad935f8e2a9c6e755ad47c3251454b41db1e33d`  
		Last Modified: Fri, 23 May 2025 19:55:30 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:718c8bc57c88162b5cbd2badb30be33354f61efc8c8806984629c560b4a34add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297821007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a5551951ebcff0f5b82d67b02ff312ca44e593e2b7d17de230e76883c58be5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:27:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:27:11 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88a33dc8906274baf54eb28aeefeba84c17922e3854e6fd41883f273d87d330d`  
		Last Modified: Wed, 30 Apr 2025 01:59:51 GMT  
		Size: 47.7 MB (47672989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b5aea1d0deca854a3762f4e396dad66260211f50004210a8e73e2146af926a`  
		Last Modified: Wed, 30 Apr 2025 07:05:49 GMT  
		Size: 38.5 MB (38500810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae61dea71fffe97960c73585a14431b92aeb8e3d0f74c61e9a499ab3366f7e2`  
		Last Modified: Fri, 23 May 2025 20:04:53 GMT  
		Size: 211.6 MB (211647208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:42c48aecad577143b5593b52e62f6ed8fda58cca5c2025fe928073cc08dcb27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3652212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4e4f05548fd39e47a7e8d455e94529214c78ae6606f493c05c242b5b0481a2`

```dockerfile
```

-	Layers:
	-	`sha256:81420903c791a9b18101760879bbea835cd28a5e197ea9ff85df2cd0902b8046`  
		Last Modified: Fri, 23 May 2025 20:04:48 GMT  
		Size: 3.6 MB (3632180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8facc4c9716470d239ad620d6bfcddf1abbd560c117192e4ec115d9fdcc0abf6`  
		Last Modified: Fri, 23 May 2025 20:04:48 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.in-toto+json
