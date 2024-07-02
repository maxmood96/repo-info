## `openjdk:23-oraclelinux9`

```console
$ docker pull openjdk@sha256:687801e9685052c75ddade251af9295a66f94a74d2a72f158f00c0e7404b1c43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:7d85d6356d6b8f7890d64d98ba9ea47d2c4ced5f98e72a9a31350c42c22349ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298157327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d32c8acbc7ab384ea9cd3cb76fafe49ff59bf0b8094b19f6a81ef4ef4f27db`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a523cc422854f5fe352c82d3c00dbe4242724550d6bce00ca506ddf79528443`  
		Last Modified: Tue, 02 Jul 2024 00:57:54 GMT  
		Size: 37.9 MB (37862552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab1f912018b0e1097fdf49845e3df2416c5dd41333f1697902f7ac1f7d29c3f`  
		Last Modified: Tue, 02 Jul 2024 00:57:58 GMT  
		Size: 211.3 MB (211301122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f543691b2a3ad7663c8b3074ac8a8f811cd681cf4467561e3bf072dc5da8c848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbad3968a36cea99d9f61b3bb6c722e58d3c23a99e3097e63169455402d9b5a`

```dockerfile
```

-	Layers:
	-	`sha256:99f7bb3cfeb63b08fd6f4f570177f41ef2ff18bdf9a33f1267b703dc78b3e753`  
		Last Modified: Tue, 02 Jul 2024 00:57:54 GMT  
		Size: 3.3 MB (3333244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98a7ac16d7077c9e0c7b1e52e24258f38b88a795d0cfbdab0adcac83c9bd8571`  
		Last Modified: Tue, 02 Jul 2024 00:57:53 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:83665cf4c7f316f76a093fd60b492317bafe1e78b765e4e0dc82f281c004455a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295077940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7a984ee775039e51303457e75f855cb03e87d4c3f0010665d1543317ed4a99`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ed45272c7719731d967108403425288bfe312d1a6e9b1c0035540ac6a1674`  
		Last Modified: Tue, 02 Jul 2024 08:45:27 GMT  
		Size: 38.3 MB (38256468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b2abd3226f5a6303548fc6461d37fc7ca9319a043206386a613c987675e114`  
		Last Modified: Tue, 02 Jul 2024 08:48:17 GMT  
		Size: 209.2 MB (209168706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:0ac0c31bd43e2480bcb164f7563a50534e6f8bd2c100fb1cc34547c0f4504c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d182c88dfd72ac44f01bac8638d560f8c53c5b2627c3c73c5fd9943ee70fdc6`

```dockerfile
```

-	Layers:
	-	`sha256:7166d48b543c2705ba132ce09e233c89f2384f965ab2ec28979b77563361383b`  
		Last Modified: Tue, 02 Jul 2024 08:48:13 GMT  
		Size: 3.3 MB (3331627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afdee68e1be924170b5fccfec9156cdc33931f260f85265ebe6d0ca5f501c122`  
		Last Modified: Tue, 02 Jul 2024 08:48:13 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json
