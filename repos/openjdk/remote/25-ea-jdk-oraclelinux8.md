## `openjdk:25-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:a4465b47efe713e59bc31d1479f343aa76743df77dae7142b0173e152a1424f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:97702fed0bfa9ed6b9ea8cdf9bde2288576918f8773fc9bbf1c99ea1d8749c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289402469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fdffcc41a448115d453c0157b05f09f38998172029bc35d92fed398491ba88`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 06:48:10 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["/bin/bash"]
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1a7000049ecfef865d125a112ed40237daf19bc27e872529fef00770b81ebc3`  
		Last Modified: Tue, 03 Jun 2025 22:07:40 GMT  
		Size: 51.3 MB (51313330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d0ff85a969dca188e2dab085b1dc9b55527c77012af20132f382acb9b19ec6`  
		Last Modified: Tue, 03 Jun 2025 22:09:14 GMT  
		Size: 15.0 MB (14996663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28a4c386c0392800d871c9fc36f9150f66e630403c1fe5050324f6cd318ab7`  
		Last Modified: Tue, 03 Jun 2025 22:08:46 GMT  
		Size: 223.1 MB (223092476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b34fea86788e57f5632f4c3b70abda1a6772df519c6c7531d6429bcc65d155b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ece70b6ca4cade1b2001ff5af2e3b1250f742c3b12b96f1a467cf501682f45`

```dockerfile
```

-	Layers:
	-	`sha256:198fae0d5a818ef9f1eaca9db461d78920291438608b155ec6350f40bb9692da`  
		Last Modified: Wed, 04 Jun 2025 00:23:27 GMT  
		Size: 2.5 MB (2451048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008b390d4f58e2cc5be94420f34ae8950abd8d9d8a077ea01b048d94a7943dc3`  
		Last Modified: Wed, 04 Jun 2025 00:23:28 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fd87334ed39fdb4d6c55f4642f6e451baee3913ba1fc2375c85279105c1695d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286566158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f84eb9e9109f842bb013115929aae759fec86687d9b9cd8fddd045658f8a40`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 06:48:10 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["/bin/bash"]
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:44b8a99d3aa3536846330d8b29cdcd8db5a0cb5f437d15e0651b4265acba376d`  
		Last Modified: Tue, 03 Jun 2025 22:02:54 GMT  
		Size: 50.0 MB (50031883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b00391e55b48ca359f7e73a227e9716652430842522c8307dea78a7e6106ece`  
		Last Modified: Tue, 03 Jun 2025 22:08:14 GMT  
		Size: 15.7 MB (15667780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e085c85c0aedc03802cdf38361b9d353331db170f815c1e6a9c9c7517014da`  
		Last Modified: Tue, 03 Jun 2025 22:08:20 GMT  
		Size: 220.9 MB (220866495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:54a194fb444377db71491f3a9977e31ab719c4a94afdb2197f397d58889da54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb406faa8518851d2042855f29707b3c1cd3b7b109885a2025bc51e32c6c424f`

```dockerfile
```

-	Layers:
	-	`sha256:817024743fc9128f59f22478a2117b1ca28832418f13344b7f98dd7effabb84e`  
		Last Modified: Wed, 04 Jun 2025 00:23:32 GMT  
		Size: 2.4 MB (2449894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a5a4f306702196fdd66f7d381bc2f595d98f28740eb38def396f47faddcbab`  
		Last Modified: Wed, 04 Jun 2025 00:23:33 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
