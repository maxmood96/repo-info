## `openjdk:16-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:9584bb0dfb1edff6ce9c8802df1f44e91623bd1f4a1cfafecf10ee73bc262c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:9f0bc7799ca6519c6313ac740938acc86d6d64f241a454111aed729b51846123
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240064089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feffb9b7b8582ecbb4f97b0207824852ed2d4cfc6e2bd68e3d0d974059493890`
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
# Mon, 16 Nov 2020 20:19:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 16 Nov 2020 20:19:27 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Dec 2020 22:27:21 GMT
ENV JAVA_VERSION=16-ea+27
# Thu, 03 Dec 2020 22:27:33 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/27/GPL/openjdk-16-ea+27_linux-aarch64_bin.tar.gz; 			downloadSha256=7c667e8a1806b76ab4970334f7b4d88ea96860876cdd1566f9b1936dc03c5d85; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/27/GPL/openjdk-16-ea+27_linux-x64_bin.tar.gz; 			downloadSha256=dcaff2a2377fbf6fc3fc87e6d4ad1e73827f535c2bf7591c63a416e766f303d6; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 03 Dec 2020 22:27:33 GMT
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
	-	`sha256:479adf3ae32a7b08fb1722c8a1bd94e8d69cc2220f3b72084f40b528eea98a34`  
		Last Modified: Thu, 03 Dec 2020 22:30:57 GMT  
		Size: 184.7 MB (184747395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e47dd69ddd68cbbfc238a46841002626e07ae6c0af86d6a4a4cde7b282faa696
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234966000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1386aa3b41c7e568d41226a51f07c87b0a188623e1aadfc1354458e80e14a69c`
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
# Mon, 16 Nov 2020 20:04:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 16 Nov 2020 20:04:06 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Dec 2020 00:10:50 GMT
ENV JAVA_VERSION=16-ea+26
# Wed, 02 Dec 2020 00:11:43 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/26/GPL/openjdk-16-ea+26_linux-aarch64_bin.tar.gz; 			downloadSha256=1e2fefe414a16aceeae6816b4e48b426e79bb647927a44bbfe4d692156096e74; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/26/GPL/openjdk-16-ea+26_linux-x64_bin.tar.gz; 			downloadSha256=e74300f3f770122358d768d45e181d29c710e8d41bbc4ab8e492929f2867347c; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Dec 2020 00:11:45 GMT
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
	-	`sha256:c464ce8024c9cc54c2bb807a3b0d792271a6d1566a551480a6bcf7b96d662013`  
		Last Modified: Wed, 02 Dec 2020 00:17:00 GMT  
		Size: 178.9 MB (178923171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
