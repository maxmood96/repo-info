## `openjdk:25-ea-28-oraclelinux8`

```console
$ docker pull openjdk@sha256:78abdf0010a36e1eee2c1ab00d31b383e8fdf316758b0c3bfafae6584f2ce4d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-28-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:1c61a7726ae0ad2aa052b2c5ceefd1e1ad23037fdb1c7bf5abdafa70d6311d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289757205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5b514a7be2c69cbe1f103fae9ee843bcdd372ac4fedebbc06a7dcc3d277b27`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:42:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:42:18 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 20 Jun 2025 18:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_VERSION=25-ea+28
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='ddd476f5dc6e80fc93f06ba240cf3537fd8aed344823abfd64c1cfe470f441b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfbc99aedd5015a5ab41d74f53972f7cb6616032c983216add8cf2de21a1fa5b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0915556054e5fcd1f04e454b0deedf305bb209616c5a72a8b2d83db9191e5115`  
		Last Modified: Thu, 12 Jun 2025 21:07:27 GMT  
		Size: 51.3 MB (51311558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346eb5d1457461f63ac76c75001abc05aeed484c40989be50d6a42c45fbd2641`  
		Last Modified: Sat, 21 Jun 2025 03:34:31 GMT  
		Size: 15.0 MB (14979310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6281df7a0b688b6d305bfe069d82d99420798589c4d18732efda47aead914238`  
		Last Modified: Sat, 21 Jun 2025 03:34:56 GMT  
		Size: 223.5 MB (223466337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-28-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:43bbeb700ca21b271b5fbd59eff93b18bb7aceb9d879370c011cb740ef2dd260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167955bc263ea252693becd78a901e880d7b4c48e505b2b2febb4e0529a70db5`

```dockerfile
```

-	Layers:
	-	`sha256:4f121c9e874350e000e405cf1b106e54a6310127edacba1a590f63d094decff9`  
		Last Modified: Sat, 21 Jun 2025 03:24:01 GMT  
		Size: 2.5 MB (2451706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417ca93c6405a1d368256bbef21124c4ae7ceb18366072590d32b33436fb045e`  
		Last Modified: Sat, 21 Jun 2025 03:24:02 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-28-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7911ffac4706a6f527ab0c26e4ae5948b9f6a2cb526cd5e18d48dd69f317b646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284211690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4630d8be6d521c1dd857b2726578513999f81d2a2d9bd7e14f73323f1958d6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:43:09 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:43:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 20 Jun 2025 18:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:48:11 GMT
ENV JAVA_VERSION=25-ea+28
# Fri, 20 Jun 2025 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='ddd476f5dc6e80fc93f06ba240cf3537fd8aed344823abfd64c1cfe470f441b4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/28/GPL/openjdk-25-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfbc99aedd5015a5ab41d74f53972f7cb6616032c983216add8cf2de21a1fa5b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d998890baf088acce50ef79f8e8dc3eab36a2dc008c7774fa6e1e1140c89c3c3`  
		Last Modified: Fri, 13 Jun 2025 01:08:32 GMT  
		Size: 50.0 MB (50039112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cddf61b157a492a5e9e87c2aa66c8d9d39517125432aef6e1db78ce8635515`  
		Last Modified: Fri, 13 Jun 2025 00:42:33 GMT  
		Size: 12.9 MB (12917586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce35bf1fdf3bdb13b72e8d329b378a555aaea8dd82c7c785dea34ee858d77e6`  
		Last Modified: Sat, 21 Jun 2025 04:20:59 GMT  
		Size: 221.3 MB (221254992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-28-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e6c53a52b59bd1ba9b12b6227098097f278663ff3cedb4d707e3ae432d3173bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d591c91e2a0eed96d768a4c3b08c3edc2046f6a5ab946b42735acdca458ac51`

```dockerfile
```

-	Layers:
	-	`sha256:c0a67fce0c36fa2942d149559ff9928e3d5a6f1bab1c5cad9ed78a2ed3161971`  
		Last Modified: Sat, 21 Jun 2025 03:24:06 GMT  
		Size: 2.4 MB (2436995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aca596e02b6a15a507eb392e42e501a4bf58effd0cb7374462e35b52caf2595c`  
		Last Modified: Sat, 21 Jun 2025 03:24:07 GMT  
		Size: 16.2 KB (16180 bytes)  
		MIME: application/vnd.in-toto+json
