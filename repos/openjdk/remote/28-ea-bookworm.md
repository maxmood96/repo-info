## `openjdk:28-ea-bookworm`

```console
$ docker pull openjdk@sha256:e66910b090366c0c97a590024beaad11793e7a6f16c9528aa682bde59a502376
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:9b320ffaceca5366750e828c2ec8a88349cb2bfb5a074a508f95816aab61ca82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 MB (381393452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa938f8282f3d9d7660334cae6b1f09bfdb2df01e0e7aaa39e049cca8735fcc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Tue, 16 Jun 2026 23:32:31 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:31 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:31 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110e4c484720e96aaabb81a9b9f8596aeadbbfad2c3b5cd92033db779fccb0f3`  
		Last Modified: Tue, 16 Jun 2026 23:32:57 GMT  
		Size: 16.9 MB (16946412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6b2505c0cb05224e89abb0d43fc71ac539bae924767475517a9cac41f80ac7`  
		Last Modified: Tue, 16 Jun 2026 23:33:02 GMT  
		Size: 227.5 MB (227496882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:24eefb24bc22d35672e310423f947ddb87cc165ae20a42d7968cae195c01340b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8684285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3220ce89ed190a5c7fe1c8abdaba474dad23d038c4a76244f6a38254da993576`

```dockerfile
```

-	Layers:
	-	`sha256:00240130cfe1a1295686c3ef04ef0237e5ec8edb463b1f4332b18b62794e5fbd`  
		Last Modified: Tue, 16 Jun 2026 23:32:57 GMT  
		Size: 8.7 MB (8666364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da8d0cc2f0dd7fbb49641d78fe7c1cbbcc9bb90a5d6ee1dd93ec610259ca2cb`  
		Last Modified: Tue, 16 Jun 2026 23:32:56 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f21fc8431eccfb8878e6ee53cbf02a50869180b19af96d36368a63a41af5d26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379747374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda9983886c1bde041c19f8e225883cfdebca11778cd1065c938f8b103ef364b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Tue, 16 Jun 2026 23:32:17 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:17 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:17 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1f341799d8d55d7594d49f3ea1286eddaf44615595f3dece9e243ab42df7bb`  
		Last Modified: Tue, 16 Jun 2026 23:32:42 GMT  
		Size: 17.7 MB (17730087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1d6bffb9ef2550f9d88356da573e682d24d43af16860ad95366933d747d75e`  
		Last Modified: Tue, 16 Jun 2026 23:32:47 GMT  
		Size: 225.5 MB (225527097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d9d30e5e2f2da1cc3a2602fcb2b4d92e869c22caaa01bb52c891331030e1d790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8821250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e60b1c9a10fb629ad63c115410350bf452163a9a091420751b7dc3b19d286f`

```dockerfile
```

-	Layers:
	-	`sha256:ad9282ae550927fc68d4fc26fe8e7aeea88589b24a150f8d3e4929b06133b6d0`  
		Last Modified: Tue, 16 Jun 2026 23:32:42 GMT  
		Size: 8.8 MB (8803209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e5a4d7a3f61c44ba7fdc7af03c1285de3344196ebd47ffdba785cc44451f2c6`  
		Last Modified: Tue, 16 Jun 2026 23:32:42 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
