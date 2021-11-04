## `openjdk:8-oracle`

```console
$ docker pull openjdk@sha256:791a4056fc9d3f7d4059e2a8b1ada19c9e90d54ce7ee700deccb73e21bdf9f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:515922f221a7742315f3f84a976807f32db7c493906f3e502c02d31f7e2044fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161354460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cafe44c1f0403a6099f49df85529be50e6642a2a275545958888de8f2915dd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Nov 2021 22:20:09 GMT
ADD file:ee2c184d933cfe1848f54f94d92f5c14d073160b62ec403259b18392d4ec6e1b in / 
# Wed, 03 Nov 2021 22:20:10 GMT
CMD ["/bin/bash"]
# Wed, 03 Nov 2021 22:37:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 03 Nov 2021 22:39:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Wed, 03 Nov 2021 22:39:09 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Nov 2021 22:39:09 GMT
ENV LANG=C.UTF-8
# Wed, 03 Nov 2021 22:39:09 GMT
ENV JAVA_VERSION=8u312
# Wed, 03 Nov 2021 22:39:20 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:0a6167eaa66c8f2dc1c8dbed1a335f3d4052409454c9f7fbcd8fc35d8576a7e2`  
		Last Modified: Wed, 03 Nov 2021 22:21:16 GMT  
		Size: 42.0 MB (41968115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88dabbf57eeb24f57debafeba0a2f7b2f4e4e76d1aa9a3bd27edf0682e0f15`  
		Last Modified: Wed, 03 Nov 2021 22:43:12 GMT  
		Size: 13.5 MB (13491241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39d55b2d90c3349e5d2eef4213e2d3078bb9c477d9260c276cfa0a82ad1cabc`  
		Last Modified: Wed, 03 Nov 2021 22:46:52 GMT  
		Size: 105.9 MB (105895104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8a7cd22f7728e12e1bbef01fae50cc28d0f912a6c8071622c9642a66a20a5ef3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161059363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bc2939876b9b0acd364ee1cf567b5884410ca80136e191cdf7c12bb8d3f90b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Nov 2021 22:44:10 GMT
ADD file:42d3c96053f453ca6f7155adc565cd822cd2663bd2a3862ccaabb9886c191116 in / 
# Wed, 03 Nov 2021 22:44:11 GMT
CMD ["/bin/bash"]
# Wed, 03 Nov 2021 23:01:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 03 Nov 2021 23:04:59 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Wed, 03 Nov 2021 23:05:00 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Nov 2021 23:05:01 GMT
ENV LANG=C.UTF-8
# Wed, 03 Nov 2021 23:05:02 GMT
ENV JAVA_VERSION=8u312
# Wed, 03 Nov 2021 23:05:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:f6fe8bd1b591af20f7f1bf6cabe92846a2b5f1ba33ca5fd165cf03624558cd5c`  
		Last Modified: Wed, 03 Nov 2021 22:45:11 GMT  
		Size: 41.9 MB (41879080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f82d768d0f333fffcb86fe10bab796e393363d92953d26c9435077acb1598e`  
		Last Modified: Wed, 03 Nov 2021 23:12:36 GMT  
		Size: 14.3 MB (14274012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1327ea792772c011943338b89a7ca83d6b79c3c77c6f1367ee89ff4d387b76`  
		Last Modified: Wed, 03 Nov 2021 23:17:21 GMT  
		Size: 104.9 MB (104906271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
