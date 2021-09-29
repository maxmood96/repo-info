## `openjdk:8-oraclelinux7`

```console
$ docker pull openjdk@sha256:9d713c2d47a2f2ea2a5b016d86bcb3ce90c2fae8b3de974f474082edca375922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b3aae77c799c9dd2acdb49ada58b02e7215fdc54c5c4aea2f18bd0378f12dc68
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169557333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a1ec00496c342fc40ad746445f989cc474f0b4fa5bce45850c479ac4fa9f1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 29 Sep 2021 16:28:42 GMT
ADD file:a9e7957ff3541c254a266620f438cb7ec181b31d50f939d0e687716cefdc7cf8 in / 
# Wed, 29 Sep 2021 16:28:43 GMT
CMD ["/bin/bash"]
# Wed, 29 Sep 2021 16:54:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 29 Sep 2021 16:57:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Wed, 29 Sep 2021 16:57:55 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 16:57:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 29 Sep 2021 16:57:56 GMT
ENV JAVA_VERSION=8u302
# Wed, 29 Sep 2021 16:58:05 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_8u302b08.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:2294629c97e56d38612a31e50aa9a544bb9ea9a60646d016dcde035fd309dfe8`  
		Last Modified: Wed, 29 Sep 2021 16:30:26 GMT  
		Size: 48.2 MB (48241319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa27d00ff441932dc4be9fc9662577510adff660e4486fa443768e0ca6d260e`  
		Last Modified: Wed, 29 Sep 2021 17:03:16 GMT  
		Size: 15.4 MB (15433173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cad29576c7ede36eb34575e3df393a8f5ed83800675617e84ca2f6eb7b3d9b`  
		Last Modified: Wed, 29 Sep 2021 17:09:32 GMT  
		Size: 105.9 MB (105882841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d75166310e71f147163eb19e8a651c445ff26c384623024027e6077e76f2de42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170161049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f530d1aecbb0c33d34680cfebf092432e62cb3e8c5db30c6e6ff6a7ab9b81b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 29 Sep 2021 09:28:50 GMT
ADD file:affde62a0aaf80f490cc93e1f691166a15a32c6ef6bc21af35a6659d24c8b6ef in / 
# Wed, 29 Sep 2021 09:28:51 GMT
CMD ["/bin/bash"]
# Wed, 29 Sep 2021 10:14:29 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 29 Sep 2021 10:20:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Wed, 29 Sep 2021 10:20:21 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 10:20:21 GMT
ENV LANG=en_US.UTF-8
# Wed, 29 Sep 2021 10:20:21 GMT
ENV JAVA_VERSION=8u302
# Wed, 29 Sep 2021 10:20:46 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_8u302b08.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:2f5eee715870559160403451bcd7b891478e0df052b7f9456144f3e89e5b994f`  
		Last Modified: Wed, 29 Sep 2021 09:30:28 GMT  
		Size: 48.8 MB (48828923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101207ebea4e1f8fc9adeec0fe8c82c5b0639e2e9c6f0f0bf26e459dc1665d66`  
		Last Modified: Wed, 29 Sep 2021 10:30:47 GMT  
		Size: 16.4 MB (16438786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1787929a59978b30c708917ad04cf4e5ff6a4589466edba061bc74db8038255b`  
		Last Modified: Wed, 29 Sep 2021 10:38:36 GMT  
		Size: 104.9 MB (104893340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
