## `openjdk:24-ea-32-oraclelinux8`

```console
$ docker pull openjdk@sha256:c57839cd6b7c7e8ab56650efbf00c6a26200c038a8622ab0372b84e105c3bcea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-32-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c5f45c67a8389962a405903118e060eb05a1fe8f7d70a73d88368d6d280a68af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279491119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b032fe9a75e079bcaaac691a69cf53276899230583b44a4fd2329d25f613c7db`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 15 Nov 2024 23:04:32 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccf911d17c44efb78bc80e5c0d6677cf48806c8ce504c0dc36080f3cfcf89eb`  
		Last Modified: Thu, 23 Jan 2025 22:26:57 GMT  
		Size: 15.0 MB (14974931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6669dddf275e658e6f3f8ff3dd7a689d5ad58b6245a25692084ac3faea4868bd`  
		Last Modified: Thu, 23 Jan 2025 22:26:59 GMT  
		Size: 213.2 MB (213241196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-32-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c547d32c96b8fe154d5bc799de22dfaa93f0f1b75625ef06b5ccb2ec485cfc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cdf889c57e24470625a5e910c504e7f5bcc7de5039c6774d4f6105b2d3a84f`

```dockerfile
```

-	Layers:
	-	`sha256:27a30eef99bcbac0c00242a6bf40ceb3a40ccb10ae144b08910c8a9269c743c5`  
		Last Modified: Thu, 23 Jan 2025 22:26:57 GMT  
		Size: 2.4 MB (2441585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfafcc9d3d77909c5ba1c39304e9dbd8b374ea961ab7235579bd8973104bbd85`  
		Last Modified: Thu, 23 Jan 2025 22:26:57 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-32-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:53d6f1fd8a531ca33a605e7d9706784812d34f174e25e2f0bd2ce9cd529cfab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276841144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adce6f3c37ef26789f8ed8d96040e182c7fec42da32d22157875c82b6a3c20a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
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
	-	`sha256:3d1f44a283e8b041db1f24cd86b03671638f650ab0c41c0933100d1f153c9f31`  
		Last Modified: Thu, 23 Jan 2025 22:30:43 GMT  
		Size: 211.2 MB (211200885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-32-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:3a28d62d3afee02437e850d18c5563592c1e2d9012416df5d223f0ba92943a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a86f9631083baa8999ebd1278489eac58e0917fa6babbc3b612f6c850fc6`

```dockerfile
```

-	Layers:
	-	`sha256:14374321886c7035fbbc5a62cdb25ffef695fc7b27501578ac5502e57361fdfc`  
		Last Modified: Thu, 23 Jan 2025 22:30:38 GMT  
		Size: 2.4 MB (2440431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad26bdd2aa2343edfc75b28b4b67e37dc8acfd69306fa5391b98d786b11c9ad2`  
		Last Modified: Thu, 23 Jan 2025 22:30:38 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
