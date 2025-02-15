## `openjdk:24-rc-jdk-oracle`

```console
$ docker pull openjdk@sha256:cbee40fe618e1e31c8695706f89c5ef0abb14259c0228a71cac8f86f308cefd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-rc-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:c523c191d7e471170f6a4184da41f07b579869f531865823e931c43f7c1db1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310696539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deea31ac117607ba80134d346eb1dc2f0d8b4ab32eb292d8ed6591fd5154da0c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43759093d4f6232b149ce0851c768f0287c95e1e0e34de29dac7c632ed93cc86`  
		Last Modified: Sat, 15 Feb 2025 00:31:02 GMT  
		Size: 49.1 MB (49090891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758b5cdc0820cd282118aa6035c71428802b729afa056fccb151397acccf0a`  
		Last Modified: Sat, 15 Feb 2025 02:10:02 GMT  
		Size: 48.8 MB (48768601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d04b07e7673fe63f27989699cac217c32fca630b277edca3b6b2e6a9186373`  
		Last Modified: Sat, 15 Feb 2025 02:10:06 GMT  
		Size: 212.8 MB (212837047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:73346847fd2bb9a7b8f07f733b2a3d03f9cfb9be048cfc1bb3c2bb567ce73fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7564c366311efb7099bb044c07cfc7977fb68702d0ba2cf04c527a34f93e7208`

```dockerfile
```

-	Layers:
	-	`sha256:d4a2100e9eb7b770519cfde2d824374c6061ab932bca9c5d7c1f81a23071f5cd`  
		Last Modified: Sat, 15 Feb 2025 01:23:16 GMT  
		Size: 4.9 MB (4909455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eda9eb3385d5fa1b05c68bc5d519801cdcfff2f99dd428c3fc59977266e7e06`  
		Last Modified: Sat, 15 Feb 2025 01:23:16 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-rc-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d4a7076dce6978cee80eef34e446cbd8b61617349af5bf647eb863d18c425b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307651734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d36ff4a2ab5cbe91ba2e331d9f67550a6e6656be316ba62f847f079e02fe9ab`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63067de277ccb20d99a5e9991dc66234bee83ce4c0d53f55d9f51995ad436f8b`  
		Last Modified: Mon, 10 Feb 2025 21:15:36 GMT  
		Size: 47.7 MB (47669546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e55e0b8b34ea5b3ba919ce4a6401eeba17103634f66be3d05c3f942cc693f8`  
		Last Modified: Mon, 10 Feb 2025 23:18:51 GMT  
		Size: 49.2 MB (49194060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27ede2ef31a0a006fd3b58ac657a29f1ad30becc262050f9e222a742da5da85`  
		Last Modified: Tue, 11 Feb 2025 06:52:00 GMT  
		Size: 210.8 MB (210788128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:3f7fe8a8c1bd89405d98331ef2e6601b270cb665b6542195eee1085a42b3302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0490355895e7db11a6fa68698f4f01d500415448097fa9c6a211c178285b6584`

```dockerfile
```

-	Layers:
	-	`sha256:818bc08ea752736b53beb19a41ed1f7130dd02afe75b266bb9d21d75eeee0ec9`  
		Last Modified: Thu, 13 Feb 2025 01:23:22 GMT  
		Size: 4.9 MB (4907121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46da155058db13adf74fa4b04674bba7f561232363b364be3d9f2b1ccb226539`  
		Last Modified: Thu, 13 Feb 2025 01:23:22 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json
