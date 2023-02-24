## `openjdk:20-jdk-oracle`

```console
$ docker pull openjdk@sha256:9994b8c7a83e38d5892e595e54fe96d68c4b3d745307f97904a2f369ada8b685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ec062f28f88f8455cde6746071d8aea311f1aa8370154569af5670e54b725738
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254925241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b610e334aeb074516e6b92e734e7b1c97742058e48b15d17256aeac0fbc00a3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Feb 2023 19:37:08 GMT
ADD file:7c92981e2fed9bedfca663209480ce9006dce0edc6c44c25640255683952b929 in / 
# Thu, 23 Feb 2023 19:37:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 19:56:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Feb 2023 19:56:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 23 Feb 2023 19:56:42 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Feb 2023 19:56:42 GMT
ENV LANG=C.UTF-8
# Thu, 23 Feb 2023 19:56:42 GMT
ENV JAVA_VERSION=20
# Thu, 23 Feb 2023 19:56:52 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz'; 			downloadSha256='bb863b2d542976d1ae4b7b81af3e78b1e4247a64644350b552d298d8dc5980dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-aarch64_bin.tar.gz'; 			downloadSha256='b671dd1513e7bd4f3de6b1424a90a4998997a67593bf259936d55f5e83e31959'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 23 Feb 2023 19:56:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1319f85bbd2aad3767d41a6c767c94c23f7432642c7bda3df878c147ba384902`  
		Last Modified: Thu, 23 Feb 2023 19:38:02 GMT  
		Size: 44.6 MB (44552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565fe2a72fd544bf059ba3dab17c20dd57232b65e41885f9004b841d0106f73b`  
		Last Modified: Thu, 23 Feb 2023 19:58:20 GMT  
		Size: 12.2 MB (12246468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677222843d4d6aaf2c835d46702235d78f22d46a5ea33993c035be791245f5ca`  
		Last Modified: Thu, 23 Feb 2023 19:59:32 GMT  
		Size: 198.1 MB (198126321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3b590fe684765d114188c4afc5194dd899113fd8c0883fdc4ebbb5a3a47ca5b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255926719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b68bc9c7fd15a512c4f4d7c3bba6ed31ee37837261bb89572f8ba978be80624`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Feb 2023 23:40:03 GMT
ADD file:b9db410ba951fb740a34187417442b96a27a7fd918b16023c16cb1b0777b292f in / 
# Thu, 23 Feb 2023 23:40:04 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 23:58:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Feb 2023 23:59:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 23 Feb 2023 23:59:17 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Feb 2023 23:59:17 GMT
ENV LANG=C.UTF-8
# Thu, 23 Feb 2023 23:59:17 GMT
ENV JAVA_VERSION=20
# Thu, 23 Feb 2023 23:59:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz'; 			downloadSha256='bb863b2d542976d1ae4b7b81af3e78b1e4247a64644350b552d298d8dc5980dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-aarch64_bin.tar.gz'; 			downloadSha256='b671dd1513e7bd4f3de6b1424a90a4998997a67593bf259936d55f5e83e31959'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 23 Feb 2023 23:59:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf42ad2544e3a5379ea5e0050457e87df46409adba81dba4686a3efc595ccd2`  
		Last Modified: Thu, 23 Feb 2023 23:40:48 GMT  
		Size: 43.5 MB (43461050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2911a20ed1ec4cf4241519f3d97458f77a1eaded44c42d9ae79a999075ef4c`  
		Last Modified: Fri, 24 Feb 2023 00:01:00 GMT  
		Size: 15.8 MB (15838054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb14c31d1bbe3445069886c7ae16975d2fd32ef20ea20ff1e88571f61ea9c91`  
		Last Modified: Fri, 24 Feb 2023 00:02:05 GMT  
		Size: 196.6 MB (196627615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
