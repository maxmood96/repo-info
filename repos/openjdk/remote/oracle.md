## `openjdk:oracle`

```console
$ docker pull openjdk@sha256:1a0c226b355ed06015a600d39cb16de62d372337752a998271cb8278e703f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:98f0304b3a3b7c12ce641177a99d1f3be56f532473a528fda38d53d519cafb13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243167391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e28ba2b4cdb3a7c3bd0ee2e635a5f6481682b77eabf8b51a17ea8bfe1c05697`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 Apr 2022 20:33:04 GMT
ADD file:9893213a9ea238f53ac68d87a3cf2f05d86763688392e5ddb6a2c9b60d3550a6 in / 
# Wed, 27 Apr 2022 20:33:05 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 21:53:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 27 Apr 2022 21:54:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 27 Apr 2022 21:54:18 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 21:54:18 GMT
ENV LANG=C.UTF-8
# Wed, 27 Apr 2022 21:54:18 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 27 Apr 2022 21:54:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 27 Apr 2022 21:54:28 GMT
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
	-	`sha256:a7203ca35e75e068651c9907d659adc721dba823441b78639fde66fc988f042f`  
		Last Modified: Wed, 27 Apr 2022 22:04:15 GMT  
		Size: 187.5 MB (187528104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d54ae710d5f8fd20e788796f6c1c9f3436bb54b8bcd31affd9220e57135fd425
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239931514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819ff7c55acc27b6897202f4a90df4bef5c24c2533e772702c66b61952317555`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 17 May 2022 22:52:38 GMT
ADD file:263fe8ce0663428b324fa2909814084a77bf17118d772058d41546b804a4b968 in / 
# Tue, 17 May 2022 22:52:39 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:12:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 17 May 2022 23:13:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Tue, 17 May 2022 23:13:09 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 May 2022 23:13:10 GMT
ENV LANG=C.UTF-8
# Tue, 17 May 2022 23:13:11 GMT
ENV JAVA_VERSION=18.0.1.1
# Tue, 17 May 2022 23:13:21 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 May 2022 23:13:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dbddf5847a3e154a061766ddebe6a3cae471c97cabb3be2871f6d91f265d137`  
		Last Modified: Tue, 17 May 2022 22:53:43 GMT  
		Size: 38.0 MB (38012703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6f1a9466bd7ec91933e510c0258839b2df2301b1d385203492a27a3d66f0ab`  
		Last Modified: Tue, 17 May 2022 23:23:18 GMT  
		Size: 14.3 MB (14273985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3719ea44a5b1f9b64a08e21e76812caac05b904b287c315559c054b99b94181f`  
		Last Modified: Tue, 17 May 2022 23:24:57 GMT  
		Size: 187.6 MB (187644826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
