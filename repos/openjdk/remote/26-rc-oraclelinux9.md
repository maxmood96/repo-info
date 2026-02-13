## `openjdk:26-rc-oraclelinux9`

```console
$ docker pull openjdk@sha256:0ed2d6f53e7a77723976fa6518c9c485fc33a9ff794a935ae42fbeb9ace354b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:b5694ef0a3082279bcb1bc10a0466c1be1cdd7df4240680d16a101712a1db447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313477407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d956b6953e6c1fedf2f37cb9da3dcb8590bf78bb8460b4dc1be266a8d4990437`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 12 Feb 2026 23:59:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 12 Feb 2026 23:59:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 12 Feb 2026 23:59:36 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Feb 2026 23:59:36 GMT
ENV LANG=C.UTF-8
# Thu, 12 Feb 2026 23:59:36 GMT
ENV JAVA_VERSION=26
# Thu, 12 Feb 2026 23:59:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 12 Feb 2026 23:59:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc04cd488c09d72e5aeebae6deb3a0cc39b7f0a1582f1b008f4fc84eeb9ea2b`  
		Last Modified: Thu, 12 Feb 2026 23:59:58 GMT  
		Size: 38.3 MB (38300053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c35c70c9cbbfee9aa78a4ca8b58185e1fb12e041da619e98c80ba416e544a8`  
		Last Modified: Fri, 13 Feb 2026 00:00:02 GMT  
		Size: 227.9 MB (227869812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:fc5810fc60a9d56c7a98fe999471cda85253b86c6a87a360b6d4d11ae63c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3669454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe9a77daf86e05252cda05b40cfe771f31c87a39ee042b247f71db8e759b5db`

```dockerfile
```

-	Layers:
	-	`sha256:dd1c04ad53d4f4e89ae7ebb4eddc07242aecc4b96b0576712e267effd3e88d3d`  
		Last Modified: Thu, 12 Feb 2026 23:59:57 GMT  
		Size: 3.7 MB (3653479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b648766e99e68bd3c57a7545bbc86f66e5274e0465176381953e10b4c2c66138`  
		Last Modified: Thu, 12 Feb 2026 23:59:57 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e6d1b60bf0b055f2bb38741498d70ef4092289d01cdeb3147ee7699dac04a4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310384598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6306accfb1b30cf052f3c2877039eba3e17151cde18ddac718a1be9b6f3c2bd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 12 Feb 2026 23:59:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 12 Feb 2026 23:59:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 12 Feb 2026 23:59:49 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Feb 2026 23:59:49 GMT
ENV LANG=C.UTF-8
# Thu, 12 Feb 2026 23:59:49 GMT
ENV JAVA_VERSION=26
# Thu, 12 Feb 2026 23:59:49 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 12 Feb 2026 23:59:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161b7d807fdc9ca001a9155d2e8d4b32e0dc82f545d25e47d4c803adf602dc6`  
		Last Modified: Fri, 13 Feb 2026 00:00:14 GMT  
		Size: 38.7 MB (38697204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d680b27ca7d1ebae4c0f4562030ca675dd37021b3a855706a14d8b1ed7abb`  
		Last Modified: Fri, 13 Feb 2026 00:00:17 GMT  
		Size: 225.8 MB (225783984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:485cc14d9c99281165b3509ff3738119d3e73e6681deb362fc4ccc2e60b691e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dbbe9f44b9bfbdcba40c346298ab40baa93f505012b3774f48ed83cc26f4a2`

```dockerfile
```

-	Layers:
	-	`sha256:f95912b118a0306606f7d85bcf0a2ab9adfd4f4fdb0de66988d3fed5a252aa05`  
		Last Modified: Fri, 13 Feb 2026 00:00:13 GMT  
		Size: 3.7 MB (3651097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d29dbbc6fb0c92b4248ef3c8c40b21232c418b3ae6a2a18bf1d90d6c4b65e0`  
		Last Modified: Fri, 13 Feb 2026 00:00:13 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json
