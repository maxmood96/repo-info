## `openjdk:25-ea-27-oracle`

```console
$ docker pull openjdk@sha256:8ada874f07636c7924c8b30ad25713bd456b42f795b81e99ebfea35d99a081d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-27-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:2f0cc3aa42198d3f7d9e0770d1565ba6eb4dbaa676376607b5f4a151318bf2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290254679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe98b9181930f4c85b3a3f621339a526c3538fa919c76d8c135bfde6253c7bf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:36:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:36:51 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42004ae9d93b45f1c4e7f6585e70821b076801d64a1ef22a312489b0bd4e637f`  
		Last Modified: Mon, 16 Jun 2025 17:51:20 GMT  
		Size: 17.8 MB (17776003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9649a60a07b0e3b887b50dc945839deb1275ed5433cb38787c041ffbd93de5d4`  
		Last Modified: Mon, 16 Jun 2025 18:25:06 GMT  
		Size: 223.0 MB (222977779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-27-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:85f05377f0ff2e0cc397188ae958b0e89f0f11b0809566c330985a406fa5683e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447bd3d37850e0ff7d429384dc3aca25352b3d15a043f5bddb97f433f764d6ed`

```dockerfile
```

-	Layers:
	-	`sha256:da56d2cb3373d2e8411087235656cc5943fc67cfb696df4ebf07cd3cdf712a64`  
		Last Modified: Mon, 16 Jun 2025 18:23:28 GMT  
		Size: 2.6 MB (2603123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7d6235fc1e1e828e6bc256cf7322f5c4f3491acd8a02ebd7fad0b46d42432d`  
		Last Modified: Mon, 16 Jun 2025 18:23:29 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-27-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1ef8b4846a36b36de08ff4df971e174338b40022b575536accf2933f6cadb202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287176142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ed4b905854081d7fd6ec63ca5db77b64b0d263a32bca75dffa55a642aef530`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:37:07 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:37:07 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7e489c978e38b5afa5d393fea94c54ad3525e6f544c411be6e80f47ef76d0a`  
		Last Modified: Thu, 12 Jun 2025 06:41:39 GMT  
		Size: 18.3 MB (18321513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de6e926efa27e66ef90c1626ec5b81feeab041bdfea8873819fac96b83c393e`  
		Last Modified: Mon, 16 Jun 2025 19:24:08 GMT  
		Size: 220.8 MB (220764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-27-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:2e8ea2aea82375d2d18cf1e1de241a1a0844cd24def36e13ede8cecd78b0d846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9193138c38392f6c5ef3f1c9575f2bcdace7ec660770070991a39dbc8a71e1`

```dockerfile
```

-	Layers:
	-	`sha256:e35dc631e515c27ddd4fd677bdf56aeaead9ffc6c90bc27ebaa2220016c16917`  
		Last Modified: Mon, 16 Jun 2025 18:23:33 GMT  
		Size: 2.6 MB (2602115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68914a3996e7a0c439078b169b7b37e4a0038be3d868ec5408e58f6195366d55`  
		Last Modified: Mon, 16 Jun 2025 18:23:34 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
