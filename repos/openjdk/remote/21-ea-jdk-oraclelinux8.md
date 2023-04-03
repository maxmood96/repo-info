## `openjdk:21-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:c66a705f653e2003b658963ac2de605c984d2b9a509b1e0bdadbe6f9cff68ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:be837a5f4d3849ab9fb9a4cbd8127150b7fcb907a72fb242dfb39f656c56ec76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261140017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde69c93a2d7e17c2950d701ee74506f5848679d0931a7fb6bcc310bc409bd39`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Mar 2023 22:28:38 GMT
ADD file:eb1e763165388ee7a658322d710f5ec8dcbdb26f4dcb475d4e157642940faa38 in / 
# Fri, 31 Mar 2023 22:28:39 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:12:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 31 Mar 2023 23:12:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 31 Mar 2023 23:12:13 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Mar 2023 23:12:13 GMT
ENV LANG=C.UTF-8
# Fri, 31 Mar 2023 23:12:13 GMT
ENV JAVA_VERSION=21-ea+15
# Fri, 31 Mar 2023 23:12:23 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='0fec1002b8c8975b181bd6966a817028d6b373cbc759254231f9b96db1fe6edd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93cc1eb6202093a127f1f9ed2e866a51dff29321f878085c18f317cefb113ffc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 31 Mar 2023 23:12:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9bd56b05f662450b6562fb8e5475401bb7581d5c57e696ff759fbc2640ad7df8`  
		Last Modified: Fri, 31 Mar 2023 22:30:06 GMT  
		Size: 44.6 MB (44562359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871be9159963ac26b08a05a3aee26e8faa1164ddfa288410491538bb1e5ad6d9`  
		Last Modified: Fri, 31 Mar 2023 23:13:26 GMT  
		Size: 15.0 MB (15006510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b358d57b6e3f13988c133144c60f0b7f53da6c2c73e3ad638674ac3d1679e15d`  
		Last Modified: Fri, 31 Mar 2023 23:13:38 GMT  
		Size: 201.6 MB (201571148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f93c5a38c3646c9a4dcad97bbd39b9b7f2220f4b23b38e63c516b64fd4ad5f79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259287713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4badaf408d7ddbfcab241d900dbc6b278ac9066d054916e7780910beee0c90`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:18 GMT
ADD file:c201d04749a3d092a7936542e4e280194ac00d3a3f3e3cd1722455429b0c4d18 in / 
# Fri, 31 Mar 2023 21:40:19 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:07:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 31 Mar 2023 22:07:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 31 Mar 2023 22:07:22 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Mar 2023 22:07:22 GMT
ENV LANG=C.UTF-8
# Mon, 03 Apr 2023 20:58:48 GMT
ENV JAVA_VERSION=21-ea+16
# Mon, 03 Apr 2023 20:58:58 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/16/GPL/openjdk-21-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='8b74ac1059c78a2abf829bd3b88c0c95c609e961af90f380a4032af52f2db0a3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/16/GPL/openjdk-21-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='f81acca52a81f2739b9a8c5c69bd066666a024c1e072b7f8b7646fb69ca25b31'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 03 Apr 2023 20:59:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e83b78392ad9185bc4dcd144ceb39aea57035dc1457949ceaa1ac05c786aeaab`  
		Last Modified: Fri, 31 Mar 2023 21:41:31 GMT  
		Size: 43.5 MB (43477120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e92b3e3d0e23cc44a53dbd0cd2db3c27142b9fab15cb207c1444dad9ab16eb`  
		Last Modified: Fri, 31 Mar 2023 22:08:55 GMT  
		Size: 15.8 MB (15844880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f63196cc7cbe8a18e2d176f3332cdb3249b2357e430929e1b9a21432d9a2d0f`  
		Last Modified: Mon, 03 Apr 2023 21:01:06 GMT  
		Size: 200.0 MB (199965713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
