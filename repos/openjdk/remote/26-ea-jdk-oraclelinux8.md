## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:01f967e044f8244d4ef985766d47c2eb7bc89781bd6a6d12726a59231b0e8ebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:2a40b4d01f54bb03349131e61624e85cc1697b40466511ab67b8b17774f7b44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289615855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31918dbba61ec2ee290b4a584bcb1b9a698747802aa3fcdccabca10a5407c93`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:42:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:42:18 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 18:54:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 20 Jun 2025 18:54:20 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:54:20 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:54:20 GMT
ENV JAVA_VERSION=26-ea+3
# Fri, 20 Jun 2025 18:54:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='f043a64fd0a2cacf76196c3e6a05de743c7e40f992e4e268ff829d094995e367'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='62251f3d724a03e4c25ceeca4bb75755b9e70ce275e5a4bf2cbb1e6579699839'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0915556054e5fcd1f04e454b0deedf305bb209616c5a72a8b2d83db9191e5115`  
		Last Modified: Thu, 12 Jun 2025 21:07:27 GMT  
		Size: 51.3 MB (51311558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322ac18f9f9f549a94cd58912caf90c3a8053601e3ed87e7005e75454a315a1c`  
		Last Modified: Sat, 21 Jun 2025 03:30:38 GMT  
		Size: 15.0 MB (14979248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb4b92b2ccaa301159d4f43f8e2052910226e015268968bdfb45279511d1fdf`  
		Last Modified: Sat, 21 Jun 2025 03:30:43 GMT  
		Size: 223.3 MB (223325049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:cbc2e74e8c3e5a40f5822487367853fdd9f77b42bbb594a2c1dde3d66b5674b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a0984254fe6133e52ef34790bd53d949d7c2c28880c4c55b54d506abcfe25e`

```dockerfile
```

-	Layers:
	-	`sha256:7f9f9fffed2ef076b3e5dd24869a666754508ff8c6624465bda5714d03ec90e1`  
		Last Modified: Sat, 21 Jun 2025 03:26:00 GMT  
		Size: 2.5 MB (2451698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c203d593756f1047759872634baae0ac300831cc6aba67d480f9a0f74150da2d`  
		Last Modified: Sat, 21 Jun 2025 03:26:00 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:de44afc0299c238465aec3113d57d3af6397c3e06c453f4e16b70d6c0aa61b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284083530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07651628dcf2e63446d790150e99d297b558dc81f3187a89de07c125d8c4e1a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:43:09 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:43:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 18:54:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 20 Jun 2025 18:54:20 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:54:20 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:54:20 GMT
ENV JAVA_VERSION=26-ea+3
# Fri, 20 Jun 2025 18:54:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='f043a64fd0a2cacf76196c3e6a05de743c7e40f992e4e268ff829d094995e367'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='62251f3d724a03e4c25ceeca4bb75755b9e70ce275e5a4bf2cbb1e6579699839'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d998890baf088acce50ef79f8e8dc3eab36a2dc008c7774fa6e1e1140c89c3c3`  
		Last Modified: Fri, 13 Jun 2025 01:08:32 GMT  
		Size: 50.0 MB (50039112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cddf61b157a492a5e9e87c2aa66c8d9d39517125432aef6e1db78ce8635515`  
		Last Modified: Fri, 13 Jun 2025 00:42:33 GMT  
		Size: 12.9 MB (12917586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3ac470ea7e30b6e5a35a060efd1c2cbf605f7dd3edaaafb19f952ae242da78`  
		Last Modified: Sat, 21 Jun 2025 03:46:08 GMT  
		Size: 221.1 MB (221126832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:3b2eb112d88ffa3de9fa206c3995a693cc88efaf77e5732c498b0cd1d00a9c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d72a7cea6af0dad101d90fab52b478096d076f784f7fef7c392512ebd07b44b`

```dockerfile
```

-	Layers:
	-	`sha256:a0bf026cfc84a7e1350d8305d12567bd11bff4046b627c09f84f22a0770beeb1`  
		Last Modified: Sat, 21 Jun 2025 03:26:04 GMT  
		Size: 2.4 MB (2436987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df6f1c154e495695481de70e285107009a3d11c95e97537d40d73d795bd17340`  
		Last Modified: Sat, 21 Jun 2025 03:26:05 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
