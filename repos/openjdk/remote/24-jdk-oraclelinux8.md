## `openjdk:24-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:ef1150035f473740e52e9a4e66d3b064a071dcfaa4281674568087c47ef884b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3e0e647c303955dbcb5fe410c3c32c590c077da3eaeae4fc3c18a166304ced14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279561875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16ceab6b51ff639e7167039e8ffe74a32bc77004db154c1e1a2dea7a5fbaa4a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 18:59:24 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 30 Jan 2025 18:59:24 GMT
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
	-	`sha256:b976166ae00f0fda8e12b934d92a7265904c082bbb675e0cb9bd4bbe93bedb30`  
		Last Modified: Thu, 30 Jan 2025 23:27:50 GMT  
		Size: 51.3 MB (51277963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f722755cb0bafed35b98ed85e4d99aad697196c067ade205f0fe490bac37a1e5`  
		Last Modified: Tue, 04 Feb 2025 23:32:59 GMT  
		Size: 15.0 MB (14975269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbfde12fead67e27126f45f59aa859f2d728c10ddfc1e94b773a7b058968874`  
		Last Modified: Tue, 04 Feb 2025 23:33:03 GMT  
		Size: 213.3 MB (213308643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8938dddb49bd987a9b1e350fa27d9475d368cc857ceeeb654ac6ea7790465f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f97e23cd7c92dae5be54160dd506cbcf81923fdfaeba74b0993396e165e36e`

```dockerfile
```

-	Layers:
	-	`sha256:351f7f753903fe10d5694b5579c4714f7adb7443c6a9367565458fe14bf36277`  
		Last Modified: Tue, 04 Feb 2025 23:32:59 GMT  
		Size: 2.4 MB (2445351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2d6a671978134af5e8171ce91783c20f42adf06a202c746ab283e089b99bd0`  
		Last Modified: Tue, 04 Feb 2025 23:32:58 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:69a639af4c485a770cbcb1b2a7d947b544ee1f35a9bf4e28eda1e15781591147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276878583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fffb5779ed8df61f18e7c8e8c2640373a49acd9f0ba3821ac94d64237f85fd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 19:00:17 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 30 Jan 2025 19:00:17 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 31 Jan 2025 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:48:14 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d49c0df93307a9bd06c9ca7b35ce6d068246a0938d0802933910b42574c173d3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/34/GPL/openjdk-24-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='ffab3ade32683a348fbb81aef96107b38545d1df7daa4e7ca81fe0f6775002ea'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bce860c27508f058f4bac6fca02fb3ef33ecf5c8331d2635b7c34a8b0af94e0`  
		Last Modified: Thu, 30 Jan 2025 23:30:11 GMT  
		Size: 50.0 MB (49984693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20da80e2bd804d65a47238fa85705492fc406b2b8cbad4cb1a153d9b26b0720f`  
		Last Modified: Fri, 31 Jan 2025 00:27:46 GMT  
		Size: 15.7 MB (15659413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679e17040834cc5dd67208c9a923eaa6831597e0d705d2029968c7a40806a0d4`  
		Last Modified: Fri, 31 Jan 2025 22:32:38 GMT  
		Size: 211.2 MB (211234477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:170a64d748849af71e8bce71068185853d55e771acfd1c1f9582dbed5cfb515c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34038f86c37cfda6b8285c6325b5643c1726fe80e71ee70dfe6bf11d21dc776`

```dockerfile
```

-	Layers:
	-	`sha256:fe78e42fafba7e30491a84d187568a58ed383640c2c9bd9447d0ff80fa59ff3a`  
		Last Modified: Fri, 31 Jan 2025 22:32:32 GMT  
		Size: 2.4 MB (2440443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d41b8c87342ffc442c847879c064dd6e1a1acd040edf59b8a235b14e6b10518a`  
		Last Modified: Fri, 31 Jan 2025 22:32:32 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
