## `openjdk:25-ea-26-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:44bd0931c9deb0087d9d4ff95f25af4753981a6eb457c8910ff0232e888cfe08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-26-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:97c8e0b4dca3da07f64dd8e3247a7024aae8e79a6ce79c60adec7941f0b4e16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289769028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1aab3a1d62155f93721f3df809cbdb4dcb3685ce61e6e89552736eded7bee3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 03 Jun 2025 19:32:58 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 03 Jun 2025 19:32:58 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1a7000049ecfef865d125a112ed40237daf19bc27e872529fef00770b81ebc3`  
		Last Modified: Tue, 03 Jun 2025 22:07:40 GMT  
		Size: 51.3 MB (51313330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e660856ac9db99013379592b8dcf72a53e959e2e0d80dc7c8c2fa5c150de6b17`  
		Last Modified: Mon, 09 Jun 2025 22:07:04 GMT  
		Size: 15.0 MB (14996676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143eca03870010a19da5eabd2f369b78da4b54243ecc612940a30323e63d101`  
		Last Modified: Mon, 09 Jun 2025 22:06:50 GMT  
		Size: 223.5 MB (223459022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:4fde938df54d79df21abae18ecb6e9d2167ca61d9cf841f4b3513f4423d672ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36372bd22156aa90b9ab7ce7215124f05b8d4b0ba9abc29c8f9b23457a59d27e`

```dockerfile
```

-	Layers:
	-	`sha256:c8a9e333d23c3cd805918cd52f750d5a84ad608b8d35bae865be980c8ffc454e`  
		Last Modified: Tue, 10 Jun 2025 00:24:02 GMT  
		Size: 2.5 MB (2451686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207196271d1723652b407df93320cd315cb90e46d69934ccca92b27b9e93b576`  
		Last Modified: Tue, 10 Jun 2025 00:24:03 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-26-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d7c56d609b514afa3bd71fc6b0f37d1c88b4cd864b727427e73adacb9eb6b0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286941656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad695ce2dee063ec5b1b70007cc52a5cb6e2b441fa08ff39a41f75768ff691`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 03 Jun 2025 19:33:50 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 03 Jun 2025 19:33:50 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:44b8a99d3aa3536846330d8b29cdcd8db5a0cb5f437d15e0651b4265acba376d`  
		Last Modified: Tue, 03 Jun 2025 22:02:54 GMT  
		Size: 50.0 MB (50031883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b00391e55b48ca359f7e73a227e9716652430842522c8307dea78a7e6106ece`  
		Last Modified: Wed, 04 Jun 2025 02:15:38 GMT  
		Size: 15.7 MB (15667780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52022c3386e659d9eb43a95f29d5a09b2260721406b58276c0d1a72ae71a15dc`  
		Last Modified: Mon, 09 Jun 2025 22:31:42 GMT  
		Size: 221.2 MB (221241993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d8a42089b370d39015a1c11767cbf8afcbb937e10dfd1a7c8b75f2f6fc8c89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd5806d79304295ace49f3939a02043d58de3f6c52cea9499e320a312fb00a4`

```dockerfile
```

-	Layers:
	-	`sha256:0fb15901c4c6a6ce70492b2afb5f7c06dcea1bf66e20c87d6272493aa44405df`  
		Last Modified: Tue, 10 Jun 2025 00:24:07 GMT  
		Size: 2.5 MB (2450532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d5aecfca02489b7b4f7026d5d0c833f8faea6d945041c109834563dc10f919`  
		Last Modified: Tue, 10 Jun 2025 00:24:08 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
