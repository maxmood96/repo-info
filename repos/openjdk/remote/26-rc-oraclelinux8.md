## `openjdk:26-rc-oraclelinux8`

```console
$ docker pull openjdk@sha256:a475e375f5d5a6f4830e21b833ca525483d3792a6a7745723fabd75e5eb4d1f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c45f06175c9b3e5de506122c99182fcee4d7b2e0892e74f9f05ced7f72f908f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294837691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89867a9831be28cb6dc33417b2c89a11a70ccdb27ed1b2049d8bf7ad457f3c3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:12:15 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:12:15 GMT
CMD ["/bin/bash"]
# Tue, 24 Feb 2026 22:15:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 24 Feb 2026 22:15:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 24 Feb 2026 22:15:33 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 22:15:33 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 22:15:33 GMT
ENV JAVA_VERSION=26
# Tue, 24 Feb 2026 22:15:33 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 22:15:33 GMT
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
	-	`sha256:4fe4181d5ea91e104cf8054d11c3c8e2b3c5a26a4d3f83f0203875483b68c5fa`  
		Last Modified: Tue, 24 Feb 2026 22:16:00 GMT  
		Size: 228.4 MB (228388089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d19eecb9163f4c1d0a4fb82ab665f138542a0510a0fcad85b390bd6d446fff75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd27e8259677f8aebc3503ce8142a0c2364e172efaab09cb79d4c487ba2b32eb`

```dockerfile
```

-	Layers:
	-	`sha256:a1faa71662819f1ecd45d732a469fd9d57a71999ddfb5c130f26a87c180f8ddc`  
		Last Modified: Tue, 24 Feb 2026 22:15:54 GMT  
		Size: 2.4 MB (2448638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d37f522abd3eb9a346171bbdca644ffda7109ec28f00561b03f2bac535a273`  
		Last Modified: Tue, 24 Feb 2026 22:15:53 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:221ef792bbee6bf8d414c834927fc531993298269d49a2ac067605bbc27a0449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292245698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c189c3c30d43f62f009d171b4760171087654b50e5dcc39e248bc5a485f360`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 21:25:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 24 Feb 2026 21:25:54 GMT
CMD ["/bin/bash"]
# Tue, 24 Feb 2026 22:23:28 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 24 Feb 2026 22:23:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 24 Feb 2026 22:23:37 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 22:23:37 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 22:23:37 GMT
ENV JAVA_VERSION=26
# Tue, 24 Feb 2026 22:23:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 22:23:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:308b2ffa0912bdff2bf3b77a5f2634a00c2761e38a51260adbdfe882bc668185`  
		Last Modified: Tue, 24 Feb 2026 21:26:05 GMT  
		Size: 50.2 MB (50199180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3b088c92189b7c9a43f00f3d7c9be2a9f603a29dbdbcf18124c983ef5ca83a`  
		Last Modified: Tue, 24 Feb 2026 22:23:59 GMT  
		Size: 15.7 MB (15700053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dfa2f844e2095152878cedf1b95097434e57792e525a55326553e0b7cf3c1c`  
		Last Modified: Tue, 24 Feb 2026 22:24:03 GMT  
		Size: 226.3 MB (226346465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:fca0326233f1f46cdac153a1543222a550bc296176b012785d7b93d548f940c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d004d992b7f6aee51ecdcf61882d6ed5dff8ed8028f7e182dec78a7a7ff1b95`

```dockerfile
```

-	Layers:
	-	`sha256:6174969b44c0757b888feca26f51316186d2bc6d7e78d8491bebc6a3ce0958ba`  
		Last Modified: Tue, 24 Feb 2026 22:23:58 GMT  
		Size: 2.4 MB (2447424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31321f3068564c8ab7079356f084a2ec8e1446714dca2a6f78dfd433c1b7d851`  
		Last Modified: Tue, 24 Feb 2026 22:23:58 GMT  
		Size: 14.8 KB (14834 bytes)  
		MIME: application/vnd.in-toto+json
