## `openjdk:21-oraclelinux8`

```console
$ docker pull openjdk@sha256:d8e325644d27ea9bbd8fbafec429c1ff87d89ebf0824858e8f251f38709427be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:a4e6c624d3d2eacb63e043a31204762a3609b7158a8f8316da37b995a52b6585
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258929745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e6f0b4530b07a48a81cbeeb66bbbd18734fb8678b8d3fb458bb52784bf544a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 24 Feb 2023 00:20:27 GMT
ADD file:9c8b13ccecebc19a9105d94b9b8060d87741d158a6de27ec96b14028de164443 in / 
# Fri, 24 Feb 2023 00:20:28 GMT
CMD ["/bin/bash"]
# Fri, 24 Feb 2023 00:40:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 24 Feb 2023 00:40:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 24 Feb 2023 00:40:14 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Feb 2023 00:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2023 01:29:51 GMT
ENV JAVA_VERSION=21-ea+11
# Tue, 28 Feb 2023 01:30:01 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='44d5639ae3005e8f6a494ab42506f7fbbe7c366a17c7da792bcaf21a04f5be13'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4f1bfbab4042464ed8c0b6e462354db5e97320b7c74d257639fc4c05d3ce4827'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Feb 2023 01:30:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b4ddc423e0463a3d58b6c40ac1d97a950af62e9db703bb4c9d55afad67394149`  
		Last Modified: Fri, 24 Feb 2023 00:21:21 GMT  
		Size: 44.6 MB (44556861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f918ee7b32337dedda10e8566b1e5d96678ad53c0527e878e3866a6f713189e`  
		Last Modified: Fri, 24 Feb 2023 00:42:24 GMT  
		Size: 15.0 MB (15015003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595610a8757d0a3ad4d0a76bf2d7f3db1e4754527ed36176d7e17953ca828566`  
		Last Modified: Tue, 28 Feb 2023 01:33:12 GMT  
		Size: 199.4 MB (199357881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:539169e08153598dc1eb11a8cdd739b1c6c485407dba28890b2467a6771deb4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257151036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3e8975a0e3b414bd8d55c31a1738b5676eca4e76c892fac773fcaab617e714`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Feb 2023 23:40:03 GMT
ADD file:b9db410ba951fb740a34187417442b96a27a7fd918b16023c16cb1b0777b292f in / 
# Thu, 23 Feb 2023 23:40:04 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 23:58:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Feb 2023 23:58:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Thu, 23 Feb 2023 23:58:52 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Feb 2023 23:58:52 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2023 01:57:40 GMT
ENV JAVA_VERSION=21-ea+11
# Tue, 28 Feb 2023 01:57:49 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='44d5639ae3005e8f6a494ab42506f7fbbe7c366a17c7da792bcaf21a04f5be13'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4f1bfbab4042464ed8c0b6e462354db5e97320b7c74d257639fc4c05d3ce4827'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Feb 2023 01:57:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf42ad2544e3a5379ea5e0050457e87df46409adba81dba4686a3efc595ccd2`  
		Last Modified: Thu, 23 Feb 2023 23:40:48 GMT  
		Size: 43.5 MB (43461050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2911a20ed1ec4cf4241519f3d97458f77a1eaded44c42d9ae79a999075ef4c`  
		Last Modified: Fri, 24 Feb 2023 00:01:00 GMT  
		Size: 15.8 MB (15838054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea441af366bd6a21882e8f44b87118d00337847ad39e17782decbfd4d836e28d`  
		Last Modified: Tue, 28 Feb 2023 02:01:04 GMT  
		Size: 197.9 MB (197851932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
