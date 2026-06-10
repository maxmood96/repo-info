## `openjdk:28-ea-1-oracle`

```console
$ docker pull openjdk@sha256:938347fbb1ca2fdb41c51bd1df0721faa76eeae21e8972450605656db385bed8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-1-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:092ad86b9fc2fdaf3955d7f30b8985c06804d8e12e42add329064486e485d556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307793454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e398da793db8d5cdb458d4b142ebcc8315bf2417478b114dfcf1ca8432b22162`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2026 20:16:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 10 Jun 2026 20:16:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Wed, 10 Jun 2026 20:16:29 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:29 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:29 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:29 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3a091d5bf5b9502925e9432eb207c1e269cea76781504abe4ffd9be89d00a5`  
		Last Modified: Wed, 10 Jun 2026 20:16:52 GMT  
		Size: 37.7 MB (37687689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e612be402a1f97457f0ff44cdfba0879958f85287bd20ed6ef04ffb7340c61`  
		Last Modified: Wed, 10 Jun 2026 20:16:59 GMT  
		Size: 227.0 MB (227025183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b13bd0cf7b159c3e2b23a249b3a0dfcd31396c1c9708ad02a11832d1e6b98036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af8b7fef2bda17054befe0ecc542fa216acd8d1c06dc099b33ed1c58600fe1f`

```dockerfile
```

-	Layers:
	-	`sha256:3644e1b3b8082f138c69cf5ccd4a6c62783c37b5bfa96088eecd6894f605d634`  
		Last Modified: Wed, 10 Jun 2026 20:16:50 GMT  
		Size: 2.4 MB (2366442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0f629ca202dac09e735bf63f81efc0d6812965b7b632bb7cb6e477816648a92`  
		Last Modified: Wed, 10 Jun 2026 20:16:50 GMT  
		Size: 17.8 KB (17828 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-1-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:20b1d1b42b945ab2a8e7ea27be70668e87965fcd455026135fa417c8f4e68dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304181662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d36397dde5fd3050f037bd964b55271df3117ef2595832472cf0ec9485c84c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2026 20:15:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 10 Jun 2026 20:16:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Wed, 10 Jun 2026 20:16:12 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:12 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fcf0680d775f190e076763c19c1adb68b65a9decebf73c200e4f214b1bc363`  
		Last Modified: Wed, 10 Jun 2026 20:16:35 GMT  
		Size: 37.7 MB (37695966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d149bcac8c1193d9dadfe6075d2599b1dc6987f325aa6a5ad1dc73012acdcb29`  
		Last Modified: Wed, 10 Jun 2026 20:16:39 GMT  
		Size: 225.0 MB (224990001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:68d646933bc1fea93857bbcc14c9f97e186587944cb25ce260f2c89ab36a4750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6b858552d02644b46c2ac5e63ceb8e3e7072d1365d7c29fe7bb76634e8e143`

```dockerfile
```

-	Layers:
	-	`sha256:fe886f602ede219d9c08eeb25b858d2c22eeca534b595a08e8f6a96f8d29f50f`  
		Last Modified: Wed, 10 Jun 2026 20:16:33 GMT  
		Size: 2.4 MB (2365970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9c35f6fe368b799a9be8a8dbc25cf35519cbf3ec4eb3b39ae96bcd17316536`  
		Last Modified: Wed, 10 Jun 2026 20:16:33 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json
