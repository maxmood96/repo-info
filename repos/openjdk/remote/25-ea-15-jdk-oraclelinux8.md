## `openjdk:25-ea-15-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:286029b5d40db413fb85684d48d08194cada5d50fbcd711d2996af7d087e3ecc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-15-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:170b4533d29e9fe9486f22eb4e7a17d1dce855339190bdf7a6c89e2bc9333d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278564756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e144856cd9a7d73b7b36c4e8713f88472def47e5fddb65cb3f0e06cf5bdcc1f9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Mar 2025 17:20:06 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 14 Mar 2025 17:20:06 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:035e56311411a7644fa1341dfc093e1b278feac7d55c98ae09177e1755672600`  
		Last Modified: Fri, 14 Mar 2025 19:00:09 GMT  
		Size: 51.3 MB (51288940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9c5a4a4030a61acc7b39980eba1e70f55d38acc12b1e5f36a393954edbfff6`  
		Last Modified: Fri, 21 Mar 2025 17:13:17 GMT  
		Size: 15.0 MB (14996360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4feacd7bf9442e616f01ab877e2df6017cb450b3ee9aa12d75a8824de9ef66a`  
		Last Modified: Fri, 21 Mar 2025 17:13:21 GMT  
		Size: 212.3 MB (212279456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-15-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:288b142e518d2e13f24111aa8196de4dd185dc5708f7aa7cf0865faa34cccb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049e0a8db4ee93e7359543607fb454e7f8467e0644f13a1b21bd59ee47beb640`

```dockerfile
```

-	Layers:
	-	`sha256:a9a3f3fd73139610bd20f25a7c0de3986888c5400ea5f5e720556a1f735dbe35`  
		Last Modified: Fri, 21 Mar 2025 17:13:17 GMT  
		Size: 2.4 MB (2440967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06567a6d4c290ff7e97f0f87038ca66773be0b41513c5ceb51fce067f838ac3`  
		Last Modified: Fri, 21 Mar 2025 17:13:17 GMT  
		Size: 16.0 KB (16036 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-15-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b4af66d9d2998f42f1b8e921a484c5170ea1f70735b3103d6f02e90b593f9442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275912226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755e76c9af83ac790d394c28931504b4792b3fe3086908b94157724f7c188cc9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Mar 2025 17:20:57 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 14 Mar 2025 17:20:57 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f8eb825c1fc22ded5eda8a11c91fd13cd2b63722a0fdbe5ed89339ba10aabad`  
		Last Modified: Fri, 14 Mar 2025 21:52:22 GMT  
		Size: 50.0 MB (49989226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d2d63d00da99812eb8285d347cd8a68c6913a3b4f406a756d3804e277dc4d6`  
		Last Modified: Fri, 21 Mar 2025 17:24:29 GMT  
		Size: 15.7 MB (15683223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cbeec94e373caefb3c1ed4073210a2aa6a4e4bb49db4fad9c94f5e7a9feb77`  
		Last Modified: Fri, 21 Mar 2025 17:24:35 GMT  
		Size: 210.2 MB (210239777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-15-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:65729f8d7d369c5a63ad33164c7bd75dbe906f91ba8a8a3c3e8b6776a268bfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c941a5987b7f1db0c09ccb4ca4c7672a004868f980b75788946bed77585c30d`

```dockerfile
```

-	Layers:
	-	`sha256:5e20314b1e71b0cdbdc0ff4bd20bfad848cf3fe2a10550961d798bb7da4adc3c`  
		Last Modified: Fri, 21 Mar 2025 17:24:29 GMT  
		Size: 2.4 MB (2439813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce2a05db9e71aa7b7e6094d82f8141e74b97478998f2a822ade71a8840fb7dd`  
		Last Modified: Fri, 21 Mar 2025 17:24:29 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
