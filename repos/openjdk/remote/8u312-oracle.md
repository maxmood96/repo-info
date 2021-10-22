## `openjdk:8u312-oracle`

```console
$ docker pull openjdk@sha256:3c027354b1870ac5bd0265a48a403b3c6134ddb2d58e9aab8fb917f7cdc8aaca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8u312-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:51967e10955934df2270887af4a2b5c58f3db4d0aff3f3511e6405192c92ce67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161345651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da4d1269499504d73d77dd6c3378d799a29c477d17d5515af438443f47e8cf0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Oct 2021 18:29:51 GMT
ADD file:3223e5829b65b376c23e1faa6f519d37b0166b38063f91b793a8ed710a39fe33 in / 
# Wed, 13 Oct 2021 18:29:51 GMT
CMD ["/bin/bash"]
# Wed, 13 Oct 2021 18:47:48 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 13 Oct 2021 18:51:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Wed, 13 Oct 2021 18:51:58 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 18:51:58 GMT
ENV LANG=C.UTF-8
# Thu, 21 Oct 2021 23:46:19 GMT
ENV JAVA_VERSION=8u312
# Thu, 21 Oct 2021 23:46:32 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:58c4eaffce77ac1fb013bf82c91927c631802ad54465ebc9b687b5dc8ee73c02`  
		Last Modified: Wed, 13 Oct 2021 18:31:20 GMT  
		Size: 42.0 MB (41961111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a22c806ee8aa2b360bd5818a4f78bc3da280abb86f3db09805b1daddd78324`  
		Last Modified: Wed, 13 Oct 2021 18:56:49 GMT  
		Size: 13.5 MB (13489427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd07611f7ef2bf7e08245af7a173d3db9ff5d1b390de36c81babc2aa771798f4`  
		Last Modified: Fri, 22 Oct 2021 00:02:22 GMT  
		Size: 105.9 MB (105895113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8u312-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:277d6129b971773ea1b3908802e6b2016ae8f34aec2eaaee67710513d72aae2e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161053983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff50808846d0f5a600dcfc45f977dc618e72dee64149ca0f3a923929fcfe637`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 14 Oct 2021 03:43:23 GMT
ADD file:f161e88dde917cf9d761056277b85a1880719b445048fc52649306cec001db66 in / 
# Thu, 14 Oct 2021 03:43:24 GMT
CMD ["/bin/bash"]
# Thu, 14 Oct 2021 05:42:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 14 Oct 2021 05:49:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Thu, 14 Oct 2021 05:49:02 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Oct 2021 05:49:03 GMT
ENV LANG=C.UTF-8
# Fri, 22 Oct 2021 02:23:43 GMT
ENV JAVA_VERSION=8u312
# Fri, 22 Oct 2021 02:23:52 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:a1eec3e47437e3334dd709f3a36be617982ec7579fa52be305301bb95c0d4be1`  
		Last Modified: Thu, 14 Oct 2021 03:44:37 GMT  
		Size: 41.9 MB (41877085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ec5552a84ea6485845e8e0a4d9b09b5e8f78d742440c18650d1ec9b1aacd89`  
		Last Modified: Thu, 14 Oct 2021 05:57:59 GMT  
		Size: 14.3 MB (14270572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eaedc9aaad4e465fc5cdaddb05ce2cd6631a8bb88056d50dfa5d286849a4d0`  
		Last Modified: Fri, 22 Oct 2021 02:44:30 GMT  
		Size: 104.9 MB (104906326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
