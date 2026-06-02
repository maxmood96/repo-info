## `openjdk:27-ea-24-bookworm`

```console
$ docker pull openjdk@sha256:e431fcee41121f9201dcf8449aa2c3db08a1ece74249a660129feef2ab9a5adb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-24-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:dbe525a56a67b1cf93912b012f4e8b853e0115e7f7128f282693160fd63939b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.9 MB (380882325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3073a39a65eb6be693acaf76ac6813cb79ade3d61fe57e7572e88fff9db68cd8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:12:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 02 Jun 2026 07:12:17 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:12:17 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:12:17 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:12:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:12:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5360f81107cb507af633e9631d88a40526527289dbba97308c803d66352b0c53`  
		Last Modified: Tue, 02 Jun 2026 07:12:40 GMT  
		Size: 16.9 MB (16946621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28540d0dd6b83792fd8ef9222ffa26e76675319b733f090dec2740a592f97678`  
		Last Modified: Tue, 02 Jun 2026 07:12:45 GMT  
		Size: 227.0 MB (226992447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:82a50ef980d18b184732883ae0d97be2b65e6aae45838ab14e02a2342414a48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8684295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4dab3e58638e192a25566fcc79fa06bbc9146fa4db5395902a3512a6faaa25`

```dockerfile
```

-	Layers:
	-	`sha256:17a9c15955cbecfff1974a52676a6df108a4cff66854e684eceae5e57660bc20`  
		Last Modified: Tue, 02 Jun 2026 07:12:40 GMT  
		Size: 8.7 MB (8666356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046cdde434048ed902d69fdaaed1e4567da532c6ac89fe48e045269f538433d6`  
		Last Modified: Tue, 02 Jun 2026 07:12:39 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-24-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:004e0b19e74fb2e60356af1bf6781f25f44223bfc8cd5f9767307173059ed680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.2 MB (379221582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14e87f55da3849bd5babb1d1f85ea3932fe1a9284f53836688c45b75e798476`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:12:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 02 Jun 2026 07:12:25 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:12:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:12:25 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:12:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:12:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06a7ee52c9e23d4209ba46cbf17de96373911e9399859f91b3585121176146d`  
		Last Modified: Tue, 02 Jun 2026 07:12:51 GMT  
		Size: 17.7 MB (17730402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968a2a42d119845835f284cc6f9ff58e4f59ed58869c82b6bdcba5770be3578e`  
		Last Modified: Tue, 02 Jun 2026 07:12:56 GMT  
		Size: 225.0 MB (225010699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9eb8c728ea21747879e40d8fdc71307a6a0260afabc2d091c8b470ff1b0073de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8821259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3512e6404ec9eb0172f3a98fe3ac91ee3bbdd2b8f8e0c29cd6bbfc73ec2e7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8ed24bc76e57703bb7d1728b21a9ab6a223843015aa8b2846a19916350cad795`  
		Last Modified: Tue, 02 Jun 2026 07:12:51 GMT  
		Size: 8.8 MB (8803201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5882a3b67c2cb8ad3d8680f9ddfb6ee2d64aa67156c393552a668c0f6a1fbeab`  
		Last Modified: Tue, 02 Jun 2026 07:12:50 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
