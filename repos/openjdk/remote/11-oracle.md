## `openjdk:11-oracle`

```console
$ docker pull openjdk@sha256:b620f76dac9634c67656900aaaae1a1b3bbe7e37c0f070003da59ad15c801d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:11-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:87b5b9f660a4b290f518638d23aad7df68307173235bb7da08a0a5aa2222a2c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258788863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d75d017da25ac9ef38742e9ade6c0166cec6509341120a461cca019dd055bd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Dec 2021 02:20:57 GMT
ADD file:15b307e0b1aafead42c103e34d3e51a271acea1ab0b68961e239f11af3b0d179 in / 
# Thu, 23 Dec 2021 02:20:57 GMT
CMD ["/bin/bash"]
# Thu, 23 Dec 2021 02:37:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Dec 2021 02:39:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Thu, 23 Dec 2021 02:39:38 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Dec 2021 02:39:39 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:31:12 GMT
ENV JAVA_VERSION=11.0.14
# Thu, 03 Feb 2022 20:32:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jdk_x64_linux_11.0.14_9.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.14_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 03 Feb 2022 20:32:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:155aced2666332ddff5a741b0236f360820e7aa3fc3dde2224fc17a91fc48db6`  
		Last Modified: Thu, 23 Dec 2021 02:21:56 GMT  
		Size: 42.1 MB (42105152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5901c58ecb29b61159b5e3a63dfbb0fb520b2de1d33c9fb038d9b697e3fcd4`  
		Last Modified: Thu, 23 Dec 2021 02:45:32 GMT  
		Size: 13.5 MB (13520734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db784d31746bfa08e187033eeff7a8431a42d7dbd553034cf1c0c8f031573db`  
		Last Modified: Thu, 03 Feb 2022 20:56:49 GMT  
		Size: 203.2 MB (203162977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:af41b445234f1fa876aee3ce4e2d44e807c67e8d16d4c2c641b524def7650d8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257103729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8aa3d1189065f31a50dc8c08f88adf9b53f8f1cb8840d7da3ba8ee82f62cfd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Dec 2021 02:40:45 GMT
ADD file:140d632303428d802f77f473aef33fa52daacdfc76b23edde4344be661c1d4b0 in / 
# Thu, 23 Dec 2021 02:40:46 GMT
CMD ["/bin/bash"]
# Thu, 23 Dec 2021 02:58:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Dec 2021 03:00:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Thu, 23 Dec 2021 03:00:47 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Dec 2021 03:00:48 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:46:56 GMT
ENV JAVA_VERSION=11.0.14
# Thu, 03 Feb 2022 20:48:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jdk_x64_linux_11.0.14_9.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.14_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 03 Feb 2022 20:48:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53f096d4aa0757c30613f325df1e03a90db9d9879ea251b394e3ab0a068b5610`  
		Last Modified: Thu, 23 Dec 2021 02:41:44 GMT  
		Size: 42.0 MB (42018351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921862a08fd8bc652539d62804daf06ab6464bd5b42061f5bedbdfa73bd62136`  
		Last Modified: Thu, 23 Dec 2021 03:11:46 GMT  
		Size: 14.3 MB (14303905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baf2b5e61b56d58faa36f2e3b431e8fa4d31ccd7a4cb6270212ba842cbbeca6`  
		Last Modified: Thu, 03 Feb 2022 21:10:44 GMT  
		Size: 200.8 MB (200781473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
