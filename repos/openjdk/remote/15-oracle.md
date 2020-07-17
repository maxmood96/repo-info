## `openjdk:15-oracle`

```console
$ docker pull openjdk@sha256:d12688cfb143e922e96e8b02bfb5cdecbe81ad2f12d2818cd0da44fc1e6bdbc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:15-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:3349e3858cef51eb34d5e81284cdb777b0732b2e7b9f813228bd3a3ed42201be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253973973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0904f2fd8da419d7ef27d596ab22830632e911dcae3bca0555963669cd3442a2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Wed, 10 Jun 2020 18:22:32 GMT
ADD file:79bb5b8b89fe54ba99fd9d42d4f8774bfb9c1319ac3ead17a2005a3bde852451 in / 
# Wed, 10 Jun 2020 18:22:32 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2020 18:39:27 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 10 Jun 2020 18:39:28 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Jun 2020 18:39:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 10 Jun 2020 18:39:28 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jul 2020 22:36:53 GMT
ENV JAVA_VERSION=15-ea+32
# Thu, 16 Jul 2020 22:37:43 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_linux-aarch64_bin.tar.gz; 			downloadSha256=9480832ee9344c7e87ab39c4a4c7c1a224a576a9442e0eedfc52bb67acb7788b; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_linux-x64_bin.tar.gz; 			downloadSha256=70521c1fa8a44e3073862fc10bcae2f1c2b688b5ce354734ceb242dd52145c51; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Thu, 16 Jul 2020 22:37:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa926a7d213a8145d6a906d68a085b21909a4b26871f142804e68b322bf8881f`  
		Last Modified: Wed, 10 Jun 2020 18:23:43 GMT  
		Size: 43.5 MB (43457466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aed8993d2fb0bb3a658c631a1dfbd05c0e5d42218f419d18238996bd06ea08`  
		Last Modified: Wed, 10 Jun 2020 18:42:25 GMT  
		Size: 14.8 MB (14760261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4a5e0bdb18a83e535f2782d6ee4dd4304856b05f7c4a31aa891165b974011a`  
		Last Modified: Thu, 16 Jul 2020 22:43:32 GMT  
		Size: 195.8 MB (195756246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d10dd83d22d4afaaf03ae29e33a5b8ad39b3680eab80f6f799755e6b2d4d6258
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233948669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd19e65d78ad3219c02922654ebb7dbaf86fede568a010c1ad588d15ae53bed`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Wed, 10 Jun 2020 18:54:47 GMT
ADD file:64c488ae0df14676929e149538eb50b12e9a99518a126c88ee9704e8a88424e5 in / 
# Wed, 10 Jun 2020 18:54:49 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2020 19:12:05 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 10 Jun 2020 19:12:06 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Jun 2020 19:12:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 10 Jun 2020 19:12:07 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jul 2020 22:15:32 GMT
ENV JAVA_VERSION=15-ea+32
# Thu, 16 Jul 2020 22:16:18 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_linux-aarch64_bin.tar.gz; 			downloadSha256=9480832ee9344c7e87ab39c4a4c7c1a224a576a9442e0eedfc52bb67acb7788b; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_linux-x64_bin.tar.gz; 			downloadSha256=70521c1fa8a44e3073862fc10bcae2f1c2b688b5ce354734ceb242dd52145c51; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Thu, 16 Jul 2020 22:16:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b791ce794f1b8ac779f7e2bb939c8f822209f7507dbc7f70d072d98b700e55a`  
		Last Modified: Wed, 10 Jun 2020 18:55:52 GMT  
		Size: 44.1 MB (44072411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7857b3d293f1062b1c04189b86491b9bbfd2e793fec6975e1bdcabf4ef9ed3`  
		Last Modified: Wed, 10 Jun 2020 19:14:19 GMT  
		Size: 15.0 MB (15012793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6c796e666b6e6631550b7db226cc95adb3c6e49a3eb07bd1d51bda7f74acc1`  
		Last Modified: Thu, 16 Jul 2020 22:23:17 GMT  
		Size: 174.9 MB (174863465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
