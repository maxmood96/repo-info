## `openjdk:11-oraclelinux7`

```console
$ docker pull openjdk@sha256:18e26aa3e8d6058589e9c6bce1910e278896eb6ebe459d49a32c4e2978056426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:11-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:4aee873c93cd7dd4b71310c3ec9c47dfdce2def4a72dee3e1afdaa9f606a28ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266500783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e3de212ac83a6c741444acc301095606877211032b726b63eeaef119e1fb85`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 May 2021 00:10:37 GMT
ADD file:7532c4c6850a2e95d341f39828f60573728d50ba1fc6264ed19bb36eb4b24d1c in / 
# Thu, 06 May 2021 00:10:37 GMT
CMD ["/bin/bash"]
# Thu, 06 May 2021 00:27:43 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 06 May 2021 00:28:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Thu, 06 May 2021 00:28:53 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 00:28:53 GMT
ENV LANG=en_US.UTF-8
# Thu, 06 May 2021 00:28:53 GMT
ENV JAVA_VERSION=11.0.11+9
# Thu, 06 May 2021 00:29:08 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_11.0.11_9.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.11_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 06 May 2021 00:29:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:22f7711cf64307564c3293688489295d9458bac2ca47cd6576382cfb75c9d2b9`  
		Last Modified: Thu, 06 May 2021 00:11:49 GMT  
		Size: 48.3 MB (48258661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87180291cc45c5c610f6909495ba989b36ef14701a331d8689e264f9d7c23796`  
		Last Modified: Thu, 06 May 2021 00:32:56 GMT  
		Size: 15.4 MB (15423518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a772db1694d3a2f7e38221ee61c901b3529528149319d594e8d474a3abfb731f`  
		Last Modified: Thu, 06 May 2021 00:35:04 GMT  
		Size: 202.8 MB (202818604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:96005e9f460d04c952c3d9200868f7179da9778b6bac180323cc3e6fed534df8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265777428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e58ffa8a60ba731da7fc93c5c82c205642160c6bdab7674f643fe27b4e6ae9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 May 2021 00:13:32 GMT
ADD file:57303578fa11d312dcc51eb7aef116316c2b60e48b533a1471e2f2ba915ee46a in / 
# Thu, 06 May 2021 00:13:35 GMT
CMD ["/bin/bash"]
# Thu, 06 May 2021 00:32:13 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 06 May 2021 00:34:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Thu, 06 May 2021 00:34:49 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 00:34:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 06 May 2021 00:34:51 GMT
ENV JAVA_VERSION=11.0.11+9
# Thu, 06 May 2021 00:35:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_11.0.11_9.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.11_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 06 May 2021 00:35:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d575bf1166e11ab792c567b7bdfab507a987976bc375994e3516987e6e1e600`  
		Last Modified: Thu, 06 May 2021 00:14:38 GMT  
		Size: 48.9 MB (48869643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7892e1551bf2c1decd5f1f367d2f9dbf15317e29aa12b267cf59b9c255a91b34`  
		Last Modified: Thu, 06 May 2021 00:39:13 GMT  
		Size: 16.5 MB (16472243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be30ccc6de50f77a83e26c8adcf718ca37787bd5bbe728d83b62bb7e6f0db5b`  
		Last Modified: Thu, 06 May 2021 00:41:34 GMT  
		Size: 200.4 MB (200435542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
