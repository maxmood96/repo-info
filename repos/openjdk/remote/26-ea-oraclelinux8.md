## `openjdk:26-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:6f6c389b97ea83f6660f03229b453b6508fbf8a734755b56cb6bb6fd0f1e010d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7a699fd6baa85a4093c8e22f4a13183ff93f37addfdde2fd94bb38c9ebb55cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292448583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dc7f55855f240602cb312c55eccffe43f34e1623552afec476258ab5e28e14`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 18:48:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70e7deeb6fb1025fbac694ef1855ba75493ab45e96d46a5423af063e321cfd2a`  
		Last Modified: Tue, 21 Oct 2025 00:13:40 GMT  
		Size: 51.3 MB (51317328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7873a86a2a8b6bf6a74b81d06a7ebc594defca7963595dd6155f2a85ed12afaf`  
		Last Modified: Tue, 21 Oct 2025 20:20:49 GMT  
		Size: 15.0 MB (14989284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e8980ca86ecb9819a6e44a82d49c5aefc7b7eedb9266309def06a46fe0a871`  
		Last Modified: Tue, 21 Oct 2025 21:39:26 GMT  
		Size: 226.1 MB (226141971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7c6b7acaec9b3425a5a4301bd8d253688e41a8e6b9d972ae8285ed960d0d971c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dac4ced29ec6496b32dd2303aa743b2015809caf18054e92e3d55b9040e349d`

```dockerfile
```

-	Layers:
	-	`sha256:633992ba684fa0930912096b34b1eeeba826fe896d9c56e746e8fd9f4fd1d86e`  
		Last Modified: Tue, 21 Oct 2025 21:24:04 GMT  
		Size: 2.4 MB (2449882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae63426f488771769f7d56b44d55e8b8aae8ae22d34638aacd89128c127f425d`  
		Last Modified: Tue, 21 Oct 2025 21:24:05 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:81a0652a6d0f20e09933c933000afb173fc0a6e0c8af657e9ec502f5c0e8b754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289709035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3c0e3f5befd602dc7517e44ccf7e176b612d8219210dd61bca5fb140a91790`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 18:48:18 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["/bin/bash"]
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb2cbf1306f13796052df61db1ffdb76b5d1db3837223eec0859c6a0d6f6cdff`  
		Last Modified: Tue, 21 Oct 2025 00:12:37 GMT  
		Size: 50.0 MB (50043445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2baadf4b60cbaf11d0e3496b2d92c94a1c9ae00660674e4acbdce0a393ac09f`  
		Last Modified: Tue, 21 Oct 2025 18:13:50 GMT  
		Size: 15.7 MB (15663133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0ffcf11aef5e65ff2b3a2a163c70d36b68d298b9c1d82713ce676b4c5961fa`  
		Last Modified: Tue, 21 Oct 2025 21:42:37 GMT  
		Size: 224.0 MB (224002457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b3826f104ac647aab72549679ffbf1cf50e6b4f5b90eb93d6b78f49729312af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220a6ab3206499eb0d4f308457ce53a909bf76c5f195d681bcd192973019f48e`

```dockerfile
```

-	Layers:
	-	`sha256:370018be265e3e5a74a74c02ad6aaee208d14b9c8d77cc01abd42de6410602b6`  
		Last Modified: Tue, 21 Oct 2025 21:24:10 GMT  
		Size: 2.4 MB (2448716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1898ed3e9807616c75506ad25ae90adc72793b1058384e871d5125ac5e46d2`  
		Last Modified: Tue, 21 Oct 2025 21:24:11 GMT  
		Size: 16.2 KB (16180 bytes)  
		MIME: application/vnd.in-toto+json
