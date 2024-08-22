## `openjdk:23-oraclelinux8`

```console
$ docker pull openjdk@sha256:7d4932e242502f4fbadeba390ec3157d4ac187e045730ed2ee2abcac60c1e927
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ee4df0a8f47b815078492a3901a461ec3f08b2a6119dd815f6903044b6c325fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278001001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8161ea15717154c06953728087d7ef62f973ec85dc4bb36b17ea7f48371368`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:50 GMT
ADD file:f88a328d16b39a012900e14f6463799b448cd9796472d5fb3c58c2cc5ebdee21 in / 
# Thu, 15 Aug 2024 00:20:50 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:964443381b57e80f40937734e7dfea9e93836abe517bd3e9e9c0fc9f21af4ee5`  
		Last Modified: Thu, 15 Aug 2024 00:21:56 GMT  
		Size: 51.2 MB (51221701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fe253de49acd9ffaa99b541612b0fdac7dc007c65f3aadc3f37ddef689287d`  
		Last Modified: Wed, 21 Aug 2024 21:03:46 GMT  
		Size: 15.0 MB (15036094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de935fa6c91d46094a4b59ee98a7ca34c801b0d7c41574b2b673a31979556c6`  
		Last Modified: Wed, 21 Aug 2024 21:03:48 GMT  
		Size: 211.7 MB (211743206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:dd0ab74a1b1c039679f39797e745f186dd790a589170a0a9c6d06715cb4c1f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edf5240ab3179150dcbfdfa1b5ea236413bfca3d22a19ac31630d45b46c6224`

```dockerfile
```

-	Layers:
	-	`sha256:bdb246dc55f83503a13f01e4c26af9b2494a67766fb958da52a8829fd625e602`  
		Last Modified: Wed, 21 Aug 2024 21:03:46 GMT  
		Size: 2.3 MB (2287161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457a3933694954707064dee1bc3cc06c7b76dcca8071da76bb66eb71833faf72`  
		Last Modified: Wed, 21 Aug 2024 21:03:45 GMT  
		Size: 15.2 KB (15216 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:31d15adf47576c8a8e1d19bc215f169b1fdeac3a89ee88fa09b0e704bbad6694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275242579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27218d46f66e2775da8dbe11b455a464d410c3c9e218d461e90d860be334002a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Aug 2024 00:40:24 GMT
ADD file:ddad218f4909f6f7002ab7531840c692add651f86b77e1e847d3d9b2bfc8c8b6 in / 
# Thu, 15 Aug 2024 00:40:24 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed876bde92ee249d3e0143b5e51b17dcecf0128d775998e97e0812e3218cde0e`  
		Last Modified: Thu, 15 Aug 2024 00:41:13 GMT  
		Size: 49.9 MB (49924065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ff93538bc6272378ffb755908dacde2dad43d975364d67e19f6ad1f4763010`  
		Last Modified: Thu, 15 Aug 2024 01:50:06 GMT  
		Size: 15.7 MB (15687212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbfe344663677d64a7a4cf6fba66e8ad546c796b939f85f8c82f5edfbc8d204`  
		Last Modified: Wed, 21 Aug 2024 22:03:12 GMT  
		Size: 209.6 MB (209631302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:55486b67440224c70075e29cd8e0f25e50ee80012a0ac293d5229d02cc4f60a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7361070378145a3a7192d51812da727eae8bd26aa065c244e0b6bba1f25c7d6`

```dockerfile
```

-	Layers:
	-	`sha256:fda9c13934ea2d3b8ad24c6c393a4e1791badeba1851bfc406f211f69552bbfc`  
		Last Modified: Wed, 21 Aug 2024 22:03:08 GMT  
		Size: 2.3 MB (2286606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8b9cf2a1d84c6d004885c6c594e7d7100a81c14cf82ddb20ea00e3b2ba6402`  
		Last Modified: Wed, 21 Aug 2024 22:03:08 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json
