## `openjdk:24-jdk-oracle`

```console
$ docker pull openjdk@sha256:9947e97f0ac12257dcfa63ab2b0fab43cac5a2f28f7320e9deb5776d069ef1e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:8bc4e525c1929b5249aa5c9bdfc55a1b640f4fb571af4509af958b31e7736ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310633907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011d37185def7340179612c944d1148abb1a0da7b341c83d513283a47080bc70`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 03 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+30
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='613ff61d4553e9e8c17793cec42c93db99b73ee18bb41d5ceefcdcdfee0d826b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f89ccf3b004d95bdedd0fdd10cee362f00be006ebe79a394b0539057e8d8ff6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3d59505e59f7752fb155bd3cfb2597a2969a2674bf6772205f8ef370f0c21b`  
		Last Modified: Mon, 06 Jan 2025 20:28:37 GMT  
		Size: 48.8 MB (48774245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23b45f4adc554a3a273730b0ba32e0a600992c82579f08989bc8633351df2c1`  
		Last Modified: Mon, 06 Jan 2025 20:28:39 GMT  
		Size: 212.8 MB (212760960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c823951ffc56dff5b3b8485638be60e1ae5041c9c2bfba4bfb66804d0f60261c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86c7139dadf2fdc5a561adae4e990c25647a629763604a709688fe0ead74da5`

```dockerfile
```

-	Layers:
	-	`sha256:16a7f61fa0c20a421f7ea4e936d4a6a272687924f6fe8ebfe6a83437e39c1570`  
		Last Modified: Mon, 06 Jan 2025 20:28:36 GMT  
		Size: 4.9 MB (4907575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d503b273d20cb5877e21c6ad55a84f914f6dcb9007a2e6cd11de88ed363188`  
		Last Modified: Mon, 06 Jan 2025 20:28:36 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0794fd45329c9d19265bac1e26acb0dcd79e98c2a498eb2ed81232675618f175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307578180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85d5c2d470d26915c45a03a11444dc0b67c9180fbb18aef5d14649ec43f6a6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 03 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+30
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='613ff61d4553e9e8c17793cec42c93db99b73ee18bb41d5ceefcdcdfee0d826b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f89ccf3b004d95bdedd0fdd10cee362f00be006ebe79a394b0539057e8d8ff6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50730d7cdebc9dd971fe547b229ac9b36632531d0634a0903681766460bf2cf8`  
		Last Modified: Tue, 10 Dec 2024 01:26:17 GMT  
		Size: 49.2 MB (49196487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908b77bb4af733fddd6a2a44d87781125169d879a7dc5005c79cb7497bbb5a0e`  
		Last Modified: Mon, 06 Jan 2025 20:33:43 GMT  
		Size: 210.7 MB (210714301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:95d21298fbee671ebd722f6ad2ab10b10c5603f56bbb9667b014f864af3e5541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68e78eea0c16587ec4d24b1dd4621da3d4b6392d4436b4f18fe5ed775dc68ee`

```dockerfile
```

-	Layers:
	-	`sha256:0621227d093da6d409775d9292f31e2cf7f6e5985d760b64b5343aef4a7dfd07`  
		Last Modified: Mon, 06 Jan 2025 20:33:39 GMT  
		Size: 4.9 MB (4905337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:567eed38c322db959d962e9d81b326ed673e43601d3cad638b73e620accd1d69`  
		Last Modified: Mon, 06 Jan 2025 20:33:38 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
