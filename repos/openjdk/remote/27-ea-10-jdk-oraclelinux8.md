## `openjdk:27-ea-10-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:8807b68a1404f52f5f3c55a00d6a632774bcc9999a93b9e095007f13bd579bba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-10-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c1462f83da95d0f391c4faccae7b69b8e632c3f9e1073931f4371ce07509c88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295281043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca3f1ca40c322f762797a09ff07f9a50d359732a9bc53072c60c1110f13cb31`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:12:15 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:12:15 GMT
CMD ["/bin/bash"]
# Tue, 24 Feb 2026 22:15:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 24 Feb 2026 22:16:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 24 Feb 2026 22:16:16 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 22:16:16 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 22:16:16 GMT
ENV JAVA_VERSION=27-ea+10
# Tue, 24 Feb 2026 22:16:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 22:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:910e0c7025a94af1bf4f9980abe31c6c0541dbb5c579f5a09497c1a5d667c578`  
		Last Modified: Tue, 24 Feb 2026 21:12:26 GMT  
		Size: 51.5 MB (51462874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be180aaf3a1dafacd71690730fcd2b92d75f576eb04cfe548ae410060787eb0e`  
		Last Modified: Tue, 24 Feb 2026 22:15:54 GMT  
		Size: 15.0 MB (14986728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3c6e6f214461667e1aa56241351831db76d45c86dea12b5794245bf0d485cf`  
		Last Modified: Tue, 24 Feb 2026 22:16:40 GMT  
		Size: 228.8 MB (228831441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d149b821e895f7400b49e29ad078f80b3e3c97108e720f3bb172f7e8c02f8e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cff81afcb4ecbbd6d869b59d71f99dbfbcc9e41554041e90ecefa216af705b9`

```dockerfile
```

-	Layers:
	-	`sha256:bd23168afd772ff1e82200d17ad526d536f65105d8d2a4f16cf9a48c8dc86c1c`  
		Last Modified: Tue, 24 Feb 2026 22:16:35 GMT  
		Size: 2.4 MB (2448696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c047be355fa293be056dcb22308ead70a81334be1e8fffc3df41d801feafef`  
		Last Modified: Tue, 24 Feb 2026 22:16:35 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-10-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4150b5d8d60a402e71db92714a5e4d813317300de4a1e7cee27fbe289434a4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292715913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2dd9c73d64f7f1d27f1f6fafa592abfef6416e614544597fe65500d3da0cf4c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:25:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:25:54 GMT
CMD ["/bin/bash"]
# Tue, 24 Feb 2026 22:23:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 24 Feb 2026 22:23:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 24 Feb 2026 22:23:39 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 22:23:39 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 22:23:39 GMT
ENV JAVA_VERSION=27-ea+10
# Tue, 24 Feb 2026 22:23:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 22:23:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:308b2ffa0912bdff2bf3b77a5f2634a00c2761e38a51260adbdfe882bc668185`  
		Last Modified: Tue, 24 Feb 2026 21:26:05 GMT  
		Size: 50.2 MB (50199180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f82bd92409231f4765a1af699d12aa3e1fa5f5b569ddcd1b74d8cac3cb8a4fb`  
		Last Modified: Tue, 24 Feb 2026 22:24:00 GMT  
		Size: 15.7 MB (15700120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246889b21682e59ee5dbf3dfbe328be8bb635a7bb626be0990b533fcd10478b8`  
		Last Modified: Tue, 24 Feb 2026 22:24:05 GMT  
		Size: 226.8 MB (226816613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f1d5a67c8226ec9ac903929249230916122cd8b335bb2224544b278d20e9907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fc7606d306eb935bf51dbcd63e5ab42d7d64321e4b55f276007cefd16a733d`

```dockerfile
```

-	Layers:
	-	`sha256:be1313adac159981b9cf6b3f724e636e357eddee72231d2ff1c84197a643d56e`  
		Last Modified: Tue, 24 Feb 2026 22:24:00 GMT  
		Size: 2.4 MB (2447506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab9d390922ed55b9c60ac08d883e105fefafa6a7139b3c4fa64a9dccdd8544c`  
		Last Modified: Tue, 24 Feb 2026 22:23:59 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
