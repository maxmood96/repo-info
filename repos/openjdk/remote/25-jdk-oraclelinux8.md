## `openjdk:25-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:6d58f24d56008b58f7ac2d6529e103d236e65929e8f7b1e3fe0b4cd3b3714df8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:af6557ccb57fd9784851954a11e7ec24f973149f7b6cdb65143f06c77e6a8de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278411328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9234ad87a927bd4c10cf42b0bdf66e1c5c1e0747dd207af3ea39a473316156a3`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 25 Jan 2025 01:52:19 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b976166ae00f0fda8e12b934d92a7265904c082bbb675e0cb9bd4bbe93bedb30`  
		Last Modified: Thu, 30 Jan 2025 23:27:50 GMT  
		Size: 51.3 MB (51277963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a764691b769a50ac88bc866e2d04789a1851393d231b5220fc1ffcb60beab5`  
		Last Modified: Fri, 31 Jan 2025 00:27:27 GMT  
		Size: 15.0 MB (14975092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031a0581a26e3ee9bbf4055c321b46352c67c3ac5ed500199137f6cefa691b40`  
		Last Modified: Fri, 31 Jan 2025 00:27:31 GMT  
		Size: 212.2 MB (212158273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:fe63d1c43ca9d06ec45f7ae91bdadcc51522d5d8dcbe6358619722a0778d5415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4df58f44a523c0e44a774911dee0e7f25a136bef4fab5a952a2dee974dc426c`

```dockerfile
```

-	Layers:
	-	`sha256:49ac2cf9b4ac9f65e09a1c3a5aa6ca13c392dc5fd682c6082401ee21f8983cad`  
		Last Modified: Fri, 31 Jan 2025 00:27:27 GMT  
		Size: 2.4 MB (2440961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ffd13c3a28853289c05786b0e0bae58f18b70b08226807577d1230472b1d32`  
		Last Modified: Fri, 31 Jan 2025 00:27:27 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:01b68173ee5530677bec52d702e592483d781bda57973bb86867de64cb61370d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275761246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58b38174a407c91cd90885596175c87abd62345dbaeb1346872ffdbe31d14ff`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 25 Jan 2025 01:52:19 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bce860c27508f058f4bac6fca02fb3ef33ecf5c8331d2635b7c34a8b0af94e0`  
		Last Modified: Thu, 30 Jan 2025 23:30:11 GMT  
		Size: 50.0 MB (49984693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20da80e2bd804d65a47238fa85705492fc406b2b8cbad4cb1a153d9b26b0720f`  
		Last Modified: Fri, 31 Jan 2025 00:27:46 GMT  
		Size: 15.7 MB (15659413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d834afcccb0cae40628745856e69bee8680ad2f71f011e2862d253a8d1412`  
		Last Modified: Fri, 31 Jan 2025 00:27:50 GMT  
		Size: 210.1 MB (210117140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:aeb2cb309f3c4cfef1b721d3fd86ee94bd746e267bd3f95dc77eb9efce020ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53ca1997ca01767d619d4ba358e7b03dd415fb4e3e6e3e31535e8b2dbc4184a`

```dockerfile
```

-	Layers:
	-	`sha256:26dcde308b2ab21741fb0ce082475eeed3325376221c59f93449725377de6089`  
		Last Modified: Fri, 31 Jan 2025 00:27:46 GMT  
		Size: 2.4 MB (2439807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e2a624ed5e2dadfe8c41612e4ce44eef775c3f168152d4b3362273a9d72723`  
		Last Modified: Fri, 31 Jan 2025 00:27:45 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
