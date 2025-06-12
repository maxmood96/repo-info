## `openjdk:25-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:93a56f34538fc1c18577964848f713a3a4e537eab4df01acf7fed4dbb2aae8a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:6f573ae0e21b5915a99e0c7c7bc4b5d2b9792c622ae273d03fd6a3e1a2e14f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289744363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882aeb0265654f737b2bbfb7230e255a3785ed9cd51a4ac9c38cb9bd3069b6fe`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Jun 2025 06:48:11 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
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
	-	`sha256:6987fb89a70d9360470c7d0a557d09b1376bb71b0da1a493ca4adfb203bedf83`  
		Last Modified: Thu, 12 Jun 2025 01:08:11 GMT  
		Size: 51.3 MB (51315459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555fb9501b98ab4f16912c3845b4f8368b9645fe1dc6e75a61f1392bccf5955`  
		Last Modified: Thu, 12 Jun 2025 01:09:54 GMT  
		Size: 15.0 MB (14984399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c31c993ab6b628a476ba6e12146d754b55ded48d4714b4e1e0f01434e11f014`  
		Last Modified: Thu, 12 Jun 2025 03:29:04 GMT  
		Size: 223.4 MB (223444505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e3ee6f175d77cc3dfc3629235e6988031394b85d6aedc1eeac3234ce6d64022b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c582f63f4a03f34f1fde2c937f75c70095c611005b4c4d8714664d929be1a48`

```dockerfile
```

-	Layers:
	-	`sha256:c6838041a2cc372af43b92db9c78c2a801788295113b96d44b785d684bb7b9bb`  
		Last Modified: Thu, 12 Jun 2025 03:23:24 GMT  
		Size: 2.5 MB (2451698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fafb4436ab946e8a3f53353a80d6dcff0a6181678f8950639dc4b109cd340d`  
		Last Modified: Thu, 12 Jun 2025 03:23:25 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oraclelinux8` - linux; arm64 variant v8

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
		Last Modified: Tue, 10 Jun 2025 01:51:36 GMT  
		Size: 221.2 MB (221241993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

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
