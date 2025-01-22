## `openjdk:25-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:5b711b151cd3b53be926406b5c76a911006d54ec17b7ef28555fa608a70f0a4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:0c4bdebf07b705f2cb9c138f0b1bd69ec261d830c97ef3f027c897eccbc658f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278397465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e294134d39a46273e6efc6aa340af6375150cccfce9a3176de7e358249289b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 15 Nov 2024 23:04:32 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84682b744719b8c788489aafe06c1b2b56649dee4348dca9ea3b0390b843a59b`  
		Last Modified: Wed, 22 Jan 2025 02:28:44 GMT  
		Size: 15.0 MB (14974938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2c0c87e8f2d35896cb6cf4a988d28e2722d01a3a392a0d2292dcd506fc1bf3`  
		Last Modified: Wed, 22 Jan 2025 02:28:47 GMT  
		Size: 212.1 MB (212147535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:4bce045cec78bcb1ed1b745a81f126c46417fb3106acd16ed682f97adac38393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f809f888a68a534d0997c5a176592360e20a1a799807d706c7442b259a946018`

```dockerfile
```

-	Layers:
	-	`sha256:a3687bfbcd42bc129e91b79c72d7fb9308664523df3d980fc3b6a677c0cbcf8f`  
		Last Modified: Wed, 22 Jan 2025 02:28:44 GMT  
		Size: 2.4 MB (2440949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b85ed31bb53df2c6628493f13d6426384fc6f89d8a87195dc6cdebc73ad22d`  
		Last Modified: Wed, 22 Jan 2025 02:28:44 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4e9ed0819621c023c7dce821df1ebac903289337db13604a4fb9f6c7b4dc557b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275744121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53191f58f895f89efe8ee94e07914472441c94d1fa663205ef5575376da8c6c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:54 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad1cd9205a89581b21ab3876711618f2acded12b00d2b5d3a9daefffa65ac7c`  
		Last Modified: Wed, 22 Jan 2025 02:31:00 GMT  
		Size: 15.7 MB (15659984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5de16d52bb143d994cee6253d15c35b54305b4a12d03a545427d376027794`  
		Last Modified: Wed, 22 Jan 2025 02:31:05 GMT  
		Size: 210.1 MB (210103862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef192f928794ef6dd4f16da26f7ac66084eb974d7efa012c8180e48c901644f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0beeb4542cbbc25a696816f14cf81b898b5ac45408cf341b6813687dbb5da8bc`

```dockerfile
```

-	Layers:
	-	`sha256:34a9c9fbc13d5b6f9adcaf198fcc16358a0894db2c600e24c2f1e3a68233f963`  
		Last Modified: Wed, 22 Jan 2025 02:31:00 GMT  
		Size: 2.4 MB (2439795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c487adbe7cecbc69e8baa24db4cd8c6ed76fe3e3dd222d7fac5b701b648dced`  
		Last Modified: Wed, 22 Jan 2025 02:30:59 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
