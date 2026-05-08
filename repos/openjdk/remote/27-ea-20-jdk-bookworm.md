## `openjdk:27-ea-20-jdk-bookworm`

```console
$ docker pull openjdk@sha256:e55ba339e1f3954b68fbd4c97e5e16c3e820a19fc0724003e7d052293cc728c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-20-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:ae06e1c549483854311cd2bb5c2b4fc15453661c4b0270ce5869a5cea82203c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382460130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4c890c9d70b1b5efef47f8f74a4422411f07de5f945dbfd95cbe97cc9e0cba`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:19:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:19:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 08 May 2026 21:19:15 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:19:15 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 21:19:15 GMT
ENV JAVA_VERSION=27-ea+20
# Fri, 08 May 2026 21:19:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 May 2026 21:19:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757794fe1145fb01159e0b72f788ca79e553309f14b4450d5902a55cd5c07fc`  
		Last Modified: Fri, 08 May 2026 21:19:40 GMT  
		Size: 16.9 MB (16945748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f521f0be32ab8c52ef3f479c5c6ff92bbff0bb7b201a4ef74ff32d2b26b98aff`  
		Last Modified: Fri, 08 May 2026 21:19:45 GMT  
		Size: 228.6 MB (228586490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-20-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:424886a3977924e864bf184d60463f4f3c792cdd36937e7fd19b40182df2de55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8685555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d874ccfd67d144d803a7a94f61bcbe5fcfe18e44f0dee8b51688df691c2764`

```dockerfile
```

-	Layers:
	-	`sha256:670ace32a85a819612ebd75229c3e65cdf82c05dc63bc32ae3ffb66d7123109e`  
		Last Modified: Fri, 08 May 2026 21:19:40 GMT  
		Size: 8.7 MB (8667617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce0a1a9cac848e3760ab212b0d29146277dd3130179a38d4bb439d03e30b8ad`  
		Last Modified: Fri, 08 May 2026 21:19:39 GMT  
		Size: 17.9 KB (17938 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-20-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4392c902ca2d193771aec1e6555fbd1ce69e55ad8ba14699b1f2a4ac044edeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380746348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310a3551a51a6b94e479b8e75bec70b8ae2cb5993c8ad9ca4b564e8a3e00633c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:19:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:19:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 08 May 2026 21:19:51 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:19:51 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 21:19:51 GMT
ENV JAVA_VERSION=27-ea+20
# Fri, 08 May 2026 21:19:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 May 2026 21:19:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de40e5d4f23473b053255e3f5ce4d43dc92766f01846f459d75deaae3032c46`  
		Last Modified: Fri, 08 May 2026 21:20:16 GMT  
		Size: 17.7 MB (17728996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d08dec0e21b8b39e1b8a64196db458e5d9be85b750d3230cc83e93167a836a`  
		Last Modified: Fri, 08 May 2026 21:20:26 GMT  
		Size: 226.6 MB (226555104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-20-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1fa601a4521cdf8fc315056ada24a4b23a1cbb8aa46b607e5a2fa528bea11a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180d754bce982a3e493d35b04032168a5c3333cb73273816ab6b766cb28d2b3e`

```dockerfile
```

-	Layers:
	-	`sha256:cc4bc4ee89f8885bd192d4ecd8f6197ac3a8e6e401275b9582a34c55575a7eb1`  
		Last Modified: Fri, 08 May 2026 21:20:16 GMT  
		Size: 8.8 MB (8804462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6bc10fc2ddb1388eba44b46627ad9868c77716b81ab54107cfcdcf2525d2f98`  
		Last Modified: Fri, 08 May 2026 21:20:15 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
