## `openjdk:26-oracle`

```console
$ docker pull openjdk@sha256:76cd2fe5bf0c2d03105b466e931809bec1b567fb9314a28395c928143049a9f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:5108149da74cc1ccaf37f13fa66b095cb2f2d697e2f4dca8ce9678581c420d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313240347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151ffd8225e54fceab42a8caa7c5fed7045441c714bd0582857ac939e98c7b1d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Sep 2025 21:47:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 21:47:11 GMT
CMD ["/bin/bash"]
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:806f49275cbff8773a3d3cb9c7e11efc00cbe434b66b9896fdad5064c4cb5355`  
		Last Modified: Mon, 22 Sep 2025 23:40:59 GMT  
		Size: 49.5 MB (49496996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8960df118c2b230a985e449210da36accb69a2746c9912a6b5edb6977dccc6`  
		Last Modified: Mon, 06 Oct 2025 21:05:17 GMT  
		Size: 38.1 MB (38082909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4d74d55f22604847d0ba3518f825d70b7dcfe930176070c4c82f95f5571b8f`  
		Last Modified: Mon, 06 Oct 2025 21:05:09 GMT  
		Size: 225.7 MB (225660442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6ce1522cca9e70e92eb3d90056ad55005c9649a2199c0568720f212367931bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81406fb806c61989ca4c9e013358bc880da5a3c55f0ed21b1ef496cfc00c7384`

```dockerfile
```

-	Layers:
	-	`sha256:6e1275d633fd63ac965e1616c71795f757cccc9f1c884b5fc81db3219fba473e`  
		Last Modified: Mon, 06 Oct 2025 21:23:21 GMT  
		Size: 3.6 MB (3640737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88085107e59f8b3544aa85dd482e8fecfc99e9662879dd10ea1d78b3ae7089b0`  
		Last Modified: Mon, 06 Oct 2025 21:23:22 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:035de73af39905c478efd641c41c8ade4fcbeef7d5bc50a59860bfc267e00db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310097754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0a0e1afbf36566a0c97ec0dd7a05d6897244c5d36abbd1e690b4594fbc7bf6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Sep 2025 19:54:28 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 22 Sep 2025 19:54:28 GMT
CMD ["/bin/bash"]
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecb83b09a418867c3572bbbf142e6346af9e39d392d18d601ecc594e5a1edcb1`  
		Last Modified: Mon, 22 Sep 2025 20:46:25 GMT  
		Size: 48.1 MB (48088297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a949650dafc78b81dae1f25e40a9eb944a24b7ead3b8dc846488235591de7a5a`  
		Last Modified: Mon, 06 Oct 2025 21:07:34 GMT  
		Size: 38.5 MB (38490334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275c3d6d6c5a9d98e31ce63f820b1e132400861db754e1ac38b476572d2cc45a`  
		Last Modified: Mon, 06 Oct 2025 21:11:03 GMT  
		Size: 223.5 MB (223519123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f17ff307839acf12a280ea9dcde4b8f3b17e24f7017f8cb6ab91271f638e72ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11d1b186179982f3280b0e81eaed3decd0907a61a1ea74e5950c539df1efe56`

```dockerfile
```

-	Layers:
	-	`sha256:b1f33e4eafbcd454542458caeaa0cb8ff2c473cdb431e8e706fc65f5742167d5`  
		Last Modified: Mon, 06 Oct 2025 21:23:26 GMT  
		Size: 3.6 MB (3638499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc8d184b29021275424a731172fb7f4d03bf56074f8a9bf7be68ad000201042`  
		Last Modified: Mon, 06 Oct 2025 21:23:27 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
