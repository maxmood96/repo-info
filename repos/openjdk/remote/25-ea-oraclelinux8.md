## `openjdk:25-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:8bcc19b73db84e63f7db50f95505f99e22e9fb8eb9a4ded5e6a0c002d3e31a90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:8d982bee3dbef80167c387aa084ea1a78f72d379b297379c70790f70c1b535ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278498226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf734583b818bcdf78f61437438d8180e414225146c6681c793cb9bbf34da62`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Feb 2025 17:31:06 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 19 Feb 2025 17:31:06 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07087e9c7fccbae68acd597cafa717397418263ef1da41fe5445a3d4776d1df8`  
		Last Modified: Thu, 20 Feb 2025 02:28:06 GMT  
		Size: 51.3 MB (51282175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182353ba993d549269878f6af6d118a426d52121aec21eb80ece1f047a8155a9`  
		Last Modified: Tue, 04 Mar 2025 21:57:25 GMT  
		Size: 15.0 MB (14976476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749df1772de0a52c29b6b67679e1ec34fc6370379b1cd59d5f50a6dbb2f229b5`  
		Last Modified: Tue, 04 Mar 2025 21:57:28 GMT  
		Size: 212.2 MB (212239575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c4e926c5b16a4f15d85a9ab618a9c272d1ac54f3a02e41ab16e59f83bff2f5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5badeae71ed6b0356e7dc0f1d7a80af2393fb5b295b603f4fd9e5e31829a85cb`

```dockerfile
```

-	Layers:
	-	`sha256:3d19cdfdff1a921ab37dcb8dc44c4c951dd6c9170f5e87e1af7a3496146fb8ec`  
		Last Modified: Tue, 04 Mar 2025 21:57:25 GMT  
		Size: 2.4 MB (2440969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d4150aeeda7fa9352577c1055231d667cd19e1486d840dc211736de4df8b0d`  
		Last Modified: Tue, 04 Mar 2025 21:57:25 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e4289d7a0ae09d6dcd15ad617e88ae49f2b98fe1d527543bcb35f0aabb61803d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275851835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4513dddbae57ea45d119f99654dbcc26bf17bceacea18ad5bc3e975795ae6d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Feb 2025 17:31:56 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 19 Feb 2025 17:31:56 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Tue, 04 Mar 2025 01:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 01:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='305d3cbac7f43dcb43c278417001c8759d9462722654a384d9f8a4182f095193'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/12/GPL/openjdk-25-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b950bcc42a84435edf559f93b411dc6f28c067bd78717b26a0195b692af4e20'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Mar 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:978d351c82d6622560a8ee00b3a217333d2e989aa95df7bcb554a799b63d5a32`  
		Last Modified: Thu, 20 Feb 2025 02:30:36 GMT  
		Size: 50.0 MB (49985763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20b66a0de13ad014c01f41cb19d71b7da9df4146e44920c3f1289afa45bf268`  
		Last Modified: Tue, 04 Mar 2025 22:03:16 GMT  
		Size: 15.7 MB (15671676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f6f8a673f10190ad9d63dbc3f2983e7926bf9535eb310d7d0ba37a2ca9de7d`  
		Last Modified: Tue, 04 Mar 2025 22:03:21 GMT  
		Size: 210.2 MB (210194396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8e5ba7bdf61141c6f27f5eedb86a28985e2393adcdb67c59d1612eaf01156ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d929f3b34c7f8b80adf7732778b3549f9aba9a1f8ecbe3cf760ab8542148b28b`

```dockerfile
```

-	Layers:
	-	`sha256:d29bf5ce69a06854e521ccfb7dc50adf61c75f942da36bfc42d831136e246415`  
		Last Modified: Tue, 04 Mar 2025 22:03:16 GMT  
		Size: 2.4 MB (2439815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54bc21171179c9bf78ff79702caa2e94784b6413086c5e5936f45d2c16c345b9`  
		Last Modified: Tue, 04 Mar 2025 22:03:16 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
