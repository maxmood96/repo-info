## `openjdk:26-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:c89ba38f4e220a04c0d177d8778758998b510928d698276972a064a20c89482f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:bd4fdc282e33d9fdae81c638d8361e0ab780cedae26dd2354060c392d8e6ee4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de72a7cbc40112d4220459d9ad879133e8ee81b08fdab6371ba0ba28d39e0e4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:50:37 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:50:37 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:34:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:34:59 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Dec 2025 00:34:59 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:34:59 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:34:59 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:34:59 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:34:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b436d89f13c92f9703618820d992b4e1f2b38ba243024b251c81a610f04c67b1`  
		Last Modified: Tue, 25 Nov 2025 23:51:01 GMT  
		Size: 51.4 MB (51378078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e14ae49eb09e787c4211a7261cf8893db2454069b6d0c1ddd099987769b4c6d`  
		Last Modified: Sat, 06 Dec 2025 00:35:35 GMT  
		Size: 15.0 MB (14999286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb6630c92487a04e56fa91cc55a4d751f8f44b7e3bc9a33c23995e6733183f`  
		Last Modified: Sat, 06 Dec 2025 00:35:43 GMT  
		Size: 228.3 MB (228280521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:93985a8a17c4d0bd1181828877de28f01b3ce3446053f3900285d527f9369052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d520bd837e4dd9732c3ca79cb8a5d7c9deb80d74e5e6782a2afa52b694a7081f`

```dockerfile
```

-	Layers:
	-	`sha256:7567268a63da2dd2e91793041abf9767beac9eb315e1a6718c79e1785773825a`  
		Last Modified: Sat, 06 Dec 2025 01:24:01 GMT  
		Size: 2.4 MB (2448013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f24b9096521094ace1bc6ba495c1d276a650110ecec406d5e7d7a9f0cde96fce`  
		Last Modified: Sat, 06 Dec 2025 01:24:02 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a28edf1b7f134bc10be28a90380cc5eec2dad9c4ffa7f302ec68b4b33e3658eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292006500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc42c8d7bd17ec2b3ce0e5ae390f634ddf9313a19ed364c0324e0639ea9e3f47`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:37:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:37:54 GMT
CMD ["/bin/bash"]
# Sat, 06 Dec 2025 00:35:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Dec 2025 00:35:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 06 Dec 2025 00:35:24 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:24 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:24 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:35:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:674388ef21c06396c4d40407ba2af1c3a42c30a5cb162fd4355950be7600edf7`  
		Last Modified: Tue, 25 Nov 2025 23:38:20 GMT  
		Size: 50.1 MB (50103076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80ff6bc025d30295e802397134cd2dca67164dde2f4574aa140bb719e94e55d`  
		Last Modified: Sat, 06 Dec 2025 00:36:00 GMT  
		Size: 15.7 MB (15691553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa3ca045585104e03c4a2df065d4bb7ab94dd51fe0308493714c01abe1fbe97`  
		Last Modified: Sat, 06 Dec 2025 00:36:12 GMT  
		Size: 226.2 MB (226211871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:de48fdf220633ce1c4c384f4bad0b0a72b19d4d1fffdb06dd4fd99573e3883b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bab4f9acbd60a572fcfe976e6e3b868a29bfc84f1c6e604e10d0971fb70797`

```dockerfile
```

-	Layers:
	-	`sha256:bd40e06184abdd8a867487a35544762aaba22ff38a0f4b39d75ee04fc58946f7`  
		Last Modified: Sat, 06 Dec 2025 01:24:30 GMT  
		Size: 2.4 MB (2446823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dc7f1443600ef7e30354e0efad2870bf7ba4783f51532e3352745da3d28d6ac`  
		Last Modified: Sat, 06 Dec 2025 01:24:31 GMT  
		Size: 15.5 KB (15461 bytes)  
		MIME: application/vnd.in-toto+json
