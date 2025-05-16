## `openjdk:25-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:31dd56e6a52fa566f71f86fc69bd5d9cfcd35ec912fc8638f5d241fe2cc4656b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:43e04e6a477c938527cc98e5852d9ab871267e18b53157ecf782181e1c5652f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 MB (300042167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0fe4760580025fea19aa74b74ff23a72fdf6d7321686cd1674f0c952a4f5a0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:26:20 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:26:20 GMT
CMD ["/bin/bash"]
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2eb5d06bfeaafd2195d3612935e86f925a4620bf5bbcea5112a1fb07138dd80`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 49.1 MB (49093011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4c710ff4e969a9223c716321c9ce4a806ed32c2ebfe30f03a3b3825be2ad41`  
		Last Modified: Thu, 15 May 2025 19:28:56 GMT  
		Size: 38.1 MB (38107429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d49b942cfdfaf2cd73fe2ea6449fe3fdfd7a49a5d0de1eec0552f2d14e8dcdf`  
		Last Modified: Thu, 15 May 2025 19:29:06 GMT  
		Size: 212.8 MB (212841727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ffe66c4aef2cd753ecc86edb768ac8362e90f96cf7bd234dde536c634829a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3644252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb29685782d0ce485897bdf50a63ba6f9f41e35912d432375a52a7cd96e1166d`

```dockerfile
```

-	Layers:
	-	`sha256:4ebb8684fb65fcb14a8f6cf68afa2424b1f93637b59c5e5f984113d729b9365c`  
		Last Modified: Mon, 12 May 2025 19:12:54 GMT  
		Size: 3.6 MB (3624506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a544f493a09d2de07f9d0ecb515984c3655b96b58ff88deff69c8fba4b47182`  
		Last Modified: Mon, 12 May 2025 19:12:54 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e5df4af198207a471a2b8a90ea6b94883da1be94b6fdba26754da4ca7573c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296820604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bb978b8265f72ccf19265a49021c2a979e514514362b0b5c782e19701a8bdd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:27:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:27:11 GMT
CMD ["/bin/bash"]
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88a33dc8906274baf54eb28aeefeba84c17922e3854e6fd41883f273d87d330d`  
		Last Modified: Thu, 08 May 2025 17:05:28 GMT  
		Size: 47.7 MB (47672989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b5aea1d0deca854a3762f4e396dad66260211f50004210a8e73e2146af926a`  
		Last Modified: Thu, 08 May 2025 18:03:59 GMT  
		Size: 38.5 MB (38500810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2459ddd545b85e50a4b92ff1a7e6b4b44a14dcadedb662f631a2282cc1811c91`  
		Last Modified: Tue, 13 May 2025 19:18:52 GMT  
		Size: 210.6 MB (210646805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9448ca1bde7e23f389351c8a23058670e2c170a9632dede1384e13a35049b595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3642301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb001a75e6c7f7fe454dada0a73df49988e64fae56aef2d06086793f209c4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:1ce780b9a8e62e9669b2b15d0dbd4949df4adf569035c644e41513a778931729`  
		Last Modified: Mon, 12 May 2025 19:21:06 GMT  
		Size: 3.6 MB (3622268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61a0d7ee57cda374f35bc305d88cb8e0d831023ae6b27ced689785dcbb48160`  
		Last Modified: Mon, 12 May 2025 19:21:06 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
