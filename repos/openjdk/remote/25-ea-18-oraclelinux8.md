## `openjdk:25-ea-18-oraclelinux8`

```console
$ docker pull openjdk@sha256:b0ab9f0c0d17132a7464e765d4495f65ea04d4f568c6201b0a19240aa831b9aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-18-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:4c25308de150edff7e9c7fc125a87a66b6e1d3e630d4e3a6daa41b612384714b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278611095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05badb293ef0beb8ece8cd88371732bda7bb2224a05968e878afc1251d019489`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Apr 2025 00:24:58 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 01 Apr 2025 00:24:58 GMT
CMD ["/bin/bash"]
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:079caf22b235d19accaab46f0177ccda24bfe8b1c7622e0cd0cfa34e087ba3ad`  
		Last Modified: Tue, 01 Apr 2025 17:12:53 GMT  
		Size: 51.3 MB (51287468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bfd30413d7cae739f2324937a2e0f73c4abbc07d88a0429cf6a3d3c7d2f945`  
		Last Modified: Mon, 14 Apr 2025 22:59:16 GMT  
		Size: 15.0 MB (14987332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693d85487343a201b39f969b2099a8bbbdd78998777486d2ab505cf932c3c8f`  
		Last Modified: Mon, 14 Apr 2025 22:59:20 GMT  
		Size: 212.3 MB (212336295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-18-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c9af344cf41f6105f7e0f2dfce7e0ea3e1eba45a1bf620dee25038d18e650443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ea4bb318139fc7e7d658734dfa9b1bbad00a4a3125702ca32d16d195978665`

```dockerfile
```

-	Layers:
	-	`sha256:5a7d23aa3fa47f2fd5d229a3b4dc08ca93a62293cfb5db8ca78e4fcd094c9725`  
		Last Modified: Mon, 14 Apr 2025 22:59:15 GMT  
		Size: 2.4 MB (2442869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9159b6f87c9975594f42c40b143c9d762b9c3f33b3e019a10bc9debea424f00a`  
		Last Modified: Mon, 14 Apr 2025 22:59:15 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-18-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d36b0075a566a0a1a24c95a348f9fb831c8fbc27782015145557f72cbea2ad02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275844959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f23198aeb2aeb34ffb88df9288bd74ae95c2d789a3dc60cd73872d23162983f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Apr 2025 00:25:48 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 01 Apr 2025 00:25:48 GMT
CMD ["/bin/bash"]
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4489284649094031c9d59de175b95cba54b287149fda3f89f7719455b8603092`  
		Last Modified: Tue, 01 Apr 2025 19:38:33 GMT  
		Size: 50.0 MB (49996692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285b648462667f633c7ba37dc32d609732fbd0fbbbc03f430ded3f8244784199`  
		Last Modified: Mon, 14 Apr 2025 23:00:00 GMT  
		Size: 15.7 MB (15686765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbcd23c8097991a4e6fdcd6e8c2ed45d59f42f02a716dd9af334293b17636a7`  
		Last Modified: Mon, 14 Apr 2025 23:00:09 GMT  
		Size: 210.2 MB (210161502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-18-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a1a3ef37f73e87790e2c8976c13fe738cc8e35f6ac4e8c8305d6268a78a8d059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39d09a14202cbb64d5f1398d450a6d90dc31dda3d8ceea5b537fcd78309984e`

```dockerfile
```

-	Layers:
	-	`sha256:4f6025ce7790d77c7b03d8d9fdd260beb954b65f76cf2b96bddbfcc6a2f799c6`  
		Last Modified: Mon, 14 Apr 2025 23:00:00 GMT  
		Size: 2.4 MB (2441715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fca6827a6159cfd95d9eae3f4f070cbd9a646d0d04acba1862ec725ce5b3d34`  
		Last Modified: Mon, 14 Apr 2025 22:59:59 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
