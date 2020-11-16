## `openjdk:oracle`

```console
$ docker pull openjdk@sha256:16b1c1005e18ec9e9ca1034eb59689e8e2136f627e8887f1276a63aa3506daa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:06bd36ad06e052ea3ec0cc18c971a2e514d57c7a80764d9469dc86ecb650dc4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251094936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f057dde245afb7b9289214141d669cb17ff21b99abad41ca0ffababf5833278`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Mon, 16 Nov 2020 19:37:29 GMT
ADD file:c6983fc83bb99ae9a8b343abf1e6852c64556f7c59e869f14f3f8835130d087d in / 
# Mon, 16 Nov 2020 19:37:29 GMT
CMD ["/bin/bash"]
# Mon, 16 Nov 2020 20:19:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 16 Nov 2020 20:19:26 GMT
ENV LANG=C.UTF-8
# Mon, 16 Nov 2020 20:20:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 16 Nov 2020 20:20:32 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Nov 2020 20:20:32 GMT
ENV JAVA_VERSION=15.0.1
# Mon, 16 Nov 2020 20:21:14 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 16 Nov 2020 20:21:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e69ec1c7b788c406991d1ce5f4a8f26a7ae9c0c9410d652237e2a6646ef53305`  
		Last Modified: Mon, 16 Nov 2020 19:38:51 GMT  
		Size: 42.1 MB (42053575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2259f1956e4980849285f91a1fd9fcc0f27002dddd076924e6801a2ae978db5a`  
		Last Modified: Mon, 16 Nov 2020 20:23:44 GMT  
		Size: 13.3 MB (13263119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5c7ae0cae52fe2ca4367d2f66cd46ade0cedbbef429266f702a4ef4a8b4bb`  
		Last Modified: Mon, 16 Nov 2020 20:24:58 GMT  
		Size: 195.8 MB (195778242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:07156e86090a503e9a8a4a6293c684588a159fc8323bb94f507e51211ae3ace1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230930304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15cf9375acadcc7a75936df60176e61edea1c43c3b5211edb4c459290545c44`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Mon, 16 Nov 2020 19:46:09 GMT
ADD file:91f2f5092142d551bd5542d693b0d6f9d6f9de47a18e19492b8db9dd24ef0786 in / 
# Mon, 16 Nov 2020 19:46:11 GMT
CMD ["/bin/bash"]
# Mon, 16 Nov 2020 20:04:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 16 Nov 2020 20:04:05 GMT
ENV LANG=C.UTF-8
# Mon, 16 Nov 2020 20:04:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 16 Nov 2020 20:04:56 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Nov 2020 20:04:57 GMT
ENV JAVA_VERSION=15.0.1
# Mon, 16 Nov 2020 20:05:32 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 16 Nov 2020 20:05:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74c8bc77d8380334fed77b152e6228e91ad4e881fb67a762337f88c14031e719`  
		Last Modified: Mon, 16 Nov 2020 19:47:43 GMT  
		Size: 42.0 MB (41982578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01f480947edbfcab3306d055a8959aa86cba86597ea1e29c498fa3fd689e7e4`  
		Last Modified: Mon, 16 Nov 2020 20:08:26 GMT  
		Size: 14.1 MB (14060251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6e98a2b7b4dbf76fa2199daa71043c6f525bb5079d2816332adcc87670e7b2`  
		Last Modified: Mon, 16 Nov 2020 20:10:29 GMT  
		Size: 174.9 MB (174887475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
