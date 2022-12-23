## `openjdk:21-oraclelinux7`

```console
$ docker pull openjdk@sha256:2f7203bf064c7279ec68b4129192250773bed33e7f18819c82d0984025045565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:35315b788eb473851a0ae6aea580787d0a57ed441249b37e7907ac042d446a1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263147522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80940e0349354e6c6b5a6d568bd36113745604acd435b4fded9b9e421f5529d0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:56 GMT
ADD file:3853624d773c4bf6fc1464ca06bd07366109fab78072fcab59075073a5da6525 in / 
# Wed, 07 Dec 2022 01:51:56 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:27:36 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Dec 2022 00:33:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 14 Dec 2022 00:33:09 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2022 00:33:09 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 Dec 2022 01:20:16 GMT
ENV JAVA_VERSION=21-ea+3
# Fri, 23 Dec 2022 01:20:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/3/GPL/openjdk-21-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='21c02c2f76e385cca3ddd75d2913d3b6e16e4a1fa934fe038c0ab3c8c1184149'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/3/GPL/openjdk-21-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='84936b271d7997ca809075582a686eee89f8f37ac9252f33b8292260518000dd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Dec 2022 01:20:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d26998a7c52d2b84e7927f97651d1d703a805c8e4d3f658a03138721f5a5dd44`  
		Last Modified: Wed, 07 Dec 2022 01:53:46 GMT  
		Size: 49.8 MB (49818482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13169d9a90276a4f8190fd6edcdf29f7dd28e38d5919cd950939ffe59628af48`  
		Last Modified: Wed, 07 Dec 2022 02:31:28 GMT  
		Size: 14.2 MB (14217950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7398983bab2b288732775d78b52b9a93d6e36d788456ee54339b5740c07b56fc`  
		Last Modified: Fri, 23 Dec 2022 01:27:02 GMT  
		Size: 199.1 MB (199111090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4073510d56edf3b204ecd79c12cf97cd81db99788f777b0311cb1b63aaa63d41
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263212258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a263e036c92b2d21f058c390b51b451102395ee7848861b4df4efeb450953670`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 02:11:05 GMT
ADD file:811a8ff51774a6c04c874e49a9bf2f3ef1a447402946740d2128a81809dc1a22 in / 
# Wed, 07 Dec 2022 02:11:06 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:53:45 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Dec 2022 00:53:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 14 Dec 2022 00:53:44 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2022 00:53:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 Dec 2022 00:40:03 GMT
ENV JAVA_VERSION=21-ea+3
# Fri, 23 Dec 2022 00:40:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/3/GPL/openjdk-21-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='21c02c2f76e385cca3ddd75d2913d3b6e16e4a1fa934fe038c0ab3c8c1184149'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/3/GPL/openjdk-21-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='84936b271d7997ca809075582a686eee89f8f37ac9252f33b8292260518000dd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Dec 2022 00:40:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81ac616e14aefb691216238b73174a9efd12a5e52bc4e297c5c1cf38561e5aca`  
		Last Modified: Wed, 07 Dec 2022 02:12:40 GMT  
		Size: 50.4 MB (50386463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804baa16591d133fbd09bac6a9223716dbf71fec46b68197f09b7ad836238810`  
		Last Modified: Wed, 07 Dec 2022 02:57:50 GMT  
		Size: 15.3 MB (15268238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74eea22fdd3568e4427692fbfd71259316c309a3d71f0531523687167349fa2`  
		Last Modified: Fri, 23 Dec 2022 00:46:40 GMT  
		Size: 197.6 MB (197557557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
