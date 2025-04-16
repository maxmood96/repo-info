## `openjdk:25-ea-18-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:218907585db0423f6a5f01a1803ba20cb95d13987550ebbbbecfceb5799ad8ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-18-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3f7e3e38b18ffc69ccb5827c5409b50d97df58591434005c7e9f62fe7e4a995b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278666913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799d274b55095dbd14303a5a53a1fbc3069643dcf3017661e781da386ae3ed56`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 12 Apr 2025 00:48:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
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
	-	`sha256:6f3b2ad924e7ca97331fdfa1452577e2714860bf1ca5f6771b23be815f3ec81c`  
		Last Modified: Tue, 15 Apr 2025 21:51:32 GMT  
		Size: 51.3 MB (51312414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e771eaf75d43bf28293aad16cb4f301dfccd2cc475b8761fe39215faab3fcd`  
		Last Modified: Tue, 15 Apr 2025 21:54:22 GMT  
		Size: 15.0 MB (15002402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812a2bd9dc4147954a32b309dd257ea21d0123d3db731d858bf25b25e89b0ac4`  
		Last Modified: Tue, 15 Apr 2025 21:54:25 GMT  
		Size: 212.4 MB (212352097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-18-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:71f5edfd3539959193d367b020783c0eaaba6dda930865bac36a29458e7dd6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd1b54402488ef69c0a712e817b26b2cf249fea30321c2775e8db056ba67e91`

```dockerfile
```

-	Layers:
	-	`sha256:6d0859cbc7e14a4a3e712393be5b1f481faa3e2314670e314ff5f145083ec1ad`  
		Last Modified: Tue, 15 Apr 2025 21:54:22 GMT  
		Size: 2.4 MB (2442869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0211c9e440cdbd406e1c73b97c5440cb9d32cdca39304c07476c09b914f30600`  
		Last Modified: Tue, 15 Apr 2025 21:54:22 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-18-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9102f5a2734ffd0633799d0c742aa6d9798cb76aa8952e4680d45c5fcb2178d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275859092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3473d924cd10f2f9e39d847789b96dbdb1d0b6896c048cd4bb917a797b5b1b9`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 12 Apr 2025 00:48:17 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
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
	-	`sha256:321e78d03edef700126a05493206e74311bcaec7bfcbffcdb1632706eeb5635d`  
		Last Modified: Tue, 15 Apr 2025 21:51:19 GMT  
		Size: 50.0 MB (50020274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd1f69440985768661d39f21920c1138fde7a0693e9d51d5a207dfc34788b6`  
		Last Modified: Tue, 15 Apr 2025 21:58:35 GMT  
		Size: 15.7 MB (15675726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503ff062208ab53c7b67f7af9367cee2f81f6783d4462305441654e2681f31a7`  
		Last Modified: Tue, 15 Apr 2025 21:58:40 GMT  
		Size: 210.2 MB (210163092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-18-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4184385d4773ad99086b8a4003175440a0117d4a6b0541846e99e3a660f1d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db20c98b1ecb095e14381aa85193d5352b8866b5655256357c410eb01c17506`

```dockerfile
```

-	Layers:
	-	`sha256:cafd72fa1bf96c1e369628c8de3e47569a25b3556e299f9225db329c454b56e5`  
		Last Modified: Tue, 15 Apr 2025 21:58:35 GMT  
		Size: 2.4 MB (2441715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ca22b914f97bc073a975319c6a29a4ccd73babbf8c9dbc1dd8139ab4c98d13`  
		Last Modified: Tue, 15 Apr 2025 21:58:34 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
