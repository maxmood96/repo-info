## `openjdk:27-ea-7-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:f4eb624d7b96ed03068f1fbcb14c8ae14fd9313f8ac11f1bd629a18c61fd7512
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-7-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:2561fa45a29be25d56a67b667f7d5a24c6fb05b197c1305d9de10d2ac5ec5ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295147132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c83ce20fdb2afdfa5ec59ebb95e8c2ab760e9ac55c8c45940eb6d9bec0d3b3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:50 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:50 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 23:10:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 10 Feb 2026 23:11:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 10 Feb 2026 23:11:19 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 23:11:19 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 23:11:19 GMT
ENV JAVA_VERSION=27-ea+7
# Tue, 10 Feb 2026 23:11:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 10 Feb 2026 23:11:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df558405081e8d5c6af13745e322e2d270802ff99fe9a1eea2b63615844efa1a`  
		Last Modified: Tue, 10 Feb 2026 23:03:01 GMT  
		Size: 51.5 MB (51464982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22f5df7ea3096a28583fb0932dc662f53498604ecaa8662f0e513238fc5f313`  
		Last Modified: Tue, 10 Feb 2026 23:11:01 GMT  
		Size: 15.0 MB (14991677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd9838a5f9eef1ab90d9bd9cd8b1140cbffab0d5ab8668950949c57eed0a6dd`  
		Last Modified: Tue, 10 Feb 2026 23:11:42 GMT  
		Size: 228.7 MB (228690473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f748630564ce7229829febaf53feea5a69f6d3f1bc93d85fd73f1bd18c3fcdf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748ddeb3e123928b74b293e6e894ed119ae489bb679084e82a4cad9ce92cbd50`

```dockerfile
```

-	Layers:
	-	`sha256:c061a4e440416779e7eec8e0c80c3de2f13e3fedb75d579adc494f7cf7ae24d5`  
		Last Modified: Tue, 10 Feb 2026 23:11:38 GMT  
		Size: 2.4 MB (2448066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c27306fb0616aa2b11f50e7367bbc45b42c873d84a78d8ef0f4cff20b511dd`  
		Last Modified: Tue, 10 Feb 2026 23:11:38 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-7-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7f5d657fa5e537c58b2b2c2ddf93cb58e74161289dca541600bc7cf6f1f1c15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292531849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7243a03a7fc3218f9b9ef517e06db15433026aee9ed9505cad28079f9ac1d7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:07 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:07 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 23:10:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 10 Feb 2026 23:11:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 10 Feb 2026 23:11:41 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 23:11:41 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 23:11:41 GMT
ENV JAVA_VERSION=27-ea+7
# Tue, 10 Feb 2026 23:11:41 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 10 Feb 2026 23:11:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07a1effc9605f90c3e2f6e8e5b85d7de94a80b436a975fd605cfe7f53acd6ca5`  
		Last Modified: Tue, 10 Feb 2026 23:02:19 GMT  
		Size: 50.2 MB (50191339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ceb8831e0da270203511acfa003af3f6ff1ec2905dfd1b73812f9d17b572d2`  
		Last Modified: Tue, 10 Feb 2026 23:11:21 GMT  
		Size: 15.7 MB (15690775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbd9c6633965ff5e1ad67f4386b08ee59fe8f97ccae20b02a7143098382fd61`  
		Last Modified: Tue, 10 Feb 2026 23:12:07 GMT  
		Size: 226.6 MB (226649735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ac11a408e17905cfe898ba3d864578bf33602a7671959bd435d1423d96831e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bc2c68c8a7d4e872e2779db16e41880fa52061cd000510509cc7ebedf4e7b6`

```dockerfile
```

-	Layers:
	-	`sha256:8ee8cd2a99dd73d2072c3a399c23c67f32a9df7ba914737e5c0f62681808f9f8`  
		Last Modified: Tue, 10 Feb 2026 23:12:03 GMT  
		Size: 2.4 MB (2446876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a56f5069246622648d4ddb7e973e1dfeb90a8e873a37deaf429891b95eb4794c`  
		Last Modified: Tue, 10 Feb 2026 23:12:03 GMT  
		Size: 15.4 KB (15444 bytes)  
		MIME: application/vnd.in-toto+json
