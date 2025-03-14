## `openjdk:24-rc-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:27dd625c10e397af492e16f49660c3e33b8d7762e2f014ae4a52d7782933f915
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-rc-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:07b020b6df39f17ed05bae576179079b7fe18dec5be49ef17a42e855fd6b321c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279600338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094088c4f4cd66cd7d7df06cba06b7ba92a63448f09762c447a0a9386c392f95`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9eaa108e19c50f27b324537cc9caf3425a1bc778f71bb2fd855bc5db74356e2`  
		Last Modified: Thu, 13 Mar 2025 21:06:47 GMT  
		Size: 51.3 MB (51288479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5720b31a35ae8a68ef444b503fd544193df83a1ae0658ba7445f396b2e18fb11`  
		Last Modified: Thu, 13 Mar 2025 22:09:47 GMT  
		Size: 15.0 MB (14995576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8516eb91a4dc6c1f7281998751b7c1652fa671e439bf1b917447dcdb1d543b6`  
		Last Modified: Thu, 13 Mar 2025 22:09:52 GMT  
		Size: 213.3 MB (213316283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a1e10cd286257d2fc9c01c11856a24f082b00e63c63ac01b389e10d2d9518b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae237acbb71eb3835560602b06adca2dfea76a534853d353f8d1867575d34ef`

```dockerfile
```

-	Layers:
	-	`sha256:65a7bc3a74aaf00f21e2dc1c75e3f69479514ad96b4003fbd269c5c4a951b011`  
		Last Modified: Thu, 13 Mar 2025 22:09:47 GMT  
		Size: 2.4 MB (2444669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7480a642d7fad5f2eb0fe0e0d40038a1cb3945d00edc9a8f11253adc98a7fd40`  
		Last Modified: Thu, 13 Mar 2025 22:09:47 GMT  
		Size: 15.4 KB (15434 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-rc-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a0447cdb9f98a03c1eb4309c3c6243d1bc6d168584da04737c1d0e6c5f5f7af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276943758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e882e656ed4c421ccd29d55ecedea1e9bd19afc8061de4075addc97be1d3b1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e6d27d0384ed91610f17d7a9ef2bb948c3574306ac40526f54329f54140d2f0`  
		Last Modified: Thu, 13 Mar 2025 21:07:17 GMT  
		Size: 50.0 MB (49989436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69e77c2995841cd0e340bc286b91ceb1b42cf941fc975e2014d23fdda3f999b`  
		Last Modified: Thu, 13 Mar 2025 22:09:21 GMT  
		Size: 15.7 MB (15683725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d9e8326543766e2fc20b993b6f691315ea0c0617d54d68c704baa122fd49ad`  
		Last Modified: Thu, 13 Mar 2025 22:10:17 GMT  
		Size: 211.3 MB (211270597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9e031d850f43e8f81e1621f6ef58723033118a995218b9d69030f87319f9b861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24a97158e32586e6e68b8a0ce5fce886c69b18ad636ff5916a3847ab83af9d4`

```dockerfile
```

-	Layers:
	-	`sha256:04b675de4959872b8dbaa6d79cd917ab14b24a696e00d092280bafc977ff4f8c`  
		Last Modified: Thu, 13 Mar 2025 22:10:12 GMT  
		Size: 2.4 MB (2443491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b70aca8e1ba44a99c3650284748484740795f20c97698da8ded9f064b692a7b`  
		Last Modified: Thu, 13 Mar 2025 22:10:11 GMT  
		Size: 15.6 KB (15553 bytes)  
		MIME: application/vnd.in-toto+json
