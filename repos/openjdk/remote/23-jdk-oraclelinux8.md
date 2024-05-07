## `openjdk:23-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:0ebce76686ba69056566fee8da2e2c39f012867b017e5de317a83a8aa567523e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:289431cd01b98e34647ff0f8942bb7c3a4d1e0f23b11ce7aaeae9092ad358d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276208672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb26d3f92421068d52d034c5d5ff48b2c52c871a2ffa78d36908e2e5bfaf9ac`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 16 Apr 2024 19:54:30 GMT
ADD file:c53be7373aad45b6ab1d0accc144396269617e0efcd2892e9521c25fe73fd71e in / 
# Tue, 16 Apr 2024 19:54:30 GMT
CMD ["/bin/bash"]
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd37f6d992035c9959b83f8f96b15cac9d66542a608f378e6e97c17830b72d80`  
		Last Modified: Tue, 16 Apr 2024 19:55:43 GMT  
		Size: 51.3 MB (51320403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba07ce15eef9397ca8c80441e2da3f68d25591d8c38cc68976f04f5e98d555`  
		Last Modified: Mon, 06 May 2024 23:05:56 GMT  
		Size: 15.0 MB (15015695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c9587d3175724ed8221bb79314871768dbd3d568db439b10ef0caf000d4014`  
		Last Modified: Mon, 06 May 2024 23:05:59 GMT  
		Size: 209.9 MB (209872574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ae77a711e4f11872b5e5c4fcd5a12710a01a4a60513ba15415538c283006b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7aeddc4596ff227785eb3d4b9abe4f8818d29bfe494a370ecb69a2a96124d1`

```dockerfile
```

-	Layers:
	-	`sha256:0cefd90df6692dbe67f6ccfb219b60c11a202a24f1cd0aaad25aa65b7612b1f8`  
		Last Modified: Mon, 06 May 2024 23:05:56 GMT  
		Size: 2.3 MB (2267589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b1bd23de6403e72e11cba3e3fe95288cb622c11d21b4e6b8d99b78794c1952`  
		Last Modified: Mon, 06 May 2024 23:05:55 GMT  
		Size: 16.2 KB (16184 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2fd5b78ef490b766ee88d45dfac0d9531fb61fc68d23b34d1b07071f04857862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273534691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b446ff5ed795a0f12586607d828cfc3e739553df889dcd4e4b8eff0f2371a80`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 16 Apr 2024 19:12:16 GMT
ADD file:a0ae0c9fd36b325bb47e6dfda7b2f31a63d9b28ca3352bf4aa4aa8819940f1de in / 
# Tue, 16 Apr 2024 19:12:17 GMT
CMD ["/bin/bash"]
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c6a0976a2dbedfeb9ad1ab09e887e49a58ae8bc68480745fc5d1a97c201cda78`  
		Last Modified: Tue, 16 Apr 2024 19:13:10 GMT  
		Size: 50.1 MB (50082278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1cff57d28c1710a96ad0fd875e48d2d366fd897af56be5fdc8d3c8749947ee`  
		Last Modified: Mon, 06 May 2024 23:48:28 GMT  
		Size: 15.7 MB (15699245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ae5fbd0cf2952c7edb41e31d5612224a8b0827ae2a768479cf5558bda5e47`  
		Last Modified: Mon, 06 May 2024 23:48:31 GMT  
		Size: 207.8 MB (207753168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8425ef340f60642123dccd9c0ffb85cf65b3d07f6beb7e9a5d91883181fd2e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128b8e30c3a59a03a45155b2c65923ecb1e02979373e1ae0eaeca72d4587d76c`

```dockerfile
```

-	Layers:
	-	`sha256:5b72ec28b6388f5f48f8c89688057d874a384b43ba8417567f2ac695555ff419`  
		Last Modified: Mon, 06 May 2024 23:48:27 GMT  
		Size: 2.3 MB (2266993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e19830e5c7373af15d49931c35c50f8b95416dd9e3ca89571e7c8f7cf6b96dd`  
		Last Modified: Mon, 06 May 2024 23:48:27 GMT  
		Size: 16.2 KB (16198 bytes)  
		MIME: application/vnd.in-toto+json
