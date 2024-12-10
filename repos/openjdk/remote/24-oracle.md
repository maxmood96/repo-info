## `openjdk:24-oracle`

```console
$ docker pull openjdk@sha256:f2530d839790d60bd127239c9db568dc4cf7bd979aa37b65f35b7e67bda57a9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:8f50aca69e4ae4b2a0f294219062f5e72c7bd77a765cd61187fa7960b4288991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310597100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a962d6c899c98c937c90712bd50aef693b84c0bf2795fd33109aeaa1edd35c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fae50f56b36a6ef37e2d64967256eece8bc4241191f4bffd8cc53fc3376277`  
		Last Modified: Mon, 09 Dec 2024 23:31:01 GMT  
		Size: 48.8 MB (48765011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bca0abcf0f39f646e365e743e151008edf21a8d79acd485930909a203697e0`  
		Last Modified: Mon, 09 Dec 2024 23:31:03 GMT  
		Size: 212.7 MB (212733387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:50ee0f277b8ae6dc8ccf52ceddbf361d2a01d8d2dbe2a3a75223983989556c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4937412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe4d71c4214849417adc1477eaaf8eef7e75231a4e413187749d3340219816b`

```dockerfile
```

-	Layers:
	-	`sha256:52bbfc0dcecfa8b2b96d9d131829a05be6678eb39dbd2ce3bf32d3711b5f4dfd`  
		Last Modified: Mon, 09 Dec 2024 23:31:00 GMT  
		Size: 4.9 MB (4917666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a2783963a6b2909062836f09447d88ce067a06cb7721d48662f58fa5a487b0`  
		Last Modified: Mon, 09 Dec 2024 23:31:00 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3db4912bad40a54497b1012de25034bfda00dfd5a00318e600467e523d43e3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307555613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1a437c9a132ba975b65e8b7930fda0d9ae0eee9a38e8c013aaae93eea0d799`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 07 Dec 2024 01:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Dec 2024 01:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 07 Dec 2024 01:48:13 GMT
ENV JAVA_VERSION=24-ea+27
# Sat, 07 Dec 2024 01:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='99196f78561dace922e06c52af4d33157ded8ae02a8009f35ea2fb7075dda452'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='e78b5c2b599fd835fb88bfe9155b27e16dfcab3e0488bb63051c073acabd5cba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Dec 2024 01:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50730d7cdebc9dd971fe547b229ac9b36632531d0634a0903681766460bf2cf8`  
		Last Modified: Tue, 10 Dec 2024 01:26:17 GMT  
		Size: 49.2 MB (49196487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec434e8507dfa043f27fc3cda33331d949053a5a072673bd598f1aca4d83fad`  
		Last Modified: Tue, 10 Dec 2024 01:32:31 GMT  
		Size: 210.7 MB (210691734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5b6e9b5aad9557d1d1a11ec2d4f433204e145e3d478a46e9fa02ab7a2666a984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565af30f8393d7d661061745dd926095df16805da3076f8f17337f4e275d03d3`

```dockerfile
```

-	Layers:
	-	`sha256:191176c400d338ab25018a8709459e235fae393bf44eed65f8c739e562b9ad56`  
		Last Modified: Tue, 10 Dec 2024 01:32:27 GMT  
		Size: 4.9 MB (4915424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:138ff9cc3d8c570f829d9a8244b42f88a9fe1199ac6e5c546f821048c18f4f4a`  
		Last Modified: Tue, 10 Dec 2024 01:32:26 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
