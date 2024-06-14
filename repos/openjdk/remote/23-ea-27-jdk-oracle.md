## `openjdk:23-ea-27-jdk-oracle`

```console
$ docker pull openjdk@sha256:4389ae294409a648d08d7d5aede532e569ca32a7cf30c3e8f38f24145239e549
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-27-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:9900b7c3c04ee49ef8b41de47df98b44faf35e9da85c49a6a6c3ae61be61c505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298125085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad68eccd0a68696ad008887610b4f061a82110c93dc77560b79f08bb8edcf4a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3438ace9b700899918a4d7fa283bc2a9c9444b4e13d6030a796e0acaedc9344a`  
		Last Modified: Fri, 14 Jun 2024 01:01:21 GMT  
		Size: 37.9 MB (37862545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ffa77baeabed864482cf37cae3a8fad33fdf2ecadcbdd2d8c561abe716ff97`  
		Last Modified: Fri, 14 Jun 2024 01:01:24 GMT  
		Size: 211.3 MB (211267662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-27-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6aeaffa40915da6dc0489339b525ccb67c5ab7e494a702cae9c9c988f6fa18bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370a75e9258dc718b60debea759b1e5ade99e95fa582d524a2dde0111e8903b5`

```dockerfile
```

-	Layers:
	-	`sha256:3f69901d198c7b7d7d9c76696d1d4a45d4f9a0ea04aeb8d4d130b1d3ea434604`  
		Last Modified: Fri, 14 Jun 2024 01:01:21 GMT  
		Size: 3.3 MB (3333243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd51c1d1d4a5d218b6caa105ac0f2176f31d7287949e9a4a71a64400e6bee02`  
		Last Modified: Fri, 14 Jun 2024 01:01:21 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-27-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fc06c6d54051daa35fbb898d23213a39040884437bdfdbb760c1576a633f6535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295064098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c9163652c7120bb9ce439db65d5a09566b71e8eb3821a8a82c046a94ff0d0b`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 13 Jun 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+27
# Thu, 13 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='eb59f2d5cf2c02ad25096fde5f25de34e18f9404effb811ef08c38de667d96a2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/27/GPL/openjdk-23-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9156c3cb3861374cf11e8f8175a0a129a0e063ff39a58b83123ca817758982'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:48:11 GMT
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
	-	`sha256:90424573fc8c144ff5249d39aae6a2d2e035f37793b4e3c0ca7f9e4d5aa015ed`  
		Last Modified: Fri, 14 Jun 2024 04:10:00 GMT  
		Size: 209.2 MB (209152950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-27-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:930a7bc1cea1b1e4dd832d7bf8504d5278e9062d6fd22cc42cd4485b2d6a7664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af084258555680edfb25dcd65e1c091e918e46f9b49078006708b98c43de675`

```dockerfile
```

-	Layers:
	-	`sha256:7e1360cdc9177fdf122a6c16cfed2ed836316dfa2d1db227ee755df42f3d4600`  
		Last Modified: Fri, 14 Jun 2024 04:09:55 GMT  
		Size: 3.3 MB (3331626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a49364ed681df37d96b067a795becc43f07f96ff1bd91fbb7f429e38eb6afc`  
		Last Modified: Fri, 14 Jun 2024 04:09:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json
