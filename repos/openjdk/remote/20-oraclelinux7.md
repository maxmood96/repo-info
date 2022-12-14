## `openjdk:20-oraclelinux7`

```console
$ docker pull openjdk@sha256:09a131413f363bf00df64b10e05c891783fb49a88ed5b43c3eddce73eca04e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:874fdecc2af788f178ea79a22a88cae494ec13652697be9878aca4a7d127f738
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262126872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d04bb0e70983992efdf30d240f05bb83a2e67dbf1928379e2fe9358809835de`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:56 GMT
ADD file:3853624d773c4bf6fc1464ca06bd07366109fab78072fcab59075073a5da6525 in / 
# Wed, 07 Dec 2022 01:51:56 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:27:36 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 07 Dec 2022 02:27:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 07 Dec 2022 02:27:36 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:27:36 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Dec 2022 20:57:56 GMT
ENV JAVA_VERSION=20-ea+27
# Mon, 12 Dec 2022 20:58:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='fc3bc8e77b3b556d06a55cf2c2e5510c94359858d5c691b38575aa164eade92b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7828ad1bee0c3e813c02057353eca047c86f3799cfe3c76cbe21b15d57b239bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Dec 2022 20:58:07 GMT
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
	-	`sha256:fe404b7662baf6a59985e2b2d5d6149d2be73d3d38cf207343d202a84546af53`  
		Last Modified: Mon, 12 Dec 2022 21:02:34 GMT  
		Size: 198.1 MB (198090440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ea15383c8ad1e3c57fc33d096c75b9534ae54093de96063b44d8b9fa0c4b949c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262236573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d0eac053bc2c20659a20c05b92bfbd8979258687e209ad9fa06aec3011f8aa`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 02:11:05 GMT
ADD file:811a8ff51774a6c04c874e49a9bf2f3ef1a447402946740d2128a81809dc1a22 in / 
# Wed, 07 Dec 2022 02:11:06 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:53:45 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 07 Dec 2022 02:53:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 07 Dec 2022 02:53:45 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:53:45 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Dec 2022 19:53:33 GMT
ENV JAVA_VERSION=20-ea+27
# Mon, 12 Dec 2022 19:53:45 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='fc3bc8e77b3b556d06a55cf2c2e5510c94359858d5c691b38575aa164eade92b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/27/GPL/openjdk-20-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='7828ad1bee0c3e813c02057353eca047c86f3799cfe3c76cbe21b15d57b239bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Dec 2022 19:53:47 GMT
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
	-	`sha256:f74dc0b2d7014b5574edf4bd1b2f112c65123827904fba7ac107b75e2b8565f2`  
		Last Modified: Mon, 12 Dec 2022 19:58:22 GMT  
		Size: 196.6 MB (196581872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
