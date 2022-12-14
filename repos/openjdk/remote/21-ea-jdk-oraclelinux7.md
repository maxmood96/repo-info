## `openjdk:21-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:717c6d3ad4cca327fee9290e2c847ef2b5d53ddb381567d6a1720d78ef11517c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:eebbc83a12194f548c0fd1e3b3af5bd23d3868abf6de75889280ef0b72604fb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262979444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16860e69534436b4cef7e31af77c142ea7b868124f6687d7bbe7e9c08b19aabc`
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
# Wed, 14 Dec 2022 00:33:09 GMT
ENV JAVA_VERSION=21-ea+1
# Wed, 14 Dec 2022 00:33:20 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='46d9f514e49067eebb9e3bf5033195e2ca1b834be98f3910ea1726c40e97dc22'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='950a4a33ac9737bc7ecf824d2292f4fea92b1d9301a4f89d3c32e86f4d04bd23'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 14 Dec 2022 00:33:21 GMT
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
	-	`sha256:ae4dfdcb5e356d603d15c6a955c241d6d9e2adc0a97d77c7285299f77820433c`  
		Last Modified: Wed, 14 Dec 2022 00:38:44 GMT  
		Size: 198.9 MB (198943012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:70c8f9e1c8ac92d8412b6bb67e6cacfb226f47e25865564774c534eca725a3be
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263089985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ec61acf42f99470f9acc507225ce2fb4d22ba0d71c89bb0ae97e4b8e14c37b`
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
# Wed, 14 Dec 2022 00:53:44 GMT
ENV JAVA_VERSION=21-ea+1
# Wed, 14 Dec 2022 00:53:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='46d9f514e49067eebb9e3bf5033195e2ca1b834be98f3910ea1726c40e97dc22'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='950a4a33ac9737bc7ecf824d2292f4fea92b1d9301a4f89d3c32e86f4d04bd23'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 14 Dec 2022 00:53:58 GMT
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
	-	`sha256:36148cfc9f22ee24c7134ba9b28c36c657f716dcd8c9e5520c740cfbeb4890e6`  
		Last Modified: Wed, 14 Dec 2022 00:59:23 GMT  
		Size: 197.4 MB (197435284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
