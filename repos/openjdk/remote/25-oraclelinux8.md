## `openjdk:25-oraclelinux8`

```console
$ docker pull openjdk@sha256:2f300b677c773c225e1622dace4d038632fc98af4ee7c294f8cde66a9d5e8d8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:19647a7ed11c1734492dde8a73e380d5980df26c246a184547b6ae27c7ab8875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289739589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2204045fd43469ebe8dc4d8a31a47d7cc1f3ac983ab6e3a3e118cc8d69653d5f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:42:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:42:18 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0915556054e5fcd1f04e454b0deedf305bb209616c5a72a8b2d83db9191e5115`  
		Last Modified: Thu, 12 Jun 2025 21:07:27 GMT  
		Size: 51.3 MB (51311558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7483e7edbd3b08762846e92dfa0b927397ca622419a13ca8c8b05bfb35e9354c`  
		Last Modified: Mon, 16 Jun 2025 17:51:33 GMT  
		Size: 15.0 MB (14979447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0626f3a8afbcbb4ee9878c82bcc9a60c1175c147b689ebc1f7b4bf47138c149`  
		Last Modified: Mon, 16 Jun 2025 19:24:39 GMT  
		Size: 223.4 MB (223448584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:84c2aac2f30addf8ea236328cb2a125a04dba659e8d98de6d449d9d38d8bf34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9af646e4c929c4c921198638c4a4acc4d1f0ef58e5d5e9da2a945ec91ba737b`

```dockerfile
```

-	Layers:
	-	`sha256:0abf8958375730703cb9243542ac4ec218754607445158c4dabec5a7cf19cd3d`  
		Last Modified: Mon, 16 Jun 2025 18:24:00 GMT  
		Size: 2.5 MB (2451706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635280559e2c886bae2c4f73339b208dc6ebca75368b56b7453e9a12a6b65df9`  
		Last Modified: Mon, 16 Jun 2025 18:24:01 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:01c64821586a74f4f56f8320c070399e4eca60d827bd6de1fae64c5b6a67ce4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284201796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27eb3cca4bf07538292c2efa493c62209acba6b3393fa4ee71fd4a7b122d087d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:43:09 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:43:09 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d998890baf088acce50ef79f8e8dc3eab36a2dc008c7774fa6e1e1140c89c3c3`  
		Last Modified: Fri, 13 Jun 2025 01:08:32 GMT  
		Size: 50.0 MB (50039112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cddf61b157a492a5e9e87c2aa66c8d9d39517125432aef6e1db78ce8635515`  
		Last Modified: Fri, 13 Jun 2025 00:42:33 GMT  
		Size: 12.9 MB (12917586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82249ba406a45af11f56f05aa5103439b0a084b514bc3cfba510a029d9a67420`  
		Last Modified: Mon, 16 Jun 2025 19:25:28 GMT  
		Size: 221.2 MB (221245098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:4655615ce39af046e0029afedbe5a9d389d3c993be227fdd4b83756964dc015a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7272376fd40501ba478b3569b0adb0debc81592f4dc6a29c49f464629b59aad`

```dockerfile
```

-	Layers:
	-	`sha256:ecd593deaaa3935fe80726062c81004b33fb2198175d58c2b2962d9b52ab5216`  
		Last Modified: Mon, 16 Jun 2025 18:24:05 GMT  
		Size: 2.4 MB (2436995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f7f69770c7bc7e40fabe7691e6e825289e9c61c3fee63349d2c692a9039a152`  
		Last Modified: Mon, 16 Jun 2025 18:24:06 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
