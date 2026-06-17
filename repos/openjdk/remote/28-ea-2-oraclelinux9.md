## `openjdk:28-ea-2-oraclelinux9`

```console
$ docker pull openjdk@sha256:aad15f7a696cd602f09918846861aba1bfc0e390798cfa5e572b3bd9f46d53e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-2-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:844264a96efbad17c1c9e71d196decd71fd583a0eadadf11db243739dcc080c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312958826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40adf0bbbada29fd1728efaef8f03c1544e8b6f273e9b7fc52146fad4778cf1a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:32:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:32:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Tue, 16 Jun 2026 23:32:40 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:40 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f10db5027e9352fae2734fd2faa242d22970e0793db7d4a54980bf7852e438`  
		Last Modified: Tue, 16 Jun 2026 23:33:04 GMT  
		Size: 38.3 MB (38267812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949efa6619952b8195ac95d6e5d36594ee199f21a523568d72b5b2c400bcbb89`  
		Last Modified: Tue, 16 Jun 2026 23:33:07 GMT  
		Size: 227.4 MB (227381441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-2-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:7600fd1d88fbfa4ae7ada0d76d5d131b82e491ad289b09222afd5f728010093d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a26281e35a2025095a818fff8680aefc234905e2d6d3db9bd3856c64cf59fd`

```dockerfile
```

-	Layers:
	-	`sha256:02a66fd396ebeed2e8890590b379d72d9cacbc9bad4ba80e74a83fd89cc1723c`  
		Last Modified: Tue, 16 Jun 2026 23:33:02 GMT  
		Size: 3.7 MB (3650412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603c0b93b92f2c9c05274986fc932b196725fc102fb9188c460a07034fff8efb`  
		Last Modified: Tue, 16 Jun 2026 23:33:02 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-2-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6465797712aed33126ed127bdf6c355e1936af8e188687ad9e616b8a6f72402b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (309970011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59c7f6c60718db62cd9dd95e432a1ae051c206ef9bbbbdddb3b552910efebf2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:32:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:32:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Tue, 16 Jun 2026 23:32:31 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:31 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:31 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:31 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10c0c76d67e5adaf70c8562a1f9681094f2fa81db7426ec50b698ac1aee1ff1`  
		Last Modified: Tue, 16 Jun 2026 23:32:54 GMT  
		Size: 38.7 MB (38665545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef57c50f0865e11f67ff8c53091d51a77435e223f8bd4d916fd0bda0f859d7e`  
		Last Modified: Tue, 16 Jun 2026 23:32:59 GMT  
		Size: 225.4 MB (225405376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-2-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:2345df4717c9ceea8614409e42a505930ca6e597976e9dd787fffa7eb6c3ee5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719c58746cb81618c54beab063d81554476fe8cfd911a0cbaa3072cf88872fd3`

```dockerfile
```

-	Layers:
	-	`sha256:f3a931756171bd8b057bc3e482b91159cca424fb97d13fe4b1df202c25064ddf`  
		Last Modified: Tue, 16 Jun 2026 23:32:52 GMT  
		Size: 3.6 MB (3648006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af69edae15b28b6865e45df7f65aea83a84bdf6900731817d9f82c535dd93b3e`  
		Last Modified: Tue, 16 Jun 2026 23:32:52 GMT  
		Size: 15.4 KB (15441 bytes)  
		MIME: application/vnd.in-toto+json
