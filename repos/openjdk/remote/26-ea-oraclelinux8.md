## `openjdk:26-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:58a360ce6f8fc4ae5a7eee4c5e98d20d01a5c457e7ee4e9dd790338dc57939e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b2a34248872c275afc16d1f605710685288219981c1d8c4e0aad610b471507c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289699509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94cdfafb1cc96a26733c156219bf469f3f3a438e2851542c90310f984e878e33`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:42:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:42:18 GMT
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
	-	`sha256:0915556054e5fcd1f04e454b0deedf305bb209616c5a72a8b2d83db9191e5115`  
		Last Modified: Thu, 12 Jun 2025 21:07:27 GMT  
		Size: 51.3 MB (51311558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc759c8e682a4c47cd4aaf29ecf5f6f87b893af25f2689f2b53ef77450fcb12`  
		Last Modified: Mon, 07 Jul 2025 20:59:56 GMT  
		Size: 15.0 MB (14979447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34534c00051652a31a75ec9187f8bee0b7fd5398956cde17a59b734411fa000f`  
		Last Modified: Mon, 07 Jul 2025 21:41:54 GMT  
		Size: 223.4 MB (223408504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:bf4ffba243a374e417752055b1bf73cce28c3e52c0ed711768abb25ede941447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88121d63681b97dbefb7c90fffe7d49245ceea3fd1d94138b87ddd03f95fa01`

```dockerfile
```

-	Layers:
	-	`sha256:7f3bc4717bc3136e1a6813e72bf38c6213e1929830043b781f1ee8e9d816888a`  
		Last Modified: Mon, 07 Jul 2025 21:25:24 GMT  
		Size: 2.5 MB (2451698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14403cf5e12ee4b811269826af38ebaa3bf1c282aab905dbc3fb48c9aaad5eb1`  
		Last Modified: Mon, 07 Jul 2025 21:25:25 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:97e3eb95f9f7209b96d104d9d65d25ef8c69b019a2072a971716578c2abaf686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286890010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44db6030750ef1c718aeecfc9d56978762bc68b780182173f937556f97fd7dbe`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:43:09 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:43:09 GMT
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
	-	`sha256:d998890baf088acce50ef79f8e8dc3eab36a2dc008c7774fa6e1e1140c89c3c3`  
		Last Modified: Fri, 13 Jun 2025 01:08:32 GMT  
		Size: 50.0 MB (50039112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0837aedf5b6ec0f11183649f1e317d9f31eebbb043f054199a45f60d9d7fb1`  
		Last Modified: Tue, 08 Jul 2025 02:05:29 GMT  
		Size: 15.7 MB (15681963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef6d31a8e62ed43ee1a0e33f9f858cb37c5dc39ecc6f2cd121656b3bf7739ef`  
		Last Modified: Tue, 08 Jul 2025 14:08:21 GMT  
		Size: 221.2 MB (221168935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f9ededcfd33852e95043a3d2ae2718f5dd33319075ad5fe031d289855ba750a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb78b5311c01106cbf67083decbcfd25d605f8f2082b3ef42a46747151742573`

```dockerfile
```

-	Layers:
	-	`sha256:fe2d296dd892f9590886e53b59f5bfb676b2fb8b935e21884a11d4dd09f43afd`  
		Last Modified: Tue, 08 Jul 2025 03:25:04 GMT  
		Size: 2.5 MB (2450532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51994a6b4b581c29bda12cdeb7f00d5b566a0be53ef07f01b734b0edbb7010ea`  
		Last Modified: Tue, 08 Jul 2025 03:25:05 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
