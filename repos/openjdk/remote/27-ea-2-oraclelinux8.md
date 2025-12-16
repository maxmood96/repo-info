## `openjdk:27-ea-2-oraclelinux8`

```console
$ docker pull openjdk@sha256:1c7665fa47bb654d3330335542ce722d4b40ad450c90c4b8e270b21a73ab41eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-2-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ad775af7d610ec1574d75af4c5869100ac5e5400f3a41974916be208de4c5026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294844504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09012bf09104ff22a0e097dbfe6aa20ecfb5939462666c3ff9027da614f709c7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:50:37 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:03:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:04:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 16 Dec 2025 00:04:01 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:01 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:01 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:01 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b436d89f13c92f9703618820d992b4e1f2b38ba243024b251c81a610f04c67b1`  
		Last Modified: Tue, 25 Nov 2025 23:51:01 GMT  
		Size: 51.4 MB (51378078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95769401666213eb38f9add13a5ec9747802ba0c7139c8d7651cf9336bf4443c`  
		Last Modified: Tue, 16 Dec 2025 00:04:36 GMT  
		Size: 15.0 MB (14999259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e228616008aa23361bc4f0551441f9fa95572f1363bd03733ffe403a5867329b`  
		Last Modified: Tue, 16 Dec 2025 00:05:16 GMT  
		Size: 228.5 MB (228467167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-2-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b826187c9e4fb4f7db1e0be493a4de5051d5d4c1043c6efc0af3661213e386bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cc82905d50a29e0fe51fb5f8263626e6d8e37ce937cea0604ac4d9179ccb82`

```dockerfile
```

-	Layers:
	-	`sha256:1bc4d206dfaf295d229a5e8f13315cd6e5cec7d04245a944a4871b084c467dbe`  
		Last Modified: Tue, 16 Dec 2025 01:26:11 GMT  
		Size: 2.4 MB (2448003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa750e258b60c8e736198a5780656b438181f86772a0897590d3b6c59eaed3b4`  
		Last Modified: Tue, 16 Dec 2025 01:26:12 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-2-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:de3d12733b3b56d1d5b71fa5295fda841b255241b1d2ba3becf29e41a418eef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292203316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d82d1a57530f1aebfc6e25fe479f4120e7c1396d2ef67d376612aaf5870f2d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:37:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:37:54 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:04:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:04:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 16 Dec 2025 00:04:30 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:30 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:30 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:30 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:674388ef21c06396c4d40407ba2af1c3a42c30a5cb162fd4355950be7600edf7`  
		Last Modified: Tue, 25 Nov 2025 23:38:20 GMT  
		Size: 50.1 MB (50103076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2e17b516cdf5e841a3e83ccabd0b7900e739b517de3c4269531d7df21c2176`  
		Last Modified: Tue, 16 Dec 2025 00:05:03 GMT  
		Size: 15.7 MB (15691649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d678f69cbfc15c50d686b52fd9a748719aafa1c6aa74e0c5c706609a248195c`  
		Last Modified: Tue, 16 Dec 2025 00:07:02 GMT  
		Size: 226.4 MB (226408591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-2-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9d28799aebaf0bd220465391cc7f6c3c85e26040dc2a2e7a171aed096f1deb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20503af4991081210a1b4392e67d8161ed38beca7125df5e65ac6afa2ce9e9d`

```dockerfile
```

-	Layers:
	-	`sha256:d43377b3348ff394ec98e8c0c353e870baa84c892eab0691eccca99263f245dc`  
		Last Modified: Tue, 16 Dec 2025 01:26:19 GMT  
		Size: 2.4 MB (2446813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98a21f2ba50830ed04fff05fcc251cfb44c206b56ef538d78cdf2781cb5cf2b4`  
		Last Modified: Tue, 16 Dec 2025 01:26:19 GMT  
		Size: 15.4 KB (15444 bytes)  
		MIME: application/vnd.in-toto+json
