## `openjdk:11-oraclelinux7`

```console
$ docker pull openjdk@sha256:ee36853584ea64e44549cbb435ad4bac468a96e00756b211650958cdd7571efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:11-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:de855f73deede47f5cd1c0566450d7445dd5882266e2e73156fdb117e9b89182
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266386190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4b9d112717a314a668890b069fec1cb24c54f253f186e9cc39502f2a8a7797`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 20:32:48 GMT
ADD file:430ae887b8a202818526e7c39819c089bee09a496bbd4cab85759814c30dde4b in / 
# Mon, 01 Feb 2021 20:32:49 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 23:55:53 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 02 Feb 2021 00:00:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Tue, 02 Feb 2021 00:00:13 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Feb 2021 00:00:13 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Feb 2021 00:00:13 GMT
ENV JAVA_VERSION=11.0.10
# Tue, 02 Feb 2021 00:00:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_11.0.10_9.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 02 Feb 2021 00:00:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69d77e45731bec64e61a0f08021494f9c0f93a8dc00071bebe5ce614dec1f72a`  
		Last Modified: Mon, 01 Feb 2021 20:34:46 GMT  
		Size: 48.3 MB (48263590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5df3ce42f8a33f03c8ac097c0e1adc969007d8424ef47e9b638a58b42e82a6a`  
		Last Modified: Tue, 02 Feb 2021 00:04:46 GMT  
		Size: 15.4 MB (15437017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d83c1da4b5091e23666621cc4a21cf327da4f62ad09195a25c37308198c47`  
		Last Modified: Tue, 02 Feb 2021 00:08:21 GMT  
		Size: 202.7 MB (202685583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:de218ba1b1ba6d0c16eb6ef15b1c3398d53b0bcd707aa3da5a196eab74b4392b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265599004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e407b7226fd21c015c9bba26260042d0bfd9958dba39dc31e040d6d792b1604e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 21:01:37 GMT
ADD file:515797e9c94114d9811e4f5e7ef89e24a7c02f5496694320cf17c5b2c2c62577 in / 
# Mon, 01 Feb 2021 21:01:39 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:07:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 01 Feb 2021 21:12:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Mon, 01 Feb 2021 21:12:31 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:12:31 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Feb 2021 21:12:32 GMT
ENV JAVA_VERSION=11.0.10
# Mon, 01 Feb 2021 21:12:58 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_11.0.10_9.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 21:13:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:679e771030bbd97d6d7a7cf8b0a2290601de0b646eaa29d88c48562a70464c12`  
		Last Modified: Mon, 01 Feb 2021 21:03:42 GMT  
		Size: 48.9 MB (48851459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff96049663e262709e8d337b37d084629a90f0707979070456acf5338444948`  
		Last Modified: Mon, 01 Feb 2021 21:16:24 GMT  
		Size: 16.5 MB (16466150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2060d509bdfefb5e18317596fa95c2c78a655bee11d34359443d56bb134e7279`  
		Last Modified: Mon, 01 Feb 2021 21:21:16 GMT  
		Size: 200.3 MB (200281395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
