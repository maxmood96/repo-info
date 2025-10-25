## `openjdk:26-oraclelinux8`

```console
$ docker pull openjdk@sha256:c4389047556771e4177b6a2c210fac640fddbb75eff27abc6e982ec027bf3bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:317caf13c1bae7bcb4c9c80d175c3f7f2891bb5fa7f94dacddbcb1d3f6d72e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292507095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35de2c9cc899b232d04b301e05bd3badd3889a3b5d823eed7a038bab2ed0cdcc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 20:06:10 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 20 Oct 2025 20:06:10 GMT
CMD ["/bin/bash"]
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 24 Oct 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Oct 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='3189ce7f96b6fb0b69ce1e8ca7bc626aa30009023f9e2ddf7faeaa5ddf9e8626'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f2d4dc408e6fe82574fb9ad9cff97da63a897a887198c666cb1bd0987fa690c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70e7deeb6fb1025fbac694ef1855ba75493ab45e96d46a5423af063e321cfd2a`  
		Last Modified: Tue, 21 Oct 2025 00:13:40 GMT  
		Size: 51.3 MB (51317328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ea3ef2e49ea2abad0cdfb012a0fbc1e2b22f84d43cdc6f5b4b690cdfd6067d`  
		Last Modified: Fri, 24 Oct 2025 23:21:33 GMT  
		Size: 15.0 MB (14989622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760c9fd4136b7e8b3d85a904ec2ccbe9ed3d5545a13794d299c01690ff57be9e`  
		Last Modified: Fri, 24 Oct 2025 23:24:00 GMT  
		Size: 226.2 MB (226200145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:cd26c292ea3fdd70918884de0de199a788c878ed933b20c0b4d0fd951a181d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4c0401184debffb5983a09d93878ccaa46ada30b81e9aa43a08ce02d1ce915`

```dockerfile
```

-	Layers:
	-	`sha256:26f49423c850455db409572f13fa5664c8b2d9adcb46511a784791143b34ef68`  
		Last Modified: Sat, 25 Oct 2025 00:23:59 GMT  
		Size: 2.4 MB (2449882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:761424620092574e838f04321edc5a58f0f2ff8afb0e717cfbfc6889947eb6e0`  
		Last Modified: Sat, 25 Oct 2025 00:24:00 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cf5c582bb4627d983ac92d936f20227f44ab1082e431b696b1e424462de9244d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289758900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92627b1cd899d149ad0ad98284f88f90c90869131c4b5cf7a67bd94d45701e8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 20:07:14 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 20 Oct 2025 20:07:14 GMT
CMD ["/bin/bash"]
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 24 Oct 2025 18:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Oct 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='3189ce7f96b6fb0b69ce1e8ca7bc626aa30009023f9e2ddf7faeaa5ddf9e8626'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f2d4dc408e6fe82574fb9ad9cff97da63a897a887198c666cb1bd0987fa690c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb2cbf1306f13796052df61db1ffdb76b5d1db3837223eec0859c6a0d6f6cdff`  
		Last Modified: Tue, 21 Oct 2025 00:12:37 GMT  
		Size: 50.0 MB (50043445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13104b4aab4a4eb128595d400e88a29c48bfd0ea1cae2d777c0f1c307219bb79`  
		Last Modified: Fri, 24 Oct 2025 23:23:54 GMT  
		Size: 15.7 MB (15663159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001518ea2aa87c15470e5090313dcf5e9740acfa0a2c068a11adda0a59270e14`  
		Last Modified: Sat, 25 Oct 2025 00:41:14 GMT  
		Size: 224.1 MB (224052296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:75b9fce5c85a99b52c24d434bce5da2b108b2f3cca8ad2d57445e1ceb44009e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b25fbbbc35ca0e4946b86740c50d02d87f350e80a198727a3b8c3b3e959bf4`

```dockerfile
```

-	Layers:
	-	`sha256:2ddca645141da81b204b4c49dd804130cf3735363129bac21bf78bd8fed0846b`  
		Last Modified: Sat, 25 Oct 2025 00:24:03 GMT  
		Size: 2.4 MB (2448716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881e8631c213a602aaaadf346fc65c983552faf2d4fd9ada3ec20fe1ec7407ee`  
		Last Modified: Sat, 25 Oct 2025 00:24:04 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
