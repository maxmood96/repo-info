## `openjdk:26-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:864d8b982f0dff8b3693746127392b757b09a324ab89823154f1f9c4b8c777c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:2ed8c280fa3d101af66d9952eae9349e12c98eb569fba8a776aa932c8f8b1ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292662538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b5e4f9ae8641b04fe51a5c6430cbb2a03f76131adc6540bb585959da894c51`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Oct 2025 17:25:39 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 31 Oct 2025 17:25:39 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 20:29:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Oct 2025 20:30:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 31 Oct 2025 20:30:07 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:30:07 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:30:07 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:30:07 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:30:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fff3d29c5b5b28d342ba8d967679d9f76705eab0cf1b9c1c2a8d43102cc524c8`  
		Last Modified: Fri, 31 Oct 2025 17:26:00 GMT  
		Size: 51.4 MB (51383677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6865009cd31700a547919928c07465e9da4ad7536526f4b69cd1f5bbc9d9e3ab`  
		Last Modified: Fri, 31 Oct 2025 20:30:42 GMT  
		Size: 15.0 MB (14997598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab853676ff611c213199d7a6e422264170514ea3a1ee36d65c9f7b8051ee82e`  
		Last Modified: Fri, 31 Oct 2025 21:26:53 GMT  
		Size: 226.3 MB (226281263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce203099d07e48c953b41c84d001cf9aec84116b989211027b6b7942ab5f995a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfcf915d27cca9670c459d9add4d1c525a001b20fd300f7ee4909065e398014`

```dockerfile
```

-	Layers:
	-	`sha256:a88a0c030edb875e17988f13082531303c70006cdd08f3ba376ae2af936377a7`  
		Last Modified: Fri, 31 Oct 2025 21:24:02 GMT  
		Size: 2.4 MB (2449298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca5a2d8057a0bd5d6b24038890b77d6b5f55157a03e1d3447d4e9fae25a3ab2`  
		Last Modified: Fri, 31 Oct 2025 21:24:02 GMT  
		Size: 16.0 KB (15995 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2c26059de0506326b3193ba5c5c2a3e19ee3e8eb06c5a95abbb8503a5f9886f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289879604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b90e0ddd74b7c78d049a8f3790396b2972dbcd8343bd2b2e5257f7cda092be`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Oct 2025 17:25:14 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 31 Oct 2025 17:25:14 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 20:09:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Oct 2025 20:10:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 31 Oct 2025 20:10:05 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:10:05 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:10:05 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:10:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:10:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:913708617406390e2c3446d7f989f45259d9e8bc8c18aeb2c7030c867ecfb5d6`  
		Last Modified: Fri, 31 Oct 2025 17:25:36 GMT  
		Size: 50.1 MB (50102610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154afc532908d5f0f72c0e27575038df4431d30b6097d1e1928eb10470ad3abc`  
		Last Modified: Fri, 31 Oct 2025 20:10:40 GMT  
		Size: 15.7 MB (15663490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6a193245c46a0248977329972551667d869dafd7e4e16a5706936acb700d7d`  
		Last Modified: Fri, 31 Oct 2025 21:26:00 GMT  
		Size: 224.1 MB (224113504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d2137c6ae9bf057ef62d3f71259b985400c03a3ebdfd66c4730ed038092d2b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3310b81c97889111e1bac4f56c535186c0ca9cff4d496fdd06c1a615585b66`

```dockerfile
```

-	Layers:
	-	`sha256:cb705340e1c28f927eaec92158baa75b5c0555314680ad4345525de78fa4fe8c`  
		Last Modified: Fri, 31 Oct 2025 21:24:06 GMT  
		Size: 2.4 MB (2448132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892a39e71c2e7934add02d96ed5938b03c33bc701793b578a874cd23b3f053e1`  
		Last Modified: Fri, 31 Oct 2025 21:24:07 GMT  
		Size: 16.1 KB (16138 bytes)  
		MIME: application/vnd.in-toto+json
