## `openjdk:24-jdk-oracle`

```console
$ docker pull openjdk@sha256:3086bce100d7e5a60d453bc4e0100b9d6745eaf5e169d3c1e284706bd53bbff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:53109ca4df8989f0e9b99028fcd2bddafe29cbc8d01ae74fc21f9ca215a20651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298197257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d444e96ecbee110a0d9ecd94cd45a532424d49b533fded25cb4074be98e0b4d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dac3e7a7894e1f152fef3ceea49f758a9134375e11651bfef76daabcbe30c2e`  
		Last Modified: Wed, 12 Jun 2024 00:55:28 GMT  
		Size: 37.9 MB (37862346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3983018790f8a4853f62b2c3e4f77564cea2d829393bd63ce4f2654b17347c`  
		Last Modified: Wed, 12 Jun 2024 00:55:30 GMT  
		Size: 211.3 MB (211340033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:292914f5cc6fea0c26678df52c4f06fe7975f7bdd4ff577714fdc686f0f569e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7feae9fee59972d43a9bf743ff6b5ddac11b957fb65198b7d6434563270dd17`

```dockerfile
```

-	Layers:
	-	`sha256:840fa447018054a17c07ec502938be29d2b7b3c9d13b71565d5f0375a8521a49`  
		Last Modified: Wed, 12 Jun 2024 00:55:27 GMT  
		Size: 3.3 MB (3333225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db05f006aa673c6b67f8cf1ce87bf0274b91a0ff0649ede120d5c7b353cd113`  
		Last Modified: Wed, 12 Jun 2024 00:55:27 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dd7c6028b974c418d53be2da62804679d2d1bd40d4221919914cbde89abaf781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295131743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5cdf3011367375ac6f195ad44651481697846c77b3169dba8246b4120f3e7d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4126ceeefbe5a1d06272578a6b6a99a1d422489b25511cbccbaaeb1576551bfd`  
		Last Modified: Sun, 02 Jun 2024 01:54:26 GMT  
		Size: 38.3 MB (38259157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0618ad044643ca31138a43cd8e7de71086151d7e9479f075a9c3daeedb0fc0f`  
		Last Modified: Wed, 12 Jun 2024 01:47:21 GMT  
		Size: 209.2 MB (209220595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5c72be83e6cec76372b88ecf4546a120f7554525a4b677ea0b79a3b8e4e39990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450c7de385bc3a0946fda90353889a36dfa035508844aefafdd7c25210644b43`

```dockerfile
```

-	Layers:
	-	`sha256:c4969f4f3ebd9c7e670fe34cb1b727403f5405d35241d0207d37c551c439e146`  
		Last Modified: Wed, 12 Jun 2024 01:47:17 GMT  
		Size: 3.3 MB (3331608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cdc44e9ad48c6c8ceacd45c56cb5cdc8c0892cb1358b20a16d888f6e4e465d5`  
		Last Modified: Wed, 12 Jun 2024 01:47:16 GMT  
		Size: 20.0 KB (19978 bytes)  
		MIME: application/vnd.in-toto+json
