## `openjdk:24-jdk-oracle`

```console
$ docker pull openjdk@sha256:b8682b25e0b61af6ae70016d9c3bfa4f7b94dccfafd1bcb93b4818d5808b0bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:392962dfffdc968e04ca6b533aa30dffd175929ac4a59575cc842fcf5b4875b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (319968794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78637fc9eae62dd1ea91682e7e7800ea7b9fd1db06e550510292411e1c6ab3c7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 01:48:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d46195ad810e47f2f605ee915f01aa5f77ee87ca12244f70dcfddb4ff90f23`  
		Last Modified: Thu, 21 Nov 2024 23:10:22 GMT  
		Size: 48.8 MB (48768074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde490c9f50353f1e3ba401a1ca94adace16ae458d6f24d9e62663ecc3004448`  
		Last Modified: Thu, 21 Nov 2024 23:10:25 GMT  
		Size: 222.1 MB (222102018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6fd33e8c33627560d2ffe8ddad98a877930c5f8bf9922facef5b0cbd39c9ccbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e494062242321765f56152fd3e2bdf1d643128f05ca7e931ad743b32ea818afb`

```dockerfile
```

-	Layers:
	-	`sha256:5661756d46ce82f6bb767d7208f1ec438e4feb4dccc59005475c0e778cd12ca7`  
		Last Modified: Thu, 21 Nov 2024 23:10:22 GMT  
		Size: 4.9 MB (4913857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bc8c060f17dd06683cdae38ee12a08fe6da7d5c79d7e16681be2eda69c6f08`  
		Last Modified: Thu, 21 Nov 2024 23:10:22 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bc05dd9b0557038cda36b7c02ed444ba171155f6866ab56e3a2dd3c9e7d8c12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316907567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f456277405a472744993f2958f260c2ced4f278b5f458c8dfaf92a6369862e84`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 01:48:14 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff9f5494a427d9d8a40a0f42c60afadac361e3515d52601f7d74bf0d09b993`  
		Last Modified: Fri, 22 Nov 2024 05:14:01 GMT  
		Size: 49.2 MB (49188086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464052b08c30f0526b69c962ae0efd4979e621dcd22acac8eaafc5833c975ac4`  
		Last Modified: Fri, 22 Nov 2024 05:14:04 GMT  
		Size: 220.1 MB (220052089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d07146861dab48f05a23860f9a28b037f5c7236fa14d83f348f8be76c743b2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748007b935d946a794f6e1f84f2c9e82c8eafbe396b26110a355568dd61d079d`

```dockerfile
```

-	Layers:
	-	`sha256:ca69c100c049f3e4dff00225556f4e40064c27e6f7633c69d54035d5a702924c`  
		Last Modified: Fri, 22 Nov 2024 05:14:00 GMT  
		Size: 4.9 MB (4911615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8163a1adb34041db5d46c2817f2f001227ab3810e1f78c89cdeada68ba57a313`  
		Last Modified: Fri, 22 Nov 2024 05:13:59 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
