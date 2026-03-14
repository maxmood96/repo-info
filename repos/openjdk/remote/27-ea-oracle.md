## `openjdk:27-ea-oracle`

```console
$ docker pull openjdk@sha256:9f791f1e2ac4836dceb92c21a42a7a2d4e730141436fca18fa795c0c5e674421
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:b55bd2c50e134a707b04e5e8f4354fa4a8cf0e46485f69255ec7f6e7d844fca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314018445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9883cd9d9be718dc03106a2c4a20fa4ca77a1528a5c7a91a8af1404b494689da`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:13:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:13:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 13 Mar 2026 23:13:17 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 23:13:17 GMT
ENV LANG=C.UTF-8
# Fri, 13 Mar 2026 23:13:17 GMT
ENV JAVA_VERSION=27-ea+12
# Fri, 13 Mar 2026 23:13:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Mar 2026 23:13:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19963c898cfd3dd849a50a1be10c95ed60b7eabef4f980da61f0c38a1805e5ae`  
		Last Modified: Fri, 13 Mar 2026 23:13:41 GMT  
		Size: 38.3 MB (38297059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43be1159af622e44ad2b8eaacd0bf3701e121ca6fee84152234b038ca8997ae4`  
		Last Modified: Fri, 13 Mar 2026 23:13:45 GMT  
		Size: 228.4 MB (228417176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:feb7b5e86306c51c0496e40b573ab2516861a7bbd6820a85086ef27acd6fac15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66936b2074f7d4791c881f4d6a5eb930fdd67bb78e5207032ad2ded2831da11c`

```dockerfile
```

-	Layers:
	-	`sha256:4307867cad64f1c40345a8c580254c7863edd9e4fbc9019921ed07d6c1e3541e`  
		Last Modified: Fri, 13 Mar 2026 23:13:38 GMT  
		Size: 3.7 MB (3655443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c339b5e7b3e571a7e3e89432ff6f5c094f1ca8d4ab81c00c153e12df2a5df0e2`  
		Last Modified: Fri, 13 Mar 2026 23:13:38 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:889c1bc7e4376e5d0b0bdd6cea94082bab87c7f8c81da7e455d5596f9c5433fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310962823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb8563b338d517f64f7172fd0263acc4902a8581a625956aaeb569ee9e86f15`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:12:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:12:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 13 Mar 2026 23:12:14 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 23:12:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Mar 2026 23:12:14 GMT
ENV JAVA_VERSION=27-ea+12
# Fri, 13 Mar 2026 23:12:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Mar 2026 23:12:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9090277a63d33048b52571c08e664efbdea827ab322526c5ebbf44f78f3d1d6`  
		Last Modified: Fri, 13 Mar 2026 23:12:37 GMT  
		Size: 38.7 MB (38695442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab4939af86f86bfad95ef9849a1ecd381f710083b44fcbf0b02e3a196376721`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 226.4 MB (226367195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6803df034679558d0fc30110967c31922b4faa50898148cfbc6885e8c671d014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8d72a5d0ac763640c94edef3ae14d27389f0b769837780fb6d9d6c13fa4264`

```dockerfile
```

-	Layers:
	-	`sha256:90412a76004ca6bef10b02f501300ed74c9dc259eeb6dfdac4016d1641631395`  
		Last Modified: Fri, 13 Mar 2026 23:12:36 GMT  
		Size: 3.7 MB (3653133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f8e6e1590e45f5b28240df085eb0fc091e4f6745b90f91ca946c51a0e01803`  
		Last Modified: Fri, 13 Mar 2026 23:12:36 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
