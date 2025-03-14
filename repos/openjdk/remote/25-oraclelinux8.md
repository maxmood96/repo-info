## `openjdk:25-oraclelinux8`

```console
$ docker pull openjdk@sha256:2cf7d3a5ab57baa531b4088f49af499440de9d156c7e684fab52b7ab3b32a1ba
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
$ docker pull openjdk@sha256:b6c77f54c66e2c001f7ac5361d11529e57004777b2bbb7df539a03db6bf590b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275760462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763b9368bde8e22d1753741b94dd46562706b3d6c113b795b5669f50a4a6ae6c`
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
	-	`sha256:0e6d27d0384ed91610f17d7a9ef2bb948c3574306ac40526f54329f54140d2f0`  
		Last Modified: Thu, 13 Mar 2025 21:07:17 GMT  
		Size: 50.0 MB (49989436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69e77c2995841cd0e340bc286b91ceb1b42cf941fc975e2014d23fdda3f999b`  
		Last Modified: Thu, 13 Mar 2025 22:09:21 GMT  
		Size: 15.7 MB (15683725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62f55d9f46229089a701c9ff830647a9874879d7134bd81191fecdde493600d`  
		Last Modified: Thu, 13 Mar 2025 22:09:25 GMT  
		Size: 210.1 MB (210087301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ea79c821a9bd9a45ea4d9bc73b0cd1058c463d513b5c969f1a01546278f6e2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b2cd5512dd80a0e162993524ed829590159f2505dc1364827705a375b68c6d`

```dockerfile
```

-	Layers:
	-	`sha256:b8f445dad1f317cea792056deaedb5a06043510073e02aff1457becedde1c269`  
		Last Modified: Thu, 13 Mar 2025 22:09:21 GMT  
		Size: 2.4 MB (2439813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15211018196236091f761af21e4fa47724ddcf2d238fd9a4783dc067dbf946d5`  
		Last Modified: Thu, 13 Mar 2025 22:09:20 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
