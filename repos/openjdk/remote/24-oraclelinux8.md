## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:ff44ab11fb8c70e8fd19066fa75338bf551965a64a9721552436c260870e758e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f91692a6af4cc4b368a632028ca59ba6ded57e80a97d2cb2ae135e596f27adb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279578624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127c6493e60731b0cf609b3570c2e841ca908aa5244dead6f5b4a8a51a17d212`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Feb 2025 19:48:14 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf5a3c7d8890a64c60d60ea38b6b8682451c6b3cd9ae69910ffebb43788bbd38`  
		Last Modified: Mon, 10 Feb 2025 19:28:36 GMT  
		Size: 51.3 MB (51276195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace3f3f5d7fb6d68e89d8966e17f9bbc014eb50fcf2bfea77965296d70559fe7`  
		Last Modified: Mon, 10 Feb 2025 20:09:14 GMT  
		Size: 15.0 MB (14987319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd4d9597f5db871bb5e7343cc0824aa48153ad9b0d9f199e863365952dcfb41`  
		Last Modified: Mon, 10 Feb 2025 20:09:17 GMT  
		Size: 213.3 MB (213315110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:656c546a7e9a499828229d840b4f74d34e8532d9704a500869a690e8feff9ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d0a7bca3a9dec8c5531f4e32196ea0209208e3de36fbb43544408c0ecba03e`

```dockerfile
```

-	Layers:
	-	`sha256:65d49555f42ffa223ae0ab4bb95068def29304c0fc5c3e87a4fb13e505b75426`  
		Last Modified: Mon, 10 Feb 2025 20:09:14 GMT  
		Size: 2.4 MB (2445351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7b9494749affde23544e99dbaa1068cf56cb792fb282ca00022106f78bda08`  
		Last Modified: Mon, 10 Feb 2025 20:09:14 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c378f8d727b846f3705f64576ad1c6e678d266722f47cf23ea849285ab6b34f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276916629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd7f2edfc69034eaa867639b9167b2ec324a63ee34171b2ec6ed62e0cfe961c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Feb 2025 19:48:14 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
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
	-	`sha256:e88397691f340af5a6fc9426d02cf3c24ef43c042f4cebceee15a0a17a46e911`  
		Last Modified: Mon, 10 Feb 2025 20:57:56 GMT  
		Size: 211.3 MB (211262939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e031894bf9f28ce35213fc8c4c130948eb4dd4c4b5d29d1edd55ef8f205d5d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8861ee441a3ad013289cd84ff1410a8ef59e0ea859c5037fbe026996623fd0`

```dockerfile
```

-	Layers:
	-	`sha256:68fe7bad9673df29d17a74e1acd9f4cef29372ce143cb9da82c86d1df6e0a0ed`  
		Last Modified: Mon, 10 Feb 2025 20:57:51 GMT  
		Size: 2.4 MB (2444197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7670d6344b6a796f04cddcc8f723746ab9130e2fee76be97cca00a9c56b1d729`  
		Last Modified: Mon, 10 Feb 2025 20:57:51 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
