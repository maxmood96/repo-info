## `openjdk:26-ea-26-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:8bdddd7312cfdfeff2c2e9c4d5372dfb32f0cd09f3b8fe6b5ed8a2478418433a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-26-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:e551dca3424b8d315c43ce547600ccd402cb132a7ca62028140ba594ac92d751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313228083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923b7a63fce630d647766fd557b4ec34e0544946305b61b01510753eef6133be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 01:08:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 01:08:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 02 Dec 2025 01:08:33 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:08:33 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 01:08:33 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 01:08:33 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 01:08:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c62b7a94006ee51ec5083e9c1fd89f197714677d2bd53086cf1b227ed8577bd`  
		Last Modified: Tue, 02 Dec 2025 01:09:27 GMT  
		Size: 38.3 MB (38298489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac5abdc2b9c8e1f438155de32c03ad06cf2e07eecaeab886452faa156f255cb`  
		Last Modified: Tue, 02 Dec 2025 04:24:11 GMT  
		Size: 227.6 MB (227617420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-26-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:a153b342d338be31a21bc29c79260674be7cf4f19273e39d2e457f3a5dd79412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593bcb2af0e761fc3028633c78d2ac567a4a943b20e6ec001b517b6366eaee57`

```dockerfile
```

-	Layers:
	-	`sha256:3146c67f37678eef63d5c314ada26f33203721455d23e4e5584d54484677b5e7`  
		Last Modified: Tue, 02 Dec 2025 04:23:28 GMT  
		Size: 3.7 MB (3655335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf5e0678f4c6270e4245e9c3e33b42df3d998b5f1ef9ade1462fc42550bc50f`  
		Last Modified: Tue, 02 Dec 2025 04:23:29 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-26-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5b719da9a6a93d54947cc8e65e29557642fbfce5a69c16ecddde8426fd577917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310134048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb20d50249496233ddd43f8a99edd8a394aafc94d09c6e9c923fe4c784e16c8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 02:32:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 02:32:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 02 Dec 2025 02:32:39 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:32:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 02:32:39 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 02:32:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 02:32:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91605a62d6e12b816a855308c55c223c85a90ca71e4f4268eeae02ea353d13`  
		Last Modified: Tue, 02 Dec 2025 02:33:16 GMT  
		Size: 38.7 MB (38699716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc64a72146da61906a2b292835f54e14a1bad12d448fb222baa57fe205c2bbb2`  
		Last Modified: Tue, 02 Dec 2025 03:48:35 GMT  
		Size: 225.5 MB (225537355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-26-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:403091159ad220de93b6885b2e78d60b9f65580ac1f135b843f982eff406f9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f270c5780574977ed773e97bdf80034b1fadec99b081f79a6ae388d13e4333d`

```dockerfile
```

-	Layers:
	-	`sha256:d445388cd64c9dbd27248948118a79cf3c59d0f37a5352bf5b6f83a5012a2183`  
		Last Modified: Tue, 02 Dec 2025 04:23:33 GMT  
		Size: 3.7 MB (3653025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1034ff4508a0bb680901ac463b5349ad0d92e3cba5c19468acec697fc348d8cc`  
		Last Modified: Tue, 02 Dec 2025 04:23:34 GMT  
		Size: 18.1 KB (18053 bytes)  
		MIME: application/vnd.in-toto+json
