## `openjdk:26-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:44bcbb75fe1fa085b508efce070ed8830b0eb3deb2fc15652f23f2fb010a868f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:7ce390ce47f8ca964b4d4b218da66b0c1694fda40d8168cde41a22fecaf49b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313453563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3482d46e9b36582b5aa4068400223c49c89e32570b7548bd726a7b18a6af90`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:56:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 01 Dec 2025 23:56:04 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:56:04 GMT
ENV LANG=C.UTF-8
# Mon, 01 Dec 2025 23:56:04 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 01 Dec 2025 23:56:04 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 01 Dec 2025 23:56:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1e7beca9da8929a21cf0bbc290c7a45ebb91f2912dce755c3b892a2ca75314`  
		Last Modified: Mon, 01 Dec 2025 23:56:44 GMT  
		Size: 38.3 MB (38298549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277b75919ed638d6ed14626c901bc99b869b5d3b995e798433e472bd185d522a`  
		Last Modified: Tue, 02 Dec 2025 01:24:23 GMT  
		Size: 227.8 MB (227842840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:7889d6a3ff4cbfd1cb66118197f4b6a063016b013eb8133c1f2f181dc75647a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8834590f09bffaade9195c9bfefcb0afe3e3d01efcc05d1a21aa9d973e88ec77`

```dockerfile
```

-	Layers:
	-	`sha256:5445f306acaef5a945b32f02db4174b07ed621f4f781d2262149be9f030fab52`  
		Last Modified: Tue, 02 Dec 2025 01:23:21 GMT  
		Size: 3.7 MB (3655335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb4e53b0c2c0041ab613176e474aceb0a9876752d38d2e2c4cad71eb961a5510`  
		Last Modified: Tue, 02 Dec 2025 01:23:22 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a91e91a154409c3f9ba7216a00fc8cae257d8f4344c70405e10a907ac622e664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310296281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64dc69982d8738f5a6c315707c548f15c64cbaacfc74cc00d1cd43ac07a62d8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:32 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 02 Dec 2025 00:00:54 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:00:54 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 00:00:54 GMT
ENV JAVA_VERSION=26-ea+25
# Tue, 02 Dec 2025 00:00:54 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 00:00:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308df83357c5198d9277ca2a56e4edc736d61264b59da41ecae0f16b7695865d`  
		Last Modified: Tue, 02 Dec 2025 00:01:32 GMT  
		Size: 38.7 MB (38699069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fd18358ce2f86d83d28d9c52d7bebf954d10eb85a45ae2fbf515ba0c1b7d29`  
		Last Modified: Tue, 02 Dec 2025 00:01:22 GMT  
		Size: 225.7 MB (225700235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:4ff1ffe5d540d788944b3e14409b0bec3eb7de9b37db1dd0bb1f788fbeee3c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88e6c08b476c0dd3cd4e705a2e33354acbafa6eb6c8a061085c1b8a3d62cf29`

```dockerfile
```

-	Layers:
	-	`sha256:27736733cd9d3c4b58053c700d47f8ccba3f284221ae776807160a0d759514fc`  
		Last Modified: Tue, 02 Dec 2025 01:23:26 GMT  
		Size: 3.7 MB (3653025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a18f53bdf932e0a8c609a99d7e1142ed7abd5f1fbd14d4474e38d3dcab6201c2`  
		Last Modified: Tue, 02 Dec 2025 01:23:27 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
