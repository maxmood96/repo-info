## `openjdk:25-ea-13-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:5caeb31d31a551a6a8300dc33a69f2f4beb0feb8685afb666f42ec447995f65a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-13-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:2ebdc30ddd257053e6204c7387ee1e1bbb3cef9afcf42b6dbc8087593bdbea58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278417983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9203e37723e517bf89e98c3afec2b28d1bf9315c71ccba69e86c0b202eebb8d`
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
	-	`sha256:b9eaa108e19c50f27b324537cc9caf3425a1bc778f71bb2fd855bc5db74356e2`  
		Last Modified: Thu, 13 Mar 2025 21:06:47 GMT  
		Size: 51.3 MB (51288479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2624939974a83a76fe938e56c6ac75b4a562b5b934cd62040873f6c4c7730`  
		Last Modified: Thu, 13 Mar 2025 22:09:47 GMT  
		Size: 15.0 MB (14995586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fce1512d6fc2f0a02c2195205299bcf321c8cf769b852a20503867a814c628`  
		Last Modified: Thu, 13 Mar 2025 22:09:50 GMT  
		Size: 212.1 MB (212133918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-13-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:fc022059cd0db6fd683b6ace4fcba8f565622f9098533e2f2808900dc31ff81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a956b7be48b87ad499f79d2de03086caa89991f2c3783fd9a632ffe872b7beb1`

```dockerfile
```

-	Layers:
	-	`sha256:45d12780535fb32c8907751accf920e95b5df8aca3564334a23500e41905a59d`  
		Last Modified: Thu, 13 Mar 2025 22:09:47 GMT  
		Size: 2.4 MB (2440967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f6f690cd870e00d6f1a10d44429c160c8c761c11583bbdc7ba8ef030b8d2e40`  
		Last Modified: Thu, 13 Mar 2025 22:09:47 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-13-jdk-oraclelinux8` - linux; arm64 variant v8

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

### `openjdk:25-ea-13-jdk-oraclelinux8` - unknown; unknown

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
