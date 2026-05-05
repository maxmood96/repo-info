## `openjdk:27-ea-oraclelinux10`

```console
$ docker pull openjdk@sha256:475ec0eec329f04a57f8a1506e6f3fae2cd2cd7dd888fbc0b32990a4ec842604
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:d4b233106be730d4dd34ba2dcba88b0a3dad34da53f949b26af8549bd3ea30b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309180084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003b854a77eeb5708a26dc712f0cefd4dab78aecb812ccb0f6227b429b156415`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 22:03:00 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 22:03:00 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:59:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 23:00:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 04 May 2026 23:00:04 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 23:00:04 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 23:00:04 GMT
ENV JAVA_VERSION=27-ea+19
# Mon, 04 May 2026 23:00:04 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 04 May 2026 23:00:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec2c75dc3bcdc3cbe3d81597cf6bc4be9a4be0da377a5e9e20a8ca4ce05ceafe`  
		Last Modified: Mon, 04 May 2026 22:03:10 GMT  
		Size: 43.1 MB (43077903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5477c4e7894a79281aad253f28bf7ef232feb4bf449034996abac3f22b50b287`  
		Last Modified: Mon, 04 May 2026 23:00:30 GMT  
		Size: 37.7 MB (37678569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ec3b1d8544cd70745311d98e1aa0316643644aa7852ff23655a26ed6d23fe9`  
		Last Modified: Mon, 04 May 2026 23:00:31 GMT  
		Size: 228.4 MB (228423612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:e1f428869bb3852014c77fe440f1f90941146566855f491237b5618a86eff597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c75bcb3f50d209a5d36c6cb39d4b8015e058a627edae1a15d2fc12bcfbd1d7`

```dockerfile
```

-	Layers:
	-	`sha256:f745f9eb54b254e3b1c8c32ac01ec63db7c80a137d771ac8de25fdaf16dfcf20`  
		Last Modified: Mon, 04 May 2026 23:00:25 GMT  
		Size: 2.4 MB (2367759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdfd150025c79e5e1e172a3975e8cdd2fb53541c029c6b7b6083a244d1531a76`  
		Last Modified: Mon, 04 May 2026 23:00:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fcd9e5b44865cb1c4d613735eec4ee76278b80f30aff7377d6d2b903531799f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305557370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418609454bb0a07d6380398f0d26da79426ef58fef0e8e5d8dd96a9b00f39296`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 21:01:45 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 04 May 2026 21:01:45 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 21:09:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 04 May 2026 21:09:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 04 May 2026 21:09:26 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2026 21:09:26 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 21:09:26 GMT
ENV JAVA_VERSION=27-ea+19
# Mon, 04 May 2026 21:09:26 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 04 May 2026 21:09:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5668b0574ccb4784e2840d685216839b685818991f45396bc2df53f234772cca`  
		Last Modified: Mon, 04 May 2026 21:01:55 GMT  
		Size: 41.5 MB (41471545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916e7b3d42db0cb9970635e799101dd72c9a6ebb780561373ae611f5e6656b30`  
		Last Modified: Mon, 04 May 2026 21:09:50 GMT  
		Size: 37.7 MB (37697936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa5896ab8b15341360d30bdcf85c014ecacfe159708fcde17116a1cfb5b7586`  
		Last Modified: Mon, 04 May 2026 21:09:53 GMT  
		Size: 226.4 MB (226387889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:883e12b6a1160e768835720c125ccffd2762797bfda4cd683e23e6ecb23a2838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341e524f79ece69f082cbe029e504350e5a0ee0f6985adae5e32a065c643616d`

```dockerfile
```

-	Layers:
	-	`sha256:ba5212a56fd087f74a673625fb7d917022a45270c814ed190e92139e38c264ca`  
		Last Modified: Mon, 04 May 2026 21:09:48 GMT  
		Size: 2.4 MB (2367287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9584c52deac5581887b3d2e0cf57b02451cabb1bbfb6422dfdae57e7c98da680`  
		Last Modified: Mon, 04 May 2026 21:09:48 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
