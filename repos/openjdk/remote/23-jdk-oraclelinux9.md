## `openjdk:23-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:7f1f3197dee9f81b54db7d97765e46b7b2c3d1f9ef4ea5478f5fa8605d0e116f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:98cf64d706845d928540cc01a1db7656010b41eace830d6ad62412139c87320d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296766378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d8e4045837982a129377c0a91c4cb9c237d0e6054e8d057798c47ad348705e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 18:48:15 GMT
ADD file:95cf7039855dd392d2faa5bb16415fdb79680afe50aecf7c299b8b2dd377328e in / 
# Thu, 09 May 2024 18:48:15 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fcbdc4090331ae224779b095ccebf7fa4fd896fb807b7d6bdb37776132e9710f`  
		Last Modified: Thu, 09 May 2024 22:31:50 GMT  
		Size: 49.0 MB (48998671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2a314d9887d1e4006fd4fb544fb1fbfd091992a79adf007b72460fa5ed7b13`  
		Last Modified: Fri, 10 May 2024 00:51:56 GMT  
		Size: 37.9 MB (37862337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a6b3472b2139ed2b1edfe18a7222a85ce7ecca167e82ea290701a6f3636f9`  
		Last Modified: Fri, 10 May 2024 00:52:00 GMT  
		Size: 209.9 MB (209905370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:d3f35ff7d7a0beac1671cf742600a8d52cb1c3ee765c2236a555ad65f15cf0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3353113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ad10db1cfc9a9b5af3f2f944e883ed66ba1d6d8b259189ce5bb7f58d2a7b89`

```dockerfile
```

-	Layers:
	-	`sha256:4a6caa97271757286b65e94afd43e23f26b719f88a9fd37007dd4f2c1c92829f`  
		Last Modified: Fri, 10 May 2024 00:51:56 GMT  
		Size: 3.3 MB (3333220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd2eecbfa451374dde47fe91d1f717d12c6fc6c7f8f2fca9d1f4a792af7cf98`  
		Last Modified: Fri, 10 May 2024 00:51:56 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8e0244c35f97e1b6a73722347e2de17b40b3eeddc243ea7e5e0d99bc06792a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293701170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d8bfec162c1fc4a53e2898605aab031d2cbc45eff11b00d1c14c02223abfc5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 May 2024 18:48:15 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Thu, 09 May 2024 18:48:15 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a4be78b09aad15f916c85a97d9c9410e09e7e9b619c370b687ef5f9e20a44d`  
		Last Modified: Thu, 09 May 2024 23:52:47 GMT  
		Size: 38.3 MB (38259792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e16324649ff2078771a0c4462393a30105723fa51d90ce9fef72725b1c19ba`  
		Last Modified: Fri, 10 May 2024 01:13:47 GMT  
		Size: 207.8 MB (207787578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:c58d455ad155b111b5f17127be582667a6a8dfb0852c5d76422047699b9a7c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d2b2c847ff5babc9aeec86852580d82bcc6f14cfada32d25bba7ec3f634425`

```dockerfile
```

-	Layers:
	-	`sha256:7b872bed7a7fe783a55891443a095bda9d8c36086dd4b8b338aa40ad902b861a`  
		Last Modified: Fri, 10 May 2024 01:13:38 GMT  
		Size: 3.3 MB (3331418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59cb15adf6ff03ba4b31939ea60e9e5f71c1e90eca427772b7191f2463eafadd`  
		Last Modified: Fri, 10 May 2024 01:13:37 GMT  
		Size: 19.8 KB (19764 bytes)  
		MIME: application/vnd.in-toto+json
