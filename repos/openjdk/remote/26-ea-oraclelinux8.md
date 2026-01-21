## `openjdk:26-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:65661b5d0a4c63843d3fb22f435e4997c7fdaa71104bd8df7ee1c7042bd2769c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b3570f7bb898a349df475c8d9005f2af74bf49aec87a8bcda7d0a897d769d356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294768102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f32be42d44c577f610476ce22c6ab911ee7b2bd36378bb385d40e9ac8e9c1f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:45:16 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:45:16 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:47:49 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:47:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 20 Jan 2026 18:47:57 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:57 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:57 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:47:57 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9c709a374865394632aa738429a90691dd8d7699af8be91820b62e8c54881b2`  
		Last Modified: Fri, 16 Jan 2026 23:45:35 GMT  
		Size: 51.5 MB (51468262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acd1695f3f4827351935b3c652e5d8eb4eddf309487b42574a4b727cd1cb3e0`  
		Last Modified: Tue, 20 Jan 2026 19:32:37 GMT  
		Size: 15.0 MB (14993927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba12e27fd604f0cc113444751e7254e732d0836b7c5cffe4294e30fc351c52`  
		Last Modified: Tue, 20 Jan 2026 18:56:48 GMT  
		Size: 228.3 MB (228305913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:54fb7b7de371bc336b00ef8906304c561c270ddaeac9c1b79fe410600d3db715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008b415c394a147877b68b2e39d16897b01beb96fd5efb90d7dca24285c6db8c`

```dockerfile
```

-	Layers:
	-	`sha256:38dc707cfd83d4c764e8a26be0631c45416bc142cc31fc9c430fe294a17d9e7f`  
		Last Modified: Tue, 20 Jan 2026 19:23:55 GMT  
		Size: 2.4 MB (2448684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2070da32f77e1ed06bd4529755412219494875a202cd94670dbfb3aaf85cb593`  
		Last Modified: Tue, 20 Jan 2026 19:23:56 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:381c913a6745028265186c450b55ba0f647482f0b6adaf60625b0fae33cc2ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292141642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d6e9f7190a79ec5b779b869e7a39b7d470b9c6f32d9d4b904240d4db9a4ce5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:45:22 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:45:22 GMT
CMD ["/bin/bash"]
# Tue, 20 Jan 2026 18:47:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 20 Jan 2026 18:47:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 20 Jan 2026 18:47:15 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:15 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:15 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:47:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d32cf4966caecd91a10183493338f37f77a209057fd98d8c3aff049ad44e3619`  
		Last Modified: Fri, 16 Jan 2026 23:45:44 GMT  
		Size: 50.2 MB (50200257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cf7d5d385374c014a99fd006f3ee5295c64e1c2e2a387c2050d76a5ac5d9d4`  
		Last Modified: Tue, 20 Jan 2026 20:35:47 GMT  
		Size: 15.7 MB (15692701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74597d75091e1d43a1c039b7b700327e930765628b8ab79f1b6bc9580d18e40`  
		Last Modified: Tue, 20 Jan 2026 18:47:41 GMT  
		Size: 226.2 MB (226248684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4c4df6d7007f8359ea9aeb217b4956e36a70ed8f88ba3d27547991023cc8e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c580dcbdc6f8c36a71959d66742ba83e7432f0cb390e5aa0a9def1b217c4937`

```dockerfile
```

-	Layers:
	-	`sha256:cf7bd8761800deb7397f22706047e16943f181c0ad0c77496c87e36f8e87d3a0`  
		Last Modified: Tue, 20 Jan 2026 19:24:02 GMT  
		Size: 2.4 MB (2447494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2547910a718b5da4639cfeec0f53ba70c2e4ec999ca2f08d09b3616b09ec29bf`  
		Last Modified: Tue, 20 Jan 2026 19:24:03 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
