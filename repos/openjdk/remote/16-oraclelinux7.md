## `openjdk:16-oraclelinux7`

```console
$ docker pull openjdk@sha256:30166398d5ec5608c66b2c4da20207388469efd53c533324107e9741fa3f658f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:6f06bd3dda1225ff08cf11589f57fb9b8f90a0fbb8f46ab3ebd135ed677346f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248476161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8679bea73a0852d8ace7ba691b132dee1814addcb9ec9b5f59ee35b712478c7f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 20:32:48 GMT
ADD file:430ae887b8a202818526e7c39819c089bee09a496bbd4cab85759814c30dde4b in / 
# Mon, 01 Feb 2021 20:32:49 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 23:55:53 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 01 Feb 2021 23:57:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 01 Feb 2021 23:57:20 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:57:20 GMT
ENV LANG=en_US.UTF-8
# Fri, 05 Feb 2021 22:38:34 GMT
ENV JAVA_VERSION=16
# Fri, 05 Feb 2021 22:38:49 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/35/GPL/openjdk-16_linux-x64_bin.tar.gz'; 			downloadSha256='25f51624a17545a769e97ded5d51075ab31f9a52de925f7292cff951becf8fd2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/35/GPL/openjdk-16_linux-aarch64_bin.tar.gz'; 			downloadSha256='5afe8561d1c6f777bf0f70bf5d994187ff607b8c4c6ff1194f849a0bb933d805'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 05 Feb 2021 22:38:49 GMT
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
	-	`sha256:1ae3ada2bafe65ab19619b9ea1b338d10d4bf045ce6f52b65ff9e34a48b7849a`  
		Last Modified: Fri, 05 Feb 2021 22:46:05 GMT  
		Size: 184.8 MB (184775554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0aaf3350398d963bcc292c173aff25e092a9da356e292fded57dd6f643abc649
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa78c88a6f0bf7c2f5be2a305574c3d9429ab1a76232cc3698746e9b3a96041c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 21:01:37 GMT
ADD file:515797e9c94114d9811e4f5e7ef89e24a7c02f5496694320cf17c5b2c2c62577 in / 
# Mon, 01 Feb 2021 21:01:39 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:07:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 01 Feb 2021 21:09:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 01 Feb 2021 21:09:40 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:09:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 05 Feb 2021 23:06:09 GMT
ENV JAVA_VERSION=16
# Fri, 05 Feb 2021 23:06:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/35/GPL/openjdk-16_linux-x64_bin.tar.gz'; 			downloadSha256='25f51624a17545a769e97ded5d51075ab31f9a52de925f7292cff951becf8fd2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/35/GPL/openjdk-16_linux-aarch64_bin.tar.gz'; 			downloadSha256='5afe8561d1c6f777bf0f70bf5d994187ff607b8c4c6ff1194f849a0bb933d805'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 05 Feb 2021 23:06:38 GMT
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
	-	`sha256:45328c663f60e03e52aa913193f6348635c1587494a0e06f94b95e5417ee23e6`  
		Last Modified: Fri, 05 Feb 2021 23:15:28 GMT  
		Size: 179.1 MB (179146841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
