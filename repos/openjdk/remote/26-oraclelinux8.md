## `openjdk:26-oraclelinux8`

```console
$ docker pull openjdk@sha256:d02ff04a843617108ddf0db8112335ae759a5973b5edef1aab541cb84b51f13a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:13b3aa58fa38aac22c4be21b178921c5278439376c933d9b9ec1658b718181a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290081325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3718789650732f4df4a96e989abdb53af67c4aaa3c4446225f91e05d77717994`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
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
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4de16bc4730947e7bc3373b90e99cca123b3dca551031790db50d33b0feeb8`  
		Last Modified: Mon, 15 Sep 2025 16:58:07 GMT  
		Size: 15.0 MB (14979184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09501e0a5246cd80245f62e5a21ebcff428b758b2c768fe5e1322d4efa2cf07d`  
		Last Modified: Mon, 15 Sep 2025 18:41:36 GMT  
		Size: 223.8 MB (223778578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1b3d98879f8735e548b96bb4a6b9b9c18ba8d28caab49d6c634962d2248d31ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb3c7ba6de2838834cf77705d8f170dd9b6e70da2a99a7d30fa1e49d976b88a`

```dockerfile
```

-	Layers:
	-	`sha256:e69b19cf97c8a149d11c64465febd856283f42e306378065a38700799f0ef977`  
		Last Modified: Mon, 15 Sep 2025 18:24:31 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0feb14cabb79131e1cff4af41249b7fed57af8ecbe8ae600b0969aea892352`  
		Last Modified: Mon, 15 Sep 2025 18:24:32 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7062107edd93a59376a8313eb221840d42811c33afc0a63a05d76e1d954a564f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287349257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06df20676919e59b994ad2d7d539776ff87e5cb219aaf456aad1b3482e7d52e7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:9866c68be293aa81b529074549b7f38395dba71a8ea8fc528f721fbf8543b957`  
		Last Modified: Thu, 21 Aug 2025 18:57:24 GMT  
		Size: 50.0 MB (50039817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebfb48a360976f1f79f03ed76334fc0738149ee099c09cfcc466fabe532441d`  
		Last Modified: Mon, 15 Sep 2025 16:57:54 GMT  
		Size: 15.7 MB (15672287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d894335c4ae2647d4f1a5519ecf77381aee99b05280cdba03c08ac01781778`  
		Last Modified: Mon, 15 Sep 2025 16:58:01 GMT  
		Size: 221.6 MB (221637153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:237a742b5490ea859e8ba857d037a6ccac4fe0d88cbbfbb6c5a3548e27d7e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc88b11d5309066845775127191a058cefe255c6fea2938821e514f51f80fae5`

```dockerfile
```

-	Layers:
	-	`sha256:db9b884d1b9185fa196710fc4e77eb692aedccde9122072d42e69858b76299de`  
		Last Modified: Mon, 15 Sep 2025 18:24:37 GMT  
		Size: 2.4 MB (2449933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600da2f3183ec1cb8ce146286d13997055ffb387ef7d728be83c535cfca259fd`  
		Last Modified: Mon, 15 Sep 2025 18:24:38 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
