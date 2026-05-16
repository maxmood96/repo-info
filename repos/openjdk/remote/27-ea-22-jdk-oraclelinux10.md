## `openjdk:27-ea-22-jdk-oraclelinux10`

```console
$ docker pull openjdk@sha256:f2d4282f31a16f2e4bc8f1569cd1c603fea91917dd9ebbca9711cc1fba583a94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-22-jdk-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:15b38b210402e3de2f629029f1862611aa80c40410bfd278357c969799e2e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309574667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4190ab05ae216f5b9aa05e6775f2a86e8ffd8911b47ef12af276ca13ad7c7f2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 20:18:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 May 2026 20:18:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 15 May 2026 20:18:39 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:39 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:39 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:39 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ebf29aec2dec2e17e26d8c2c7669305e946fb12da2410c3089793aeb38196`  
		Last Modified: Fri, 15 May 2026 20:19:01 GMT  
		Size: 37.7 MB (37687895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b99930b49e490efad118f74bd9ad8d36f25982bec8fac52b508ae5de2dad10d`  
		Last Modified: Fri, 15 May 2026 20:19:05 GMT  
		Size: 228.8 MB (228806190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-22-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:9f24d387ba46f03ef53460f14577240518cc604f467a0ae63dce1abbada35baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c5de8f7eb291535c50a97fa30a7ac992160a6067ec73027d8f9d8c9f3fb943`

```dockerfile
```

-	Layers:
	-	`sha256:a7e34bc63a6b8b54834ad94bb801902126683d8a9f7ecf7d1bb0ce5d58f97486`  
		Last Modified: Fri, 15 May 2026 20:18:59 GMT  
		Size: 2.4 MB (2367743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20f59eac3ec7e40b94635381f278fbd39c25ab4d08d4d9bede84a7a4a23e9c1`  
		Last Modified: Fri, 15 May 2026 20:18:59 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-22-jdk-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:286ea803910a21946f30839f5a4f9ee9c86fad2773bf59073a0d74494f9b6e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305960720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a6b129c0701c2d72aae2480c47050113f51d274d515163415383f8f44c1d7a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 20:18:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 May 2026 20:18:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 15 May 2026 20:18:23 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:23 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:23 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:23 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211bee5ff420ccd7d1e415cecdf86fb1ca49a2aed221aec6cb952520b42cab2a`  
		Last Modified: Fri, 15 May 2026 20:18:47 GMT  
		Size: 37.7 MB (37701706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9b3cabe86e6f5dfb87dac4208ac2d6704fa8324cb61a8a042159f0d1c9ed71`  
		Last Modified: Fri, 15 May 2026 20:18:53 GMT  
		Size: 226.8 MB (226763319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-22-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:f1ad0838554683df68f560cffd810ff83ae9fdd0874ce012a2390a9f86716506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86a63b9a1771a1991a40008fd36c0a740ad617b704e631f4f3e2007e16e4a30`

```dockerfile
```

-	Layers:
	-	`sha256:8bd64f1ba2ea2ea031a203af12f036ebca4776207e0fb07d091e54826a6236cd`  
		Last Modified: Fri, 15 May 2026 20:18:44 GMT  
		Size: 2.4 MB (2367271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc176cce0b08aa7dcc86ab9db0ee931303b0fae1140f099f1fdc1db5707d3f89`  
		Last Modified: Fri, 15 May 2026 20:18:45 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
