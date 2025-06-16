## `openjdk:26-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:38b9afa172f5120a4cd52275a1a432a1dc222ce434335503c44e8a1c8ab04afa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:42aa34c1f965025fa035e2d9f5f41b7acf9b618f5aaf98f9baa6158638fa02d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289528550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342b45ccf49bb20596e42fca059a07b4906705df25478f4a71a1da3b780a16d6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:42:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:42:18 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0915556054e5fcd1f04e454b0deedf305bb209616c5a72a8b2d83db9191e5115`  
		Last Modified: Thu, 12 Jun 2025 21:07:27 GMT  
		Size: 51.3 MB (51311558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac3313a7cb6946fff62780471126e2f2c56956f76d2d9f52a306aa958d87b3d`  
		Last Modified: Mon, 16 Jun 2025 17:51:31 GMT  
		Size: 15.0 MB (14979404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349ef2b439c744b6e15cb40ddfe920af429ae4fef2a64194a6154450dc1afa5f`  
		Last Modified: Mon, 16 Jun 2025 18:35:20 GMT  
		Size: 223.2 MB (223237588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6b2aeb8db3c1f736476dbaef9f007e54bf3941d0468c87f8702f2302dc4e8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362d06787e532e53c614771bc0a16281c02c42f51ecd7588271a6c07d500de92`

```dockerfile
```

-	Layers:
	-	`sha256:626c54e72e6e12b27bed7f605e47b23d235dc6b824ac1fc2106068be3215e973`  
		Last Modified: Mon, 16 Jun 2025 18:25:43 GMT  
		Size: 2.5 MB (2451696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e42eb4a44d85e6e3a40e987ea990271010a67ad7a488be78a1fe8b7035d6978`  
		Last Modified: Mon, 16 Jun 2025 18:25:44 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bd4a702ce713683e251ddbddd2e5689073515cff8c8a065fd16443f1164959ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.0 MB (284013215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1400fd9a87c4371c14a1966babbff606ceffafe9587fcae95180432084f683fd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:43:09 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:43:09 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
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
	-	`sha256:f141abbd1ffaa3f8fc7267a947a45d8028fb48896fc0793a11993558f8724be6`  
		Last Modified: Mon, 16 Jun 2025 19:06:57 GMT  
		Size: 221.1 MB (221056517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d71312159298f183c616086800ef17441b62df977a0630212e454a553d9fda71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9081141395a3d66e4cbf19ec6547bbbcb7566bf551bd7245ea202a2dba0c767`

```dockerfile
```

-	Layers:
	-	`sha256:a38fcb52d2e33c9c199406c847c2c0f57efb7d5178945fa44a18b07e16e1fbb4`  
		Last Modified: Mon, 16 Jun 2025 18:25:48 GMT  
		Size: 2.4 MB (2436985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9122423eba6763e3f368d10d299d2538f5c00b8cfcde55dcb6515854042d9646`  
		Last Modified: Mon, 16 Jun 2025 18:25:49 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
