## `openjdk:8u282-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:3c124550016dc4fb2fce6871be8fba2acee1ac4d3b3b7fd09ee35a576416dadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:8u282-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:e4af95cba13e8db99e20882fde8308fe890eb99a44c019703c7ccb0e770a3800
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169506684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e585f2f7eec28382765484a5f98c8ffad112629e4e0e7a41f4ed9275c7dbd9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 20:36:55 GMT
ADD file:361f165903526126476b03dd2afac1fff0b334906bb56d024e5aee87b948b0cf in / 
# Tue, 09 Mar 2021 20:36:56 GMT
CMD ["/bin/bash"]
# Tue, 09 Mar 2021 20:56:14 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 09 Mar 2021 21:04:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 09 Mar 2021 21:04:11 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 21:04:11 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Mar 2021 21:04:12 GMT
ENV JAVA_VERSION=8u282
# Tue, 09 Mar 2021 21:04:20 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:a61503a3b32ea964eb926d54dcfe6cd7e21f4e0cca1b1373df21cf904388c445`  
		Last Modified: Fri, 12 Feb 2021 00:54:42 GMT  
		Size: 48.3 MB (48263629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bec9c0e7fad6eb1470aa0268ede53633bb156c1b1700c2347ea7c1b36ddfaba`  
		Last Modified: Tue, 09 Mar 2021 21:09:25 GMT  
		Size: 15.4 MB (15439846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ab799c0e79a3addbb6efd03cf30303474382c146e88d9f2d842899ce3048d`  
		Last Modified: Tue, 09 Mar 2021 21:23:39 GMT  
		Size: 105.8 MB (105803209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
