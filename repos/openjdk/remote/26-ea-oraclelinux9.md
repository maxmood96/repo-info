## `openjdk:26-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:1d61e28cd5947f72e3ab07d9bed131d5da35b298c28cb33aa6e0be0b5d3b72a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux9` - linux; amd64

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

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

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

### `openjdk:26-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2e157edc9b0eb4f2def59c9cdbd5fb1089604122e1d68517665734cf3d656c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307780096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6066d45d46f81ac53132e0619f3de33f6e1ec0ebf503ac88e057ed69953cd53`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 20 Sep 2025 00:48:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["/bin/bash"]
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 20 Sep 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Sep 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+16
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='87ee3d9cfd07f66858b6e519b07d2f23375fb1c1827faeebce6580c31045879f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='116ea44265700afbfe2c15b751ef9e34921fa449663ac0dfb439adef9db9c379'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7ced48bfda3c88462c42fbc52f44e23314673e78a25a1ac9998494789919ca`  
		Last Modified: Mon, 22 Sep 2025 22:11:08 GMT  
		Size: 38.5 MB (38490225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e8ae45614697f1763ba9a45df2879272de94e33ada887f42c34f3115f2fb85`  
		Last Modified: Tue, 23 Sep 2025 00:24:23 GMT  
		Size: 221.2 MB (221201574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:34d9c76b01991c7e7f45cc3fbb64f7800b6af1706ffe45c89c7b031f9dbfdb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9c7b725229cd5559a84392d18a3adf316bc8033d2c39d2546c923bd1d837f7`

```dockerfile
```

-	Layers:
	-	`sha256:95bb26bfc9be2c62d26277a23d6a1791cd7f013d76d63cdf1909d10183ccea3a`  
		Last Modified: Tue, 23 Sep 2025 00:23:27 GMT  
		Size: 3.6 MB (3638499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881391057b32f455b1fd55e4d5b55cbb09fec6eb203a1b00e624176780421afe`  
		Last Modified: Tue, 23 Sep 2025 00:23:28 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
