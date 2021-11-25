## `openjdk:8u312-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:15d0a7c66157ba22bf0029f952c6b937e1ea2a34a018ec1d45c39fa83de4c48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8u312-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:acfb381334c72e0f7bb37c36b8340df55d589879a2877446ee74e50759b780d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169613330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7b2335b1dc54032ccd4305edfa59f6d9c742e080daf2241370e25739464a04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 24 Nov 2021 22:08:59 GMT
ADD file:8d11c56c80a6b0631722a882ffccf6c4e58297273c4e164138c0f855a670ff79 in / 
# Wed, 24 Nov 2021 22:09:00 GMT
CMD ["/bin/bash"]
# Wed, 24 Nov 2021 22:28:21 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 24 Nov 2021 22:30:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Wed, 24 Nov 2021 22:30:34 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 22:30:34 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Nov 2021 22:30:35 GMT
ENV JAVA_VERSION=8u312
# Wed, 24 Nov 2021 22:30:48 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:4ade2748332d656c71c6288f12ab88613792b5c90b329ffdae521095f84faf66`  
		Last Modified: Wed, 24 Nov 2021 22:09:48 GMT  
		Size: 48.3 MB (48331000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6069e51d0239f313c0aee52bbfcdf9d451dba131643e5953161b601efac3d0`  
		Last Modified: Wed, 24 Nov 2021 22:34:59 GMT  
		Size: 15.4 MB (15388482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b458d766ad9baf442ce32527b5826441b3ccbcaa30bf1d1e4826f1578902f228`  
		Last Modified: Wed, 24 Nov 2021 22:38:03 GMT  
		Size: 105.9 MB (105893848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8u312-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5fe8697860043e3ad5827b9cf6eaeab8d59dc578db4827e9862b83b506bf73f4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170278718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce9ddd4392dba51d9fb1848985b36a7fddac337e80e879e8f117c4bec6f3cea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 24 Nov 2021 22:01:36 GMT
ADD file:718e42489681d6e9446ec4bb10ba8e24c85d645eb9a303e587f767bedcf668d1 in / 
# Wed, 24 Nov 2021 22:01:37 GMT
CMD ["/bin/bash"]
# Wed, 24 Nov 2021 23:34:39 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 24 Nov 2021 23:38:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Wed, 24 Nov 2021 23:38:44 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Nov 2021 23:38:45 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Nov 2021 23:38:46 GMT
ENV JAVA_VERSION=8u312
# Wed, 24 Nov 2021 23:39:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:53ff3b63a7657067cd7642c8106127a05a5ea45e3b68cbf830d4120a127e9c82`  
		Last Modified: Wed, 24 Nov 2021 22:02:31 GMT  
		Size: 48.9 MB (48907823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef6b8fb533810fdc95b689d95dd39d5a3f59cb3d3147fddf5bbdf7df183774b`  
		Last Modified: Wed, 24 Nov 2021 23:46:39 GMT  
		Size: 16.5 MB (16464628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672f3ebd21414dc870a92688c2f26801968369acf8022dfcf9e9f60ea291c5bd`  
		Last Modified: Wed, 24 Nov 2021 23:50:31 GMT  
		Size: 104.9 MB (104906267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
