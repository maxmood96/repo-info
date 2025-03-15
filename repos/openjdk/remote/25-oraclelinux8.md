## `openjdk:25-oraclelinux8`

```console
$ docker pull openjdk@sha256:8de280403d7516e263721f45d8e872d6532f9486a3c3e23ea877d99ab6cc3da2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:0327e991e24461bb8f3c0843c91bb729a42e17e22b83393ed7fee6ddf12422ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278419316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719d9060abf250fcb29220ec4057f9ec53a072a92777f19730848a17bc6aaa49`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 08 Mar 2025 01:48:16 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["/bin/bash"]
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 08 Mar 2025 01:48:16 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 01:48:16 GMT
ENV LANG=C.UTF-8
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_VERSION=25-ea+13
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='456a1dced4795cf35e28459b6289a9eb1d6921f83c79cf460c5c694cb52e11ba'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='518a0d1c64c68f4563c167e052f135827c1b218933dd68a481a7973694fc64b2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:035e56311411a7644fa1341dfc093e1b278feac7d55c98ae09177e1755672600`  
		Last Modified: Fri, 14 Mar 2025 19:00:09 GMT  
		Size: 51.3 MB (51288940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8762ebc7b66332cf60eb6714b7c1a896f56ddb9c00953a7e47328b37b0b01383`  
		Last Modified: Fri, 14 Mar 2025 19:09:08 GMT  
		Size: 15.0 MB (14996352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1744bb7bf3a6ec2c2d688cd4ed8ea8477699199b73f3d484f4d5320460271f`  
		Last Modified: Fri, 14 Mar 2025 19:09:11 GMT  
		Size: 212.1 MB (212134024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5bcaa942010e789f8e7858276a075289f650de984cc228a743442bce920dd02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faae1ee868c41887b8b09aec1f711b2e2931e33b2f7b41e4618690a06169c87`

```dockerfile
```

-	Layers:
	-	`sha256:69496d5a63f018b5ef28f42c192dda5b046f821b3b1fc9bf36c6162ae7388af5`  
		Last Modified: Fri, 14 Mar 2025 19:09:08 GMT  
		Size: 2.4 MB (2440967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c63a271b712aaab2e986bdf22fdf5be42a075c2a043345689ae5c969b08ab20`  
		Last Modified: Fri, 14 Mar 2025 19:09:08 GMT  
		Size: 16.0 KB (16035 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ba321f6613536e75112996c0acf02ba9478f1e34c615cdb9a4f3952203f81c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275752727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e96db18f3874e8bc2f83fd4322a77f81fa50aad1f7e1a5412112723a35e0b7`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 08 Mar 2025 01:48:16 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["/bin/bash"]
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 08 Mar 2025 01:48:16 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 01:48:16 GMT
ENV LANG=C.UTF-8
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_VERSION=25-ea+13
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='456a1dced4795cf35e28459b6289a9eb1d6921f83c79cf460c5c694cb52e11ba'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='518a0d1c64c68f4563c167e052f135827c1b218933dd68a481a7973694fc64b2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f8eb825c1fc22ded5eda8a11c91fd13cd2b63722a0fdbe5ed89339ba10aabad`  
		Last Modified: Fri, 14 Mar 2025 21:52:22 GMT  
		Size: 50.0 MB (49989226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4c823150405b1ef7ccbc1dc0f1e827fe6ed012030d38106e8e85863c6e52ef`  
		Last Modified: Fri, 14 Mar 2025 23:48:44 GMT  
		Size: 15.7 MB (15683327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe400ff1244e38ea59df1eadfed969758c43b4429e00ea8911897afe7ab2a41b`  
		Last Modified: Fri, 14 Mar 2025 23:48:48 GMT  
		Size: 210.1 MB (210080174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7e783c485c999d8278d00e1a476babd107173f7c1bf48377c2965e24b0b24a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7537caabda49118581294e69051aa86a74eff6e10bf06b5ac34288c7d0c04c5`

```dockerfile
```

-	Layers:
	-	`sha256:4712aeaccaf78de62bf2a0e3725526e3124df5aec1395ad86b213e86356b720f`  
		Last Modified: Fri, 14 Mar 2025 23:48:44 GMT  
		Size: 2.4 MB (2439813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1506e9bd5e25ed113dd040b91f8efb8ea28ced20f0ed491b0adeaa08d69ef1db`  
		Last Modified: Fri, 14 Mar 2025 23:48:43 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
