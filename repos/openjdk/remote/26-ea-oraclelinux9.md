## `openjdk:26-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:f836fce4a12f7b9c91ccf125031cd02ebc0edc6d4e762f5e55db56b9bca725ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:7e818fc65441af6afb28a269f990c9c5abc74c13e61237d1a4c91321b85cb031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310531368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481dcd0af8c3231f1ccd767a2b49712717e0691aab59d07c26c742b4ee608f00`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:54:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90dac1e734aa2e08c0e4e8bb7d30232985487cf8abfb490025986f98bc2e5382`  
		Last Modified: Thu, 10 Jul 2025 23:20:44 GMT  
		Size: 49.5 MB (49500230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6483f9c15a4efd5e153cead57406bbca7391b3a395ace4d59b65f7ee90a147fe`  
		Last Modified: Fri, 11 Jul 2025 00:09:23 GMT  
		Size: 38.1 MB (38093387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a868c353f94ff44e834a112788787ec3212d520303f1686b97120d409e2691`  
		Last Modified: Fri, 11 Jul 2025 00:08:26 GMT  
		Size: 222.9 MB (222937751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:99421b5dd0b5362edb1ffc4b21fbb8414bcadee37b5f0e06695bd2cdda70806c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e19282a560d271c8f6c857ecacc049b890c80091abc45227e64d5759d04c7d`

```dockerfile
```

-	Layers:
	-	`sha256:5fc7253c2327a3de482c0d88e06e9d595fdeae4e10772bbf908a6fc6635ad120`  
		Last Modified: Fri, 11 Jul 2025 03:24:10 GMT  
		Size: 3.6 MB (3641294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ef956d80d70a4961575d5c5bde238e3dee4877b68ca377ad993b231d918085`  
		Last Modified: Fri, 11 Jul 2025 03:24:11 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b5addc84246b4ed846d57bd5f80e66bb9e537c69c167f5695364adb3e4043dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307270235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f728e838d8688e47b587e0e1e08a6ec223eff31736c94fb5f9ed65194c15504`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:54:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4447c51b3bde441b803aaaf0a684a8bbac02d7fce9167a7c1e87c313add07cf4`  
		Last Modified: Thu, 10 Jul 2025 23:23:17 GMT  
		Size: 48.1 MB (48085739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971f07a392e04b4b6e3af0d916043d20304174997e2490b9db70ba78668b2551`  
		Last Modified: Fri, 11 Jul 2025 00:13:53 GMT  
		Size: 38.5 MB (38493030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66999f1be9ff06af7486e93242c4d193691b57c748b895cd3ed0d14e9c5cae2`  
		Last Modified: Fri, 11 Jul 2025 00:13:44 GMT  
		Size: 220.7 MB (220691466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:2429d2d49cc4625b5986ebaf4168e8293a44b3048fbb54bb1d0557bdbda11386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461929500f59712d76b0218f79e3da96250d49e189ec36e0a71007af3f1c9baa`

```dockerfile
```

-	Layers:
	-	`sha256:7d133c11cfd1c0c44b0e7bd50a2c988a758aaef809a304a3472bea39bd50d5b5`  
		Last Modified: Fri, 11 Jul 2025 03:24:15 GMT  
		Size: 3.6 MB (3639056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e709db1c7466526955a7fa65f6198078ba877fdd14e8988844d5bf18928a6479`  
		Last Modified: Fri, 11 Jul 2025 03:24:16 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
