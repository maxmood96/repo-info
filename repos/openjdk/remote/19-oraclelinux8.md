## `openjdk:19-oraclelinux8`

```console
$ docker pull openjdk@sha256:519d93095e7952798b540a1960e1c78f77311fcc6ffcbaa1ffef357cab52c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:a6966970810f6c2f34b55d4fbd20144ad6fb96a6eda8bd3b9cc13bc071e9d872
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250259828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2073b67200a16c55447494c12aa34171f493b77b51770adad3de04bbe94b7f09`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 Apr 2022 20:33:04 GMT
ADD file:9893213a9ea238f53ac68d87a3cf2f05d86763688392e5ddb6a2c9b60d3550a6 in / 
# Wed, 27 Apr 2022 20:33:05 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 21:53:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 27 Apr 2022 21:53:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 27 Apr 2022 21:53:12 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 21:53:12 GMT
ENV LANG=C.UTF-8
# Wed, 27 Apr 2022 21:53:12 GMT
ENV JAVA_VERSION=19-ea+19
# Wed, 27 Apr 2022 21:53:22 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/19/GPL/openjdk-19-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5920845cb577a0883cfbd0bc3a781b5b0a4f71b19a870525c653f9815fa0596b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/19/GPL/openjdk-19-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='ad9457964256d9d43d6246a0da743a73450231506d0a8a711e28b996b7e6e6e3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 27 Apr 2022 21:53:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:38a980f2cc8accf69c23deae6743d42a87eb34a54f02396f3fcfd7c2d06e2c5b`  
		Last Modified: Wed, 27 Apr 2022 20:33:57 GMT  
		Size: 42.1 MB (42114164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de849f1cfbe60b1c06a1db83a3129ab0ea397c4852b98e3e4300b12ee57ba111`  
		Last Modified: Wed, 27 Apr 2022 22:01:52 GMT  
		Size: 13.5 MB (13525123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fae6fb2bf0901ccf6a527aec217c7346d4be89c1cf3f6d39e4d8a7b0a565e2`  
		Last Modified: Wed, 27 Apr 2022 22:02:05 GMT  
		Size: 194.6 MB (194620541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:503c9415f334fe7ca4ae07228db9d342c3475e89a40fce461af1deb8c739bc1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249774164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e74ca5de824e37e89dc69966106193205e7f6bd24b8c8a3b8e3678089321edb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 Apr 2022 22:55:53 GMT
ADD file:6fef7a4ab2de57c438dad76949e7eb87cfb1ea6f45b0f2423f71188efdaa0d8e in / 
# Wed, 27 Apr 2022 22:55:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 23:27:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 27 Apr 2022 23:27:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 27 Apr 2022 23:27:36 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 23:27:37 GMT
ENV LANG=C.UTF-8
# Wed, 27 Apr 2022 23:27:38 GMT
ENV JAVA_VERSION=19-ea+19
# Wed, 27 Apr 2022 23:27:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/19/GPL/openjdk-19-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5920845cb577a0883cfbd0bc3a781b5b0a4f71b19a870525c653f9815fa0596b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/19/GPL/openjdk-19-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='ad9457964256d9d43d6246a0da743a73450231506d0a8a711e28b996b7e6e6e3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 27 Apr 2022 23:27:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:416105dc84fc8cf66df5d2c9f81570a2cc36a6cae58aedd4d58792f041f7a2f5`  
		Last Modified: Wed, 27 Apr 2022 22:56:57 GMT  
		Size: 42.0 MB (42018977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe66142579ff5bb0bb5cf989222e2bc77a97dcbd0283887dec04d5b9dfd48cfa`  
		Last Modified: Wed, 27 Apr 2022 23:43:32 GMT  
		Size: 14.3 MB (14294224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7646fc1e6df81252129875d4ecdbef7637f07fe9b5f7d5a2e97674d6ebaa8dcb`  
		Last Modified: Wed, 27 Apr 2022 23:43:49 GMT  
		Size: 193.5 MB (193460963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
