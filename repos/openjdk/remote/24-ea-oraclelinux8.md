## `openjdk:24-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:d4ab8e493966aec28bd90b215d393d7af38b6145f9236ac370c31635cfea63fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3f1fe175050b38d98d1ed2545a72d8c6a6646751dcfd8da72fcb18d7a9cb8223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (279033237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c061bb2430bb809897a222420afe4ca942653ae619273ec071dc8baeeef9c639`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7d760ad2fe664c6995a4d9508e389d78b6bdf1b1f154b4a216d0fd3ad9a46bc`  
		Last Modified: Tue, 10 Sep 2024 01:03:41 GMT  
		Size: 51.3 MB (51293960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ecc9eea6f7896c37d9cadafe8a3020afc9ca17abd65382d4e27f36df0ae93d`  
		Last Modified: Tue, 08 Oct 2024 00:01:40 GMT  
		Size: 15.0 MB (15041577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9044fe4f6e137adf63f58163b959051da15f5fef5f39f26dea98aa172296cb2`  
		Last Modified: Tue, 08 Oct 2024 00:01:42 GMT  
		Size: 212.7 MB (212697700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e5c5a26fb1d32bd16b52a788c131750e8b13ccaa0e53dda18f88deb01fcc7306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2441785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bedd9dfd988ecf622c9fb0b8aae1e0e43f85277f762b29b51f25aa764e8ceb`

```dockerfile
```

-	Layers:
	-	`sha256:3ed0258aef43b6cc0150b42b649b8f1d765b14819d41c6544f2ce366f1675134`  
		Last Modified: Tue, 08 Oct 2024 00:01:39 GMT  
		Size: 2.4 MB (2425776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:670021a3052efc6bae91aefc4a5d85411c801fa253964784ecf569e51c03b8dd`  
		Last Modified: Tue, 08 Oct 2024 00:01:39 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0183cb637f7cb68fc0d23a6542a4c26fcd1850451cf981a0d3896bbb611f6891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276221138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227c972b7a96c5385e60cc6f82b3227cff4967affd0bc27758b194c33479593f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:35:51 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:35:51 GMT
CMD ["/bin/bash"]
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:26021d1fe840c0392b944d95d8144754412f70a5f838918b647f05d3328586c0`  
		Last Modified: Tue, 10 Sep 2024 05:36:16 GMT  
		Size: 50.0 MB (50007854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb09382512e8e5cf2ff5a711103dc9414fc83bd78340e128351f17f67c61fe6a`  
		Last Modified: Tue, 08 Oct 2024 02:30:45 GMT  
		Size: 15.7 MB (15702226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db3807f7cc5ebb1d0d78e617ba374af42a9dd63e6d9545ea7175a9f6f4a44d1`  
		Last Modified: Tue, 08 Oct 2024 02:30:49 GMT  
		Size: 210.5 MB (210511058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2044d4a1a6c2aa5d85c94efbe348802bd44cee4306e537563ed0df799fcbc17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1754edbd60c62a86047a56f9589737d09f16e3c8b3fc618d19697da2e275b25`

```dockerfile
```

-	Layers:
	-	`sha256:5a61e165c51a26b9bc9f7a393f204245e813a84e1b74c44cae0ba2e6a4ef6e3f`  
		Last Modified: Tue, 08 Oct 2024 02:30:44 GMT  
		Size: 2.4 MB (2423998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55641fabea1e1823aa3bd128e81940d961f7a2ce3c75b1ded4db8d6a48846fd9`  
		Last Modified: Tue, 08 Oct 2024 02:30:44 GMT  
		Size: 16.2 KB (16152 bytes)  
		MIME: application/vnd.in-toto+json
