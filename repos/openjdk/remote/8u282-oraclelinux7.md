## `openjdk:8u282-oraclelinux7`

```console
$ docker pull openjdk@sha256:70133363b936ed7ff749f2828928fb768e7d45ccc9c33f75f90329751d3ea316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:8u282-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:27c8d4281e72dfc34006b48d875683b1f26955dfd1f414698d3ba138651e3198
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169503794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18523d7ae40ec2ed7556a94a7ad82df45047dfcb06be40da473b2537cdcbcfc0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 01 Feb 2021 20:32:48 GMT
ADD file:430ae887b8a202818526e7c39819c089bee09a496bbd4cab85759814c30dde4b in / 
# Mon, 01 Feb 2021 20:32:49 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 23:55:53 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 02 Feb 2021 00:01:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 02 Feb 2021 00:01:08 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Feb 2021 00:01:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Feb 2021 00:01:08 GMT
ENV JAVA_VERSION=8u282
# Tue, 02 Feb 2021 00:01:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
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
	-	`sha256:2956586407f4a70ed83795610fd593c3257720f2327b451185ec05d4e4be1594`  
		Last Modified: Tue, 02 Feb 2021 00:09:23 GMT  
		Size: 105.8 MB (105803187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
