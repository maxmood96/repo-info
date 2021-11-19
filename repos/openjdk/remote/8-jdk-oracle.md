## `openjdk:8-jdk-oracle`

```console
$ docker pull openjdk@sha256:d0311837bd4419b4ef0de2c061a660caa3ceb6fce48dec20da5f2478b9316dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ec7d43b3135e80c6522ff573cc5fae8ce3b5c1a27ad020416dc9f6abe3ab4dd0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161504730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a726c7522c3368739e0b53fef3c8b3ba1a11831aedd4c4c066c477a5919fc6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 19 Nov 2021 03:08:35 GMT
ADD file:d27591ceabbe39902d88042ebe31aecc38844787fafa004cdeb0080da29c1623 in / 
# Fri, 19 Nov 2021 03:08:35 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 03:25:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 19 Nov 2021 03:27:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Fri, 19 Nov 2021 03:27:26 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 03:27:27 GMT
ENV LANG=C.UTF-8
# Fri, 19 Nov 2021 03:27:27 GMT
ENV JAVA_VERSION=8u312
# Fri, 19 Nov 2021 03:27:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:28587b6e64756a60a354301d011190fb69ea1eed25d7a5180811dab252e16a21`  
		Last Modified: Fri, 19 Nov 2021 03:09:27 GMT  
		Size: 42.1 MB (42097812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1655352c888337fbd3af21c25aa26d4561a0b9b6035a8b22c9ee0c8ae9a3784`  
		Last Modified: Fri, 19 Nov 2021 03:31:40 GMT  
		Size: 13.5 MB (13511818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41504d6f293494b2f89ab687feed3da8d0eecd70cdc87fcfc38bf513314b627d`  
		Last Modified: Fri, 19 Nov 2021 03:35:34 GMT  
		Size: 105.9 MB (105895100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0b267252d7b6c7ee687436bb53d2c3cecd9350c7cdbf22de8be5cfc58f7ff619
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161218577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c49e5d7fa2d81e2c6a3bbf6a1a84f1b294770b6cc87a0caa72f438e7699990b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 19 Nov 2021 02:35:27 GMT
ADD file:31ec2bba02fab51f683553c78815a422089e6227bd4a65d33f35bc15588da3f7 in / 
# Fri, 19 Nov 2021 02:35:27 GMT
CMD ["/bin/bash"]
# Fri, 19 Nov 2021 02:52:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 19 Nov 2021 02:56:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Fri, 19 Nov 2021 02:56:28 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Nov 2021 02:56:29 GMT
ENV LANG=C.UTF-8
# Fri, 19 Nov 2021 02:56:30 GMT
ENV JAVA_VERSION=8u312
# Fri, 19 Nov 2021 02:56:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:c621c1ca8ceb7b3c3055633f5e537023039566ffcde238e41463f74eb6396051`  
		Last Modified: Fri, 19 Nov 2021 02:36:28 GMT  
		Size: 42.0 MB (42011387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d87024ee2f6936bf9ad81953e5ec643cddc67e7055ec11cf737242c60e2c9b`  
		Last Modified: Fri, 19 Nov 2021 03:04:14 GMT  
		Size: 14.3 MB (14300939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6a854a6aeaeef7555153d17594764bf0249541976c4758b9ae4895137ed295`  
		Last Modified: Fri, 19 Nov 2021 03:09:01 GMT  
		Size: 104.9 MB (104906251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
