## `openjdk:25-ea-8-jdk-oracle`

```console
$ docker pull openjdk@sha256:4aa5334c789aa1816f743ffdd1a09d09debc8037168966435a1b63a6721fe687
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-8-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ad92d335409627cf1cf446117945d7e8400ee280ded65a46a51fe6ef1c9dbfb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309635457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe510126488bec0da1b17b1d822bbba45017a7e916c0898088e9e3c3e44dabda`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:53:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4473ac30a86889f60ea8914c724cb3cd54d1b6bbcbd1ebf35dbc71966ecf13c2`  
		Last Modified: Wed, 05 Feb 2025 20:27:27 GMT  
		Size: 49.1 MB (49097303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103981c0c5b8d6a4f21ba25801f427114ee878996dd3cff0e0091088a1cc7fd5`  
		Last Modified: Wed, 05 Feb 2025 21:08:57 GMT  
		Size: 48.8 MB (48767729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bda5d6d9c8a831cd1deafe7812bbb779017aed2527109341661b654f1ae239`  
		Last Modified: Wed, 05 Feb 2025 21:09:01 GMT  
		Size: 211.8 MB (211770425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d3fe631dc2d7cc127aafcd162934b74ab2da4e416dd3edd771c783a0963e9b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df68ec2091d749e6f3518e859c0cfd52f011298b6a4de891e72e6f10d8200a71`

```dockerfile
```

-	Layers:
	-	`sha256:411b66cea7a1d4b1664e9842609af58b87233362cc1f024501579c3cec34b3db`  
		Last Modified: Wed, 05 Feb 2025 21:08:56 GMT  
		Size: 4.9 MB (4906973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61532589ec87ac7d650785bce721cba699cab86234b93dd030d493c18550463e`  
		Last Modified: Wed, 05 Feb 2025 21:08:56 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-8-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3a73243e50f18a8642c29e518ceb63f689b6be70d7de5f98d2fa3c1d33073894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306600044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f4aa5ab50a0d9c26450ddf7f5d19f0e36ee860a25cb4460c22b6208c793920`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:53:00 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2f97c86c0c517d07b9fa71c28eb13c96bff23fd0c0c7901f5f73c962492667d`  
		Last Modified: Wed, 05 Feb 2025 20:36:01 GMT  
		Size: 47.7 MB (47669410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354218c5a9ae45d85db8f8a7c222a5a95ac10891fc8bc4e58bc61dffb50dcd3`  
		Last Modified: Wed, 05 Feb 2025 21:14:50 GMT  
		Size: 49.2 MB (49193687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4ad251f44064f4171366f03a1148ad9e51997cbac00b663e8ab156616a9b57`  
		Last Modified: Wed, 05 Feb 2025 21:14:53 GMT  
		Size: 209.7 MB (209736947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c81bc25af3689d1616137165a74cb26a1144510d739f8dbfbdfecfeef6427a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a089bfa74d361119a93e6a38aaeb3068272e64fb44319b4bd25ea7a941913de`

```dockerfile
```

-	Layers:
	-	`sha256:70edb94bf6cd79ceb226f1fb7051b593ab806b832b248b9d0971fa35d6906f3f`  
		Last Modified: Wed, 05 Feb 2025 21:14:49 GMT  
		Size: 4.9 MB (4904735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e413d22aed2f50723568f4567eb64bed1ffae3c32c85c5cb8d58a646806bb7`  
		Last Modified: Wed, 05 Feb 2025 21:14:48 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
