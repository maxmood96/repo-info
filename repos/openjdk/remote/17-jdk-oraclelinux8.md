## `openjdk:17-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:7a61d9e01b49c0acc696178b9be0c963b6028b2154276f03d32e47f5a532a110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7928e7eb217232e0ed0a248746a8ebcaba4ca7fdc0f3105789ff2584aa67322a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242597178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744cf265878b854fbae9a17dddb120eac0f5d0edde8606ff3855a3fb348595cf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 13 Oct 2021 18:29:51 GMT
ADD file:3223e5829b65b376c23e1faa6f519d37b0166b38063f91b793a8ed710a39fe33 in / 
# Wed, 13 Oct 2021 18:29:51 GMT
CMD ["/bin/bash"]
# Wed, 13 Oct 2021 18:47:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 13 Oct 2021 18:49:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 13 Oct 2021 18:49:05 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 18:49:05 GMT
ENV LANG=C.UTF-8
# Wed, 13 Oct 2021 18:49:06 GMT
ENV JAVA_VERSION=17
# Wed, 13 Oct 2021 18:49:17 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 13 Oct 2021 18:49:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:58c4eaffce77ac1fb013bf82c91927c631802ad54465ebc9b687b5dc8ee73c02`  
		Last Modified: Wed, 13 Oct 2021 18:31:20 GMT  
		Size: 42.0 MB (41961111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a22c806ee8aa2b360bd5818a4f78bc3da280abb86f3db09805b1daddd78324`  
		Last Modified: Wed, 13 Oct 2021 18:56:49 GMT  
		Size: 13.5 MB (13489427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a88e5590ad1b849be4e189b4ba765d5c709a6f42b53dfaaebbe4449ef517d35`  
		Last Modified: Wed, 13 Oct 2021 18:58:43 GMT  
		Size: 187.1 MB (187146640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:011d53d20308831d87b2e0fced6a70e53066856fccab52e2bb1bd5160785f3db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242124772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2da9d9fbde26ed500ff11845a817e953b59f51e9f3cd45827bcf1f76ed4fc01`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 14 Oct 2021 03:43:23 GMT
ADD file:f161e88dde917cf9d761056277b85a1880719b445048fc52649306cec001db66 in / 
# Thu, 14 Oct 2021 03:43:24 GMT
CMD ["/bin/bash"]
# Thu, 14 Oct 2021 05:42:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 14 Oct 2021 05:44:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 14 Oct 2021 05:44:29 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Oct 2021 05:44:30 GMT
ENV LANG=C.UTF-8
# Tue, 19 Oct 2021 21:47:11 GMT
ENV JAVA_VERSION=17.0.1
# Tue, 19 Oct 2021 21:47:23 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 19 Oct 2021 21:47:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a1eec3e47437e3334dd709f3a36be617982ec7579fa52be305301bb95c0d4be1`  
		Last Modified: Thu, 14 Oct 2021 03:44:37 GMT  
		Size: 41.9 MB (41877085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ec5552a84ea6485845e8e0a4d9b09b5e8f78d742440c18650d1ec9b1aacd89`  
		Last Modified: Thu, 14 Oct 2021 05:57:59 GMT  
		Size: 14.3 MB (14270572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ba7119c3209e816cf1a3158c4385c5863403eb5e0a81d172c5e03968b32d20`  
		Last Modified: Tue, 19 Oct 2021 22:00:54 GMT  
		Size: 186.0 MB (185977115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
