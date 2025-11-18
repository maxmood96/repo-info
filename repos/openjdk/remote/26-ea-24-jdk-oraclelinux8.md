## `openjdk:26-ea-24-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:52889726fc99895e39f11e8df955257abca9c098aaac78a1c08e47f2f8f5692c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-24-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f3b7de42ccb8de3efcdde095298889311a5c7c41f78152ecded23dc172f13b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294578358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ba18bdd3276f97165342da8afd3712de9d7d50553def7f5e990158233bbbf9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Oct 2025 17:25:39 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 31 Oct 2025 17:25:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Nov 2025 02:52:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 18 Nov 2025 02:52:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 18 Nov 2025 02:52:43 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:52:43 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:52:43 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 02:52:43 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 02:52:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fff3d29c5b5b28d342ba8d967679d9f76705eab0cf1b9c1c2a8d43102cc524c8`  
		Last Modified: Fri, 31 Oct 2025 17:26:00 GMT  
		Size: 51.4 MB (51383677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f95e3fc6fc6c03f8b545f4e555f7fb3c38ee1179d08492519d9957ac1063701`  
		Last Modified: Tue, 18 Nov 2025 02:53:16 GMT  
		Size: 15.0 MB (14997803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd99ca2cdc4359d356dc03a938950ec8ed4fa5f9a9d028ac6628e83f4390a5e`  
		Last Modified: Tue, 18 Nov 2025 02:53:09 GMT  
		Size: 228.2 MB (228196878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a5e10f198c66adfb3d9851279674c48fb40e754b7d319c6443ff5cc5c228be67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813ad86ce014896ce779487f15e255aeeb656347dbd1130f45241ef1c8bf7765`

```dockerfile
```

-	Layers:
	-	`sha256:b7680460079143051ff4167deb3962bf31b5a4378c7c586ac327e1d6517dce28`  
		Last Modified: Tue, 18 Nov 2025 04:25:41 GMT  
		Size: 2.4 MB (2448022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d168869d48ab6ac6ca3fca29b7fdc1877c6933e324f3c4e0aa4a8b8458d769d9`  
		Last Modified: Tue, 18 Nov 2025 04:25:41 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-24-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2867cceddfcefd8d684bb90ccc59c820478d47359cf9f256da000168472fc784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291805108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad51da11bb4a1b000f93e902f2420faf17c0dcfa43f65154f62a3440bbca5848`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Oct 2025 17:25:14 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 31 Oct 2025 17:25:14 GMT
CMD ["/bin/bash"]
# Tue, 18 Nov 2025 00:20:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 18 Nov 2025 00:20:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 18 Nov 2025 00:20:49 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:20:49 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 00:20:49 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 00:20:49 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 00:20:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:913708617406390e2c3446d7f989f45259d9e8bc8c18aeb2c7030c867ecfb5d6`  
		Last Modified: Fri, 31 Oct 2025 17:25:36 GMT  
		Size: 50.1 MB (50102610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bd08b81e09754a5d9902892a5a85b5fd45e5d858184ee26f7e3c6b40affb80`  
		Last Modified: Tue, 18 Nov 2025 00:21:23 GMT  
		Size: 15.7 MB (15663526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610d0c16f50cf4aa18df60bb30e41aab7491db20d36b994e8ff8ded7eacd0025`  
		Last Modified: Tue, 18 Nov 2025 00:21:16 GMT  
		Size: 226.0 MB (226038972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7a8abec8c0fa54291a166c3fe074cb577f4727157a3bdc2e091996530e75a984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd0d4ecb995e2fc04b7305eed8bd46ffd8a5f4c361d77fa72a21a2351ba664d`

```dockerfile
```

-	Layers:
	-	`sha256:deb90526f187a549a320125fb85458ca8fd2f299cf29a5f6a82804588fe00236`  
		Last Modified: Tue, 18 Nov 2025 01:23:46 GMT  
		Size: 2.4 MB (2446832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a79884e9bb4edc158eb81625f1ec7e5513acf00af2f5c10fcb95c67d4d0ebe`  
		Last Modified: Tue, 18 Nov 2025 01:23:47 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
