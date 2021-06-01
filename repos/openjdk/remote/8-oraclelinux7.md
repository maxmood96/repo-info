## `openjdk:8-oraclelinux7`

```console
$ docker pull openjdk@sha256:4a8ce80c469197495a9b36ae73835051d36af29ebdbe50eb9fa9dff810e30345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:33b3c40d6367b54cdaf30c75cbf6fab68c9518ebe98f0bd5627292207a9197de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169514136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5b4243f56075eb6cac0d474149f1445406dd54d0e5b178f719b0a3354b3f5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Jun 2021 15:21:43 GMT
ADD file:6853efe982f87a3475099ab9aaa2ec9797afac58ee8dfc54d912b966bc3405ea in / 
# Tue, 01 Jun 2021 15:21:44 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 15:38:40 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 01 Jun 2021 15:40:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 01 Jun 2021 15:40:35 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jun 2021 15:40:35 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Jun 2021 15:40:35 GMT
ENV JAVA_VERSION=8u292
# Tue, 01 Jun 2021 15:40:44 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_8u292b10.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_8u292b10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:cbf629395cd4d267c366a2b3ac4cfbe6a6c5cfd5bdd8e89a7157e0901e898cf4`  
		Last Modified: Tue, 01 Jun 2021 15:22:47 GMT  
		Size: 48.3 MB (48260748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf25dc842172d49c0f45cec26c8fe86f7a083e2e5ce7a5e6d84d2b4cd2d46ba`  
		Last Modified: Tue, 01 Jun 2021 15:43:59 GMT  
		Size: 15.4 MB (15425936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79df5d355073f99b23a5c6445ea3726cdd19fcdc550b14efd9f513b5045f063d`  
		Last Modified: Tue, 01 Jun 2021 15:46:55 GMT  
		Size: 105.8 MB (105827452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:aaac029b46c9912c48aa4a9269e80c75f4cd503a0b2490530a106485da3683da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170157470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e53ab469c955f7099dac48425ccdcadd126d862273f46a50512e534bccb2fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Jun 2021 14:41:12 GMT
ADD file:3f30763d6f4fa6cd26708a9eda4872cc48b0c874b7837e0682ea4b4ed7ac5fb2 in / 
# Tue, 01 Jun 2021 14:41:12 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 14:58:49 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 01 Jun 2021 15:02:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 01 Jun 2021 15:02:17 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jun 2021 15:02:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Jun 2021 15:02:18 GMT
ENV JAVA_VERSION=8u292
# Tue, 01 Jun 2021 15:02:34 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_8u292b10.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_8u292b10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:5216e6356b12c39a03d420e358911905653d063185ac40b7250d625cfcd46024`  
		Last Modified: Tue, 01 Jun 2021 14:42:13 GMT  
		Size: 48.9 MB (48857508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0104ba284443f9b2819e0f98ad5efb21b57c2cf4d49bd3d3cbd1af4ad0ac2c85`  
		Last Modified: Tue, 01 Jun 2021 15:09:33 GMT  
		Size: 16.4 MB (16419323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862caf9432a395c8f9acea612d1ba7a7f2a0c67c26c2840ce024428079598cfb`  
		Last Modified: Tue, 01 Jun 2021 15:13:37 GMT  
		Size: 104.9 MB (104880639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
