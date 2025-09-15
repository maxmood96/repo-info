## `openjdk:26-ea-15-oracle`

```console
$ docker pull openjdk@sha256:856ae6c5180dc2c5db19580804b4458a5802f15f42b10f113ee9dbee2073bf73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-15-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:83b9787d68da5108d6e6d3fdbdd5ebe20ec2875682cca7e8d80bb8ec05480cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310818152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79e79da933f7f99a7ed9dbe724c4335338b9c53e920f5cda6971cdc48039fc5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 12 Sep 2025 18:48:17 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 18:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_VERSION=26-ea+15
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d8fa7cffcc38d68ed218fa285958e163c48a9b0d5c968c0c8859cc0a36e0baa0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='955e3af91d63b89cb5eecc00503ca439d96a9d2cf645e38e4079ed65c5486ff2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:500d7b2546c4e2118109493e62a416f6e12fe0670ed784ab0a5ada2787573be5`  
		Last Modified: Thu, 21 Aug 2025 19:08:06 GMT  
		Size: 49.5 MB (49497016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad565c767b0d0d1e9413ddf64fd36001f66e573ae52e6ecfd9db134ccf36741c`  
		Last Modified: Mon, 15 Sep 2025 16:57:40 GMT  
		Size: 38.0 MB (38007343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745697cda05628f84bb70d792f6c2fe6013dd40d3a66a7e45583f84b5287e4d3`  
		Last Modified: Mon, 15 Sep 2025 16:58:33 GMT  
		Size: 223.3 MB (223313793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-15-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:00a9363bd6542995dba9858be8a446325992f6c44add9d6484cf0c1cb4fa8418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73980e4fa5afc72786a8f0f22c23eb27c114ca5f859167b29328b30d246388`

```dockerfile
```

-	Layers:
	-	`sha256:ff5a2842697d21cdb68d263b1b0b8cdec65eb3ee3778819d38146da122d9bbda`  
		Last Modified: Mon, 15 Sep 2025 18:23:53 GMT  
		Size: 3.6 MB (3640729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4eb6414fd513ff101b56fbb389f9458703f988c7d52d01f09ebe004dee138f8`  
		Last Modified: Mon, 15 Sep 2025 18:23:54 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-15-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2c44c30c3e211bf8833a483b9f7e0b2f29326c91d6d83ae27ad3bc7c301fb45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307661087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6415187908b55b335b9ed49c297b3acb0bc82ef5be04675caf40395064e50c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 12 Sep 2025 18:48:17 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 18:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_VERSION=26-ea+15
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d8fa7cffcc38d68ed218fa285958e163c48a9b0d5c968c0c8859cc0a36e0baa0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='955e3af91d63b89cb5eecc00503ca439d96a9d2cf645e38e4079ed65c5486ff2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5e369658cc0fdedce73e0479a85cd17ba8a09435fc3b21f6afb7e0d4783429d`  
		Last Modified: Thu, 21 Aug 2025 18:56:13 GMT  
		Size: 48.1 MB (48086723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2cadef76f612df1bfeb4e0ea348583e29066bfdd032e8069f332320ac2d57e`  
		Last Modified: Mon, 15 Sep 2025 16:57:39 GMT  
		Size: 38.4 MB (38411145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66966145c534b99e816b59d9df89ba01ebfe4186bad22ddb2f28cc0faad0542f`  
		Last Modified: Mon, 15 Sep 2025 18:25:31 GMT  
		Size: 221.2 MB (221163219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-15-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9abb0d5e7b8e97538a90ad7b108610a787180f3f2619f2120ddf7f5379a33a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b3766fef517f232b558740290c42e79930b7f08c1415644c3b19dbf55b42eb`

```dockerfile
```

-	Layers:
	-	`sha256:bdf3d46b850dc8f3d124a7499a0c1e245f551988379010e723f9b47d48910fdb`  
		Last Modified: Mon, 15 Sep 2025 18:24:01 GMT  
		Size: 3.6 MB (3638491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02cbcf7fafafc9d8ae9c45a476d3ee8c6d7b9b54dc98084d9da95b8c14a1ef5b`  
		Last Modified: Mon, 15 Sep 2025 18:24:02 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
