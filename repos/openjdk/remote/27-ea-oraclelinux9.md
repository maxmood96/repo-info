## `openjdk:27-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:606051fc1db2a3074c5798e5a7a743c57ebc3ded32b140364d41262941e9d1e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:eea1ccef564cd0e126101c49f559d930ac65e9c5df2040fdd50d7c53a10b5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313835437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5aca41f277bf60d05427282e40dae5ddffe26a0343a8ff618fcb340376334a4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 22:11:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:11:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 26 Jan 2026 22:11:49 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:11:49 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:11:49 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:11:49 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:11:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca5ec52900c47e04ce91efb280aeef445af57f0045255ebff2c015347d2bf61`  
		Last Modified: Mon, 26 Jan 2026 22:12:10 GMT  
		Size: 38.3 MB (38296468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ab52a7136cd13fb35af48655577a5c75e23cb1b14063fe4d3e3353f19061bb`  
		Last Modified: Mon, 26 Jan 2026 22:12:14 GMT  
		Size: 228.2 MB (228225421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:88dde1f1fb9a49b797b8767657802d5d4ab86d893e9ef5301e080e4a56b7e725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92a273b06d07c575a328d49d1cde9362bec6e6ad121d9bab3c0f9bc314b4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:ee6cd789ff4bd1f9f0cfaa19af2231661cdc8ded56ba2edc5ba1da86d071c021`  
		Last Modified: Mon, 26 Jan 2026 22:12:09 GMT  
		Size: 3.7 MB (3655359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b4e6b93cbd9172a4d57deb43aebca8159ce8c7a63de8f9f5f026cf5b17c16d3`  
		Last Modified: Mon, 26 Jan 2026 22:12:08 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8a19ddcc5ecc68f1f932d9c77b00af84de5eb28947672869a428dde1b4fc5d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310750005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2705d607bd384b9eabb07aaca8f219f9950e5dab090212871b72ccb73fdb42e4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 22:10:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:10:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 26 Jan 2026 22:10:55 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:10:55 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:10:55 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:10:55 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:10:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ed60f0093ebb545ea3ec474fd492977af3e25cb518ee3a3f00438b46d8897d`  
		Last Modified: Mon, 26 Jan 2026 22:11:18 GMT  
		Size: 38.7 MB (38699651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf487714f7623c8cc56a7c6e74159a39af5914ad17478f23fda960ece90ccd`  
		Last Modified: Mon, 26 Jan 2026 22:11:22 GMT  
		Size: 226.1 MB (226148444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:fc3a783fafb48077612e9fbde5f4f1dc87880b0d2db693deccf18126f040c5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb61e88edc2fc244fb56a8a22046d2ca74faa1b33a57c8f7166801aecd715b5`

```dockerfile
```

-	Layers:
	-	`sha256:176ea8504218421ad0ebd3087fb6dad686168fa94baaab99df24e1f54bf1ff57`  
		Last Modified: Mon, 26 Jan 2026 22:11:17 GMT  
		Size: 3.7 MB (3653049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590afeaf8d6ed2fbd36aefde3ce46078aa2789ba24cb7465e4e85d73b890ba54`  
		Last Modified: Mon, 26 Jan 2026 22:11:17 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
