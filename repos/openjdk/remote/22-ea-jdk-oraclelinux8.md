## `openjdk:22-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:417900c44b14dfebf45d0fded0fab95b494b61e78e0cda8b5bc5164843519a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:6eef769dc8306add05cd733e42f52846bc3db7f88542f4537f6f94d38a1d66f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263611121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df553157f497e87a0559c290fb37d6df269fb53e1419836fd60310cc25e5e4f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:45:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 20 Oct 2023 18:45:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 20 Oct 2023 18:45:06 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Oct 2023 18:45:06 GMT
ENV LANG=C.UTF-8
# Wed, 29 Nov 2023 01:44:38 GMT
ENV JAVA_VERSION=22-ea+25
# Wed, 29 Nov 2023 01:45:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/25/GPL/openjdk-22-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='0f98721a88a1dd380773adbf29dd79df25be9b69045c3266f913ecacc5e74d3e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/25/GPL/openjdk-22-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea5fc28e7b6ed0a5da04b4740a35d8dd26bb68a48a516da2d002359d817ba35c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Nov 2023 01:45:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7fcefe71b24cef619772a3adab6474d1dee79d5ec55a8ac900504be9b669d3`  
		Last Modified: Fri, 20 Oct 2023 18:46:04 GMT  
		Size: 15.0 MB (15016123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c9ab7d924d4d1de3d0241d24e9b229f363ef7600f7545d18808e6c208329f9`  
		Last Modified: Wed, 29 Nov 2023 01:48:31 GMT  
		Size: 204.3 MB (204315378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d379c3ab300011486210731b10be1f1e2eea546a051b6f92e6658f17d9931261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261647253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6838fb340d924a39b46cc997589d0b3be1396a89a36f2c135faac7bc8804e29e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 19:20:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 20 Oct 2023 19:20:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 20 Oct 2023 19:20:38 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Oct 2023 19:20:38 GMT
ENV LANG=C.UTF-8
# Fri, 17 Nov 2023 02:04:44 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 02:05:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='f2b3d5371bc7ab762205f286fc5b5da9dabbdd0477965fc87d02076faf69ab3a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='909c2841030baff026a45248785f3dc50906ce921620913a28b8d6cca0075838'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Nov 2023 02:05:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4910a471f6760b5f0bc0ef155e7afd624a4c1ea6f09bb680d43c1041cfd4fd`  
		Last Modified: Fri, 20 Oct 2023 19:21:34 GMT  
		Size: 15.7 MB (15660393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cc90748a7c7b76ab586f2f07f6f493aae771b025656dd0dd7826a57c46427d`  
		Last Modified: Fri, 17 Nov 2023 02:08:23 GMT  
		Size: 202.3 MB (202314076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
