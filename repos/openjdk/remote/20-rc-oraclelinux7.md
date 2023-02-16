## `openjdk:20-rc-oraclelinux7`

```console
$ docker pull openjdk@sha256:6b15540b0b167bdd248d09e370bdb0052ae336c0183969ede07ce448899bc920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-rc-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:5c9f05b105be09e9ab202aa6bae3487c0d1f21b2dfe058f0fe032309d874d5c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262838669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d910e5307811a84c7d6b8d6c4700ea7265f4bfd8c44aa74e3c9a24be5c7ff338`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 23:54:48 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 27 Jan 2023 23:55:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 27 Jan 2023 23:55:34 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 23:55:34 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Feb 2023 00:39:45 GMT
ENV JAVA_VERSION=20
# Thu, 16 Feb 2023 00:39:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz'; 			downloadSha256='bb863b2d542976d1ae4b7b81af3e78b1e4247a64644350b552d298d8dc5980dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-aarch64_bin.tar.gz'; 			downloadSha256='b671dd1513e7bd4f3de6b1424a90a4998997a67593bf259936d55f5e83e31959'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 16 Feb 2023 00:39:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde4d617b6d23e9a10ad76ad56ca1591c532861de431f66e6e735233eef43807`  
		Last Modified: Sat, 28 Jan 2023 00:00:16 GMT  
		Size: 14.2 MB (14244027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c5d70b1425278644dcd6b4fdba0df3304f30868b4f4920e03828bef61ce5f2`  
		Last Modified: Thu, 16 Feb 2023 00:43:44 GMT  
		Size: 198.1 MB (198128065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-rc-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7eca8c17909649d5c0b9731c1ad12a279387dbaa945ebfd59bef2bf9eef91a3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262931018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcd70bc4326ccc866de0b2fce8a9bd3253425033bbe01fe4b54bb3bcca7e797`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 22:41:24 GMT
ADD file:1081f67c6d4b6b053a45161b9968a0371ed81fc45f61729a33bffa9a470ec646 in / 
# Fri, 27 Jan 2023 22:41:25 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 22:59:27 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 27 Jan 2023 23:00:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 27 Jan 2023 23:00:22 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 23:00:22 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Feb 2023 00:54:38 GMT
ENV JAVA_VERSION=20
# Thu, 16 Feb 2023 00:54:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz'; 			downloadSha256='bb863b2d542976d1ae4b7b81af3e78b1e4247a64644350b552d298d8dc5980dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-aarch64_bin.tar.gz'; 			downloadSha256='b671dd1513e7bd4f3de6b1424a90a4998997a67593bf259936d55f5e83e31959'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 16 Feb 2023 00:54:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:114f8bb3e448153115527e27f088f4ed8912d567d8785d54c82dbf490230f6d0`  
		Last Modified: Fri, 27 Jan 2023 22:43:00 GMT  
		Size: 51.0 MB (51033896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc016fcb2fb8b8e69042ed80b5f1629423ef745bcb1ac72c0501de8b7b02850`  
		Last Modified: Fri, 27 Jan 2023 23:05:00 GMT  
		Size: 15.3 MB (15268160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7259cba08b808f391f3ec122aa307ba3c3e51fcd121f405ba555fb148227f518`  
		Last Modified: Thu, 16 Feb 2023 00:58:41 GMT  
		Size: 196.6 MB (196628962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
