## `openjdk:25-ea-9-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:3c50be3850b9d48c3d40edec9f6d704694664d6a27e6bebde4eceb544dc8a280
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-9-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c0986b35aa70c87865aa2e3aa747a6615ccbce42cc33fd34c9e2f450ece3f5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278556718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc905b762c4a84bb7233211fffcc683b2e27e84ec34b1292ec33172bfaf1db2d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:53:06 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf5a3c7d8890a64c60d60ea38b6b8682451c6b3cd9ae69910ffebb43788bbd38`  
		Last Modified: Mon, 10 Feb 2025 22:36:59 GMT  
		Size: 51.3 MB (51276195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a492cc5e753aaf56627fec96c35a7e0e74f319c7c46a2935a1f971fc63f8134`  
		Last Modified: Tue, 11 Feb 2025 05:17:08 GMT  
		Size: 15.0 MB (14987460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee85c213600db4a98833f79b2fd88618fd10e81698017a6d3a6dfb8fbfc5645`  
		Last Modified: Tue, 11 Feb 2025 20:51:53 GMT  
		Size: 212.3 MB (212293063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-9-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6f402f8e64de252c4d4b5f1c49cf1874702d0a340a5cd10b232396cb739ccaed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ecefbf8e3d2cafc8691eb667c6c7c261b75cf905bd7d35343164c8315f173f`

```dockerfile
```

-	Layers:
	-	`sha256:cc749af92a399f815db5334254daae28dc4f3176d0f6ba55de7ba4e7b7ab995d`  
		Last Modified: Tue, 11 Feb 2025 00:28:32 GMT  
		Size: 2.4 MB (2444715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2f3ec8f9bdf4e1a078b5edd20e96b58a217e569867dcbc5d5847cf3d092023`  
		Last Modified: Tue, 11 Feb 2025 00:28:31 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-9-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:07edfff3f6df1aadad818e5acb1efffc4a43c21244e5b689c8c84b4f4fa19b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275908969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a851cddf569b6bb8b74d70bb9fc0b16711e8c56981d7bbe5ca5516aef82a9f10`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:53:06 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:98af9e98299537ec5803bfae733caa43c349cbe6b0be9c5471f90fab89c45c6b`  
		Last Modified: Mon, 10 Feb 2025 23:45:58 GMT  
		Size: 50.0 MB (49984203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9af9c67dcac1b4e361524cf6db54d3404388fae351d6ce90ba33475433a67`  
		Last Modified: Tue, 11 Feb 2025 20:36:07 GMT  
		Size: 15.7 MB (15669487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e531a4a1a2283016f4e44d40b1ece1ff7ed22407acb9d5bf8d3dc82c5b845fd`  
		Last Modified: Tue, 11 Feb 2025 20:52:20 GMT  
		Size: 210.3 MB (210255279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-9-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b162fe08db069b28694be1b086e761c37c252b53ff47050207f85ceb6d38be3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9754d8ec1665962c8fa8ad9dc6ded2afedcabe8258260aa9de9bc02e4c33fc`

```dockerfile
```

-	Layers:
	-	`sha256:b13bb59d8e92465d2f51eaabdf05017c2ac1735a2d309975f8b777bd090999f9`  
		Last Modified: Tue, 11 Feb 2025 00:34:59 GMT  
		Size: 2.4 MB (2443561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a5b2e3f07fb9087bc7d180e4ca60d3b5d6523ee8c3b231e32aea134b84fb040`  
		Last Modified: Tue, 11 Feb 2025 00:34:58 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
